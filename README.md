Project Overview

In this project, I have deployed a full-stack MEAN application using Docker for containerization, Nginx as a reverse proxy, and set up a CI/CD pipeline using GitHub Actions for automated build and deployment. The primary objective was to make the application easily deployable and scalable while ensuring smooth deployment through automated pipelines.

Prerequisites

  • Before you begin, ensure you have the following installed on your machine:
   
  • Docker: For containerizing the application
    
  • Docker Compose: For managing multi-container Docker applications
    
  • Git: For cloning the repository
    
  • Nginx: For setting up the reverse proxy
    
  • AWS EC2 : For deploying to the cloud

Dockerized the Application:
    
  • I wrote Dockerfiles for both the frontend and backend services, allowing them to run as containers.
  
  • Here I have attach some images of docker build stage for frontend 
    ![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/frontend1.png?raw=true)
    ![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/frontend9.png?raw=true)
    ![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/frontend10.png?raw=true)

  • Created a Docker Compose file to manage the entire multi-container application. This ensures that all services (frontend, backend, MongoDB) are spun up and connected seamlessly.

Set Up Nginx as a Reverse Proxy:

• I configured Nginx as a reverse proxy to route traffic from port 80 (HTTP) to the frontend and backend containers.


• The Nginx configuration ensures that requests to the root of the domain go to the frontend, while requests to /api/ are routed to the backend.
![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/nginx%20conf1.png?raw=true)
![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/nginx%20conf2.png?raw=true)
• I made the necessary adjustments in the Nginx configuration to optimize the application for scalability and security.

 
Configured CI/CD Pipeline with GitHub Actions:

• I set up a CI/CD pipeline using GitHub Actions to automate the process of building Docker images, pushing them to Docker Hub, and deploying the latest version of the application to an EC2 instance.
![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/cicd1.png?raw=true)
![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/cicd2.png?raw=true)
![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/cicd3.png?raw=true)

• The pipeline is triggered on every push to the main branch, ensuring that the latest version of the code is built and deployed automatically.

Deployed the Application to EC2:

• I created an AWS EC2 instance to host the application in a cloud environment.


• I installed Docker, Nginx, and configured the security groups to allow traffic on ports 80, 8081, and 8082.


• The application was deployed to EC2 using the GitHub Actions pipeline, and the application is now accessible via the public IP of the EC2 instance.


Implemented Automated Docker Image Builds and Pushes:
• The CI/CD pipeline is configured to build Docker images for both the frontend and backend services upon changes to the code.


• The images are then automatically pushed to Docker Hub


Configured Nginx on EC2:

• The Nginx reverse proxy was set up on the EC2 instance, allowing the application to be accessed on port 80.


• Nginx forwards requests to the appropriate Docker container (frontend or backend), ensuring smooth routing of client requests to the correct service.

Monitored and Troubleshot:

• I ran various tests to ensure that all services (frontend, backend, MongoDB) are properly connected and accessible.


• I used tools like curl and docker ps to verify the connectivity and ensure that all services are running correctly within the containers.


• I troubleshot common issues like port conflicts and firewall configurations, ensuring the application is secure and accessible via the EC2 instance's public IP.

Conclusion

This project showcases a fully functional MEAN stack application with Docker-based deployment, a reverse proxy setup using Nginx, and a CI/CD pipeline for automated deployment. By using Docker, I was able to ensure the application is portable and can be deployed on any system with Docker support. The CI/CD pipeline ensures that the application is always up to date with the latest changes, while Nginx optimizes the routing and scalability of the application.


This setup is fully automated, reducing manual intervention and making the deployment process faster and more reliable.
![Alt Text](https://github.com/matheshwar/DiscoverDollarTask/blob/main/Screenshots/webpage.png?raw=true)
