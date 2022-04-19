FROM node:17.7

COPY . /code
WORKDIR /code
ENV NODE_OPTIONS=--openssl-legacy-provider
RUN rm -Rf /code/node_modules/*
RUN npm install -g typings webpack-dev-server rimraf webpack
RUN npm install
EXPOSE 4200

CMD ["npm", "start"]
