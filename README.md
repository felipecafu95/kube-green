## kube-green

Este chart é responsável pela instalação da ferramenta [kube-green](https://kube-green.dev/).

## Instalação

### Padrão
A instalação padrão é realizada utilizando o seguinte comando e parametros:

```bash
$ helm install kube-green . -f values.yaml -n kube-green
```

### Personalizada

Caso deseje, alterar configurações do chart, como nome, namespace, probes, etc.

É possível informar os novos valores atraves do parametro --set chave=valor. Exemplo:

```bash
$ helm install kube-green . -f values.yaml --set name=gold, namespace=gold, livenessProbe.httpGet.path=/cheio-de-saude
```

A outra maneira de personalizar as configurações do chart é alterando diretamente o arquivo `values.yaml`.

## Desinstalação

Para remover o chart e todos os objetos relacionados a ele, de um cluster, execute o comando abaixo:

```bash
$ helm del kube-green
```