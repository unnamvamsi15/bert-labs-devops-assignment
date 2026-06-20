FROM node:18-alpine

ENV NODE_ENV=production

WORKDIR /usr/src/app
RUN chown -R node:node /usr/src/app

USER node

COPY --chown=node:node package*.json ./
RUN npm ci --only=production

COPY --chown=node:node . .

EXPOSE 3001

CMD [ "node", "server.js" ]
