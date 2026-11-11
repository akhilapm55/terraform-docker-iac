
# Terraform Docker Infrastructure

## Project Overview
This project demonstrates Infrastructure as Code (IaC) using Terraform to provision and manage a local Docker container.

## Tools Used
- Terraform
- Docker
- Git
- GitHub
- Nginx

## Project Architecture
Terraform communicates with Docker Desktop through the Docker provider.

It performs the following operations:
1. Downloads the Nginx Docker image.
2. Creates a Docker container named `terraform-nginx`.
3. Maps host port 8081 to container port 80.
4. Makes the Nginx web server accessible through a browser.

## Project Setup

### 1. Initialize Terraform
```bash
terraform init
```

### 2. Preview Infrastructure Changes
```bash
terraform plan
```

### 3. Create Infrastructure
```bash
terraform apply
```

### 4. Verify Running Container
```bash
docker ps
```

Open http://localhost:8081 to verify the Nginx welcome page.

### 5. Inspect Terraform State
```bash
terraform state list
terraform state show docker_container.nginx
```

### 6. Destroy Infrastructure
```bash
terraform destroy
```

## Git Branching Strategy
- `main` - Stable project version
- `dev` - Development and integration
- `feature/documentation` - Documentation changes

Changes are developed in feature branches and merged through GitHub Pull Requests.

## Learning Outcomes
- Understanding Infrastructure as Code
- Working with Terraform providers and resources
- Managing Docker containers using Terraform
- Understanding Terraform state
- Practising Git branching and Pull Requests
