# Nginx reverse proxy Dockerfile for vProfile
FROM nginx
LABEL "Project"="Vprofile"
LABEL "Author"="Divyanshu"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf