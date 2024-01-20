# Base Image
FROM ubuntu 

# Install nodejs
RUN apt-get update 
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -
RUN apt-get update
RUN apt-get install -y nodejs

# Copy the files
COPY package.json package.json
COPY package-lock.json package-lock.json
COPY main.js main.js

# Install the dependencies
RUN npm install

# Run the app
ENTRYPOINT [ "node", "main.js" ]

# Build the image