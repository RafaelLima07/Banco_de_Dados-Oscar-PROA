# E o Oscar vai para?...

## Nessa atividade, proposta pelo professor Gabriel Augusto, eu deveria pesquisar em um banco de dados, utilizando comandos de MY SQL, para responder as seguintes perguntas:

### Pergunta 1 - Quantas vezes Natalie Portman foi indicada ao Oscar?
R: 3 Vezes.
SQL-Script: SELECT nome_do_indicado FROM filmes WHERE nome_do_indicado="Natalie Portman";


### Pergunta 2 - Quantos Oscars Natalie Portman ganhou?
R: 1 Vez 
SQL-Script: SELECT nome_do_indicado, vencedor FROM filmes WHERE nome_do_indicado="Natalie Portman";

### Pergunta 3 - Amy Adams já ganhou algum Oscar?
R: Não
SQL-Script: SELECT nome_do_indicado, vencedor FROM filmes WHERE nome_do_indicado="Amy Adams";

### Pergunta 4 -  A série de filmes Toy Story ganhou um Oscar em quais anos?
R: Os filmes Toy Story nunca ganharam Oscar.
SQL-Script: SELECT nome_filme, ano_cerimonia, vencedor FROM filmes WHERE nome_filme="Toy Story";

### Pergunta 5 - A partir de que ano que a categoria "Actress" deixa de existir? 
R: Depois de 1976, à categoria "Actress" deixou de existir.
SQL-Script: SELECT categoria, ano_cerimonia FROM filmes WHERE categoria="Actress";

### Pergunta 6 -  O primeiro Oscar para melhor Atriz foi para quem? Em que ano?
R: À ganhadora foi Janet Gaynor, no ano de 1928.
SQL-Script: SELECT categoria, nome_do_indicado, ano_cerimonia, vencedor FROM filmes WHERE categoria="ACTRESS";

## Pergunta 7 - Na coluna/campo "Vencedor", altere todos os valores com "Sim" para 1 e todos os valores "Não" para 0.
SQL-Script:

UPDATE filmes
SET vencedor = 1
WHERE vencedor = "Sim";

UPDATE filmes
SET vencedor = 0
WHERE vencedor = "Não";


### Pergunta 8 - Em qual edição do Oscar "Crash" ganhou o prêmio principal?
R: 2006 
SQL-Script: SELECT ano_cerimonia, categoria, nome_filme, vencedor FROM filmes WHERE nome_filme="Crash";

## Pergunta 9 - Bom... dê um Oscar para um filme que merece muito, mas não ganhou.
SQL-Script: SELECT id_filme, ano_cerimonia, categoria, nome_filme, vencedor FROM filmes WHERE nome_filme="Saving Private Ryan";

UPDATE filmes
SET vencedor = 1
WHERE id_filme = "7862";

## Pergunta 10 - O filme Central do Brasil aparece no Oscar?
R: Sim, no ano de 1999.
SQL-Script: SELECT id_filme, ano_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor FROM filmes WHERE nome_do_indicado="Fernanda Montenegro";

## Pergunta 11 - Inclua no banco 3 filmes que nunca foram nem nomeados ao Oscar, mas que merecem ser. 
#### SQL-Script: 
#### INSERT INTO filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES 
#### ('2011', '2012', '84', 'ACTOR', 'Ryan Gosling', 'Drive', '0'), 
#### ('2004', '2005', '77', 'WRITING', 'Charlie Kaufman', 'Eternal Sunshine of the Spotless Mind', '0'), 
#### ('1994', '1995', '67', 'DIRECTING', 'Frank Darabont', 'The Shawshank Redemption', '0'); 

## Pergunta 12 - Pensando no ano em que você nasceu: Qual foi o Oscar de melhor filme, Melhor Atriz e Melhor Diretor?
2004, 
Melhor Filme: "The Lord of the Rings: The Return of the King"
Melhor Atriz: Charlize Theron
Melhor Diretor: Peter Jackson.
SQL-Script: SELECT id_filme, ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor FROM filmes WHERE ano_cerimonia = 2004;

## Pergunta 13 - Agora procure 7 atrizes que não sejam americanas, europeias ou brasileiras.  Vamos cadastrá-los no nosso banco com o prêmio que você quiser. 
SQL-Script: 
INSERT INTO filmes (ano_filmagem, ano_cerimonia, edicao_cerimonia, categoria, nome_do_indicado, nome_filme, vencedor) VALUES 
('1991', '1992', '63', 'ACTRESS IN A LEADING ROLE', 'Gong Li', 'Raise the Red Lantern', '1'),
('2000', '2001', '73', 'ACTRESS IN A LEADING ROLE', 'Maggie Cheung', 'In the Mood for Love', '1'),
('2011', '2012', '84', 'ACTRESS IN A LEADING ROLE', 'Leila Hatami', 'A Separation', '1'),
('2010', '2011', '83', 'ACTRESS IN A LEADING ROLE', 'Jeon Do-yeon ', 'The Housemaid', '1'),
('2007', '2008', '80', 'ACTRESS IN A LEADING ROLE', 'Nadine Labaki ', 'Caramel', '1'),
('2010', '2011', '83', 'ACTRESS IN A LEADING ROLE', 'Lubna Azabal ', 'Incendies', '1'),
('2012', '2013', '85', 'ACTRESS IN A LEADING ROLE', 'Doona Bae', 'Cloud Atlas', '1');

## Pergunta 14 -Agora vamos falar da sua vida. Me diga o nome de uma pessoa que você admira e o que ela fez na sua vida. 
Minha mãe. Inúmeras coisas, mas a que eu quero citar é, me ensinou a enxergar possibilidades e com isso me mostrou que eu poderia fazer varias coisas boas na minha vida.
