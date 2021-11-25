FROM node:14-alpine as build
WORKDIR /app
COPY package.json .
COPY package-lock.json .

RUN npm install
COPY . .

ENV VUE_APP_API_ENDPOINT="http://localhost:4001/api"
RUN npm run build

FROM nginx:1.21.4-alpine as prod
COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 5001
CMD ["nginx", "-g", "daemon off;"]