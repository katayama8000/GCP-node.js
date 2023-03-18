FROM node:16-alpine as build
WORKDIR /app
COPY package*.json . 
RUN npm install
COPY . .
RUN npm run build

FROM node:16-alpine
WORKDIR /app
COPY package.json . 
# dependenciesのみをインストール
RUN npm install --only=production
ENV PORT=80
EXPOSE $PORT
COPY --from=build /app/dist ./dist
CMD npm run start:prod