##Install Metric server

##Deploy Metric Server through AWS Cloud9
$ kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml


##Verify Metric server deployment
$ kubectl get deployment metrics-server -n kube-system

