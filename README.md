# NLW Agents - API

Este projeto foi desenvolvido durante o evento **NLW Agents** promovido pela [RocketSeat](https://www.rocketseat.com.br/).

## Descrição

API para gerenciamento de salas (rooms), utilizando Fastify, Drizzle ORM e PostgreSQL.

---

## Tecnologias e Bibliotecas

- **Node.js** + **TypeScript**
- **Fastify**: Framework web para Node.js
- **Zod**: Validação de esquemas e tipos
- **Drizzle ORM**: ORM para PostgreSQL
- **PostgreSQL**: Banco de dados relacional
- **drizzle-kit**: Migrations e geração de schema
- **drizzle-seed**: Seed de dados fake
- **dotenv**: Variáveis de ambiente
- **@biomejs/biome**: Linter e formatter
- **Docker**: Ambiente de banco de dados

---

## Padrões de Projeto

- **Validação de dados**: Utilizando Zod e integração com Fastify.
- **Separação de responsabilidades**: Rotas, conexão com banco e schemas organizados em pastas.
- **Migrations e Seeds**: Automatizados via Drizzle.

---

## Setup e Configuração

### 1. Clone o repositório

```bash
git clone <url-do-repo>
cd api
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto com:

```
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Suba o banco de dados com Docker

```bash
docker-compose up -d
```

### 5. Rode as migrations e o seed

```bash
# (Opcional) Gere as migrations se necessário
npx drizzle-kit generate:pg

# Popule o banco com dados fake
npm run db:seed
```

### 6. Inicie a API

```bash
npm run dev
```

Acesse: [http://localhost:3333/health](http://localhost:3333/health)

---

## Endpoints

- `GET /rooms` — Lista as salas cadastradas

---

## Scripts Úteis

- `npm run dev` — Inicia o servidor em modo desenvolvimento
- `npm run db:seed` — Popula o banco com dados fake

---

## Licença

ISC
