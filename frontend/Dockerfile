# Stage 1: Build React app
FROM node:20 as build

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci --silent

COPY . .
RUN mv .env.frontend .env
RUN npm run build

# Stage 2: Serve app with Nginx
FROM nginx:1.21-alpine

COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]