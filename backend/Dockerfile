# Use official Node.js LTS version as base image
FROM node:18

# Set working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json first (for caching dependencies)
COPY package*.json ./

# Install dependencies (only production dependencies)
RUN npm install --production

# Copy the rest of the application code
COPY . .

# Expose the port your app uses (change if different)
EXPOSE 3000

# Command to run the app
CMD ["npm", "start"]
