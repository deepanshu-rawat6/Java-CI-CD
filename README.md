# Java-CI-CD
 
 ### Create an EC2 instance using Ubuntu 20.04 LTS
 
 *************************
 # Jenkins shell script
 *************************
 
 ### Make a bash script and copy the contents given below:
 
 #!/bin/bash

 sudo apt update -y

 sudo apt install default-jre -y

 java -version

 sudo apt update -y

 wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -

 curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null

 echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

 sudo apt update -y

 sudo add-apt-repository universe -y

 sudo apt-get install jenkins -y

 sudo service jenkins start

 sudo cat /var/lib/jenkins/secrets/initialAdminPassword
 
### Give permission using **chmod** command 

------------------------------------------------------------------------------------------------------------------
 
 ### To check the status of Jenkins

#sudo service jenkins status

***********************
# Docker shell script
***********************

### Make a bash script and copy the contents given below:

 #!/bin/bash
 sudo apt update -y

 sudo apt install apt-transport-https ca-certificates curl software-properties-common -y

 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

 sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable" -y

 sudo apt update -y

 apt-cache policy docker-ce -y

 sudo apt install docker-ce -y
 
### Give permission using **chmod** command 

-------------------------------------------------------------------------------------------------------------------------

## To check status of Docker

#sudo systemctl status docker

#sudo chmod 777 /var/run/docker.sock

***************************
Kubectl 
***************************

curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && chmod +x ./kubectl && sudo mv ./kubectl /usr/local/bin/kubectl

--------------------------------------------------------------------------------------------------------------------------
