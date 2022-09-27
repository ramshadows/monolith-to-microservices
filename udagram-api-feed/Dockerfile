FROM node:16.17.1-alpine

RUN node -v
# Create app directory
WORKDIR /usr/src/app


# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY ./udagram-api-feed/package*.json ./

# update npm to the latest version
RUN npm install -g npm@latest
RUN npm install
# Bundle app source
COPY . .

EXPOSE 8080
CMD [ "npm", "run", "prod" ]