# Exercícios de SQL - Visão (VIEW), CHECK OPTION e Trigger

## 1) Criar uma visão dos funcionários de Florianopolis com mais de 40 anos

Criar uma visão que apresenta o código, nome, CPF e idade dos funcionários de Florianopolis com mais de 40 anos. Defina esta visão com a cláusula `WITH CHECK OPTION`.

## 2) Consultar os dados da visãoc

Consulte os dados da visão. Qual(is) funcionário(s) voê enxerga?

## 3) Inserção através da visão - Francisco

Inserir o funcionário de nome Francisco, CPF 33300033333, 38 anos e código 9 através da visão. A inserção funcionou?

## 4) Inserção através da visão - Rodrigo

Inserir o funcionário de nome Rodrigo, CPF 22200022233, 41 anos e código 10 através da visão.

## 5) Consultar a visão após inserção

Consulte os dados da visão. Você visualiza a tupla do Rodrigo?

## 6) Definir uma trigger de inserção

Definir uma trigger que, ao invés de inserir na visão, insere diretamente na tabela Funcionários, preenchendo o atributo cidade com ‘Florianopolis’.

## 7) Inserção através da trigger - Raul

Inserir o funcionário de nome Raul, CPF 44400044433, 53 anos e código 11.

## 8) Consultar a visão após inserção via trigger

Consulte os dados da visão. Você visualiza a tupla do Raul?
