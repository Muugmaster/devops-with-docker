FROM node:14

EXPOSE 5000

ENV REACT_APP_BACKEND_URL=http://localhost:8080

WORKDIR /usr/src/app/

COPY package*.json ./

RUN npm install

RUN npm install -g serve

COPY . .

RUN npm run build


CMD ["serve", "-s", "-l", "5000", "build"]