FROM nginx:1.30.6-alpine

COPY ./hallow.conf.template /etc/nginx/templates/hallow.conf.template

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
