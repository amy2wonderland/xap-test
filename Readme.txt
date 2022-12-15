###eksctl/kubectl commands used for xap-test in Declarative way through BuildSpec################

###Deploy NGINX to EKS######
$kubectl get all
$kubectl get nodes
$kubectl apply -f nginx-deployment.yaml ########Add to CodeBuild BuildSpec######
$kubectl get all #####Will show new pods#####
$kubectl delete pod "pod name"
$kubectl get rs
$kubectl get deployment
$kubectl delete rs "rs name"
$kubectl describe pods


#####Deploy ELB (Classic) in AWS for NGINX#######
$eksctl get cluster
$kubectl apply -f loadbalancer-service.yaml  ########Add to CodeBuild BuildSpec######
$kubectl get services

#####Deploy ClusterIp service  in EKS for NGINX#######
$eksctl get cluster
$kubectl apply -f clusterip-service-service.yaml  ########Add to CodeBuild BuildSpec######
$kubectl get services

#######Deploy Nodeport Service in EKS######
$eksctl get cluster
$kubectl apply -f nodeport-service.yaml  ########Add to CodeBuild BuildSpec######
$kubectl get services
$kubectl get pods
$kubectl get pods -o wide ###Will show IPs of pods and node####

