helm install logstash --namespace=elastic -f values.yaml .


NAME: logstash
LAST DEPLOYED: Mon Jun 17 16:09:20 2024
NAMESPACE: elastic
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
1. Watch all cluster members come up.
  $ kubectl get pods --namespace=elastic -l app=logstash-logstash -w