# Base image
FROM node:22-alpine

# Create app directory
WORKDIR /usr/src/app

# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./

# Install app dependencies
RUN npm install

# Bundle app source
COPY . .

# Creates a "dist" folder with the production build
RUN npm run build

RUN npx prisma generate

# Expose the port on which the app will run
EXPOSE 3001

# Start the server using the production build
CMD ["npm", "run", "start:prod"]