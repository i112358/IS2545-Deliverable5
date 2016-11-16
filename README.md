# IS2545 Deliverable 5 - Security Testing
Team members: Rachel Chang (juc62), Zihan Xie (zix8)

### Tesing site: http://testphp.vulnweb.com/ (Acunetix WVS)

#### 1. Cross-site scripting vulnerability
  1. InfoSec triad: This vulnerability attacks the integrity of the website, it can modify the contents of the website.
  
  2. Kind/nature of security attack: It is a kind of modification attack and it is an active attack. Attackers feed malicious script to any openings and vulnerabilities.
  
  3. Business value at risk:
  
  4. Steps taken:
    1. Go to sign up page.
    2. Enter html code "\</li>\<script>alert(1);\</script>\<li>" into username column.
    3. Fill other columns.
    4. Click "signup".
    5. Signup will be successful and we can see the html code will be executed.
  
  5. Screenshot:
    1. Steps of attack:
    ![image of xss attack](/img/XSS1.JPG)
    
    2. Result of attack:
    ![image of xss attack result](/img/XSS2.JPG)
  
  6. How to fix: 

#### 2. SQL injection - MySQL
  1. InfoSec triad: This vulnerability attacks the confidentiality and integrity of the website, it can exploit and modify the contents of the database.
  
  2. Kind/nature of security attack: It may be a kind of interruption attack or modification attack and it is an active attack. Attackers may use queries in any openings and vulnerabilities.
  
  3. Business value at risk:
  
  4. Steps taken:
    1. Go to signup page.
    2. Enter query "ZAP' UNION ALL select NULL -- " into username column.
    3. Fill other columns.
    4. Click "signup".
    5. Query will be executed and a message saying that the number of columns for the SELECT statement was incorrect.
  
  5. Screenshot:
    1. Steps of attack:
    ![image of MySQL attack](/img/MySQL.JPG)
    
    2. Result of attack:
    ![image of MySQL attack result](/img/MySQL2.JPG)
  
  6. How to fix: 

#### 3. SQL injection
  1. InfoSec triad: This vulnerability attacks the confidentiality of the website, it grants access to user's information and the power to modify it.
  
  2. Kind/nature of security attack: It may be a kind of interruption attack or modification attack and it is an active attack. Attackers may use queries in any openings and vulnerabilities.
  
  3. Business value at risk:
  
  4. Steps taken:
    1. Go to login page.
    2. Enter "test" as username.
    3. Enter SQL query "ZAP' OR '1'='1' -- " as password.
    4. Click "login" button.
    5. Login will be successful and will show user's profile.
  
  5. Screenshot:
    1. Steps of attack:
    ![image of SQL attack](/img/SQL.JPG)
    
    2. Result of attack:
    ![image of SQL attack result](/img/SQL2.JPG)
  
  6. How to fix: 
