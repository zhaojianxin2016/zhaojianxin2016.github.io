---
layout: wp
title: 理解LNMP
---


### nginx start command ###

/home/work/app/nginx/sbin/nginx -c /home/work/app/nginx/conf/nginx.conf   


### nginx config file ###   

#### block ####  

```
http {
    server {
        listen 80;
        server_name xxx;
        location / {
            root /data/www;
        }

        location /images/ {
            root /data;
        }
    }
}
```


### vhosts ###
include  vhosts/*.conf;   


### 规则匹配 ###   

```
lcation / {

```
TODO 匹配方式


### cgi ###  
fastcgi_pass  


### 转发 ###   



参考资料：   

* [https://www.nginx.com/resources/wiki/start/topics/tutorials/commandline/)(https://www.nginx.com/resources/wiki/start/topics/tutorials/commandline/)  
* [nginx config file](http://nginx.org/en/docs/beginners_guide.html)  
* [nginx config file description](http://www.cnblogs.com/xiaogangqq123/archive/2011/03/02/1969006.html)   

