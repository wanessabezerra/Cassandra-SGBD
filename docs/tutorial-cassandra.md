<h1>Instalação do Ambiente</h1>

Para instalar o Cassandra, é necessário, primeiramente, ter o Java instalado e atualizado, depois baixar o arquivo no site do Cassandra. Esse arquivo virá com três diretórios: bin, data e conf. Abre-se o bin (ou o .bat, no Windows), e executa esse comando:  

```sh
./cassandra  
```  

Feito isso, pode-se iniciar o trabalho.

<h2>Instalação do Cassandra usando docker</h2>

#### 1: Docker pull cassandra

```sh
sudo docker pull cassandra:latest
```

#### 2: Execute Cassandra Docker Image como Docker Container

```sh
sudo docker run -d --name cassandra-node -p 9042:9042 cassandra
```

#### 3: Faça login no cassandra-node (Docker Container) no modo bash

```sh
sudo docker exec -it cassandra-node bash
```

#### 4: Abra o Cassandra CLI

```sh
cqlsh
```

Em seguida temos o link de um exemplo prático:

Implementação do Cassandra [Clique aqui ➡️](implementacao-pratica.md)
