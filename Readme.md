# YrpreyTasks

![yprey](https://i.imgur.com/zHoDJG9_d.webp?maxwidth=760&fidelity=grand)

**Backend created by [Fernando Mengali](https://www.linkedin.com/in/fernando-mengali-273504142/)**

YrpreyTasks is a framework based financial management systems. The framework perfectly simulates a tasks system that can help a user in managing taks and actions, but it has vulnerabilities based on OWASP TOP 10 WebApp 2021. The framework was developed to teach and learn details in Pentest (testing penetration) and Application Security. In the context of Offensive Security, vulnerabilities contained in web applications can be identified, exploited and compromised. For application security professionals and experts, the framework provides an in-depth understanding of code-level vulnerabilities. Yrprey, making it valuable for educational, learning and teaching purposes in the field of Information Security. For more information about the vulnerabilities, we recommend exploring the details available at [yrprey.com](https://yrprey.com).

#### Features
 - Based on OWASP's top 10 vulnerabilities for Web Application.

Initially, a non-registered user only has access to the index.php page. The user can authenticate to the system with the credentials admin@yrprey.com and the password 1234567890. Functionalities include adding tasks, edit and removals.
yrprey tasks is not recommended for personal or commercial use, only for laboratory use and learning about exploiting and patching vulnerabilities.

#### List of Vulnerabilities

In this section, we have a comparison of the vulnerabilities present in the framework with the routes and a comparison between the OWASP TOP 10 Web Application.
This table makes it easier to understand how to exploit vulnerabilities in each systemic function.
In the last two columns we have a parenthesis and the scenario associated with the OWASP TOP 10 Web Applications, facilitating the understanding of the theory described on the page https://owasp.org/www-project-top-ten/.
After understanding the scenario and the vulnerable route, the process of identifying and exploiting vulnerabilities becomes easier. If you are an Application Security professional, knowing the scenario and routes of endpoints makes the process of identifying and correcting vulnerabilities easier with manual Code Review Security techniques or automated SAST, SCA and DAST analyses

Complete table with points vulnerables, vulnerability details and a comparison between OWASP TOP 10 Web Application vulnerabilities:

|Qtde |          **OWASP TOP 10**                          |**Method**|            **Path**            |            **Details**                            |
|----:|:--------------------------------------------------:|:--------:|:------------------------------:|:-------------------------------------------------:|
| 01  |  A01:2021-Broken Access Control                    |   POST   |  /about.php?img=logo.webp      |                  Path Traversal                   |
| 03  |  A01:2021-Broken Access Control                    |   POST   |  /user.php                     |             View all users data                   |
| 04  |  A02:2021-Cryptographic Failures                   |   POST   |  /index.php                    |             Store password with base64            |
| 18  |  A03:2021-Injection                                |   POST   |  /index.php                    |        SQL Injection - Authentication             |
| 19  |  A03:2021-Injection                                |   POST   |  /index.php                    |            Cross-Site Request Forgery             |
| 20  |  A03:2021-Injection                                |   GET    |  /logout.php?url=http://...    |          Redirect to other url                    |
| 10  |  A02:2021-Cryptographic Failures                   |   POST   |  /.idea/workspace.xml          |                    File Exposure                  |
| 11  |  A02:2021-Cryptographic Failures                   |   POST   |  /htdocs/.htaccess             |                    File Exposure                  |
| 12  |  A02:2021-Cryptographic Failures                   |   POST   |  /Root                         |                    File Exposure                  |
| 13  |  A05:2021-Security Misconfiguration                |   GET    |  /phpinfo.php                  |                    File Exposure                  |
| 14  |  A05:2021-Security Misconfiguration                |   GET    |  /bkp.zip                      |                    File Exposure                  |
| 15  |  A02:2021-Cryptographic Failures                   |   POST   |  /db.php.old                   |             Credential harcoded database          |
| 16  |  A02:2021-Cryptographic Failures                   |   POST   |  /db.php.txt                   |             Credential harcoded database          |
| 31  |  A05:2021-Security Misconfiguration                |   POST   |  /index.php                    |   Intercept Credentials with Sniffer or BurpSuite |
| 32  |  A05:2021-Security Misconfiguration                |   GET    |  /ftp/WS_FTP.LOG               |            Misconfiguration                       |
| 33  |  A05:2021-Security Misconfiguration                |   GET    |  /ssh-key.priv                 |            Misconfiguration                       |
| 34  |  A05:2021-Security Misconfiguration                |   GET    |  /index.php                    |            Header - Not Definied HttpOnly         |
| 35  |  A05:2021-Security Misconfiguration                |   GET    |  /index.php                    |  Header - Not Definied Frame Options Header       |
| 36  |  A05:2021-Security Misconfiguration                |   GET    |  /index.php                    |            Header - Not Definied HSTS             |
| 37  |  A05:2021-Security Misconfiguration                |   GET    |  /index.php                    |   Header - Not Definied Content Security Policy   |
| 38  |  A05:2021-Security Misconfiguration                |   GET    |  /index.php                    |            Header - Not Definied XSS Protection   |
| 39  |  A05:2021-Security Misconfiguration                |   GET    |  /adminer-4.8.1.php            |            Adminer default                        |
| 40  |  A05:2021-Security Misconfiguration                |   GET    |  /phpminiadmin.php             |            PHP Mini Admin default                 |
| 41  |  A06:2021-Vulnerable and Outdated Components       |   GET    |  /js/jquery-1.5.1.js           |  XSS to function: html,append,load,after..        |
| 42  |  A06:2021-Vulnerable and Outdated Components       |   GET    |  /js/jquery-1.5.1.js           |  Prototype Pollution to function: extend          |
| 43  |  A06:2021-Vulnerable and Outdated Components       |   GET    |  /js/lodash-3.9.0.js           |  Prototype Pollution to function: zipObjectDeep.. |
| 44  |  A06:2021-Vulnerable and Outdated Components       |   GET    |  /js/lodash-3.9.0.js           |            Code Injection across template         |
| 45  |  A06:2021-Vulnerable and Outdated Components       |   GET    |  /js/lodash-3.9.0.js           | ReDoS to functions: toNumber, trim, trimEnd       |
| 46  |  A06:2021-Vulnerable and Outdated Components       |   GET    |  /js/bootstrap-4.1.3.js        | Prototype Pollution to function: data-template... |
| 47  |  A07:2021-Identif. and Authentication Failures     |   N/A    |  /Change cache cookie to admin |  Session Hijacking (Manipulation Cookie)         |
| 48  |  A07:2021-Identif. and Authentication Failures     |   POST   |  /index.php                    |             username enumeration                  |

## How Install

* 1º - Install and configure Apache, PHP and MySQL on your Linux
* 2º - Import the YRpreyPHP files to /var/www/
* 3º - Create a database named "yrprey"
* 4º - Import the yrprey.sql into the database.
* 5º - Access the address http://localhost in your browser
* 6º - In php ini change allow_url_include to "On".

## Observation
You can test on Xampp or any other platform that supports PHP and MySQL.

## Reporting Vulnerabilities

Please, avoid taking this action and requesting a CVE!

The application intentionally has some vulnerabilities, most of them are known and are treated as lessons learned. Others, in turn, are more "hidden" and can be discovered on your own. If you have a genuine desire to demonstrate your skills in finding these extra elements, we suggest you share your experience on a blog or create a video. There are certainly people interested in learning about these nuances and how you identified them. By sending us the link, we may even consider including it in our references.
