# Use an official Node.js runtime as the base image
FROM node:19-bullseye

# Set the working directory in the container
WORKDIR /

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# BUILD
RUN npm run build

# Expose the port the app runs on
EXPOSE 3000

# Define the command to run your application
CMD ["npm", "run", "start"]
