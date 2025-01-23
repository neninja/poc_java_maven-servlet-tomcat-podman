# POC de Maven + Servlet + Tomcat + Podman compose

## TL;DR

1. Suba os ambientes

```sh
podman-compose up
```

2. Compile a primeira vez e também sempre que alterar arquivos `.java`

```sh
podman-compose exec compiler mvn clean package
```

3. Acesse o sistema em `localhost:8080/poc-maven-tomcat-podman`

4. Pare o ambiente com `<c-c>` no terminal


## Mudando containers de maneira segura

Como processo de mudança no ambiente, baixe os containers e suba novamente com build

```sh
podman-compose down --remove-orphans
```

```sh
podman-compose up --build
```
