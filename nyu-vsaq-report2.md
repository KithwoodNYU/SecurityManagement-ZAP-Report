
# ZAP Scanning Report




## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 6 |
| Informational | 1 |

## Alert Detail


  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/](http://google-vsaq.s3-website-us-east-1.amazonaws.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 5
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. ALLOW-FROM allows specific websites to frame the web page in supported web browsers).</p>
  
### Reference
* http://blogs.msdn.com/b/ieinternals/archive/2010/03/30/combating-clickjacking-with-x-frame-options.aspx

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/](http://google-vsaq.s3-website-us-east-1.amazonaws.com/)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/vsaq.css](http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/vsaq.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/custom.css](http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/custom.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/sitemap.xml](http://google-vsaq.s3-website-us-east-1.amazonaws.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq_binary.js](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq_binary.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/robots.txt](http://google-vsaq.s3-website-us-east-1.amazonaws.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `AmazonS3`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="_vsaq_export_element">`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="postdata">`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="_vsaq_export_element">`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="postdata">`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="postdata">`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="_vsaq_export_element">`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="postdata">`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="_vsaq_export_element">`
  
  
  
  
Instances: 8
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret] was found in the following HTML form: [Form 2: ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
### Web Browser XSS Protection Not Enabled
##### Low (Medium)
  
  
  
  
#### Description
<p>Web Browser XSS Protection is not enabled, or is disabled by the configuration of the 'X-XSS-Protection' HTTP response header on the web server</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-XSS-Protection`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-XSS-Protection`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/sitemap.xml](http://google-vsaq.s3-website-us-east-1.amazonaws.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-XSS-Protection`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/robots.txt](http://google-vsaq.s3-website-us-east-1.amazonaws.com/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-XSS-Protection`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-XSS-Protection`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-XSS-Protection`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/](http://google-vsaq.s3-website-us-east-1.amazonaws.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-XSS-Protection`
  
  
  
  
Instances: 7
  
### Solution
<p>Ensure that the web browser's XSS filter is enabled, by setting the X-XSS-Protection HTTP response header to '1'.</p>
  
### Other information
<p>The X-XSS-Protection HTTP response header allows the web server to enable or disable the web browser's XSS protection mechanism. The following values would attempt to enable it: </p><p>X-XSS-Protection: 1; mode=block</p><p>X-XSS-Protection: 1; report=http://www.example.com/xss</p><p>The following values would disable it:</p><p>X-XSS-Protection: 0</p><p>The X-XSS-Protection HTTP response header is currently supported on Internet Explorer, Chrome and Safari (WebKit).</p><p>Note that this alert is only raised if the response body could potentially contain an XSS payload (with a text-based content type, with a non-zero length).</p>
  
### Reference
* https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet
* https://www.veracode.com/blog/2014/03/guidelines-for-setting-security-headers/

  
#### CWE Id : 933
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/](http://google-vsaq.s3-website-us-east-1.amazonaws.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.google.com/js/maia.js`
  
  
  * Evidence: `<script src="https://www.google.com/js/maia.js"></script>`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.google.com/js/maia.js`
  
  
  * Evidence: `<script src="https://www.google.com/js/maia.js"></script>`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.google.com/js/maia.js`
  
  
  * Evidence: `<script src="https://www.google.com/js/maia.js"></script>`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.google.com/js/maia.js`
  
  
  * Evidence: `<script src="https://www.google.com/js/maia.js"></script>`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.google.com/js/maia.js`
  
  
  * Evidence: `<script src="https://www.google.com/js/maia.js"></script>`
  
  
  
  
Instances: 5
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
### Content Security Policy (CSP) Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/sitemap.xml](http://google-vsaq.s3-website-us-east-1.amazonaws.com/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/robots.txt](http://google-vsaq.s3-website-us-east-1.amazonaws.com/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/](http://google-vsaq.s3-website-us-east-1.amazonaws.com/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy
* https://www.owasp.org/index.php/Content_Security_Policy
* http://www.w3.org/TR/CSP/
* http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html
* http://www.html5rocks.com/en/tutorials/security/content-security-policy/
* http://caniuse.com/#feat=contentsecuritypolicy
* http://content-security-policy.com/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/vsaq.css](http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/vsaq.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/](http://google-vsaq.s3-website-us-east-1.amazonaws.com/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/custom.css](http://google-vsaq.s3-website-us-east-1.amazonaws.com/static/custom.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq_binary.js](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq_binary.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scanner will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://www.owasp.org/index.php/List_of_useful_HTTP_headers

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `_rom_`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `draft`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `draft`
  
  
  
  
* URL: [http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json](http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/offline_data_gathering.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `_rom_`
  
  
  
  
Instances: 4
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>http://google-vsaq.s3-website-us-east-1.amazonaws.com/vsaq.html?_rom_=%7B%7Breadonly%7Clower%7D%7D&draft=false&qpath=questionnaires/test_template.json</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>_rom_={{readonly|lower}}</p><p></p><p>The user-controlled value was:</p><p>{{readonly|lower}}</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3
