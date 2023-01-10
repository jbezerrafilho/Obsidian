----
#replicaset

>[!tip] Observe os 4 campos de nível superior: apiVersion, kind, metadata e spec.


```YAML
#replicaset.yaml

apiVersion: apps/v1 
kind: ReplicaSet 
metadata: 
  name: frontend 
  labels: 
    app: mywebsite 
    tier: frontend
spec: 
  replicas: 4 
  template: 
    metadata: 
      name: myapp-pod 
      labels: 
        app: myapp
    spec: 
      containers: 
        - name: nginx 
          image: nginx
  selector: 
    matchLabels: 
      app: myapp


```
[[Pod]], [[Deployment]] 