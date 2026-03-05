# Workers

## O que são os Workers?

Os workers são os nós do cluster Kubernetes onde os pods são executados. Eles são responsáveis por executar as cargas de trabalho do cluster e fornecer os recursos necessários para que os pods sejam executados. Cada worker é gerenciado pelo control plane e se comunica com ele para receber instruções sobre quais pods executar e como alocar recursos. Os workers também são responsáveis por monitorar o estado dos pods em execução e relatar esse estado de volta para o control plane.

## Componentes dos Workers

Cada worker é composto por vários componentes, incluindo:

- **kubelet**: O kubelet é o agente que roda em cada worker e é responsável por garantir que os pods estejam em execução e saudáveis. Ele se comunica com o control plane para receber instruções sobre quais pods executar e como alocar recursos, e também monitora o estado dos pods em execução.
  O kubelet comunica-se com o control plane por meio da API do Kubernetes para receber informações sobre os pods que devem ser executados e para relatar o estado dos pods em execução. Ele também se comunica com o runtime de contêiner (como Docker ou containerd) para iniciar e gerenciar os contêineres que compõem os pods.

- **kube-proxy**: O kube-proxy é responsável por manter as regras de rede para os serviços do Kubernetes. Ele se comunica com o control plane para receber informações sobre os serviços e os endpoints, e então configura as regras de rede para garantir que o tráfego seja roteado corretamente para os pods.

## Autor: **Rafael Friederick**

## Referências

- [Kubernetes Workers](https://kubernetes.io/docs/concepts/overview/components/#worker-nodes)
- [Linux Tips: Workers](https://school.linuxtips.io/path-player?courseid=kubernetes-essentials&pathid=workers&playerid=video-1)
