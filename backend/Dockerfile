FROM node:18

WORKDIR /app

# Copy package files first for better caching
COPY package*.json ./

RUN npm install

# Copy all other files
COPY . .

CMD ["node", "server.js"]