# NLW Agents

Projeto desenvolvido durante o evento **NLW (Next Level Week)** da Rocketseat, focado em criar uma aplicação de agentes inteligentes.

## 🚀 Tecnologias Utilizadas

### Backend
- **Fastify** - Framework web rápido para Node.js
- **Drizzle ORM** - ORM moderno para TypeScript
- **PostgreSQL** - Banco de dados relacional
- **pgvector** - Extensão para vetores no PostgreSQL
- **Zod** - Validação de schemas TypeScript
- **TypeScript** - Linguagem de programação tipada

### Ferramentas de Desenvolvimento
- **Biome** - Linter e formatter de código
- **Docker Compose** - Containerização do banco de dados
- **Ultracite** - Configuração de estilo de código

## 📋 Pré-requisitos

- Node.js 18+
- Docker e Docker Compose
- PostgreSQL (via Docker)

## ⚙️ Configuração do Projeto

### 1. Clone o repositório
```bash
git clone <url-do-repositorio>
cd server
```

### 2. Instale as dependências
```bash
npm install
```

### 3. Configure as variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Inicie o banco de dados
```bash
docker-compose up -d
```

### 5. Execute as migrações (se necessário)
```bash
npx drizzle-kit migrate
```

### 6. Execute o projeto
```bash
# Desenvolvimento
npm run dev

# Produção
npm start
```

## 🗄️ Estrutura do Banco de Dados

O projeto utiliza PostgreSQL com a extensão pgvector para operações com vetores, ideal para aplicações de IA e machine learning.

## 📁 Estrutura do Projeto

```
src/
├── db/           # Configurações do banco de dados
├── http/         # Rotas da API
├── env.ts        # Validação de variáveis de ambiente
└── server.ts     # Servidor principal
```

## 🔧 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo desenvolvimento
- `npm start` - Executa o servidor em modo produção
- `npm run db:seed` - Popula o banco com dados iniciais

## 📝 Padrões de Projeto

- **Clean Architecture** - Separação clara de responsabilidades
- **Type Safety** - Uso extensivo de TypeScript e Zod
- **Environment Validation** - Validação de variáveis de ambiente
- **Database Migrations** - Controle de versão do banco de dados

---

*Este README foi criado usando IA com o Cursor* 