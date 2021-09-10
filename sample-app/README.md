# Sample App Installation Steps


##### 1) Install sample app
```
kubectl apply -f manifests.yaml -f istio-manifests.yaml
```

##### 2) Confirm that app is running
```
kubectl get pods
```

##### 3) Optional: Connect to frontend service via a local proxy
```
# If a web browser is enabled on your workstation view the app with the following commands
kubectl port-forward svc/frontend 8085:80 &

# Navigate to "http://localhost:8085" in your browser

# Terminate the proxy when you are finished
killall kubectl
```