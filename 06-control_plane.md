# Control Plane

O control plane é o cérebro do cluster Kubernetes. Ele é responsável por tomar decisões globais sobre o cluster (por exemplo, agendamento), detectar e responder a eventos do cluster (por exemplo, iniciar um novo pod quando a implantação replica um pod falhou). O control plane é composto por vários componentes, incluindo:

**etcd**: O etcd é um armazenamento de chave-valor distribuído que armazena todos os dados do cluster Kubernetes. Ele é usado para armazenar o estado do cluster, incluindo informações sobre nós, pods, serviços e outros objetos do Kubernetes.

**kube-apiserver**: O kube-apiserver é o ponto de entrada para o cluster Kubernetes. Ele expõe a API do Kubernetes e é responsável por processar as solicitações dos usuários e dos componentes do cluster. O kube-apiserver também é responsável por validar as solicitações e garantir que elas estejam em conformidade com as políticas do cluster.

**kube-scheduler**: O kube-scheduler é responsável por agendar os pods para execução nos nós do cluster. Ele analisa os requisitos dos pods e as capacidades dos nós para determinar onde os pods devem ser executados.

**kube-controller-manager**: O kube-controller-manager é responsável por executar os controladores do Kubernetes. Os controladores são loops de controle que monitoram o estado do cluster e fazem alterações para garantir que o estado desejado seja mantido. Por exemplo, o controlador de replicação garante que o número desejado de réplicas de um pod esteja sempre em execução.

## Autor: **Rafael Friederick**

## Referências

- [Kubernetes Control Plane](https://kubernetes.io/docs/concepts/overview/components/#control-plane)
- [etcd](https://etcd.io/)
- [kube-apiserver](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-apiserver/)
- [kube-scheduler](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-scheduler/)
- [kube-controller-manager](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-controller-manager/)
- [Linux Tips: Control Plane](https://school.linuxtips.io/path-player?courseid=kubernetes-essentials&pathid=control-plane&playerid=video-1)
