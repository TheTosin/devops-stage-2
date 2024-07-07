# Step 1: Build the React app
FROM node:16 AS build

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Build the React app
RUN npm run build

# Step 2: Serve the React app using Nginx
FROM nginx:alpine

# Copy the built files from the previous stage to the Nginx public directory
COPY --from=build /app/build /usr/share/nginx/html

# Copy custom Nginx configuration if needed
#COPY nginx.conf /etc/nginx/nginx.conf

# Expose port 80
EXPOSE 80

# Start Nginx server
CMD ["nginx", "-g", "daemon off;"]
