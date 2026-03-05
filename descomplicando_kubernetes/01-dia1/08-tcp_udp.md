# Quais as portas TCP e UDP dos componentes do Kubernetes?

## Control Plane

- **etcd**: Porta TCP 2379 para comunicação cliente-servidor e porta TCP 2380 para comunicação entre os membros do cluster etcd.
- **kube-apiserver**: Porta TCP 6443 para comunicação com os clientes e outros componentes do cluster.
- **kube-scheduler**: Porta TCP 10251 para comunicação com o kube-apiserver.
- **kube-controller-manager**: Porta TCP 10252 para comunicação com o kube-apiserver.

## Workers

- **kubelet**: Porta TCP 10250 para comunicação com o kube-apiserver e porta TCP 10255 para exposição de métricas (opcional).
- **kube-proxy**: Porta TCP 10256 para comunicação com o kube-apiserver e porta TCP 10257 para exposição de métricas (opcional).

## NodePort

- Os serviços do tipo NodePort expõem uma porta TCP ou UDP em cada nó do cluster. A porta é escolhida aleatoriamente dentro do intervalo de portas definido para NodePort (geralmente entre 30000 e 32767) e é usada para encaminhar o tráfego para os pods que estão executando o serviço.

## Autor: **Rafael Friederick**

## Referências

- [Kubernetes Control Plane](https://kubernetes.io/docs/concepts/overview/components/#control-plane)
- [etcd](https://etcd.io/)
- [kube-apiserver](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-apiserver/)
- [kube-scheduler](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-scheduler/)
- [kube-controller-manager](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-controller-manager/)
- [Kubernetes Workers](https://kubernetes.io/docs/concepts/overview/components/#worker-nodes)
