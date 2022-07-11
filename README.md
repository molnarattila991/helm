# Requirements
- Running Kubernetes cluster
- Helm
- KubeMQ

## Install KubeMQ
- https://docs.kubemq.io/getting-started/quick-start
- kubectl apply -f https://deploy.kubemq.io/init
- kubectl apply -f https://deploy.kubemq.io/key/3a561dc1-0454-4895-9eb7-8c9308afb14a

# Install helm
- https://helm.sh/docs/intro/install/

# Init helm repo
- helm create project-practise 

# Install application
- helm uninstall project-practise
- helm package project-practise
- helm install project-practise .\project-practise-0.1.0.tgz