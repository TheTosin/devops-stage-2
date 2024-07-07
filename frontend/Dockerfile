# Step 1: Build the React app
FROM node:14-alpine build

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json to the working directory
COPY package*.json ./
COPY package-lock.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . ./

# Run the build and capture output
RUN npm run build && echo "Build succeeded" || (echo "Build failed" && exit 1)

# Step 2: Serve the React app using Nginx
FROM nginx:alpine

# Expose port 5173
EXPOSE 5173
