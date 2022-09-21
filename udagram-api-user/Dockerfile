FROM node:12
# Create app directory
RUN mkdir -p app
WORKDIR /app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json /app/
# Bundle app source
COPY . .

RUN npm ci 



EXPOSE 8080
CMD [ "npm", "run", "prod" ]