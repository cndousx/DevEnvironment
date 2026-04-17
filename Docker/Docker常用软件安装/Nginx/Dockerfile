FROM nginx:1.30.0

LABEL maintainer="dousx_cn@163.com"
LABEL author="dousx"
LABEL description="自定义nginx镜像，配置了时区、ping 和 vim"

# 设置时区为上海
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install -y vim     
RUN apt-get install -y iputils-ping

# 备份默认配置文件
RUN mv /etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf.bak

RUN nginx -t