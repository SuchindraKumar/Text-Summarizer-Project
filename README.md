# End to End Text-Summarizer-Project

## Workflows

1. Update config.yaml
2. Update params.yaml
3. Update entity
4. Update the configuration manager in src config
5. update the conponents
6. update the pipeline
7. update the main.py
8. update the app.py


# How to Run ?

### STEPS:

Clone the Repository

```bash
git clone https://github.com/SuchindraKumar/Text-Summarizer-Project.git
```
### STEP 01- Create a Conda Environment after Opening the Repository

```bash
conda create -n txtsummary python=3.8 -y
```

```bash
conda activate txtsummary
```


### STEP 02- Install the Requirements
```bash
pip install -r requirements.txt
```

### STEP 03- Upgrade Accelerate Package
```bash
pip install --upgrade accelerate
```

### STEP 04- Uninstall Transformers Accelerate Package
```bash
pip uninstall -y transformers accelerate
```

### STEP 05- Install Transformers Accelerate Package
```bash
pip install transformers accelerate
```

# Finally Run the following Command
```bash

python app.py
```

# Now,

```bash
Open Up Your local-host and Port
```


```bash
Author: Suchindra Kumar
Data Scientist
Email: suchindra057@gmail.com

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	# With Specific Access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	# Description: About the deployment

	1. Build Docker Image of the Source Code

	2. Push your Docker Image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	# Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/text-s

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	# Optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	# Required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app