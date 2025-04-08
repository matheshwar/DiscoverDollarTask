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
