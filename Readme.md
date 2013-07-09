## OWASP CSRFGuard 3.0

[http://www.owasp.org/index.php/Category:OWASP_CSRFGuard_Project](http://www.owasp.org/index.php/Category:OWASP_CSRFGuard_Project)

Eric Sheridan [(eric@infraredsecurity.com)](mailto:eric@infraredsecurity.com), Copyright (c) 2011

BSD License, All rights reserved.

## Overview

Welcome to the home of the OWASP CSRFGuard Project! OWASP CSRFGuard is a library that implements a variant of the synchronizer token pattern to mitigate the risk of Cross-Site Request Forgery (CSRF) attacks. The OWASP CSRFGuard library is integrated through the use of a JavaEE Filter and exposes various automated and manual ways to integrate per-session or pseudo-per-request tokens into HTML. When a user interacts with this HTML, CSRF prevention tokens (i.e. cryptographically random synchronizer tokens) are submitted with the corresponding HTTP request. It is the responsibility of OWASP CSRFGuard to ensure the token is present and is valid for the current HTTP request. Any attempt to submit a request to a protected resource without the correct corresponding token is viewed as a CSRF attack in progress and is discarded. Prior to discarding the request, CSRFGuard can be configured to take one or more actions such as logging aspects of the request and redirecting the user to a landing page. The latest release enhances this strategy to support the optional verification of HTTP requests submitted using Ajax as well as the optional verification of referrer headers.

## Project Lead

Eric Sheridan [(eric@infraredsecurity.com)](mailto:eric@infraredsecurity.com) is the lead and primary developer of the OWASP CSRFGuard 3.0 project and a Managing Partner at Infrared Security (http://www.infraredsecurity.com). Aside from leading up CSRFGuard, Eric has contributed to or provided guidance on numerous other OWASP projects including CSRF Prevention Cheat Sheet, WebGoat, Stinger, CSRFTester, and Enterprise Security API (ESAPI). As Managing Partner at Infrared Security, Eric Sheridan specializes in a wide variety of application security activities including static analysis, penetration tests, code reviews, and threat modeling. In his personal time... wait, what is that?

## License

OWASP CSRFGuard 3.0 is offered under the [BSD license](http://www.opensource.org/licenses/bsd-license.php)

## Building the code

1. Make sure that you have Apache Maven 3.0.4 or higher installed;
2. Clone this repository locally;
3. Build the ```csrfguard``` project first as ```cd csrfguard``` followed by ```mvn clean install```;
4. Build and run the ```csrfguard-test``` project as ```cd ../csrfguard-test``` followed by ```mvn clean package tomcat7-run```;
5. Use a web browser to access ```http://localhost``` to open the home page of the test project.

## Email List

You can sign up for the OWASP CSRFGuard email list [here.]( https://lists.owasp.org/mailman/listinfo/owasp-csrfguard)
