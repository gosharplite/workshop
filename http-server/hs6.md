# Http server
## 6. Deploy http server on Kubernetes.
- Create replication controller object in Kubernetes.
  - $ ./kubectl create -f controller.yaml 
- Observe your creations.
  - $ ./kubectl get rc
  - $ ./kubectl get po
- Create service object in Kubernetes.
  - $ ./kubectl create -f service.json
- Observe your creations.
  - $ ./kubectl get se
- Since we are using `NodePort` type in our service, we can find out the port number assigned to our service.
  - $ ./kubectl describe se <your service name>
```
Name:			sitting-duck
Namespace:		tyd
Labels:			name=sitting-duck
Selector:		name=sitting-duck
Type:			NodePort
IP:			10.0.17.106
Port:			<unnamed>	80/TCP
NodePort:		<unnamed>	30010/TCP
Endpoints:		10.1.58.9:80
Session Affinity:	None
No events.
```
