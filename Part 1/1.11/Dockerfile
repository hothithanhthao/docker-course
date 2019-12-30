FROM ubuntu


RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN bash -c 'echo node -v && npm -v'


COPY backend-example-docker-master /Users/Risa/Desktop/www/backend
WORKDIR /Users/Risa/Desktop/www/backend



RUN npm install

EXPOSE 8000
CMD ["npm", "start"]