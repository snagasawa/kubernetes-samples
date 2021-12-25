# Getting Started
```
kubectl version
# => Client Version: version.Info{Major:"1", Minor:"23", GitVersion:"v1.23.1", GitCommit:"86ec240af8cbd1b60bcc4c03c20da9b98005b92e", GitTreeState:"clean", BuildDate:"2021-12-16T11:33:37Z", GoVersion:"go1.17.5", Compiler:"gc", Platform:"darwin/amd64"}

kubectl krew install hns
kubectl hns version
# => kubectl-hns version v0.9.0

kubectl apply -f https://github.com/kubernetes-sigs/hierarchical-namespaces/releases/download/v0.9.0/hnc-manager.yaml

kubectl apply -f namespace.yaml
kubectl apply -f subnamespaceanchor.yaml  # If you fail, try agian.
kubectl apply -k .
```


# Cleanup
```
kubectl delete subns -A -all
kubectl delete -k .
kubectl delete -f namespace.yaml
```
