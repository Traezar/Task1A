FROM nginx:alpine

COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html ./
RUN apk update && apk add bash

# send error to docker logs
RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/err.log


EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]