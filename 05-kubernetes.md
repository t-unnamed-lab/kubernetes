# Kubernetes

## O que é o Kubernetes?

O Kubernetes é um sistema de orquestração de contêineres de código aberto que automatiza a implantação, o dimensionamento e a operação de aplicativos em contêineres. Ele foi originalmente desenvolvido pelo Google e agora é mantido pela Cloud Native Computing Foundation (CNCF). O Kubernetes fornece uma plataforma para gerenciar aplicativos em contêineres em um cluster de máquinas, permitindo que os desenvolvedores se concentrem na construção de aplicativos em vez de se preocupar com a infraestrutura subjacente. Ele suporta uma ampla variedade de cargas de trabalho, incluindo aplicativos sem estado, aplicativos com estado e aplicativos sem servidor, e é amplamente utilizado em ambientes de produção em todo o mundo.

## Componentes do Kubernetes

O Kubernetes é composto por vários componentes, incluindo:

- **Control Plane**: O control plane é o cérebro do cluster Kubernetes. Ele é responsável por gerenciar o estado do cluster e garantir que o estado desejado seja mantido. O control plane é composto por vários componentes, incluindo o kube-apiserver, o etcd, o kube-scheduler e o kube-controller-manager.
- **Workers**: Os workers são os nós do cluster Kubernetes onde os pods são executados. Eles são responsáveis por executar as cargas de trabalho do cluster e fornecer os recursos necessários para que os pods sejam executados. Cada worker é gerenciado pelo control plane e se comunica com ele para receber instruções sobre quais pods executar e como alocar recursos. Os workers também são responsáveis por monitorar o estado dos pods em execução e relatar esse estado de volta para o control plane.
- **Pods**: Os pods são as menores unidades de implantação no Kubernetes. Eles são compostos por um ou mais contêineres que compartilham o mesmo namespace de rede e armazenamento. Os pods são criados e gerenciados pelo control plane e são executados nos workers do cluster.
- **Replica Sets**: Os replica sets são um recurso do Kubernetes que garante que um número específico de réplicas de um pod esteja sempre em execução. Eles monitoram o estado dos pods e, se um pod falhar ou for excluído, o replica set criará automaticamente um novo pod para substituí-lo. Os replica sets são usados para garantir a alta disponibilidade das cargas de trabalho do cluster.
- **Deployments**: Os deployments são um recurso do Kubernetes que gerencia a implantação e a atualização de aplicativos. Eles permitem que você defina o estado desejado para seus aplicativos, incluindo o número de réplicas, a imagem do contêiner e as políticas de atualização. O deployment garante que o estado desejado seja mantido, criando ou excluindo pods conforme necessário. Os deployments também permitem que você faça atualizações de forma controlada, garantindo que as novas versões do aplicativo sejam implantadas sem interrupção.
- **Services**: Os services são um recurso do Kubernetes que fornece uma maneira de expor os pods para o tráfego de rede. Eles permitem que você defina um conjunto de pods como um serviço e fornecem um endereço IP estável e um nome DNS para acessar esses pods. Os services também podem ser configurados para balancear a carga entre os pods, garantindo que o tráfego seja distribuído de forma eficiente.

## Autor: **Rafael Friederick**

## Referências

- [What is Kubernetes?](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)
- [Kubernetes Components](https://kubernetes.io/docs/concepts/overview/components/)
- [Linux Tips: Kubernetes](https://school.linuxtips.io/path-player?courseid=kubernetes-essentials&pathid=kubernetes&playerid=video-1)
