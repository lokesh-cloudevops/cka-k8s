Namespaces:

It provides another layer of isolation within the cluster, so that we can separate our objects and resources within a cluster.

Ex: Different projects in same cluster. (namespace will make separate every projects).

kubectl get ns
kubectl create ns my-ns
kubectl get all --namespace=kube-system
or
kubectl get all -n kube-system

kubectl create deploy nginx-demo --image nginx -n my-ns

