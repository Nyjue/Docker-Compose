# Use Node.js base image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package files
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy all application files
COPY . .

# Create directory for the SQLite database
RUN mkdir -p /app/data

# Expose port 5000
EXPOSE 5000

# Start the application
CMD ["npm", "start"]