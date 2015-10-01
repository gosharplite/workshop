# Http server
## 4. Create Kubernetes replica-controller and service setup files.
- Understand [Kubernetes architecture](https://github.com/kubernetes/kubernetes/blob/master/docs/design/architecture.md).
- Understand different ways to [access the cluster](https://github.com/kubernetes/kubernetes/blob/master/docs/user-guide/accessing-the-cluster.md).
- Get command line binary `kubectl` and credential file `config`.
  - $ wget http://10.128.3.11:8087/kubernetes/v1.0.6/kubectl
  - $ sudo chmod +x kubectl
  - $ wget http://10.128.3.11:8087/tyd/v0.3/srv/kube-apiserver/config
  - $ ./kubectl version
- You should see below output.
```
$ ./kubectl version
Client Version: version.Info{Major:"1", Minor:"0", GitVersion:"v1.0.6", GitCommit:"388061f00f0d9e4d641f9ed4971c775e1654579d", GitTreeState:"clean"}
Server Version: version.Info{Major:"1", Minor:"0", GitVersion:"v1.0.6", GitCommit:"388061f00f0d9e4d641f9ed4971c775e1654579d", GitTreeState:"clean"}
```
- Read the doc.
  - $ ./kubectl -h