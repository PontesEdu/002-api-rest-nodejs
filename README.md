Transactions API

Este é um pequeno projeto de estudos utilizando Node.js com TypeScript. Ele fornece uma API para gerenciar transações financeiras, utilizando Fastify, Knex e suporte para SQLite e PostgreSQL. O projeto também faz uso de cookies para gerenciamento de sessão e foi hospedado no Render.

Tecnologias Utilizadas

Node.js + TypeScript

Fastify (framework web)

Knex.js (query builder para banco de dados)

SQLite e PostgreSQL (bancos de dados suportados)

Dotenv (gerenciamento de variáveis de ambiente)

Tsup (compilação do projeto)

Render (deploy da API)

Como Executar o Projeto Localmente

Clone este repositório:

git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_PROJETO>

Instale as dependências:

yarn install  # ou npm install

Configure as variáveis de ambiente:

Crie um arquivo .env na raiz do projeto e defina as variáveis necessárias. Exemplo:

DATABASE_CLIENT=sqlite  # ou postgres
DATABASE_URL=file:./db.sqlite  # Para SQLite

Execute as migrações do banco de dados:

yarn knex migrate:latest

Inicie o servidor:

yarn dev

A API estará rodando em http://localhost:3333.

Rotas Disponíveis

Criar uma transação

POST /transactions

Body:

{
  "title": "Salário",
  "amount": 5000,
  "type": "credit"
}

Listar transações

GET /transactions

Buscar transação por ID

GET /transactions/:id

Obter o saldo total

GET /transactions/balance

Compilação e Deploy

Para gerar o build do projeto, utilize:

yarn build

O deploy foi realizado no Render. Caso precise configurar a aplicação, defina as variáveis de ambiente no Render conforme o arquivo .env.

Licença

Este é um projeto de estudos, sem licença específica.

