# Appendix: ZAP Scanning Report

## Introduction 
The Zed Attack Proxy (ZAP) is an open source web application security scanner which can be used to help security analysts to find security 
vulnerabilities in web applications. ZAP is supported by OWASP® (Open Web Application Security Project) and is an OWASP Flagship project. 
Oceans Eleven used ZAP to assess the risk posture of Google’s Vendor Security Assessment Questionnaire (VSAQ) software and find applicable 
vulnerabilities. The following document provides a risk analysis of the scan results.

## Scan Results
ZAP found a total of 8 Alerts:
| Risk Level | Number of Alerts | 
| --- | --- |
| High | 0 |
| Medium | 1 | 
| Low | 6 |
| Informational| 1 |

---
### **Finding**: X-Frame-Options Header Not Set
The X-Frame-Option is a HTTP response header which tells the browser whether or not it should allow the website to be rendered within in a 
frame, iframe, embed, or object. Click jacking can occur as a result of this if a malicious site embeds a link in, say an iframe, with a link 
overlaid which appears to be some other content. The result is that the click comes from theUser’s origin and can perform unauthorized actions 
on the behalf of the user (potentially authenticated via a http session cookie).

**Risk**: Medium. 

**Remediation Recommendation**: However Google VASQ is a web application implemented entirely client side using java script. The web 
application keepstrack of no state or authentication; rather it exports it locally in the browser to a JSON object which is sent to NYU 
via PGP encrypted email. Correspondingly click jacking vulnerabilities do not pose a risk to this web application. Consequently, this 
vulnerability does not present risk to NYU. However to address this vulnerability would require that the AWS Lambda serverless instance 
would need to be configured to set the x-frame-option. 







---
### **Finding**: Cross-Domain JavaScript Source File Inclusion
The page includes one or more script files from a third-party domain.

**Risk**: Low

**Remediation Recommendation**: This finding does not affect the VSAQ instance as we ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.

---
### **Finding**: Content Security Policy (CSP) Header Not Set
Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.

**Risk**: Low

**Remediation Recommendation**: The AWS Lambda serverless instance should be configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.


---
### **Finding**: X-Content-Type-Options Header Missing
The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.

**Risk**: Low

**Remediation Recommendation**: The AWS Lambda serverless instance should be configured to set the X-Content-Type-Options header to 'nosniff' for all web pages. If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.


---
### **Finding**: User Controllable HTML Element Attribute (Potential XSS)
This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.

**Risk**: Informational

**Remediation Recommendation**: This finding does not affect the VSAQ questionnaire as the inputs are not written into HTML elements. That said, when the inputs are written to CSV, they should be sanitized for output.
