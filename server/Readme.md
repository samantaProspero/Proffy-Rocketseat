# Rocketseat Next Level Week 02


## Segunda aula: 
- Typescript
- backend da aplicação com Node
- Banco de dados com Sqlite3


# Intalações: 

yarn init -y

yarn add typescript -D
yarn tsc -init

em tsconfig.json: troca na linha 7: es5 por es2017

yarn add ts-node-dev -D

cria o script: 
"start": "tsnd --transpile-only --ignore-watch node_modules --respawn src/server.ts"

yarn add express
yarn add @types/express -D

Para o express conseguir ler json, em server.ts: 
app.use(express.json())


# Funcionalidades:

## Conexões:
- Rota para listas o total de conexões realizadas;
- Rota para criar uma nova conexão;

## Aulas:
- Rota pra criar uma aula;
- Rota para listar aulas;
  - Filtrar por matéria, dia da semana e horário

# Banco Relacional-sqlite3

- sudo apt-get install sqlite3
- yarn add knex sqlite3

-Obs: as migrations controlam a versão do db

-Para o knex criar/ler as migrations em typescript, cria o script:
"knex:migrate": "knex --knexfile knexfile.ts migrate:latest"
e esse comando vai sobescrever o comando padrão 

- Para desfazer:
"knex:migrate:rollback": "knex --knexfile knexfile.ts migrate:rollback"