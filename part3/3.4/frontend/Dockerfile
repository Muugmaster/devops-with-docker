FROM ubuntu:18.04

EXPOSE 5000

RUN apt-get update && apt-get install curl -y && curl -fsSL https://deb.nodesource.com/setup_14.x | bash - && apt-get install -y nodejs && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /usr/src/app/

COPY package*.json ./

RUN npm install && npm install -g serve

COPY . .

RUN npm run build && useradd -m appuser 

USER appuser

CMD ["serve", "-s", "-l", "5000", "build"]