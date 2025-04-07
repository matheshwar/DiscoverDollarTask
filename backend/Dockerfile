# Stage 1: Build the app
FROM node:18-alpine as builder

WORKDIR /app

# Only copy the files needed to install dependencies
COPY package*.json ./

# Install only production dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# Stage 2: Minimal final image using distroless
FROM gcr.io/distroless/nodejs18-debian11

WORKDIR /app

# Copy the built app from the builder stage
COPY --from=builder /app .

# Specify the Node.js entry point file
CMD ["server.js"]
