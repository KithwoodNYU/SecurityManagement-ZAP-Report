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

**Finding**: X-Frame-Options Header Not Set
The X-Frame-Option is a HTTP response header which tells the browser whether or not it should allow the website to be rendered within in a 
frame, iframe, embed, or object. Click jacking can occur as a result of this if a malicious site embeds a link in, say an iframe, with a link 
overlaid which appears to be some other content. The result is that the click comes from theUser’s origin and can perform unauthorized actions 
on the behalf of the user (potentially authenticated via a http session cookie).
**Risk**: Medium. 
However Google VASQ is a web application implemented entirely client side using java script. The web application keepstrack of no state or 
authentication; rather it exports it locally in the browser to a JSON object which is sent to NYU via PGP encrypted email.Correspondingly 
click jacking vulnerabilities do not pose a risk to this web application. 
**Remediation Recommendation**:As noted above, this vulnerability does not present risk to NYU. However to clean this vulnerability up, our AWS 
Lambda serverless instance would need to be configured to set the x-frame-option. 
