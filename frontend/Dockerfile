# Use Node.js version 21 as the base image
FROM node:21

# Set the working directory inside the container
WORKDIR /frontend

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Copy .env.sample as .env.local for local environment setup
COPY .env.sample .env.local

# Expose the port the app runs on
EXPOSE 3000

# Command to start the development server
CMD ["npm", "run", "dev", "--", "--host"]

