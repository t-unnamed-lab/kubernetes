# Configurando o nosso primeiro volume EmptyDir

Para criar um volume do tipo `EmptyDir`, basta adicionar a seção `volumes` no nosso manifesto de pod, e depois referenciar o volume criado dentro do container, usando a seção `volumeMounts`.

```yaml
volumeMounts:
  - name: meu-volume
    mountPath: /dados
```

```yaml
volumes:
  - name: meu-volume
    emptyDir:
      sizeLimit: 1Gi
```

No exemplo acima, criamos um volume do tipo `EmptyDir` chamado `meu-volume`, com um limite de tamanho de 1Gi. Em seguida, montamos esse volume dentro do container no caminho `/dados`.

O volume `EmptyDir` é um tipo de volume temporário que é criado quando o pod é iniciado e é excluído quando o pod é destruído. Ele é útil para armazenar dados temporários que não precisam ser persistidos além da vida útil do pod.

Os volumes não servem para persistir dados, pois são destruídos junto com o pod. Portanto, é importante usar volumes para dados temporários ou para compartilhar dados entre containers dentro do mesmo pod, mas não para armazenar dados que precisam ser persistidos além da vida útil do pod.
