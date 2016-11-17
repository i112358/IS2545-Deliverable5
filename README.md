# IS2545 Deliverable 5 - Security Testing
Team members: Rachel Chang (juc62), Zihan Xie (zix8)

### Tesing site: http://testphp.vulnweb.com/ (Acunetix WVS)

#### 1. Cross-site scripting vulnerability
  1. **InfoSec triad**: This vulnerability attacks the integrity of the website, it can modify the contents of the website.
  
  2. **Kind/nature of security attack**: It is a kind of modification attack and it is an active attack. Attackers feed malicious script to any openings and vulnerabilities.
  
  3. **Business value at risk**: XSS enables attackers to inject client-side scripts into web pages viewed by other users. Through XSS,  cookies, session tokens, or other private information retained by the browser could be accessed. Attackers could take control of database, or steal account information, which are the most important business values.
  
  4. **Steps taken**:
    1. Go to sign up page.
    2. Enter html code "\</li>\<script>alert(1);\</script>\<li>" into username column.
    3. Fill other columns.
    4. Click "signup".
    5. Signup will be successful and we can see the html code will be executed.
  
  5. **Screenshot**:
    1. Steps of attack:
    ![image of xss attack](/img/XSS1.JPG)
    
    2. Result of attack:
    ![image of xss attack result](/img/XSS2.JPG)
  
  6. **How to fix**:
    1. Contextual output encoding/escaping could be used as the primary defense mechanism to stop XSS attacks.
    2. Safely validating untrusted HTML input.

#### 2. SQL injection - MySQL
  1. **InfoSec triad**: This vulnerability attacks the confidentiality and integrity of the website, it can exploit and modify the contents of the database.
  
  2. **Kind/nature of security attack**: It may be a kind of interruption attack or modification attack and it is an active attack. Attackers may use queries in any openings and vulnerabilities.
  
  3. **Business value at risk**: It's very dangrous to let the attackers have unauthorized access to the database. Since SQL databases generally hold sensitive data, loss of confidentiality is a frequent problem with SQL Injection vulnerabilities. Attackers could gain control of the site.
  
  4. **Steps taken**:
    1. Go to signup page.
    2. Enter query "ZAP' UNION ALL select NULL -- " into username column.
    3. Fill other columns.
    4. Click "signup".
    5. Query will be executed and a message saying that the number of columns for the SELECT statement was incorrect.
  
  5. **Screenshot**:
    1. Steps of attack:
    ![image of MySQL attack](/img/MySQL.JPG)
    
    2. Result of attack:
    ![image of MySQL attack result](/img/MySQL2.JPG)
  
  6. **How to fix**: 
    1. Providing a string when the SQL query is expecting an integer, or purposely inserting a syntax error in an SQL statement cause the database server to throw an error.
    2. To leverage the UNION SQL operator, allowing an attacker to combine the results of two or more SELECT statements into a single result. This forces the application to return data within the HTTP response – this technique is referred to as union-based SQL Injection.

#### 3. SQL injection
  1. **InfoSec triad**: This vulnerability attacks the confidentiality of the website, it grants access to user's information and the power to modify it.
  
  2. **Kind/nature of security attack**: It may be a kind of interruption attack or modification attack and it is an active attack. Attackers may use queries in any openings and vulnerabilities.
  
  3. **Business value at risk**: If poor SQL commands are used to check user names and passwords, it may be possible to connect to a system as another user with no previous knowledge of the password. With the exposed directory, attackers could get unauthorized access to customer's data, which is one of the most valuble assets for a site. The attacker may even gain powers as an administrator, which would be very dangerous.
  
  4. **Steps taken**:
    1. Go to login page.
    2. Enter "test" as username.
    3. Enter SQL query "ZAP' OR '1'='1' -- " as password.
    4. Click "login" button.
    5. Login will be successful and will show user's profile.
  
  5. **Screenshot**:
    1. Steps of attack:
    ![image of SQL attack](/img/SQL.JPG)
    
    2. Result of attack:
    ![image of SQL attack result](/img/SQL2.JPG)
  
  6. **How to fix**: 
    1. Providing a string when the SQL query is expecting an integer, or purposely inserting a syntax error in an SQL statement cause the database server to throw an error.
    2. To leverage the UNION SQL operator, allowing an attacker to combine the results of two or more SELECT statements into a single result. This forces the application to return data within the HTTP response – this technique is referred to as union-based SQL Injection.
