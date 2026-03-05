# Criando o nosso primeiro cluster com kind

Neste exercício, vamos criar um cluster Kubernetes usando o kind (Kubernetes IN Docker). O kind é uma ferramenta que permite criar clusters Kubernetes locais usando contêineres Docker. Ele é útil para desenvolvimento e testes, pois permite criar clusters rapidamente e facilmente em um ambiente local.

## Kind

O kind é uma ferramenta de código aberto que permite criar clusters Kubernetes locais usando contêineres Docker. Ele é útil para desenvolvimento e testes, pois permite criar clusters rapidamente e facilmente em um ambiente local. O kind suporta a criação de clusters com múltiplos nós, o que é útil para testar a escalabilidade e a resiliência dos aplicativos em um ambiente Kubernetes.

### Passo 1: Instalar o kind

Para instalar o kind, você pode usar o seguinte comando:

```bash
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-$(uname)-amd64
chmod +x ./kind
mv ./kind /usr/local/bin/
```

### Passo 2: Criar um cluster com kind

Para criar um cluster Kubernetes usando o kind, você pode usar o seguinte comando:

```bash
kind create cluster --name my-cluster
```

Este comando criará um cluster Kubernetes chamado "my-cluster" usando o kind. O processo pode levar alguns minutos, dependendo do desempenho do seu sistema.

## Minikube

O minikube é uma ferramenta de código aberto que permite criar clusters Kubernetes locais em uma máquina virtual. Ele é útil para desenvolvimento e testes, pois permite criar clusters rapidamente e facilmente em um ambiente local. O Minikube suporta a criação de clusters com múltiplos nós, o que é útil para testar a escalabilidade e a resiliência dos aplicativos em um ambiente Kubernetes.

### Passo 1: Instalar o Minikube

Para instalar o Minikube, você pode usar o seguinte comando:

```bash
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
chmod +x minikube
sudo mv minikube /usr/local/bin/
```

### Passo 2: Criar um cluster com Minikube

Para criar um cluster Kubernetes usando o Minikube, você pode usar o seguinte comando:

```bash
minikube start --driver=docker
```

Este comando criará um cluster Kubernetes usando o Minikube com o driver Docker. O processo pode levar alguns minutos, dependendo do desempenho do seu sistema.

## K3D

O k3d é uma ferramenta de código aberto que permite criar clusters Kubernetes locais usando o K3S, uma distribuição leve do Kubernetes. Ele é útil para desenvolvimento e testes, pois permite criar clusters rapidamente e facilmente em um ambiente local. O k3d suporta a criação de clusters com múltiplos nós, o que é útil para testar a escalabilidade e a resiliência dos aplicativos em um ambiente Kubernetes.

### Passo 1: Instalar o K3D

Para instalar o K3D, você pode usar o seguinte comando:

```bash
curl -s https://raw.githubusercontent.com/rancher/k3d/main/install.sh | bash
```

### Passo 2: Criar um cluster com K3D

Para criar um cluster Kubernetes usando o K3D, você pode usar o seguinte comando:

```bash
k3d cluster create my-cluster
```

## K3S - [AQUI JÁ É UM CLUSTER REAL, NÃO DOCKER]

O K3S é uma distribuição leve do Kubernetes projetada para ser fácil de instalar e operar. Ele é útil para desenvolvimento e testes, pois permite criar clusters rapidamente e facilmente em um ambiente local. O K3S suporta a criação de clusters com múltiplos nós, o que é útil para testar a escalabilidade e a resiliência dos aplicativos em um ambiente Kubernetes.

### Passo 1: Instalar o K3S

Para instalar o K3S, você pode usar o seguinte comando:

```bash
curl -sfL https://get.k3s.io | sh -
```

### Passo 2: Verificar a instalação do K3S

Após a instalação do K3S, você pode verificar se ele está funcionando corretamente usando o seguinte comando:

```bash
sudo k3s kubectl cluster-info
```

Este comando exibirá informações sobre o cluster K3S, incluindo o endereço do kube-apiserver e o endereço do dashboard do Kubernetes (se estiver habilitado).

## Passos Gerais para acessar o cluster

### Passo 3: Verificar o cluster

Após a criação do cluster, você pode verificar se ele está funcionando corretamente usando o seguinte comando:

```bash
kubectl cluster-info --context <nome-do-cluster>
```

Este comando exibirá informações sobre o cluster, incluindo o endereço do kube-apiserver e o endereço do dashboard do Kubernetes (se estiver habilitado).

### Passo 4: Acessar o cluster

Para acessar o cluster, você pode usar o seguinte comando:

```bash
kubectl get nodes --context <nome-do-cluster>
```
