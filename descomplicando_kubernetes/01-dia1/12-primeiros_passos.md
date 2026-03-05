# Primeiros passos no kubernetes com o kubectl

## Namespaces do Kubernetes

O Kubernetes tem um recurso chamado namespaces, que é uma forma de organizar os recursos do cluster. Os namespaces permitem que você tenha vários ambientes (como desenvolvimento, teste e produção) dentro do mesmo cluster, isolando os recursos de cada ambiente.
Para listar os namespaces do cluster, você pode usar o comando:

```bash
kubectl get namespaces
```

Para criar um namespace, você pode usar o comando:

```bash
kubectl create namespace <nome-do-namespace>
```

Para usar um namespace específico, você pode usar o comando:

```bash
kubectl config set-context --current --namespace=<nome-do-namespace>
```

## Pods do Kubernetes

Um pod é a menor unidade de implantação do Kubernetes. Ele é composto por um ou mais contêineres que compartilham o mesmo namespace de rede e armazenamento. Os pods são usados para executar aplicativos e serviços no cluster.
Para consultar os pods do cluster, você pode usar o comando:

```bash
kubectl get pods -n <nome-do-namespace>
```

Para criar um pod, você pode usar o comando:

```bash
kubectl run <nome-do-pod> --image=<imagem-do-container> -n <nome-do-namespace>
```

Para acessar um pod, você pode usar o comando:

```bash
kubectl exec -it <nome-do-pod> -n <nome-do-namespace> -- /bin/bash
```

Para excluir um pod, você pode usar o comando:

```bash
kubectl delete pod <nome-do-pod> -n <nome-do-namespace>
```

## Deployments do Kubernetes

Um deployment é um recurso do Kubernetes que gerencia a implantação e a atualização de aplicativos. Ele garante que o número desejado de réplicas de um aplicativo esteja sempre em execução, e pode ser usado para atualizar o aplicativo sem tempo de inatividade.
Para consultar os deployments do cluster, você pode usar o comando:

```bash
kubectl get deployments -n <nome-do-namespace>
```

## Replicasets do Kubernetes

Um replicaset é um recurso do Kubernetes que garante que um número específico de réplicas de um pod esteja em execução. Ele é usado para manter a disponibilidade dos aplicativos, garantindo que haja sempre um número mínimo de réplicas em execução.
Para consultar os replicasets do cluster, você pode usar o comando:

```bash
kubectl get replicasets -n <nome-do-namespace>
```

## Services do Kubernetes

Um service é um recurso do Kubernetes que expõe um conjunto de pods como um serviço de rede. Ele permite que os aplicativos se comuniquem entre si, mesmo que os pods sejam criados e destruídos dinamicamente.
Para consultar os services do cluster, você pode usar o comando:

```bash
kubectl get services -n <nome-do-namespace>
```

## ConfigMaps do Kubernetes

Um configmap é um recurso do Kubernetes que armazena dados de configuração em formato de chave-valor. Ele é usado para separar a configuração dos aplicativos do código-fonte, permitindo que você altere a configuração sem precisar reconstruir a imagem do aplicativo.
Para consultar os configmaps do cluster, você pode usar o comando:

```bash
kubectl get configmaps -n <nome-do-namespace>
```
