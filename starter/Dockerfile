FROM node:21-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

FROM node:21-alpine
WORKDIR /app
COPY --from=build /app .
CMD ["node", "./src/server.js"]
