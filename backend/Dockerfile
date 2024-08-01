# Use the official Node.js image as the base image
FROM node:20

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the app dependencies
RUN npm ci

# Copy the rest of the app source code to the working directory
COPY . .

# Expose the port on which the app will run
EXPOSE 3000

# Set the environment variable for the ENV file
ENV ENV_FILE_PATH=/app/.env.backend

# Start the app
CMD ["npm", "start"]