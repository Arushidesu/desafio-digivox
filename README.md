# Desafio Digivox

## API 
A API foi criada com Spring Boot e Maven como gerenciador de dependências e utilizando o banco de dados PostgreSQL. A API possui ao todo 3 tabelas, sendo elas livro, cliente e info. Todos os métodos de um CRUD (GET, POST, PUT e DELETE) foram devidamente implementados.

O deploy da API foi realizada no **Heroku** com o banco de dados PostgreSQL já embutido, e está disponível através desse link: https://biblioteca-apirest-digivox.herokuapp.com/api

O código fonte da API também está no **GitHub**, disponível em: https://github.com/Arushidesu/api-rest-digivox

## Front
O front foi desenvolvido utilizando Vue juntamente com vue-router, axios, jQuery e Bootstrap 4. Tudo foi utilizado via CDN, apesar da tentativa de tentar realizar via vue-cli. 

Está hospedado no **GitHub Pages**, nesse link: https://arushidesu.github.io/desafio-digivox/index.html#/

## Contexto
Praticamente tudo que foi solicitado no desafio foi realizado. 

- É possível cadastrar, editar, deletar e visualizar tanto clientes como livros. 

- Ao alugar um livro, a diferenciação de "alugado" para "reservado" é realizado quando o usuário preenche ou não a data. Na API a data também é inserida no mesmo local, no campo **data_reserva**.

- Ao cancelar um livro, apenas as flags na API são alteradas para **cancelado** e também é inserido no campo **data_cancelamento** a data em que foi cancelada. Apenas os livros que foram reservados aparecem na lista para serem cancelados.

- Ao devolver um livro, a flag **devolvido** é acionada e é preenhcido o campo **data_devolucao**. A lista é preenchida com livros que foram alugados e livros reservados que já passaram da data de reserva.

- A home mostra um pequeno dashboard em cads e as informações de devoluções e aluguéis semanais, como foram solicitadas.
