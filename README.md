# mynodejsproject
# Node.js Web Application Deployment with Docker

## Task
Create a Dockerfile for a simple web application written in Node.js. The objective is to build a Docker image for the application, push it to GitHub, and deploy it on an AWS EC2 instance.

## Steps

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/NEELOFARKHAN22/nodejsApp.git
   cd nodejsApp
Dockerfile Creation:

**Created a Dockerfile with the following specifications:
--> dockerfile
      
      Copy code
      FROM node:14
      WORKDIR /app
      COPY package*.json ./
      RUN npm install
      COPY . .

      EXPOSE 3000
      CMD ["node", "index.js"]

--> GitHub Repository:

1. Forked the repository: https://github.com/NEELOFARKHAN22/nodejsApp.git
2. Added Dockerfile and README.md.
3. Committed changes and pushed to the repository.

--> AWS EC2 Instance:

1. Launched an EC2 instance with Node.js installed.
2. Configured security groups to allow inbound traffic on port 3000.

--> Deployment:

1. Deployed the Docker container on the EC2 instance.
2. Ensured the application is running on port 3000.
   
--> Dockerfile Overview

1. Used the official Node.js base image.
2. Set the working directory to /app.
3. Copied package.json and package-lock.json for efficient caching.
3. Installed dependencies using npm install.
4. Exposed port 3000.
5. Used a non-root user (node) to run the application.
6. Started the application with the command CMD ["node", "index.js"].
7. Accessing the Application
8. Visit http://3.7.254.19:3000 in your browser to access the web application.

--> Troubleshooting
1. If the site can't be reached, check Docker container logs, and security group settings, and verify the application code.
   



