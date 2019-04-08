#Stage 1: build angular project
FROM node:8 as builder

COPY myAppFe /myAppFe
WORKDIR /myAppFe

RUN npm install
RUN $(npm bin)/ng build

#Stage 2: serve application:
FROM nginx

COPY --from=builder /myAppFe/dist/* /usr/share/nginx/html

EXPOSE 80

