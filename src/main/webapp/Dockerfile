FROM ubuntu:18.04
RUN apt-get update -y && apt-get install net-tools
RUN apt-get install nginx -y
RUN rm -f /etc/nginx/sites-available/* && rm -f /etc/nginx/sites-enabled/*
RUN rm -rf /var/www/html/index.nginx-debian.html 
COPY .  /var/www/
COPY jay.conf /etc/nginx/sites-available/ 
# RUN rm -f /etc/nginx/nginx.conf
# 
RUN ln -s /etc/nginx/sites-available/jay.conf /etc/nginx/sites-enabled/ 
EXPOSE 80
#CMD ["service", "nginx", "start"]
CMD ["nginx", "-g", "daemon off;"]