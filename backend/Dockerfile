# Use a lightweight Node image
FROM node:14-alpine

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the backend code
COPY . .

# Expose the port your backend runs on
EXPOSE 5000

# Start the server
CMD ["npm", "start"]
