FROM nginx:alpine
# Install htpasswd
RUN apk add apache2-utils
# Create username: admin / password: admin in file /etc/nginx/passwd/htpasswd 
RUN htpasswd -b -c /etc/nginx/passwd/htpasswd admin admin
COPY nginx.conf /etc/nginx/