# Step 1: Build the React app
FROM node:18-alpine3.18

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
CMD npm run dev -- --host 0.0.0.0
