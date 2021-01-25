# Certificate Kubenernetes Application Developer

## Concepts

1. Core Concepts (13%) 
2. Multi-Container Pods (10%) 
3. Pod Design (20%) 
4. State Persistence (8%) 
5. Configuration (18%) 
6. Observability (18%) 
7. Services and Networking (13%) 

### Core Concepts (13%)

1. List all the namespaces in the cluster
```bash

kubectl get namespaces
kubectl get ns		# short name
```
2. List all the pods in all namespaces 
```bash
kubectl get po --all-namespaces
```
3. List all the pods in the particular namespace 
```bash
kubectl get po -n <namespace name>
```
4. List all the services in the particular namespace 
```bash
kubectl get svc -n <namespace name>
```
5. List all the pods showing name and namespace with a json path expression 
```bash
kubectl get pods -o=jsonpath="{.items[*]['metadata.name', 'metadata.namespace']}"
```
6. Create an nginx pod in a default namespace and verify the pod running 
```bash

# creating a pod
kubectl run nginx --image=nginx --restart=Never

# List the pod
kubectl get po
```
7. Create the same nginx pod with a yaml file 
```yaml

// get the yaml file with --dry-run flag
kubectl run nginx --image=nginx --restart=Never --dry-run -o yaml > nginx-pod.yaml

// cat nginx-pod.yaml
apiVersion: v1
kind: Pod
metadata:
  creationTimestamp: null
  labels:
    run: nginx
  name: nginx
spec:
  containers:
  - image: nginx
    name: nginx
    resources: {}
  dnsPolicy: ClusterFirst
  restartPolicy: Never
status: {}

// create a pod 
kubectl create -f nginx-pod.yaml
```
