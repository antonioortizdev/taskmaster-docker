# Use the official Node.js image as the base image
FROM node:18.12.1-slim

# Install Vite
RUN npm install -g vite

# Create a directory for the app
RUN mkdir -p /app

# Set the working directory to the app directory
WORKDIR /app

# Copy the package.json file to the app directory
COPY ./package.json /app

# Install the app's dependencies
RUN npm install

# Copy the app's source code to the app directory
COPY . .

# Expose port 8080 to the outside world
EXPOSE 8080

# Run the app using Vite
CMD ["vite", "run"]
