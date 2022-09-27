FROM node:16-alpine

# Create app directory
WORKDIR /usr/src/app
#RUN touch /usr/src/app/package.json

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./

# update npm to the latest version
RUN npm install -g npm@latest
RUN npm ci 

# Bundle app source
COPY . .

EXPOSE 8080
CMD [ "npm", "run", "prod" ]