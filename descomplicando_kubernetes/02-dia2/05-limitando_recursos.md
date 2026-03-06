# Limitando recursos do pod

Para limitar os recursos de um pod, podemos usar as seguintes chaves:

```yaml
resources:
  limits:
    cpu: "0.5"
    memory: 128Mi
  requests:
    cpu: "0.25"
    memory: 64Mi
```

- `limits`: define o limite máximo de recursos que o pod pode usar. Se o pod tentar usar mais do que o limite, ele será interrompido.
- `requests`: define a quantidade mínima de recursos que o pod precisa para ser agendado. O Kubernetes usará essa informação para decidir em qual nó o pod deve ser agendado. Se o nó não tiver recursos suficientes para atender a solicitação, o pod não será agendado naquele nó.
