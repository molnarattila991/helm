# Requirements
- Running Kubernetes cluster
- Helm
- KubeMQ

## Install Helm
- https://helm.sh/docs/intro/install/

## Install KubeMQ
- https://docs.kubemq.io/getting-started/quick-start
- kubectl apply -f https://deploy.kubemq.io/init
- kubectl apply -f https://deploy.kubemq.io/key/3a561dc1-0454-4895-9eb7-8c9308afb14a

# How to use
- firstly you have to install practise-infra helm charts
- then you can install practise-project helm charts
- https://helm.sh/docs/chart_template_guide/functions_and_pipelines/
- init repo
- install package

## Init helm repo
- helm create project-infra 
- helm create project-practise 

## Install application
- helm uninstall project-practise
- helm package project-practise
- helm install project-practise .\project-practise-0.1.0.tgz

# MongoDB
- based on: https://devopscube.com/deploy-mongodb-kubernetes/
- cloned repo into infra-be-db-mongodb (git clone https://github.com/scriptcamp/kubernetes-mongodb.git)

# Keda scaler
- based on: https://keda.sh/docs/2.7/deploy/#yaml