# NLW Agents - Projeto Fullstack

Este é um projeto fullstack desenvolvido durante o NLW (Next Level Week) Agents, que implementa um sistema de gerenciamento de salas com backend em Node.js/Fastify e frontend em React.

## 🚀 Tecnologias Utilizadas

### Backend
- **Node.js** - Runtime JavaScript
- **Fastify** - Framework web rápido e eficiente
- **TypeScript** - Linguagem de programação tipada
- **Drizzle ORM** - ORM moderno para TypeScript
- **PostgreSQL** - Banco de dados relacional
- **Zod** - Validação de schemas
- **Docker** - Containerização do banco de dados

### Frontend
- **React 19** - Biblioteca para interfaces de usuário
- **Vite** - Build tool e dev server
- **TypeScript** - Linguagem de programação tipada
- **React Router DOM** - Roteamento
- **TanStack Query** - Gerenciamento de estado do servidor
- **Tailwind CSS** - Framework CSS utilitário
- **Radix UI** - Componentes acessíveis
- **Lucide React** - Ícones

## 📁 Estrutura do Projeto

```
aulas/
├── server/                 # Backend
│   ├── src/
│   │   ├── db/           # Configuração do banco de dados
│   │   │   ├── schema/   # Schemas do Drizzle
│   │   │   └── migrations/
│   │   ├── http/         # Rotas da API
│   │   └── server.ts     # Servidor principal
│   ├── docker/           # Configuração Docker
│   └── package.json
└── web/                  # Frontend
    ├── src/
    │   ├── components/   # Componentes React
    │   ├── pages/        # Páginas da aplicação
    │   └── app.tsx       # Componente principal
    └── package.json
```

## 🛠️ Instalação e Configuração

### Pré-requisitos
- Node.js 18+
- Docker e Docker Compose
- Git

### 1. Clone o repositório
```bash
git clone <url-do-repositorio>
cd aulas
```

### 2. Configure o Backend

```bash
cd server
npm install
```

Crie um arquivo `.env` na pasta `server/`:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 3. Configure o Frontend

```bash
cd ../web
npm install
```

### 4. Inicie o Banco de Dados

```bash
cd ../server
docker-compose up -d
```

### 5. Execute as Migrações

```bash
cd server
npm run db:seed
```

### 6. Inicie os Servidores

**Backend:**
```bash
cd server
npm run dev
```

**Frontend:**
```bash
cd web
npm run dev
```

## 🌐 Endpoints da API

### Health Check
- `GET /health` - Verifica se o servidor está funcionando

### Salas
- `GET /rooms` - Lista todas as salas

## 🗄️ Banco de Dados

O projeto utiliza PostgreSQL com pgvector para suporte a vetores. A estrutura atual inclui:

### Tabela `rooms`
- `id` (UUID) - Identificador único
- `name` (TEXT) - Nome da sala
- `description` (TEXT) - Descrição da sala
- `createdAt` (TIMESTAMP) - Data de criação

## 🎯 Funcionalidades

### Backend
- ✅ Servidor Fastify configurado
- ✅ CORS habilitado para desenvolvimento
- ✅ Validação com Zod
- ✅ ORM Drizzle configurado
- ✅ Banco PostgreSQL com Docker
- ✅ Migrações automáticas

### Frontend
- ✅ Aplicação React com TypeScript
- ✅ Roteamento com React Router
- ✅ Gerenciamento de estado com TanStack Query
- ✅ UI moderna com Tailwind CSS
- ✅ Componentes acessíveis com Radix UI

## 🚀 Scripts Disponíveis

### Backend (`server/`)
```bash
npm run dev      # Inicia o servidor em modo desenvolvimento
npm start        # Inicia o servidor em produção
npm run db:seed  # Executa as migrações do banco
```

### Frontend (`web/`)
```bash
npm run dev      # Inicia o servidor de desenvolvimento
npm run build    # Gera build de produção
npm run preview  # Visualiza o build de produção
```

## 🔧 Configuração de Desenvolvimento

### Linting e Formatação
O projeto utiliza Biome para linting e formatação:
- Backend: `npx @biomejs/biome check`
- Frontend: `npx @biomejs/biome check`

### TypeScript
- Backend: `npx tsc --noEmit`
- Frontend: `npx tsc --noEmit`

## 📝 Variáveis de Ambiente

### Backend (.env)
```env
PORT=3333                                    # Porta do servidor
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents  # URL do banco
```

## 🐳 Docker

O banco de dados PostgreSQL é executado via Docker Compose:

```bash
cd server
docker-compose up -d    # Inicia o banco
docker-compose down     # Para o banco
```

## 🤝 Contribuição

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 👨‍💻 Autor

Desenvolvido durante o NLW Agents da Rocketseat.

---