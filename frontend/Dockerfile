# Dockerfile for Next.js Application

# Use Node.js 18 as the base image
FROM node:18

# Set the working directory
WORKDIR /app

# Copy package.json and yarn.lock (if available)
COPY package.json .
COPY yarn.lock .

# Install dependencies
RUN yarn install --frozen-lockfile

# Copy the rest of the application files
COPY . .

# Build the Next.js application
RUN yarn build

# Start the application
CMD [ "yarn", "start" ]
