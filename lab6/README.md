# Kubernetes Lab 6 - Multi-Tier Application Deployment

Overview

This lab demonstrates deploying a multi-tier application using Kubernetes and Minikube.

Application components:

- Frontend using Nginx
- API service using Httpbin
- Redis cache
- PostgreSQL database

Kubernetes Resources Used

- Pods
- Deployments
- Services
- StatefulSet
- PersistentVolumeClaim (PVC)
- ConfigMap
- Secret
- NetworkPolicy

Deployment

Start Minikube:

minikube start --driver=docker

Apply manifests:

kubectl apply -f k8s/

Check resources:

kubectl get pods
kubectl get services

Tests Performed
Pod self-healing after deletion
Deployment scaling
Rolling update and rollback
PostgreSQL persistent storage
ConfigMap and Secret configuration
Network Policy implementation
