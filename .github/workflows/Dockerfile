FROM node:lts-alpine

RUN mkdir -p /home/node/chat-application/node_modules && chown -R node:node /home/node/chat-application

WORKDIR /home/node/chat-application

COPY package.json yarn.* ./

USER node

RUN yarn install --production

COPY --chown=node:node . .

EXPOSE 3000

CMD ["node", "server.js"]