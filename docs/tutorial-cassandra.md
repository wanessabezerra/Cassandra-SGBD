<h1>Instalação do Cassandra usando docker</h1>


#### 1: Realizar docker pull cassandra

```bash
$ sudo docker pull cassandra:latest
```

#### 2: Execute Cassandra Docker Image como Docker Container

```bash
$ sudo docker run -d --name cassandra-node -p 9042:9042 cassandra
```

#### 3: Faça login no cassandra-node (Docker Container) no modo bash

```bash
$ sudo docker exec -it cassandra-node bash
```

#### 4: Abra o Cassandra CLI

```bash
$ cqlsh
```
