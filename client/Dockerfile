FROM node:14-alpine

LABEL Maintainer Ammly

# Create app directory
WORKDIR /usr/src/client

COPY package*.json ./

RUN npm install

# Bundle app source
COPY . .
RUN npm run build
RUN npm install -g serve
EXPOSE 3000
CMD [ "serve", "-s", "build", "-l", "3000" ]