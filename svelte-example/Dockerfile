# Base image
FROM node:18-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the entire project
COPY . .

# Build the Svelte app
RUN npm run build

# Expose the port
EXPOSE 3000

# Start the app
CMD ["npm", "run", "dev"]