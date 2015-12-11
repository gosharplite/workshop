# Http server
## 4. Access Kubernetes cluster.
- Understand [Kubernetes architecture](http://kubernetes.io/v1.0/docs/design/architecture.html).
- Understand different ways to [access the cluster](http://kubernetes.io/v1.0/docs/user-guide/accessing-the-cluster.html).
- Get command line binary `kubectl` and credential file `config-droi`.
  - $ `wget http://10.128.112.16:8087/kubernetes/v1.1.2/kubectl`
  - $ sudo chmod +x kubectl
  - $ `wget http://10.128.112.16:8087/tyd/v0.8/srv/kube-apiserver/config`
  - $ export KUBECONFIG="./config"
  - $ ./kubectl version
- You should see below output.
```
$ ./kubectl version
Client Version: version.Info{Major:"1", Minor:"0", GitVersion:"v1.1.2", GitCommit:"388061f00f0d9e4d641f9ed4971c775e1654579d", GitTreeState:"clean"}
Server Version: version.Info{Major:"1", Minor:"0", GitVersion:"v1.1.2", GitCommit:"388061f00f0d9e4d641f9ed4971c775e1654579d", GitTreeState:"clean"}
```
- Read the doc.
  - $ ./kubectl -h
