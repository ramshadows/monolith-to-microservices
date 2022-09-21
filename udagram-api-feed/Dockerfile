FROM node:12
# Create app directory
RUN mkdir -p  /usr/src/app
# Create app directory
WORKDIR /usr/src/app
#RUN touch /usr/src/app/package.json

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json /usr/src/app/

RUN ls -la

# Bundle app source
COPY . .

RUN npm ci 


EXPOSE 8080
CMD [ "npm", "run", "prod" ]