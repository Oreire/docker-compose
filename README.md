# docker-compose
Using Docker Compose to Deploy web application using Nginx image

## Step-by-step implementation:
-   Created an Amazon Linux EC2 Machine with appropriate ssh key and SGs
-   Installed git using the command: sudo yum install git -y 
-   Clone the repository of the home listing web application unto the EC2 machine
-   Installed docker on the ec2: sudo yum install docker -y
-   Started the docker service using the command: sudo service docker start
-   Removed elevated privileges by adding the EC2 machine to the docker group using usermod    
    command: sudo usermod -a -G docker ec2-user
-   Restart the ssh connection to apply changes
-   Downloaded the docker compose to the EC2 machine using the following command:  sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
-   Set the permissions to make the /usr/local/bin/docker-compose file executable using the following 
    command: sudo chmod +x /usr/local/bin/docker-compose
-   Verify the docker-compose installation : docker-compose –version
-   Create the docker-compose file: vim docker-compose.yml
-   Run the docker compose in the background: docker-compose up -d
-   Installed Tree on the Docker-Compose-Node: sudo yum install tree -y


## A file containing the artefacts created has been attached.

## Ongoing Project : Update of Docker Compose file to Deploy a three-tier application. 

   ## Setup:

    -   Nginx will serve as the ##presentation tier (Front-end web server to serve static contents.)

    -   Postgres will undertake the role of the data tier (Backend server) for the storage and 
        managemnet of the application's data.

    -   Python is acting as the application tier, which handles the application's business logic and 
        interacts with the database backend.

    However, the applications'code and design will determine how the Python application communicates
    
    with the web server (Nginx) and database (Postgres): a choce between the use of web frameworks 
    
    like Flask or Django will be pursued based on the requiremnets. 
        