FROM node:lts-alpine AS development

WORKDIR /vue/src/app

COPY package*.json ./

RUN npm install -g npm@8.8.0
# RUN npm uninstall vue-cli -g
RUN npm install -g @vue/cli@5.0.4


COPY . .

RUN  chown -R root:root /vue/src/app/node_modules
RUN chmod -R 775 /vue/src/app/node_modules

RUN npm run build

EXPOSE 4200

