FROM ubuntu
MAINTAINER zhimin.tangzm zhimin.tangzm@alibaba-inc.com
COPY sources.list /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y curl tar make gcc wget
RUN cd /usr/local/src && \
	wget http://ddbmh1.oss.aliyuncs.com/redis-2.8.19.tar.gz && \
	tar xf redis-2.8.19.tar.gz && \
	cd redis-2.8.19 && \
	make && \
	make install
EXPOSE 6379
CMD ["/usr/local/bin/redis-server"] 

