# Stock.io

Marketplace onde usuários criam suas próprias lojas, cadastram produtos e
avaliam lojas e produtos. Projeto do processo trainee da CJR, em
desenvolvimento.

## Stack

| Parte    | Tecnologias                               |
|----------|-------------------------------------------|
| Backend  | NestJS, Prisma, SQLite                    |
| Frontend | Next.js, React, Tailwind, Axios           |

## Estado atual

- **Frontend**: telas de login, cadastro e perfil do usuário, com dados de
  exemplo em `frontend/mock/`. As chamadas para o backend já estão em
  `frontend/api/api.js`.
- **Backend**: banco modelado no Prisma (`backend/prisma/schema.prisma`) com
  usuários, lojas, produtos, categorias, imagens e avaliações. As rotas da
  API ainda não foram implementadas.

## Como rodar

Precisa do Node.js.

### Backend

```bash
cd backend
npm install
echo 'DATABASE_URL="file:./dev.db"' > .env
npx prisma generate
npx prisma migrate dev
PORT=3001 npm run start:dev
```

A API sobe em http://localhost:3001, que é o endereço que o frontend usa.

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Acesse http://localhost:3000.

## Estrutura

```text
backend/
  prisma/       schema do banco e migrations
  src/          código do NestJS
frontend/
  app/          páginas (login, cadastro, perfil)
  api/          chamadas para o backend
  mock/         dados de exemplo
  public/       imagens
```

## Equipe

- [Cauê Oliveira](https://github.com/caueoliver)
- [Gabriel Simplicio](https://github.com/gabrielsimplicioo)
- [Luís Moura](https://github.com/LuisMoura18)
- [Vitor Duarte](https://github.com/vitor11-a)

O código veio dos repositórios
[pt_backend](https://github.com/caueoliver/pt_backend) e
[pt_frontend](https://github.com/caueoliver/pt_frontend), com o histórico de
commits preservado.
