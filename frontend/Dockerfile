# Stage 1: Build Angular
FROM node:18-slim as build
WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build --prod

# Stage 2: Serve via Nginx
FROM nginx:stable-alpine

# Copy ONLY the correct Angular output folder
COPY --from=build /app/dist/angular-15-crud /usr/share/nginx/html

EXPOSE 80
