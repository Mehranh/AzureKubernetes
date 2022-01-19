# Elastic Cloud Kubernetes

 - Elastic
 - Kibana
 - Ingress



Install custom resource definitions and the operator with its RBAC rules:

kubectl create -f https://download.elastic.co/downloads/eck/1.9.1/crds.yaml
kubectl apply -f https://download.elastic.co/downloads/eck/1.9.1/operator.yaml
If you are running a version of Kubernetes before 1.16 you have to use the legacy version of the manifests:

kubectl create -f https://download.elastic.co/downloads/eck/1.9.1/crds-legacy.yaml
kubectl apply -f https://download.elastic.co/downloads/eck/1.9.1/operator-legacy.yaml
Monitor the operator logs:

kubectl -n elastic-system logs -f statefulset.apps/elastic-operator




more information :

https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-deploy-eck.html