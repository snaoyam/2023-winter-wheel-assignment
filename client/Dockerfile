FROM node:16-alpine3.11

LABEL org.opencontainers.image.source=https://github.com/snaoyam/2023-winter-wheel-assignment/tree/main

COPY . /app

WORKDIR /app

EXPOSE 3000
ENV PORT 3000

RUN npm ci
RUN npm run build
RUN npx react-inject-env set
ENTRYPOINT ["npx", "serve", "-s", "build", "-l", "3000"]
# ENTRYPOINT ["sh", "-c", "npx react-inject-env set && npx serve -s build -l 3000"]