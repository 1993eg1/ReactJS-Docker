# Use an official Node.js runtime as a parent image
FROM node:14-alpine

# Set the working directory to /app
WORKDIR /app

# Install dependencies
RUN npm install

# Build the React app
RUN npx create-react-app my-app --scripts-version 1.1.5

# Set the working directory to /app
WORKDIR /app/my-app

# Set the command to start the server
CMD ["npm", "start"]
