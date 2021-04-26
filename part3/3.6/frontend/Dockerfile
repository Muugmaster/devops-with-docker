FROM node:14-alpine as build-stage

EXPOSE 5000

WORKDIR /usr/src/app/

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

FROM node:14-alpine

WORKDIR /usr/src/app/

RUN npm install -g serve

COPY --from=build-stage /usr/src/app/build/ ./build/

RUN addgroup -S appgroup && adduser -S appuser -G appgroup

USER appuser

CMD ["serve", "-s", "-l", "5000", "build"]