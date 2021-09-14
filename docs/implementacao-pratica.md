
<h1>Implementação do Cassandra</h1>

<h2>Pretende-se mostrar na demonstração prática:</h2>

- [1: Como criar uma keyspace](#1-como-criar-uma-keyspace)
- [2: Como criar uma tabela](#2-como-criar-uma-tabela)
- [3: Como inserir registros](#3-como-inserir-registros)
- [4: Como fazer selects](#4-como-fazer-selects)
- [5: Como fazer queries](#5-como-fazer-queries)

#### 1: Como criar uma keyspace

Para criar uma keyspace, primeiro executa-se o comando:  

```sh
cqlsh
```
  
Se tudo deu certo, esta tela aparecerá:  

```sh
Connected to Test Custler at 127.0.0.1:9042  
[cqlsh 5.0.1 | Cassandra 3.11.2 | CQL spec 3.4.4 | Native protocol v4]  
Use HELP for help  
cqlsh>  
```

Depois, utiliza-se os comandos para criar a keyspace:  

```sh
CREATE KEYSPACE demo WITH REPLICATION = {  
'class': 'SimpleStrategy',  
'replication_factor': 1};  
```

Com esse código, eu estou dizendo que eu quero criar uma keyspace com o nome example, utilizando a estratégia simples e com apenas 1 nó para o cluster.

#### 2: Como criar uma tabela

Para criar uma table, deve ser informado qual keyspace deseja usar.
  
Então, para criar a table.

```sh
CREATE TABLE demo.users (
  firstname TEXT,
  lastname TEXT,
  age INT,
  email TEXT,
  city TEXT,
PRIMARY KEY (lastname));
```

#### 3: Como inserir registros

Para inserir registros, usa-se esse comando:

```sh
INSERT INTO demo.users (firstname, lastname, age, email, city)
  VALUES ('Joao', 'Pedro', 15, 'jpedro.gmail.com', 'caico');
```

#### 4: Como fazer selects

O select é feito da seguinte forma, com uma query simples:

```sh
SELECT * FROM demo.users;
```

#### 5: Como fazer queries

É possível fazer uma query específica assim:

```sh
SELECT WRITETIME (firstname)
FROM demo.users
WHERE lastname = 'Pedro';
```

---

<p align="center"><strong>👁️ Cassandra NoSQL<strong></p>
 
