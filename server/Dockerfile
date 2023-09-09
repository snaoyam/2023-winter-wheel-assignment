FROM node:16-alpine3.11

COPY . /app

WORKDIR /app

EXPOSE 5000
ENV PORT 5000

RUN npm ci
ENTRYPOINT ["npm", "run", "serve"]
