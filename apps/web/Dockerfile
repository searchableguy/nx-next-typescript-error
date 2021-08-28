FROM node:lts-alpine

ENV PORT=3000

WORKDIR /app

COPY ./dist/apps/web/package.json .

RUN npm install --production

COPY ./dist/apps/web .

EXPOSE ${PORT}

CMD npm run start