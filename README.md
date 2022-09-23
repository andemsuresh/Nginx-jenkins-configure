# Nginx-jenkins-configure
Configure nginx to jenkins
## STEP-1
      unlink /etc/nginx/sites-enabled/default

## STEP-2

      vi /etc/nginx/conf.d/jenkins.conf

   upstream jenkins{
        server 127.0.0.1:8080;
                }
    server{
           listen 80 default_server;
           listen [::]:80 default_server;
           server_name jenkins.suresh;
       location / {
         proxy_pass http://jenkins;
         proxy_set_header Host $host;
         proxy_set_header X-Real-IP $remote_addr;
       } 
} 

## STEP-3

    cd /etc/nginx/conf.d

## STEP-4

To test your config file run below command

    nginx -t
