# Use Node.js LTS
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Build the application
RUN npm run build

# Expose port (NestJS default is usually 3000 or 3001)
EXPOSE 3001

# Start the server
CMD ["npm", "run", "start:prod"]
