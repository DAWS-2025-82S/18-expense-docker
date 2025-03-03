FROM node:20
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
CMD ["node", "index.js"]


# set DB_HOST="msql container name" because the container IP changes if contianer is restarted

# docker build -t backend:1.0.0 .
# docker run -d --name backend backend:1.0.0

# docker logs backend

# backend app cannot connect to mysql DB because of docker default network 

# if you are using default n/w docker containers can't communicate with each other

# For containers to communicate we need to create network