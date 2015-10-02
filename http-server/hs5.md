# Http server
## 5. Create Kubernetes replica-controller and service setup files.
- Read [Kubernetes overview](http://kubernetes.io/v1.0/docs/user-guide/overview.html) in the official user's guide.
- Use below example and create file `controller.yaml`.
  - Change
```
apiVersion: v1
kind: ReplicationController
metadata:
  name: sitting-duck
  labels:
    name: sitting-duck
spec:
  replicas: 1
  selector:
    name: sitting-duck
  template:
    metadata:
      labels:
        name: sitting-duck
    spec:
      containers:
      - name: duck
        image: gosharplite/duck:v4
        command:
        - /duck
        - -delay
        - "62"
        ports:
        - containerPort: 80
```
