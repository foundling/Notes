# Nginx Config

## Installing

````bash
# update yum
sudo yum update

# install epel to get up-to-date nginx 
sudo yum install epel-release

# install nginx
sudo yum install nginx

# start nginx
/etc/init.d/nginx start
````

## Configuring (For Virtual Servers, or Server Blocks)


```
# put this in your /etc/nginx/conf.d/virtual.conf 

server {
    listen       80;
    server_name  domain-name.com;

    location / {
        root    /path/to/webserver/document_root/;
        index  index.html index.htm;
    }
}

# restart the server
/etc/init.d/nginx restart

```

