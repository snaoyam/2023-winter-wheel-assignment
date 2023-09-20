FROM node:16-alpine3.11

LABEL org.opencontainers.image.source=https://github.com/snaoyam/2023-winter-wheel-assignment/tree/main

COPY . /app

WORKDIR /app

EXPOSE 5001
ENV PORT 5001

RUN npm ci
ENTRYPOINT ["npm", "run", "serve"]
