FROM ubuntu

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN bash -c 'echo node -v && npm -v'

COPY frontend-example-docker-master /Users/Risa/Desktop/www/frontend

WORKDIR /Users/Risa/Desktop/www/frontend

EXPOSE 5000

RUN npm install
RUN npm install -g serve

ENV API_URL=http://localhost:8000
RUN npm run build

CMD ["serve", "-s", "-l", "5000", "dist"]