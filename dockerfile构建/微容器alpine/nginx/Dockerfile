
FROM alpine:latest
MAINTAINER yang henry
 

#镜像换国内源
RUN echo "http://mirrors.ustc.edu.cn/alpine/v3.3/main/" > /etc/apk/repositories

# install nginx
RUN apk --update add nginx
 
EXPOSE 80
 
CMD ["nginx", "-g", "daemon off;"]

#操作：
# docker build -t henry/nginx:v1
# docker run -d -it -p 8888:80 --name nginx henry/nginx:v1
#docker ps -a 获取容器id
#docker exec -it 容器id /bin/sh
#本地访问 curl http://localhost:8888
