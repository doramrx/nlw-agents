# NLW Agents

Projeto desenvolvido durante o evento **NLW (Next Level Week)** da Rocketseat, focado em criar uma aplicação de agentes inteligentes.

## 🚀 Tecnologias Utilizadas

### Backend
- **Fastify** - Framework web rápido para Node.js
- **TypeScript** - Linguagem de programação tipada
- **Drizzle ORM** - ORM moderno para TypeScript
- **PostgreSQL** - Banco de dados relacional
- **Zod** - Validação de schemas
- **Docker** - Containerização da aplicação

### Ferramentas de Desenvolvimento
- **Biome** - Linter e formatter
- **Drizzle Kit** - Ferramentas para migrações e seeds

## 📁 Estrutura do Projeto

```
src/
├── db/
│   ├── connection.ts    # Configuração do banco de dados
│   ├── schema/          # Schemas do Drizzle ORM
│   └── migrations/      # Migrações do banco
├── http/
│   └── routes/          # Rotas da API
├── env.ts              # Configuração de variáveis de ambiente
└── server.ts           # Servidor Fastify
```

## 🛠️ Padrões de Projeto

- **Clean Architecture** - Separação clara entre camadas
- **Type Safety** - Uso extensivo de TypeScript
- **Schema Validation** - Validação com Zod
- **Database Migrations** - Controle de versão do banco com Drizzle
- **Environment Configuration** - Configuração centralizada de variáveis

## ⚙️ Setup e Configuração

### Pré-requisitos
- Node.js 18+
- Docker e Docker Compose
- PostgreSQL (via Docker)

### Instalação

1. **Clone o repositório**
```bash
git clone <repository-url>
cd server
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure as variáveis de ambiente**
```bash
# Crie um arquivo .env na raiz do projeto
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

4. **Inicie o banco de dados**
```bash
docker-compose up -d
```

5. **Execute as migrações**
```bash
npx drizzle-kit migrate
```

6. **Popule o banco com dados iniciais**
```bash
npm run db:seed
```

7. **Inicie o servidor**
```bash
# Desenvolvimento
npm run dev

# Produção
npm start
```

## 📡 Endpoints

- `GET /health` - Health check
- `GET /rooms` - Lista todas as salas

## 🐳 Docker

O projeto inclui configuração Docker para o banco de dados PostgreSQL com pgvector para operações de IA.

```bash
# Iniciar apenas o banco
docker-compose up -d

# Parar o banco
docker-compose down
```

## 📝 Scripts Disponíveis

- `npm run dev` - Inicia o servidor em modo desenvolvimento
- `npm start` - Inicia o servidor em modo produção
- `npm run db:seed` - Popula o banco com dados iniciais

---

Desenvolvido com 💜 durante o NLW da Rocketseat 