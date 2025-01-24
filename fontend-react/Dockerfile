# Use a lightweight Node.js base image
FROM node:alpine as build

# Set the working directory
WORKDIR /poc

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the app source code
COPY . .

# Build the app for production
RUN npm run build

# Use a lightweight web server to serve the build
FROM nginx:1.23-alpine

# Copy the built files from the previous stage
COPY --from=build /poc/build /usr/share/nginx/html

# Expose the port Nginx runs on
EXPOSE 3000

# Start the server
CMD ["nginx", "-g", "daemon off;"]
