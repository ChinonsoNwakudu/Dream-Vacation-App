FROM node:16-alpine

# Install serve globally
RUN npm install -g serve

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Build the app
RUN npm run build

# Expose port 3000
EXPOSE 3000

# Serve the built app
CMD ["serve", "-s", "build", "-l", "3000"]