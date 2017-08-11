# Tutorial here https://nodejs.org/en/docs/guides/nodejs-docker-webapp/
# docker build -t bvi/node-web-app .
# docker-compose -f nodeapp.yml up -d

FROM node:boron-alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package.json .

# RUN npm config set strict-ssl false && \
#	npm config set proxy "http://user:pwd@proxy:3128" && \ 
#	npm config set https-proxy "http://user:pwd@proxy:3128" && \
#	npm install

RUN npm install

# Bundle app source
COPY . .

EXPOSE 8080
CMD [ "npm", "start" ]