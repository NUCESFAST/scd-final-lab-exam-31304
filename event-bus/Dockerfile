
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /21I-1103_backend

# Install necessary build dependencies
RUN apk add --no-cache python3 make g++

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose port 4009
EXPOSE 41103

# Command to run the application
CMD ["node", "index.js"]
