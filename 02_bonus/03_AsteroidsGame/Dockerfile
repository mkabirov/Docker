FROM alpine

RUN apk add --update nodejs nodejs-npm

COPY src /src

WORKDIR /src

RUN npm install

EXPOSE 3000

ENTRYPOINT ["node", "./app.js"]

#Retro "Asteroids" Game containerization
#first JS app was downloaded
#setting env to run app with NodeJS

#build&run

#docker build –t asteroids .
#docker run -d -p 3000:3000 asteroids

#run the game via web browser ip&port