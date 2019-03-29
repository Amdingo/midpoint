FROM nginx:1.15-alpine

COPY nginx.conf /etc/nginx/nginx.conf
COPY nginx.key /etc/ssl/
COPY nginx.crt /etc/ssl/

EXPOSE 80
EXPOSE 443

CMD ["nginx"]