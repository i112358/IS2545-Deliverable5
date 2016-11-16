# IS2545 Deliverable 5 - Security Testing
Team members: Rachel Chang (juc62), Zihan Xie (zix8)

### Tesing site: http://testphp.vulnweb.com/ (Acunetix WVS)

#### 1. Cross-site scripting vulnerability
  1. InfoSec triad: This vulnerability attacks the integrity of the Website.
  
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
  - InfoSec triad:
  
  - Kind/nature of security attack:
  
  - Business value at risk:
  
  - Steps taken:
  
  - Screenshot:
  ![image of MySQL attack](/img/MySQL.JPG)
  ![image of MySQL attack result](/img/MySQL2.JPG)
  
  - How to fix: 

#### 3. SQL injection
  - InfoSec triad:
  
  - Kind/nature of security attack:
  
  - Business value at risk:
  
  - Steps taken:
  
  - Screenshot:
  ![image of SQL attack](/img/SQL.JPG)
  ![image of SQL attack result](/img/SQL2.JPG)
  
  - How to fix: 
