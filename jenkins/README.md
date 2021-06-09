## Intro

In this directory there are some resources to easily deploy a Jenkins service
using a Minikube K8s cluster.

## Prerequisites

- Docker: https://docs.docker.com/engine/install/
- Minikube: https://minikube.sigs.k8s.io/docs/start/
- Kubectl: https://kubernetes.io/docs/tasks/tools/
- Helm cli: https://helm.sh/docs/intro/install/

## Instructions

1. Install dependencies
2. Start minikube cluster: `minikube start`
3. Create Jenkins namespace: `kubectl create namespace jenkins`
4. Deploy Jenkins: `kubectl create -f jenkins-deployment.yaml -n jenkins`
5. Create Jenkins service: `kubectl create -f jenkins-service.yaml -n jenkins`
6. Get minikube cluter's IP: `minikube ip`
7. Connect to the service in a browser using the received IP and the port 30340
