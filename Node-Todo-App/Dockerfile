#Base image with NodeJS
FROM node:12.2.0-alpine

#Create working directory
WORKDIR /app

#Copy code from source directory to app directory
COPY . /app

#Install npm 
RUN npm install

#Run the container
CMD ["node","app.js"]
