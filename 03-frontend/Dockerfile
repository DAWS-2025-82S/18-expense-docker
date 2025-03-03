FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf
COPY code /usr/share/nginx/html/


# docker build -t frontend:1.0.0 .
# docker run -d -p 80:80 --name frontend --network expense frontend:1.0.0

# docker exec -it frontend bash
# cat /etc/nginx/nginx.conf