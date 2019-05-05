FROM centos
RUN yum -y install gcc-c++
RUN yum -y install -y pcre pcre-devel
RUN yum -y install -y zlib zlib-devel
RUN yum -y install -y openssl openssl-devel
RUN yum -y install wget
WORKDIR /app
RUN wget http://nginx.org/download/nginx-1.15.12.tar.gz
RUN tar -zxvf nginx-1.15.12.tar.gz
WORKDIR /app/nginx-1.15.12
RUN ./configure --user=nobody --group=nobody --prefix=/usr/local/nginx --with-http_stub_status_module --with-http_gzip_static_module --with-http_realip_module --with-http_sub_module --with-http_ssl_module
RUN make && make install

EXPOSE 80