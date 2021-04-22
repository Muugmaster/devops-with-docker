FROM node:14

EXPOSE 5000

WORKDIR /usr/src/app/

COPY package*.json ./

RUN npm install

RUN npm install -g serve

COPY . .

RUN npm run build

RUN useradd -m appuser 

USER appuser

CMD ["serve", "-s", "-l", "5000", "build"]