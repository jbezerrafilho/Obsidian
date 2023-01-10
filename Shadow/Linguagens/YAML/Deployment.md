-----

>[!tip] Observe os 4 campos de nível superior: apiVersion, kind, metadata e spec.


```YAML
#deployment.yml #DECLARATIVO

apiVersion: apps/v1 
kind: Deployment 
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

$ kubectl create -f deployment-definition.yml
$ kubectl delete -f deployment-definition.yml

```
[[Pod]], [[Replica Set]], [[Objetos K8S]]
