# Projeto Banco de Dados - Game of Thrones

## Objetivo do Trabalho:

<p> O trabalho consiste em criar um banco de dados com realação a série Game of Thrones e realizar a modelagem dados junto com a criação do Dashboards</p> 

<p> Neste trabalho, foram importadas as tabelas da série disponibilizada pelo Resília nas quais foram criadas questões que serão respondidas por meio de comandos SQL</p>

## Como foi realizado?

### ✔️ Criação do Banco e Importação das Tabelas.

<p> Primeiramente é necessário o comando para utilizar o mysql pelo shell via xampp.


 -  ``digitar no shell o comando: mysql -u root -p``
 -  ``Apertar enter sem utilização do password``
 -  ``create database got;``
 -  ``use got;``

Para alimentar as tabelas no banco de dados, foi feito da seguinte forma:

 -  ``Com o xampp aberto, clicar em admin no mysql para abrir o phpMyAdmin``
 -  ``Selecionar o banco -> ir em importar -> escolher arquivo ``
</p>

### ✔️ Comandos SQL para exibição de queries:

Tabela 1 Pergunta 1

- <p> Quantos episódios tiveram notas maiores que 8? </p>

``MariaDB [projeto_got]> select count(rating) from got_episodes_v4 where rating > 8;``



Tabela 1 Pergunta 2

- <p> Quantos episódios tiveram notas abaixo de 7? </p>

``MariaDB [projeto_got]> select count(rating) from got_episodes_v4 where rating < 7;``

Tabela 1 Pergunta 3

- Qual o total de episódios?

``MariaDB [projeto_got]> select count(episode) from got_episodes_v4;``

Tabela 1 Pergunta 4

- Quantos episódios George R. R. Martin escreveu na série? 

``MariaDB [projeto_got]> select season, episode, writer_1 from got_episodes_v4 where writer_1 = "george r.r. martin" limit 10;``

Tabela 1 Pergunta 5

- Mostrar quantidade de episódios agrupados por temporada e escritas por George R. R. Martin:

``MariaDB [got]> select  writer_1, count(episode)  from got_episodes_v4
    -> where writer_1 = "George R.R. Martin";``

``MariaDB [got]> select season, count(episode), writer_1 from got_episodes_v4
    -> where writer_1 = 'George R.R. Martin'
    -> group by season;``
    
    
Tabela 2 Pergunta 1

- Quais atores apareceram mais que 60 vezes na série?

``MariaDB [projeto4_got]> select * from characters_v4 where Episodes_appeared > 60;``

Tabela 2 Pergunta 2

- Quantos atores apareceram 1 vez na série?

``MariaDB [projeto4_got]> select count(ator) from characters_v4 where  Episodes_appeared < 2 ;``

Tabela 2 Pergunta 3

- Quantos atores apareceram no ano de 2012?

``MariaDB [projeto4_got]> select count(ator) from characters_v4 where First_appearance = 2012;``

Tabela 3 Pergunta 1

- Quantas regiões tem na série?

``MariaDB [projeto4_got]> select count(Region) from houses_v1;``

Tabela 3 Pergunta 2

- Quantas casas tem na região North? 

``MariaDB [projeto4_got]> select count(House_name) from houses_v1 where Region = "North";``

Tabela 3 Pergunta 3

- Quais casas começam com a letra a?

``MariaDB [projeto_got]> select * from houses_v1 where house_name like 'a%';``

Tabela 3 Pergunta 4

-  Quais regiões terminam com a letra K? 

``MariaDB [projeto_got]> select house_name from houses_v1 where house_name like '%k';``


##  ✔️ Técnicas e tecnologias utilizadas

-  ``Xampp``
-  ``Canvas``
-  ``Github``
-  ``MySql``
-  ``Workbench``
-  ``MER/DER/DDL``
-  ``SGBD / phpMyAdmin``

# Autores

| [<img src="https://avatars.githubusercontent.com/u/114115311?v=4" width=115><br><sub>Paulo Victor</sub>](https://github.com/pevehdev)  |  [<img src="https://avatars.githubusercontent.com/u/81197504?v=4" width=115><br><sub>Isabella</sub>](https://github.com/Isabellabarroos) |  [<img src="https://avatars.githubusercontent.com/u/114196729?v=4" width=115><br><sub>Victória</sub>](https://github.com/Vic-Carvalho)  | [<img src="https://avatars.githubusercontent.com/u/114114906?v=4" width=115><br><sub>Bruna Murta</sub>](https://github.com/brumurta) | [<img src="https://avatars.githubusercontent.com/u/114115205?v=4" width=115><br><sub>Andriele</sub>](https://github.com/Andriele92) |
| :---: | :---: | :---: | :---: | :---: |
