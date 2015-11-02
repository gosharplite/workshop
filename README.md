# Workshops for microservices
## Quick start
- Access Kubernetes cluster by using command line binary `kubectl` and credential file `config`.
```
$ mkdir zeta; cd zeta
$ wget http://10.128.112.15:8087/kubernetes/v1.0.6/kubectl
$ sudo chmod +x kubectl
$ wget http://10.128.112.15:8087/tyd/v0.7/srv/kube-apiserver/config-droi
$ export KUBECONFIG="./config-droi"
$ ./kubectl version
Client Version: version.Info{Major:"1", Minor:"0", GitVersion:"v1.0.6", GitCommit:"388061f00f0d9e4d641f9ed4971c775e1654579d", GitTreeState:"clean"}
Server Version: version.Info{Major:"1", Minor:"0", GitVersion:"v1.0.6", GitCommit:"388061f00f0d9e4d641f9ed4971c775e1654579d", GitTreeState:"clean"}
```
- [Guestbook](http://10.128.112.15:30000/)
- [Dashboard](http://10.128.112.15:30022/)
- [Motivation](https://github.com/gosharplite/the-new-stack/blob/master/README.md#the-new-stack)
- [Documentation](http://kubernetes.io/v1.0/)
- [Shuk's notes](https://github.com/BizShuk/k8s_doc)

## Http server
1. [Create http server by compiling golang binary.](http-server/hs1.md)
2. [Dockerize http server binary.](http-server/hs2.md)
3. [Push image into private docker registry.](http-server/hs3.md)
4. [Access Kubernetes cluster.](http-server/hs4.md)
5. [Create Kubernetes replica-controller and service setup files.](http-server/hs5.md)
6. [Deploy http server on Kubernetes.](http-server/hs6.md)
7. [Scale http server.](http-server/hs7.md)

## Guestbook
1. [Create frontend, master/slave redis setup files.](guestbook/g1.md)
2. [Deploy guestbook.](guestbook/g2.md)
3. [Scale guestbook.](guestbook/g3.md)
