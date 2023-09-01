FROM node:latest

RUN mkdir -p /usr/src/app

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package.json /usr/src/app/

RUN npm install
# If you are building your code for production
# RUN npm ci --omit=dev
ENV NODE_ENV=development
# Bundle app source
COPY /usr/src/app

EXPOSE 8080
CMD [ "npm", "server.js" ]