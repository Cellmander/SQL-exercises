# Exercício de SQL - DDL e Manipulação de Esquemas

## 1) Criar as seguintes tabelas

Considerar que os atributos sublinhados fazem parte da chave primária e os em itálico são chaves estrangeiras (não acentuar as palavras!):

### a) Ambulatorios
- **nroa** (int) - Chave Primária
- andar (numeric(2)) - NOT NULL
- capacidade (smallint)

### b) Medicos
- **codm** (int) - Chave Primária
- nome (varchar(40)) - NOT NULL
- idade (smallint) - NOT NULL
- cidade (varchar(40))
- CPF (numeric(11)) - NOT NULL e UNIQUE
- especialidade (varchar(30))
- *nroa* (int) - Chave Estrangeira

### c) Pacientes
- **codp** (int) - Chave Primária
- nome (varchar(40)) - NOT NULL
- idade (smallint) - NOT NULL
- cidade (varchar(40))
- CPF (numeric(11)) - NOT NULL e UNIQUE
- doenca (varchar(40)) - NOT NULL

### d) Funcionarios
- **codf** (int) - Chave Primária
- nome (varchar(40)) - NOT NULL
- idade (smallint) - NOT NULL
- cidade (varchar(40))
- CPF (numeric(11)) - NOT NULL e UNIQUE
- salário (numeric(10))
- cargo (varchar(40))

### e) Consultas
- **codm** (int) - Chave Primária Composta
- **codp** (int) - Chave Primária Composta
- data (date)
- hora (time)

## 2) Alterar a tabela Funcionarios

Remover o atributo cargo

## 3) Criar um índice

Criar um índice para o atributo cidade na tabela Pacientes
