# IS2545 Deliverable 5 - Security Testing
Team members: Rachel Chang (juc62), Zihan Xie (zix8)

### Tesing site: http://testphp.vulnweb.com/ (Acunetix WVS)

#### 1. Cross-site vulnerability
  - InfoSec triad:
  
  - Kind/nature of security attack:
  
  - Business value at risk:
  
  - Steps taken:
    1. Go to sign up page.
    2. Enter html code "\</li>\<script>alert(1);\</script>\<li>" into username column.
    3. Fill other columns.
    4. Click "signup".
    5. Signup will be successful and we can see the html code will be executed.
  
  - Screenshot:
  ![image of xss attack](/img/XSS1.JPG)
  ![image of xss attack result](/img/XSS2.JPG)
  
  - How to fix: 

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
