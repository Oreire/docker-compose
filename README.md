# docker-compose
Using Docker Compose to Deploy web application using Nginx image

Step-by-step implementation:
1.	Created an Amazon Linux EC2 Machine with appropriate ssh key and SGs
2.	Installed git using the command: sudo yum install git -y 
3.	Clone the repository of the home listing web application unto the EC2 machine
4.	Installed docker on the ec2: sudo yum install docker -y
5.	Started the docker service using the command: sudo service docker start
6.	Removed elevated privileges by adding the EC2 machine to the docker group using usermod command: sudo usermod -a -G docker ec2-user
7.	Restart the ssh connection to apply changes
8.	Downloaded the docker compose to the EC2 machine using the following command:  sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
9.	Set the permissions to make the /usr/local/bin/docker-compose file executable using the following command: sudo chmod +x /usr/local/bin/docker-compose
10.	Verify the docker-compose installation : docker-compose –version
11.	 Create the docker-compose file: vim docker-compose.yml
12.	Run the docker compose in the background: docker-compose up -d
13.	 Installed Tree on the Docker-Compose-Node: sudo yum install tree -y


A file containing the artefacts created has been attached.
