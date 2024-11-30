helm repo add elastic https://helm.elastic.co

helm upgrade --install apm-server elastic/apm-server --namespace=elastic --version 7.6.2 -f values.yaml