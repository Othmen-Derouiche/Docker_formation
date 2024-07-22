FROM node:17-alpine
# specify a parent image as a first layer : pull the image : node
RUN npm install -g nodemon
# 
WORKDIR /app
# define the working directory
COPY package.json . 

RUN npm install
# run this command at build time to add all dependencies

COPY . .
# copy all source files in /api to the working directory /app

EXPOSE 4000
# required for docker desktop port mapping
# expose the port 4000 by the container not directly to our computer
CMD ["npm", "run" ,"dev"]
# specify the command that will run when the container based on this image run (runtime)