# Arquitetura de Dados Essencial

###### **Conceitos Introdutórios e o que é um Banco de Dados (Objetivos da Aula)**

###### - Conceito de Dados.

###### - O que é um Banco de Dados.

###### - Banco de Dados Relacionais.

###### - Exemplo Prático.

######  

###### **Requisitos Básicos**

###### - Conhecimentos de Lógica de Programação.

###### - Conhecimentos de Tipos de Dados.

###### - Conhecimentos de Operadores Lógicos.

######  

###### **Dados**

###### - Valores, Ocorrências.

######  

###### **Importância**

###### - Dados → Informação → Conhecimento.

######  

###### **Dados Digitais**

###### - Lorem Ipsum (00) 9999-1111 120,19

###### - Velit Esse Cillum (55) 9999-2222 1.300,19

######  

###### **Modelo Sustentável**

###### - Estruturação → Durabilidade → Velocidade → Controle de Acesso → Isolamento

######  

###### **O que é um Banco de Dados**

###### **Abstração**

###### **SGDBs**

###### - Linguagem de Definição.

###### - Linguagem de Manipulação.

###### - Dicionário de Dados

######  

###### **Modelos de Banco de Dados**

###### - Flat, Hierárquico, Relacional, (etc...)

###### - Redes - Grapho, Orientado a Objetos, Objeto-Relacional, Big Data.

######  

###### **Banco de Dados Relacionais (Objetivos da Aula)**

###### **SGDBR - (RDBMS)**

###### - Formado por Tabelas, Registros/Tuplas, Colunas, Chave PK/FK

######  

###### **Modelagem**

###### - Modelo conceitual - MER

###### - Modelo lógico - Implementação

######  

###### **Normalização**

###### - 1ª ... 5ª - Formas normais

###### - 1ª, 2ª e 3ª - Mais comum

######  

###### **SGDBR - SQL (Objetivos da Aula)**

###### **SQL**

###### - DDL - Data Definition Language

###### - DML - Data Manipulation Language

###### - DQL - Data Query Language

######  

###### **Comando DDL**

```
CREATE TABLE Cliente
(
Codigo NUMERIC(10) NOT NULL PRIMARY KEY,
Nome VARCHAR(50) NOT NULL,
Telefone VARCHAR(15)
)
```

######  

###### **Comando DML**

```
INSERT INTO Cliente (Codigo, Nome, Telefone)
VALUES (1, "Lorem ipsum","(88) 999 9999")

DELETE FROM Cliente
WHERE Codigo = 1

UPDATE Cliente
SET Nome = "Lorem Ipsum"
WHERE Codigo = 1
```

######  

###### **Comando DQL**

```
SELECT Codigo,
			 Nome
FROM Cliente
<WHERE> Codigo = 1
	<GROUP BY> Profissao
	<HAVING> Count(1) > 0
<ORDER BY> Nome, Codigo

**Query**
SELECT Codigo,
			 Nome
FROM Cliente
WHERE Codigo = 2
UNION
SELECT Codigo,
		  Nome
FROM Cliente
WHERE Nome = "Lorem Ipsum"
```

######  

```
SELECT Quantidade
		 , Valor
		 , Descricao
FROM Item_venda
JOIN Produto
ON Codigo = Cod_Produto
WHERE Valor > 5

**Funções de Conjunto**
SELECT SUM(ven.Quantidade) AS QTotal
		 , SUM(ven.Valor) AS VTotal
		 , pro.Descricao
FROM Item_venda ven
JOIN Produto pro
ON pro.Codigo = ven.Cod_Produto
WHERE ven.Valor > 5
GROUP BY pro.Descricao
HAVING SUM(ven.valor) >= 10
```

######  

###### **Index**

```
SELECT ...
WHERE Profissao = 1
AND Genero = "M"
```

######  

###### **Transactions (Objetivos da Aula)**

###### **Transactions**

###### - Inicio = Insert, Delete, Update

###### - Resolução = Commit, Rollback

###### - Fim = Novos Dados ou Dados Originais

######  

###### **ACID - Transactions**

###### - Atomicidade - Todas operações executadas com sucesso. (Commit ou Rollback).

###### - Consistência - Unicidade de chaves, restrições de integridade lógica, etc...

###### - Isolamento - Várias transações podem acessar simultaneamente o mesmo registro (ou parte do registro).

###### - Durabilidade - Depois do Commit, mesmo com erros, queda de energia, etc. As alterações devem ser aplicadas.

######  

###### **SGDBR na prática (Objetivos da Aula)**

###### **SGDBs-R**

###### **Banco de Dados Pagos**

###### - Oracle, Microsoft SQL Server, IBM DB2

######  

###### **Banco de Dados Gratuitos**

###### - PostgreSQL, MySQL, SQLite

######  

###### **Link Download PostgreSQL**

###### https://www.enterprisedb.com/downloads/postgres-postgresql-downloads

######  

###### **Criando Banco de Dados (Objetivos da Aula)**

###### **Criar um Banco de Dados usando PostgreSQL (Versão Windows)**

###### - Abrir o Programa

###### - Clicar com o botão direito em cima de Server e ir em Create Server

###### - General/Name = Colocar um nome

###### - Connection/Host = localhost ou ip remoto

###### - Port = 5432

######  

###### **Código usado na Aula (PostgreSQL)**

```
CREATE TABLE cliente
(codigo NUMERIC(10) NOT NULL PRIMARY KEY,
nome VARCHAR(100) NOT NULL,
telefone VARCHAR(15)
)

INSERT INTO cliente (codigo, nome, telefone)
VALUES (1,'Lorem Ipsum', '(99) 9999 9999')

COMMIT

SELECT * FROM cliente

DELETE FROM cliente

COMMIT

SELECT * FROM cliente
```