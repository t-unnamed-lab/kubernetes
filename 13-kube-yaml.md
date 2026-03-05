# Conhecendo o YAML e o kubectl com dry-run

O Kubernetes usa arquivos YAML para definir os recursos do cluster. Esses arquivos são usados para criar, atualizar e excluir recursos no cluster. O kubectl tem um recurso chamado dry-run, que permite que você teste seus arquivos YAML sem realmente criar os recursos no cluster.
Para usar o dry-run, você pode usar o comando:

```bash
kubectl apply -f <arquivo-yaml> --dry-run=client -o yaml
```

Isso irá validar o arquivo YAML e mostrar o que seria criado, atualizado ou excluído, sem realmente fazer nenhuma alteração no cluster. Isso é útil para verificar se o arquivo YAML está correto antes de aplicá-lo no cluster.
Para criar os recursos definidos no arquivo YAML, você pode usar o comando:

```bash
kubectl apply -f <arquivo-yaml>
```

Isso irá criar os recursos no cluster de acordo com o que está definido no arquivo YAML. Se os recursos já existirem, eles serão atualizados de acordo com as mudanças feitas no arquivo YAML.
Para excluir os recursos definidos no arquivo YAML, você pode usar o comando:

```bash
kubectl delete -f <arquivo-yaml>
```

Isso irá excluir os recursos do cluster de acordo com o que está definido no arquivo YAML. Se os recursos não existirem, o comando irá retornar um erro.

O uso do dry-run é uma prática recomendada para garantir que seus arquivos YAML estejam corretos antes de aplicá-los no cluster, evitando erros e problemas de configuração.

## ConfigMaps do Kubernetes

Um ConfigMap é um recurso do Kubernetes que permite armazenar dados de configuração em formato de chave-valor. Ele é usado para separar a configuração do aplicativo do código-fonte, permitindo que você altere a configuração sem precisar reconstruir a imagem do contêiner.
Para criar um ConfigMap, você pode usar o comando:

```bash
kubectl create configmap <nome-do-configmap> --from-literal=<chave>=<valor> -n <nome-do-namespace>
```

Para consultar os ConfigMaps do cluster, você pode usar o comando:

```bash
kubectl get configmaps -n <nome-do-namespace>
```

Para acessar os dados de um ConfigMap, você pode usar o comando:

```bash
kubectl describe configmap <nome-do-configmap> -n <nome-do-namespace>
```

Para excluir um ConfigMap, você pode usar o comando:

```bash
kubectl delete configmap <nome-do-configmap> -n <nome-do-namespace>
```

## Yaml do Kubernetes

O Kubernetes usa arquivos YAML para definir os recursos do cluster. Esses arquivos são usados para criar, atualizar e excluir recursos no cluster. O YAML é um formato de serialização de dados legível por humanos, que é fácil de escrever e entender.
Um arquivo YAML do Kubernetes geralmente começa com a definição do tipo de recurso, seguida por metadados e especificações. Por exemplo, um arquivo YAML para criar um pod pode ser assim:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: meu-pod
  namespace: meu-namespace
spec:
  containers:
    - name: meu-container
      image: nginx
```
