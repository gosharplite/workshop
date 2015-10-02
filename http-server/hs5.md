# Http server
## 5. Create Kubernetes replica-controller and service setup files.
- Read [Kubernetes overview](http://kubernetes.io/v1.0/docs/user-guide/overview.html) in the official user's guide.
- Use below example and create replication controller file `controller.yaml`.
  - Pick a name and change all `sitting-duck` in the file.
  - Change the `containers` section with your docker image.
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
