# frontend/Dockerfile
FROM node:22

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . ./

# Expose the port that the React app uses
EXPOSE 3000

# Start the React development server
CMD ["npm", "start"]
