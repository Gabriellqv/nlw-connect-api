# 🚀 NLW Connect API

API RESTful desenvolvida durante o Next Level Week (NLW) da Rocketseat. Uma aplicação backend completa para gerenciamento de conexões e networking, construída com TypeScript, Node.js e as melhores práticas de desenvolvimento.

## 📋 Sobre o Projeto

A NLW Connect API é uma API robusta desenvolvida durante o evento Next Level Week, focada em criar uma plataforma de conexões profissionais. A aplicação utiliza tecnologias modernas como Drizzle ORM, Docker, e TypeScript para garantir código limpo, tipado e escalável.

## ✨ Funcionalidades

- 🔐 Autenticação de usuários
- 👤 Gerenciamento de perfis
- 🔗 Sistema de conexões
- 📝 Criação e gerenciamento de conteúdo
- 🔍 Busca e filtros avançados
- 📊 Feed de atividades
- 🐳 Containerização com Docker
- 🗄️ Banco de dados relacional com Drizzle ORM

## 🛠️ Tecnologias Utilizadas

- **TypeScript** - Linguagem de programação com tipagem estática
- **Node.js** - Runtime JavaScript
- **Drizzle ORM** - ORM moderno e type-safe para TypeScript
- **Docker** - Containerização da aplicação
- **Docker Compose** - Orquestração de containers
- **TSUP** - Bundler rápido para TypeScript
- **Biome** - Linter e formatter rápido e moderno
- **HTTP Client** - Testes de API com arquivo `.http`

## 📦 Pré-requisitos

Antes de começar, você precisa ter instalado em sua máquina:

- [Node.js](https://nodejs.org/) (versão 18 ou superior)
- [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/)
- [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/)

## 🚀 Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/Gabriellqv/nlw-connect-api.git
cd nlw-connect-api
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto com as configurações necessárias:

```env
DATABASE_URL="postgresql://user:password@localhost:5432/nlw_connect"
PORT=3333
NODE_ENV=development
# Adicione outras variáveis conforme necessário
```

### 4. Execute com Docker Compose

Para subir o banco de dados e a aplicação:

```bash
docker-compose up -d
```

### 5. Execute as migrações do banco de dados

```bash
npm run db:migrate
# ou
npm run db:push
```

### 6. Execute o projeto em modo de desenvolvimento

```bash
npm run dev
```

A API estará disponível em `http://localhost:3333` (ou a porta configurada).

### 7. Build do projeto

```bash
npm run build
```

O código TypeScript será compilado para JavaScript na pasta `dist/`.

### 8. Execute em produção

```bash
npm start
```

## 🧪 Testando a API

O projeto inclui um arquivo `api.http` para testar os endpoints diretamente no VS Code com a extensão REST Client ou em outras ferramentas compatíveis.

Exemplo de uso:

```http
GET http://localhost:3333/api/endpoint
Content-Type: application/json
```

## 📁 Estrutura do Projeto

```
nlw-connect-api/
├── src/                  # Código fonte da aplicação
│   ├── controllers/      # Controladores das rotas
│   ├── models/           # Modelos de dados
│   ├── routes/           # Definição de rotas
│   ├── middleware/       # Middlewares customizados
│   ├── services/         # Lógica de negócio
│   ├── utils/            # Funções utilitárias
│   ├── db/               # Configuração do banco de dados
│   └── app.ts            # Arquivo principal da aplicação
├── .gitignore            # Arquivos ignorados pelo Git
├── api.http              # Arquivo para testes de API
├── biome.json            # Configuração do Biome
├── docker-compose.yml    # Configuração Docker Compose
├── drizzle.config.ts     # Configuração Drizzle ORM
├── package.json          # Dependências e scripts
├── tsconfig.json         # Configuração TypeScript
├── tsup.config.ts        # Configuração TSUP
└── README.md             # Este arquivo
```

## 🎯 Endpoints da API

A API segue os padrões REST. Exemplos de endpoints:

- `POST /api/auth/register` - Registrar novo usuário
- `POST /api/auth/login` - Autenticar usuário
- `GET /api/users/:id` - Obter perfil do usuário
- `GET /api/connections` - Listar conexões
- `POST /api/connections` - Criar nova conexão
- `GET /api/feed` - Obter feed de atividades

*Nota: Os endpoints específicos podem variar conforme a implementação.*

## 🐳 Docker

O projeto utiliza Docker para facilitar o desenvolvimento e deploy:

### Subir os containers

```bash
docker-compose up -d
```

### Parar os containers

```bash
docker-compose down
```

### Ver logs

```bash
docker-compose logs -f
```

## 🗄️ Banco de Dados

O projeto utiliza Drizzle ORM para gerenciar o banco de dados:

### Executar migrações

```bash
npm run db:migrate
```

### Gerar migrações

```bash
npm run db:generate
```

### Aplicar mudanças no schema

```bash
npm run db:push
```

### Abrir Drizzle Studio

```bash
npm run db:studio
```

## 🔧 Scripts Disponíveis

- `npm run dev` - Inicia o servidor em modo desenvolvimento
- `npm run build` - Compila o TypeScript para JavaScript
- `npm start` - Inicia o servidor em modo produção
- `npm run lint` - Executa o linter (Biome)
- `npm run format` - Formata o código (Biome)
- `npm run db:migrate` - Executa migrações do banco
- `npm run db:push` - Aplica mudanças no schema
- `npm run db:studio` - Abre Drizzle Studio

## 📝 Code Quality

Este projeto utiliza [Biome](https://biomejs.dev/) para garantir qualidade e consistência do código:

- **Linting** - Identifica problemas no código
- **Formatting** - Formata o código automaticamente
- **Type checking** - Verificação de tipos do TypeScript

## 🚀 Deploy

A API pode ser deployada em plataformas como:

- [Railway](https://railway.app/)
- [Render](https://render.com/)
- [Fly.io](https://fly.io/)
- [AWS](https://aws.amazon.com/)
- [Google Cloud](https://cloud.google.com/)

Certifique-se de configurar as variáveis de ambiente e o banco de dados na plataforma escolhida.

## 🤝 Contribuindo

Contribuições são sempre bem-vindas! Sinta-se à vontade para:

1. Fazer um Fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abrir um Pull Request

## 📚 Sobre o NLW

Este projeto foi desenvolvido durante o **Next Level Week (NLW)** da [Rocketseat](https://www.rocketseat.com.br/), um evento intensivo de programação que ensina tecnologias modernas através da construção de projetos reais.

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 👤 Autor

**Gabriel L. Queiroz Vieira**

- GitHub: [@Gabriellqv](https://github.com/Gabriellqv)

## 🙏 Agradecimentos

- [Rocketseat](https://www.rocketseat.com.br/) pelo evento NLW
- Comunidade TypeScript
- Comunidade Node.js
- Todos os mantenedores das bibliotecas utilizadas

---
