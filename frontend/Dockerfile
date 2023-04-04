# base image
FROM node:16.20.0-alpine

# set working directory
WORKDIR /app

# copy package.json and package-lock.json
COPY package*.json ./

# install dependencies
RUN npm install

# copy app files
COPY . .

# build production-ready app
RUN npm run build

# serve the app
CMD ["npm", "start"]