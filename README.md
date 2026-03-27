# Kubernetes 🚀

## 📌 Kubernetes Basic Commands Cheat Sheet

---

### 🔹 1. Cluster & Context
```bash
kubectl cluster-info        # View cluster info
kubectl config view         # View kubeconfig
kubectl config current-context   # Current context
kubectl config use-context <context-name>  # Switch context
🔹 2. Nodes
kubectl get nodes           # List all nodes
kubectl describe node <node-name>  # Detailed node info
🔹 3. Pods
kubectl get pods            # List pods
kubectl get pods -o wide    # More details
kubectl describe pod <pod-name>  # Pod details
kubectl logs <pod-name>     # View logs
kubectl exec -it <pod-name> -- /bin/bash   # Access container
kubectl delete pod <pod-name>   # Delete pod
🔹 4. Deployments
kubectl get deployments
kubectl create deployment <name> --image=<image>
kubectl apply -f deployment.yaml
kubectl describe deployment <name>
kubectl scale deployment <name> --replicas=3
kubectl rollout status deployment <name>
kubectl rollout undo deployment <name>
🔹 5. Services
kubectl get services
kubectl expose deployment <name> --type=NodePort --port=80
kubectl describe service <service-name>
🔹 6. Namespaces
kubectl get namespaces
kubectl create namespace <name>
kubectl delete namespace <name>
kubectl config set-context --current --namespace=<name>
🔹 7. YAML / Resource Management
kubectl apply -f file.yaml     # Create/update resource
kubectl create -f file.yaml    # Create resource
kubectl delete -f file.yaml    # Delete resource
kubectl get all                # Get all resources
🔹 8. Debugging (🔥 Important for Interviews)
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl get events
kubectl top pod
kubectl top node
🔹 9. ConfigMaps & Secrets
kubectl create configmap <name> --from-literal=key=value
kubectl get configmaps

kubectl create secret generic <name> --from-literal=key=value
kubectl get secrets
🔹 10. Minikube (Local Kubernetes)
minikube start
minikube status
minikube stop
minikube delete
minikube service <service-name>
