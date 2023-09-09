FROM node:16-alpine3.11

COPY . /app

WORKDIR /app

EXPOSE 80
ENV PORT 80

RUN npm ci
RUN npm run build
RUN npx react-inject-env set
ENTRYPOINT ["npx", "serve", "-s", "build", "-l", "80"]