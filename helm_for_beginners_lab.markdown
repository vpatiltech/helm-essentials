

- `git clone https://github.com/sagar-jadhav/helm101.git`

- `cd ./helm101/charts/`

- `helm install --name demoone ./guestbook/`

- `helm list`

- `kubectl get pods`

- `kubectl get svc`

- `export IP=$(kubectl get nodes -o jsonpath='{ $.items[*].status.addresses[?(@.type=="ExternalIP")].address }')`

- `export PORT=$(kubectl get --namespace default -o jsonpath="{.spec.ports[0].nodePort}" services demoone-guestbook)`

- `echo http://$IP:$PORT`

- `helm status demoone`

- `helm upgrade demoone ./guestbook/ --set replicaCount=4`

- `helm rollback demoone 1` 

- `kubectl get pods`

- `helm delete --purge demoone`

- `helm inspect ./guestbook/`

- `helm package ./guestbook/`

- `helm serve`

- `helm install --name demoone local/guestbook`

- `helm delete demoone`

- `helm repo add my-repo https://ibm.github.io/helm101/`

- `helm repo list`

- `helm install --name demoone my-repo/guestbook`

- `helm delete demoone`

- `helm create my-chart`
