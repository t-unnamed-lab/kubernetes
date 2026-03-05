# Container Runtime

## O que é um container runtime?

Um container runtime é um software que executa e gerencia containers. Ele é responsável por criar, iniciar, parar e excluir containers, bem como gerenciar os recursos do sistema para garantir que os containers sejam executados de forma eficiente e segura. O container runtime é uma parte essencial do ecossistema de containers, pois fornece a infraestrutura necessária para executar aplicativos em containers. Existem vários container runtimes disponíveis, incluindo o Docker, o containerd e o CRI-O. O container runtime da OCI é o runc, que é um runtime de contêiner leve e de baixo nível que é usado por muitos outros runtimes de contêiner, como o containerd e o CRI-O. O runc é responsável por criar e gerenciar os namespaces e cgroups necessários para isolar os containers e garantir que eles sejam executados de forma eficiente e segura.

## Autor: **Rafael Friederick**

## Referências

- [What is a Container Runtime?](https://www.docker.com/resources/what-container-runtime)
- [Docker Documentation](https://docs.docker.com/)
- [containerd Documentation](https://containerd.io/)
- [CRI-O Documentation](https://cri-o.io/)
- [Linux Tips: Container Runtimes](https://school.linuxtips.io/path-player?courseid=kubernetes-essentials&pathid=container-runtimes&playerid=video-1)
