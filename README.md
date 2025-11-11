# Exercícios SQL
Exercícios realizados para a disciplina Banco de Dados I, do curso de Sistemas de Informação da UFSC

## Descrição
Exercícios para fixar os fundamentos da construção de querys utilizando SQL.

## Requisitos
Para simplificar a execução dos códigos, recomendo utilizar este site: https://sqliteonline.com/

## Conteúdos praticados
- DDL (Definição de esquemas)
- Atualização de dados (INSERT, UPDATE, DELETE, SELECT)
- Consultas, Junções e subconsultas
- Atualização com consulta, ordenação e agrupamento (ORDER BY e GROUP BY)
- Restrições de integridade
- Views

## Comandos para criação das tabelas
``` text 
create table Ambulatorios (nroa int, andar numeric(2)
not null, capacidade smallint, primary key(nroa));
create table Medicos (codm int, nome varchar(40) not
null, idade smallint not null, especialidade varchar(30),
CPF numeric(11) not null unique, cidade varchar(40),
nroa int, primary key(codm), foreign key(nroa)
references Ambulatorios);
create table Pacientes (codp int, nome varchar(40) not
null, idade smallint not null, cidade varchar(40), CPF
numeric(11) not null unique, doenca varchar(40) not null,
primary key(codp));
create table Funcionarios (codf int, nome varchar(40)
not null, idade smallint not null, cidade varchar(40),
salario numeric(10), CPF numeric(11) not null unique,
primary key(codf));
create table Consultas (codm int, codp int, data date,
hora time, primary key(codm, codp, data), foreign
key(codm) references Medicos, foreign key(codp)
references Pacientes);

```
## Comandos para inserção de dados nas tabelas
``` text
insert into Ambulatorios values (1,1,30), (2,1,50),
(3,2,40), (4,2,25), (5,2,55);
insert into Medicos (codm, nome, idade, especialidade,
CPF, cidade, nroa) values (1, 'Joao', 40, 'ortopedia',
10000100000, 'Florianopolis', 1), (2, 'Maria', 42,
'traumatologia', 10000110000, 'Blumenau', 2), (3,
'Pedro', 51, 'pediatria', 11000100000, 'Sao Jose', 2), (4,
'Carlos', 28, 'ortopedia', 11000110000, 'Joinville', NULL);
insert into Pacientes (codp, nome, idade, cidade, CPF,
doenca) values (1,'Ana', 21, 'Florianopolis',
20000200000, 'gripe'), (2,'Paulo', 24, 'Ilhota',
20000220000, 'fratura'), (3,'Lucia', 30, 'Biguacu',
22000200000, 'tendinite'), (4,'Carlos', 28,
'Joinville',11000110000, 'sarampo');
insert into Funcionarios (codf, nome, idade, CPF,
cidade, salario) values (1,'Rita', 32, 20000100000, 'Sao
Jose', 1200), (2,'Vera', 55, 30000110000, 'Palhoca',
1220), (3,'Caio', 45, 41000100000, 'Florianopolis', 1100),
(5,'Paula', 33, 61000111000, 'Florianopolis', 2500);
insert into Consultas (codm, codp, data, hora) values
(1,1,'2020/10/12','14:00'),
(1,4,'2020/11/4','12:00'),
(2,1,'2020/10/13','09:00'),
(2,2,'2020/10/13','11:00'),
(2,3,'2020/10/14','14:00'),
(2,4,'2020/10/14','17:00'),
(3,1,'2020/10/19','18:00'),
(3,3,'2020/10/12','10:00'),
(3,4,'2020/10/19','14:30'),
(4,4,'2020/10/20','13:00');
```
