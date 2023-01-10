------
#pod 

>[!tip] Observe os 4 campos de nível superior: apiVersion, kind, metadata e spec.

```
YAML
#pod-definition.yml modo declarativo

apiVersion: v1 
kind: Pod 
metadata:
  name: myapp-pod 
  labels: 
    app: myapp 
    type: front-end
spec: 
  containers: 
    - name: nginx-container 
      image: nginx

```
[[Replica Set]], [[Deployment]]
