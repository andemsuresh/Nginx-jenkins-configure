# Nginx-jenkins-configure
Configure nginx to jenkins
## STEP-1
      unlink /etc/nginx/sites-enabled/default

## STEP-2

      vi /etc/nginx/conf.d/jenkins.conf

#copy paste the "jenkins.conf" code here

## STEP-3

    cd /etc/nginx/conf.d

## STEP-4

To test your config file run below command

    nginx -t
    
## STEP-5
 
     systemctl reload nginx
   
