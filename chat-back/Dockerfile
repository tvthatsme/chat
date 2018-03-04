FROM node:latest

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY package.json /usr/src/app/

ADD src /usr/src/app/src
ADD database /usr/src/app/database

RUN npm install
RUN yarn prisma deploy

CMD [ "npm", "start" ]