FROM node:16-alpine3.11
WORKDIR /app
COPY . .

EXPOSE 3000
ENV PORT 3000

RUN npm ci
RUN npm run build
RUN npx react-inject-env set
ENTRYPOINT ["npx", "serve", "-s", "build", "-l", "3000"]
# ENTRYPOINT ["sh", "-c", "npx react-inject-env set && npx serve -s build -l 3000"]