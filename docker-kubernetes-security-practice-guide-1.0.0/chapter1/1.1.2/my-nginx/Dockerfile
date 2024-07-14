FROM nginx:1.17-alpine
RUN mkdir /html
COPY index.html /html
COPY cert.pem /etc/nginx/cert.pem
COPY ssl.conf /etc/nginx/conf.d/ssl.conf
