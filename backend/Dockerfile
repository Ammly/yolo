FROM node:14-alpine

LABEL Maintainer Ammly

# Create app directory
WORKDIR /usr/src/backend

COPY package*.json ./

RUN npm install

# Bundle app source
COPY . .

EXPOSE 5000

CMD ["node", "server.js"]
