# MongoDB Deployment with Kubernetes

This repository contains Kubernetes configuration files to deploy MongoDB and MongoDB Express using Kubernetes. The provided files include deployment configurations, services, a ConfigMap for MongoDB configuration, and a Secret for sensitive data.

## Files Included

- `mongo-depl.yaml`: Kubernetes Deployment configuration for MongoDB.
- `mongo-express.yml`: Kubernetes Deployment configuration for MongoDB Express.
- `mongodb-configmap.yml`: Kubernetes ConfigMap configuration for MongoDB.
- `mongo-secret.yaml`: Kubernetes Secret configuration for storing sensitive data.

## Prerequisites

Before using these files, make sure you have the following set up:

1. Kubernetes cluster up and running.
2. `kubectl` command-line tool installed and configured to interact with your cluster.
3. Docker images for MongoDB and MongoDB Express accessible.

## Instructions

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/your-repo.git

2. Navigate to the cloned directory:
   ```bash
   cd your-repo

3. Apply the Kubernetes configurations using "kubectl" with order:
  ```bash
  kubectl apply -f mongodb-secret.yaml
  kubectl apply -f mongodb-configmap.yml
  kubectl apply -f mongo-depl.yaml
  kubectl apply -f mongo-express.yml
