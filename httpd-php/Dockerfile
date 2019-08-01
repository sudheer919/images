#rkalluru/kb03-httpd-php:v1
FROM        centos 

## ENV
ENV         HTTPD_PREFIX=/opt/httpd 
RUN         yum install wget -y 
WORKDIR     /root
RUN         wget -q -O - http://apachemirror.wuchna.com//httpd/httpd-2.4.39.tar.gz | tar -xz
RUN         yum install apr-util-devel gcc pcre-devel make -y
WORKDIR     /root/httpd-2.4.39
RUN         ./configure --prefix=$HTTPD_PREFIX && \
            make && \
            make install 
COPY        httpd-start.sh /httpd-start.sh
RUN         chmod +x /httpd-start.sh 
CMD         /httpd-start.sh 

 