FROM node:alpine

WORKDIR /worker

COPY package.json .

RUN npm i


COPY . .

CMD ["npm","run","start"]
