Kubernetes Multi-Tier Application Deployment - Lab 6

Overview

This project demonstrates the deployment of a multi-tier application using Kubernetes and Minikube.

The application contains:

- Frontend tier using Nginx
- API tier using Httpbin
- Cache tier using Redis
- Database tier using PostgreSQL



Kubernetes Components Used

Pods

Pods are the smallest deployable units in Kubernetes. They run the application containers.

Used Pods:

- Frontend Pods
- API Pods
- Redis Pod
- PostgreSQL Pod



Deployments

Deployments manage application replicas, scaling, self-healing and rolling updates.

Created Deployments:

- Frontend Deployment
- API Deployment
- Redis Deployment


Services

Services provide stable network access to Pods.

Created Services:

- Frontend NodePort Service
- API ClusterIP Service
- Redis ClusterIP Service
- PostgreSQL Headless Service



StatefulSet

StatefulSet is used for PostgreSQL because databases require stable identities and persistent storage.

Created:

- PostgreSQL StatefulSet



Persistent Volume Claim (PVC)

PVC provides persistent storage for PostgreSQL data.

Storage:

- PostgreSQL PVC (1Gi)



ConfigMap and Secret

ConfigMap:

- Stores application configuration values.

Secret:

- Stores sensitive information such as database credentials.



Network Policy

NetworkPolicy controls communication between Pods and improves application security.

Implemented:

- API Network Policy



How to Run the Application

1. Start Minikube

```bash
minikube start --driver=docker
