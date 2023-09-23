FROM node:16-alpine3.11
WORKDIR /app
COPY ./server .

EXPOSE 5001
ENV PORT 5001

RUN npm ci
ENTRYPOINT ["npm", "run", "serve-dev"]
