-----

>[!tip] Observe os 4 campos de nível superior: apiVersion, kind, metadata e spec.


```YAML
#service.yml #DECLARATIVO

apiVersion: v1 
kind: Service 
metadata: 
  name: frontend-service 
spec:
  selector: 
    app: mywebsite
  ports:
    - protocol: 'TCP'
      port: 80
      targetPort: 80
  type: LoadBalancer
  

❯ kubectl apply -f service-definition.yml
❯ kubectl get services
❯ kubectl delete -f nginx-service.yml
```
[[Pod]], [[Replica Set]], [[Deployment]], [[Objetos K8S]]

