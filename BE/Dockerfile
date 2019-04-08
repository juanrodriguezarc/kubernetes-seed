#Stage 1: build angular project
FROM node:8 as builder

COPY myapp /myapp
WORKDIR /myapp

RUN npm install

COPY --chown=node:node . .

CMD [ "node", "app.js" ]

EXPOSE 4000