FROM nginx
ARG ENVIRONMENT
ARG API_DOMAIN
ADD ./docker/nginx/scripts/configure-$ENVIRONMENT.sh /configure.sh
# Update Nginx server block with correct domains for API
ADD ./docker/nginx/$ENVIRONMENT.conf /etc/nginx/conf.d/default.conf
RUN ["chmod", "+x", "/configure.sh"]
RUN /configure.sh
