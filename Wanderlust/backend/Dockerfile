#Stage-1

FROM node:22 AS backend-builder

WORKDIR /app

COPY . /app

RUN npm i

#Stage-2

FROM node:22-slim

WORKDIR /app

COPY --from=backend-builder /app /app

COPY .env.sample .env

EXPOSE 5000

CMD [ "npm","start" ]

