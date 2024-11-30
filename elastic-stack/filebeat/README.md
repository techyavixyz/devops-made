helm install filebeat --namespace=elastic -f values.yaml .

NAME: filebeat
LAST DEPLOYED: Mon Jun 17 16:07:35 2024
NAMESPACE: elastic
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
1. Watch all containers come up.
  $ kubectl get pods --namespace=elastic -l app=filebeat-filebeat -w