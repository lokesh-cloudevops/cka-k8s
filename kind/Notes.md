kind create cluster --config kind.yaml --name cka-cluster

kind delete cluster --name <name of cluster>

kubectl config get-contexts                          # display list of contexts
kubectl config set-cluster my-cluster-name           # set a cluster entry in the kubeconfig

kubectl cluster-info --context kind-cka-cluster