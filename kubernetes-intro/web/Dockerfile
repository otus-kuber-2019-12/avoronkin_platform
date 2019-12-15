FROM nginx:1.17

COPY nginx/nginx.conf /etc/nginx/nginx.conf

RUN useradd -u 1001 www

RUN touch /var/run/nginx.pid && \
  chown www:www /var/run/nginx.pid && \
  chown www:www /var/cache/nginx

USER www

CMD [ "nginx", "-g", "daemon off;" ]