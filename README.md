# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

## Jogos

POST /todo

para cadastrar um novo todo o usuário deve estar autenticado e enviar uma requisição com seu id

exemplo de corpo de requisição
` { 
  "todo" : "ler um livro",
  "userId": 3 
  }
`

GET /todo

para ter acesso aos todos somente o usuário que o cadastrou pode ter acesso a ele quando autenticado.

## Livros

Post /livros

Qualquer usuário autenticado pode fazer o cadastro de livros

`{ 
  "name" : "Clockwork Orange" 
}`

GET /livros

qualquer usuário pode ter acesso aos livros cadastrados sem  precisar estar autenticado
