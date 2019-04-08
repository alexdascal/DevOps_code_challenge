FROM nginx

# You need to mend that config
COPY config/nginx.conf /etc/nginx/nginx.conf

# You need to put the server config here
COPY config/conf.d/* /etc/nginx/conf.d/

# You need to put any scripts here
ADD files/bin/* /usr/local/bin/

HEALTHCHECK --interval=15s --timeout=5s --start-period=30s CMD curl -sf http://localhost/ || exit 1

# Start NGINX
RUN nginx -g "daemon off;"