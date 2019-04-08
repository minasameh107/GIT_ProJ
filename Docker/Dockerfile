FROM nginx:alpine
ARG userid
COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./default.conf /etc/nginx/conf.d/default.conf
RUN chown -R $userid:$userid /var/cache/nginx && \
touch /var/run/nginx.pid && \
chown $userid /var/run/nginx.pid
USER $userid
EXPOSE 8080
CMD nginx
