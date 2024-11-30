helm install elasticsearch --namespace=elastic -f values.yaml .


NAME: elasticsearch
LAST DEPLOYED: Mon Jun 17 15:59:35 2024
NAMESPACE: elastic
STATUS: deployed
REVISION: 1
NOTES:
1. Watch all cluster members come up.
  $ kubectl get pods --namespace=elastic -l app=elasticsearch-master -w
2. Retrieve elastic user's password.
  $ kubectl get secrets --namespace=elastic elasticsearch-master-credentials -ojsonpath='{.data.password}' | base64 -d
3. Test cluster health using Helm test.
  $ helm --namespace=elastic test elasticsearch