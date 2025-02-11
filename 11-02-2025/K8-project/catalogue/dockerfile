FROM node:18.19.1-alpine3.19
EXPOSE 8080
RUN addgroup -S sarushop && adduser -S sarushop -G sarushop
WORKDIR /opt/server
RUN chown sarushop:sarushop /opt/server
USER sarushop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]