# Http server
## 7. Scale http server.
- A pod can be scaled by directly issue kubectl command.
  - $ ./kubectl scale --replicas=3 replicationcontrollers <name of your replication controller>
  - $ ./kubectl get po
```
NAME                 READY     STATUS    RESTARTS   AGE
sitting-duck-4e4zu   1/1       Running   0          14m
sitting-duck-jbibm   1/1       Running   0          12s
sitting-duck-kp5mk   1/1       Running   0          12s
```
- You should see 3 pods instead of 1 pod.
