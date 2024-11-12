# desafio2_OficinaMecanica

Esse projeto  é um desafio proposto no curso "Análise de Dados com Power BI" da DIO (Digital Innovation One) consiste em desenvolver um esquema de banco de dados 
para gerenciar uma oficina mecânica, com foco no controle e execução de ordens de serviço. O objetivo é estruturar um modelo relacional que permita o armazenamento e a consulta 
de informações sobre clientes, veículos, serviços, mecânicos e peças, além de facilitar o cálculo de custos e a gestão das ordens de serviço.

O esquema do banco de dados deve atender aos seguintes requisitos principais:

- Gestão de Clientes e Veículos: Cada cliente pode ter múltiplos veículos registrados na oficina. Os dados do cliente incluem informações como nome, telefone, e-mail e endereço.
Cada veículo possui um identificador único, além de informações como modelo, marca, ano de fabricação e placa. Cada veículo está associado a um único cliente.
- Ordem de Serviço: Quando um cliente leva um veículo para a oficina, é gerada uma ordem de serviço (OS) que contém informações essenciais, como número da OS,
data de emissão, data de conclusão, valor total e status. A ordem de serviço é associada a um veículo e mecânicos responsáveis pela execução dos serviços.
- Serviços e Peças: A oficina oferece diferentes tipos de serviços (exemplo: "Troca de óleo", "Reparo de suspensão"), que são registrados na tabela de serviços, cada um com um valor unitário.
As peças usadas nos serviços também têm seu valor registrado. Cada peça pode ser utilizada em várias ordens de serviço.
- Mecânicos: A oficina tem mecânicos responsáveis pela execução dos serviços. Cada mecânico tem informações como nome, endereço e especialidade.
A equipe de mecânicos pode ser associada a várias ordens de serviço, sendo responsável pela execução de um ou mais serviços.
- Tabela de Mão de Obra: A oficina possui uma tabela de referência de mão de obra, onde são definidos os valores cobrados por hora de trabalho dos mecânicos para diferentes tipos de serviço.
Esse valor é utilizado para calcular o custo da mão de obra nas ordens de serviço.

Vamos descrever os relacionamentos entre essas entidades.

* Cliente ↔ Veículo: Um cliente pode ter vários veículos, mas um veículo pertence a apenas um cliente.
* Veículo ↔ Ordem de Serviço: Cada veículo pode ter várias ordens de serviço associadas a ele, mas uma ordem de serviço é sempre para um único veículo.
* Ordem de Serviço ↔ Serviço: Cada ordem de serviço pode envolver múltiplos serviços, e um serviço pode ser realizado em várias ordens de serviço.
* Ordem de Serviço ↔ Mecânico: Um mecânico pode ser designado para várias ordens de serviço, e uma ordem de serviço pode envolver um ou mais mecânicos.
* Ordem de Serviço ↔ Peça: Uma ordem de serviço pode ter várias peças associadas a ela, e uma peça pode ser utilizada em várias ordens de serviço.
* Ordem de Serviço ↔ Tabela de Mão de Obra: Cada ordem de serviço será associada a uma tabela de mão de obra que define o custo dos serviços executados (valor/hora).


O desafio do curso é construir um modelo relacional eficiente para uma oficina mecânica, com foco no gerenciamento de ordens de serviço e na análise de dados. 
Com esse modelo, a oficina pode ter um controle mais preciso de seus processos, além de gerar relatórios analíticos que auxiliem na tomada de decisão.

