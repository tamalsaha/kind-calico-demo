# kind-calico-demo

## Reading List

- [Network Policies](https://kubernetes.io/docs/concepts/services-networking/network-policies/)

## Examples

- [Whitelist kube-apiserver with Network Policy](https://stackoverflow.com/questions/58790124/whitelist-kube-apiserver-with-network-polic)

## Create cluster

```
$ kind create cluster --config hack/kubernetes/kind.yaml
```

## Install Calico

https://docs.projectcalico.org/getting-started/kubernetes/self-managed-onprem/onpremises#install-calico-with-kubernetes-api-datastore-50-nodes-or-less

```
$ kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml
$ kubectl -n kube-system set env daemonset/calico-node FELIX_IGNORELOOSERPF=true
```

## Test Script

https://kubernetes.io/docs/tasks/administer-cluster/declare-network-policy/

## Reference Links

- [NetworkPolicy support](https://github.com/kubernetes-sigs/kind/issues/842)
- [Creating a Kind Cluster With Calico Networking](https://alexbrand.dev/post/creating-a-kind-cluster-with-calico-networking/)
