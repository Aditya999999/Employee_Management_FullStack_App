FROM node:18-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

RUN npm install -g serve
ENV PM2_HOME /app
CMD ["serve", "-s", "build", "-l", "3000"]
EXPOSE 3000
