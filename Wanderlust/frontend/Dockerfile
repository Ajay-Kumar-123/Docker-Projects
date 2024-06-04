#Stage-1

FROM node:22 AS frontend-builder

WORKDIR /app

COPY . /app

RUN npm i

#Stage-2

FROM node:22-slim

WORKDIR /app

COPY --from=frontend-builder /app /app

COPY .env.sample .env.local

EXPOSE 5173

CMD [ "npm","run","dev","--","--host" ]