FROM node:18.19.1-alpine3.19
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop 
# adding user to alpine os, create new system(-S) group and adding user to group
WORKDIR /opt/server
#ENV MONGO=true
RUN chown roboshop:roboshop /opt/server
# ownership to /opt/server
USER roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
RUN echo Hello World
RUN adduser cart
CMD ["node", "server.js"]