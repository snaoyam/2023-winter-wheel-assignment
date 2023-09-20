FROM node:16-alpine3.11
WORKDIR /app
COPY ./client .

EXPOSE 3000
ENV PORT 3000

RUN npm ci
RUN npm run build
ENTRYPOINT npx react-inject-env set && npx serve -s build -l 3000