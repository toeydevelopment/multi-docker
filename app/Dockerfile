FROM node:alpine as builder

WORKDIR /worker

COPY package.json .

RUN npm i

COPY . .

RUN npm run build

EXPOSE 3000

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

FROM nginx:latest


COPY --from=builder /app/build /usr/share/nginx/html 