# Set the base image to Node 14 with Alpine
FROM node:14-alpine

# Set the working directory to /app
WORKDIR /app

# Copy the entire project to the container
COPY . .

# Install the dependencies using npm
RUN npm install

# Expose port 1004 for the application
EXPOSE 1004

# Start the application using the `node` command
CMD ["node", "index.js"]










# FROM node:14
# WORKDIR /app 
# COPY . .
# RUN npm install
# EXPOSE 1004
# CMD ["node","index.js"]