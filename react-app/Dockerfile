FROM node:16

# Set the working directory in the container
WORKDIR /app

# Copy the package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . ./

# Build the React app for production
RUN npm run build

# Expose the port the app will run on
EXPOSE 3000

# Run the app on the development server
CMD ["npm", "start"]
