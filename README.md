# github-actions-intelligent-matrix-deployment
Intelligent GitHub Actions CI/CD pipeline that automatically detects changed microservices, dynamically generates deployment matrices, builds Docker images in parallel, pushes them to Amazon ECR, and updates AWS ECS using CloudFormation.


**Repository Topics**

github-actions
aws
ecs
ecr
cloudformation
docker
microservices
devops
cicd
platform-engineering
matrix
parallel-deployment
automation
oidc
aws-devops

**ntelligent Matrix Deployment Engine**
Overview

Modern enterprise applications are built using dozens of independent microservices.

A common problem with traditional CI/CD pipelines is that every commit triggers deployment of every service, even if only one service changed.

This project solves that problem by introducing an Intelligent Matrix Deployment Engine using GitHub Actions.

Instead of deploying everything, the pipeline analyses Git changes and deploys only the required services.

If a shared component changes, the pipeline automatically deploys every dependent microservice in parallel.

**Repository Structure**
github-actions-intelligent-matrix-deployment

│
├── .github
│   └── workflows
│       └── intelligent-matrix.yml
│
│
├── backend
│   ├── shared
│   └── services
│       ├── AAA
│       ├── BBB
│       ├── CCC
│       ├── DDD
│       ├── EEE
│       ├── FFF
│       ├── GGG
│       └── HHH
│
├── AWS-Cloudformation
│
├── README.md
└── .gitignore
