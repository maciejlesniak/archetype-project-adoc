FROM nginx:stable-alpine-slim

COPY target/html/ /usr/local/share/html/
COPY nginx/docs.conf /etc/nginx/conf.d/docs.conf

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
