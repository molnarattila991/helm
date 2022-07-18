# Requirements
- Running Kubernetes cluster
- Node.js for building Node projects
- Helm
- KEDA scaler

## Pre install steps
- clone repo
- helm dependency update ./project-infra
- build applications and images
 - npm run install -f
 - npm run build
 - docker build -t app-name:app-version .

## Install application
- helm uninstall project-infra
- helm package project-infra
- helm install project-infra .\project-infra-x.x.x.tgz
- helm uninstall project-practise
- helm package project-practise
- helm install project-practise .\project-practise-x.x.x.tgz

# Third Party components

## MongoDB
- based on: https://devopscube.com/deploy-mongodb-kubernetes/
- cloned repo into infra-be-db-mongodb (git clone https://github.com/scriptcamp/kubernetes-mongodb.git)

## Keda scaler
- based on: https://keda.sh/docs/2.7/deploy/#yaml

## Redis
- based on: https://phoenixnap.com/kb/kubernetes-redis, https://stackoverflow.com/questions/52552876/configuring-third-party-helm-charts-from-my-application-helm-chart
- helm dependency update ./project-testing