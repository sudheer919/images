FROM centos 
RUN yum install httpd -y 
COPY local.html /var/www/html/index.html 
RUN chown apache:apache /var/www/html/index.html  
CMD httpd -DFOREGROUND 
