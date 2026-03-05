# Container

## O que é um container?

Um container é uma unidade de software que empacota o código e todas as suas dependências para que o aplicativo seja executado de forma rápida e confiável em diferentes ambientes. Ele é uma forma leve de virtualização que permite que os aplicativos sejam isolados uns dos outros e do sistema operacional subjacente. Os containers são criados a partir de imagens, que são arquivos imutáveis que contêm tudo o que é necessário para executar um aplicativo, incluindo o código, as bibliotecas, as dependências e as configurações. Os containers são gerenciados por um runtime de container, como o Docker, que fornece uma interface para criar, executar e gerenciar os containers.

## Como funcionam os containers?

Os containers funcionam usando recursos de isolamento do sistema operacional, como namespaces e cgroups, para criar um ambiente isolado para cada container. Os namespaces fornecem isolamento de recursos, como processos, rede e sistema de arquivos, enquanto os cgroups limitam o uso de recursos, como CPU e memória. Isso permite que os containers sejam executados de forma eficiente e segura em um ambiente compartilhado. Os containers também compartilham o kernel do sistema operacional subjacente, o que os torna mais leves do que as máquinas virtuais tradicionais, que incluem um sistema operacional completo. Isso permite que os containers sejam iniciados rapidamente e usem menos recursos do sistema, tornando-os ideais para desenvolvimento, testes e implantação de aplicativos em ambientes de produção.

## Autor: **Rafael Friederick**

## Referências

- [What is a Container?](https://www.docker.com/resources/what-container)
- [How Containers Work](https://www.docker.com/resources/what-container#how-containers-work)
- [Linux Tips: Containers](https://school.linuxtips.io/path-player?courseid=kubernetes-essentials&pathid=containers&playerid=video-1)
