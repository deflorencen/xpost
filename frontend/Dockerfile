FROM node:18-alpine

WORKDIR /xpost/

COPY public/ /xpost/public
COPY src/ /xpost/src
COPY package.json /xpost/

RUN npm install

CMD ["npm", "start"]