FROM node:14-alpine

EXPOSE 5000

WORKDIR /usr/src/app/

COPY package*.json ./

RUN npm install && npm install -g serve

COPY . .

RUN addgroup -S appgroup && adduser -S appuser -G appgroup && npm run build

USER appuser

CMD ["serve", "-s", "-l", "5000", "build"]