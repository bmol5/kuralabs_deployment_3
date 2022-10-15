<h1 align=center><strong><em>Deployment 3</em></strong></h1>
<div align=left>This repository will contain information related to the deployment of the URL-shortner flask application. Details can be found in the Deployment instructions or the documentation linked below.</div>


## Location of Documentation:
* Deployment Document: [click here](https://github.com/bmol5/kuralabs_deployment_3/blob/main/Documentation/Deployment3.pdf)

## Deployment Objectives:
``` diff
+ [x] Gain familiarity with VPC’s and subnets.
+ [x] Understand the role of the Jenkins agent and controller.
+ [x] Understand the role Nginx and Gunicorn play in application deployment.
+ [x] Understand reverse proxy and the configurations needed to deploy our flask application.
```

## Code Used:

### Jenkins Installation:
```
#!/bin/bash

sudo apt update
sudo apt -y install openjdk-11-jre
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get -y install jenkins
sudo systemctl enable jenkins
sudo systemctl start jenkins
```

### Nginx Installation:
```
sudo apt -y update
sudo apt -y install
sudo apt install -y default-jre 
sudo apt install -y python3-pip
sudo apt install -y python3.10-venv 
sudo apt install -y nginx
```

### Mypy Installation:
```
python3 -m pip install mypy
mypy –show-error-codes application.py 
```
