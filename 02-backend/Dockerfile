#FROM node:20
FROM node:20.18.3-alpine3.21
# Adding user in alpine
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/backend
RUN chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
USER expense
CMD ["node", "index.js"]


# Optimised Docker Image

# docker build -t backend:1.0.0 .

# docker compose up -d
# docker compose down

# docker exec -it  backend sh

# id  # command to check the user

