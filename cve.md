# blood-bank-system-in-php has Cross Site Scripting vulnerability in o+.php

## supplier 
https://code-projects.org/blood-bank-system-in-php-with-source-code/
## Vulnerability file
/BBfile/Blood/o+.php
## describe
There is an  Cross Site Scripting vulnerability in blood-bank-system-in-php  in /BBfile/Blood/o+.php. Control parameter: $Bloodname

A malicious attacker can use this vulnerability to obtain administrator login credentials or phishing websites

## code analysis

In O+.php.php，get $row['Bloodname'], and echo it in no filter.

![Image](https://github.com/user-attachments/assets/b299ae9c-7b53-4ad8-b8d0-a70701ae93bc)

## POC

```
GET /Blood/O+.php HTTP/1.1
Host: bloodbankmgmtsystem
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.6261.112 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Encoding: gzip, deflate, br
Accept-Language: zh-CN,zh;q=0.9
 Connection: close


```

**Result**

![Image](https://github.com/user-attachments/assets/a4e10b3b-2451-4276-8066-b3959e3d0a27)

![Image](https://github.com/user-attachments/assets/9cf96475-1759-48e5-8bf3-387c4fd597f1)

## submiter

姓名：向宏力
单位：广州大学
导师：罗熙
