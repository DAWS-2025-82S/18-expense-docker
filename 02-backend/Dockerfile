#FROM node:20
FROM node:20.18.3-alpine3.21 AS builder
WORKDIR /opt/backend
COPY package.json ./
COPY *.js ./
RUN npm install


FROM node:20.18.3-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/backend && \
    chown -R expense:expense /opt/backend
ENV DB_HOST="mysql"
WORKDIR /opt/backend
USER expense
COPY --from=builder /opt/backend /opt/backend
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

# docker multi stage builds