helm update --install kibana --namespace=elastic -f values.yaml .


NAME: kibana
LAST DEPLOYED: Mon Jun 17 16:04:30 2024
NAMESPACE: elastic
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
1. Watch all containers come up.
  $ kubectl get pods --namespace=elastic -l release=kibana -w
2. Retrieve the elastic user's password.
  $ kubectl get secrets --namespace=elastic elasticsearch-master-credentials -ojsonpath='{.data.password}' | base64 -d
3. Retrieve the kibana service account token.
  $ kubectl get secrets --namespace=elastic kibana-kibana-es-token -ojsonpath='{.data.token}' | base64 -d