
# MongoDB Deployment with Kubernetes


This repository contains Kubernetes configuration files to deploy MongoDB and MongoDB Express using Kubernetes. The provided files include deployment configurations, services, a ConfigMap for MongoDB configuration, and a Secret for sensitive data.

## Files Included
- `mongo-depl.yaml`: Kubernetes Deployment configuration for MongoDB.
- `mongo-express.yml`: Kubernetes Deployment configuration for MongoDB Express.
- `mongodb-configmap.yml`: Kubernetes ConfigMap configuration for MongoDB.
- `mongo-secret.yaml`: Kubernetes Secret configuration for storing sensitive data.

## Prerequisites

Before using these files, make sure you have the following set up:

1. Kubernetes cluster up and running with `minikube start`.
2. `kubectl` command-line tool installed and configured to interact with your cluster.
3. Docker images for MongoDB and MongoDB Express accessible.


## Instructions

1. **Clone this repository** to your local machine:

    ```bash
    git clone https://github.com/MrRfifa/MongoDB-MongoExpress-Kubernetes
    ```

2. **Navigate to the cloned directory**:

    ```bash
    cd MongoDB-MongoExpress-Kubernetes
    ```

3. **Apply the Kubernetes configurations** in the following order:

    ```bash
    kubectl apply -f mongodb-secret.yaml
    kubectl apply -f mongodb-configmap.yml
    kubectl apply -f mongo-depl.yaml
    kubectl apply -f mongo-express.yml
    ```

4. **Access MongoDB Express**:

    After applying the configurations, you can access the MongoDB Express interface using the following command:

    ```bash
    minikube service mongo-express-service
    ```

5. **Cleaning up**:

    When you're done with your work, clean up the resources by deleting the applied configurations:

    ```bash
    kubectl delete -f mongo-express.yml
    kubectl delete -f mongo-depl.yaml
    kubectl delete -f mongodb-configmap.yml
    kubectl delete -f mongodb-secret.yaml
    ```
