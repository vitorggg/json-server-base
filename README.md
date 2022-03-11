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

### Sports

GET /sports

Retorna todos os esportes cadastrados por todos os usuários. Para selecionar os esportes de apenas um usuário em especifico, utilize o param: "?userId=(user)"

POST /sports (logado/token necessário)

Recurso para cadastro de novos esportes na lista de esportes do usuário. A requisição deve ter o seguinte corpo, seguindo o exemplo:

{
type: "field",
name: "baskteball",
userId: 14
}

### Color

GET /color

Retorna toda a lista de cores favoritas dos usuários. Para selecionar a cor favorita de apenas um usuário em especifico, utilize o param: "?userId=(user)"

POST /sports (logado/token necessário)

Recurso para cadastro de uma nova cor favorita na lista de esportes do usuário. A requisição deve ter o seguinte corpo, seguindo o exemplo:

{
name: "red",
userId: 24
}
