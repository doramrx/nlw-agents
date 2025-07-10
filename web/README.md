# NLW Agents

Projeto desenvolvido durante o evento **NLW (Next Level Week)** da Rocketseat, focado em criar uma aplicação web moderna com React e TypeScript.

## 🚀 Tecnologias Utilizadas

### Core
- **React 19** - Biblioteca para construção de interfaces
- **TypeScript** - Superset do JavaScript com tipagem estática
- **Vite** - Build tool e dev server

### UI/UX
- **Tailwind CSS 4** - Framework CSS utility-first
- **Radix UI** - Componentes acessíveis e customizáveis
- **Shadcn UI** - Sistema de componentes
- **Lucide React** - Ícones modernos
- **Class Variance Authority** - Utilitário para variantes de componentes

### Estado e Roteamento
- **TanStack Query** - Gerenciamento de estado do servidor
- **React Router DOM** - Roteamento client-side

### Desenvolvimento
- **Biome** - Linter e formatter (substituindo ESLint + Prettier)
- **Ultracite** - Configuração de linting otimizada

## 📁 Estrutura do Projeto

```
src/
├── components/     # Componentes reutilizáveis
│   └── ui/        # Componentes de UI base
├── pages/         # Páginas da aplicação
├── lib/           # Utilitários e configurações
├── app.tsx        # Componente principal
└── main.tsx       # Ponto de entrada
```

## 🛠️ Configuração e Setup

### Pré-requisitos
- Node.js 18+ 
- npm ou yarn

### Instalação

1. Clone o repositório:
```bash
git clone <url-do-repositorio>
cd web
```

2. Instale as dependências:
```bash
npm install
```

3. Execute o servidor de desenvolvimento:
```bash
npm run dev
```

4. Acesse a aplicação em `http://localhost:5173`

### Scripts Disponíveis

- `npm run dev` - Inicia o servidor de desenvolvimento
- `npm run build` - Gera build de produção
- `npm run preview` - Visualiza o build de produção

## 🎯 Funcionalidades

- **Criação de Salas**: Interface para criar novas salas de chat
- **Sistema de Salas**: Navegação entre salas com IDs únicos
- **Roteamento**: Navegação client-side com React Router
- **Estado Global**: Gerenciamento de estado com TanStack Query

## 🔧 Configurações

### TypeScript
- Configuração strict com null checks
- Path mapping configurado (`@/*` → `./src/*`)

### Vite
- Plugin React configurado
- Tailwind CSS integrado
- Alias de path configurado

### Biome
- Configuração baseada no preset Ultracite
- Formatação automática com semicolons opcionais

## 📝 Padrões de Projeto

- **Componentes Funcionais**: Uso de hooks do React
- **TypeScript**: Tipagem estática em todo o projeto
- **Utility-First CSS**: Estilização com Tailwind CSS
- **Roteamento Declarativo**: Rotas definidas com React Router
- **Estado Centralizado**: Gerenciamento com TanStack Query

---

Desenvolvido com 💜 durante o **NLW Agents** da Rocketseat 