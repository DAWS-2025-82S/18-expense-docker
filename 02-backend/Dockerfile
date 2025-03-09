#FROM node:20
FROM node:20.18.3-alpine3.21
# Adding user in alpine
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/backend && \
    chown -R expense:expense /opt/backend
WORKDIR /opt/backend
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
USER expense
COPY package.json ./
COPY *.js ./
RUN npm install
CMD ["node", "index.js"]


# Optimised Docker Image

# docker build -t backend:1.0.0 .

# docker compose up -d
# docker compose down

# docker exec -it  backend sh

# id  # command to check the user


# How do you optimise docker layers?
# ==================================
# 1. less number of layers faster builds, because number of intermediate containers are less
# you can club multiple instructions into single instruction
# 2. keep the frequently changing instructions at the bottom of Dockerfile
