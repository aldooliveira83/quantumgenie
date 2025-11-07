# 🌟 QuantumGenie

> Aplicativo de bem-estar impulsionado por IA com rituais personalizados

## ✨ Features

- 🤖 IA com GPT-4 para recomendações personalizadas
- 📱 App mobile React Native com Expo
- 🔐 Autenticação JWT segura
- 💾 PostgreSQL + Redis
- 📊 Analytics e tracking de progresso
- 🔔 Sistema de notificações
- 🎯 24 endpoints REST API
- 📚 Documentação Swagger automática

## 🚀 Quick Start

### Backend (API)
```bash
cd backend
npm install
npx prisma migrate dev
npm run seed
npm run start:dev
```

API disponível em: http://localhost:3000
Swagger UI: http://localhost:3000/api

### Mobile (App)
```bash
cd mobile
npm install
npm start
```

Escaneie o QR code com Expo Go no celular.

## 🛠️ Tech Stack

**Backend:**
- NestJS (Framework Node.js)
- Prisma ORM
- PostgreSQL (Database)
- Redis (Cache)
- OpenAI GPT-4 (IA)
- JWT (Auth)
- Bull (Job Queue)
- Swagger (Docs)

**Mobile:**
- React Native
- Expo
- TypeScript
- React Navigation
- Axios

## 📁 Estrutura do Projeto
```
quantumgenie/
├── backend/              # API NestJS
│   ├── src/
│   │   ├── modules/     # Módulos da aplicação
│   │   │   ├── auth/    # Autenticação
│   │   │   ├── user/    # Usuários
│   │   │   ├── ritual/  # Rituais
│   │   │   ├── progress/# Progresso
│   │   │   ├── ai/      # IA GPT-4
│   │   │   └── ...
│   │   └── config/      # Configurações
│   ├── prisma/          # Schema do banco
│   └── package.json
│
├── mobile/              # App React Native
│   ├── src/
│   │   ├── screens/     # Telas
│   │   ├── components/  # Componentes
│   │   ├── services/    # APIs
│   │   └── contexts/    # Estado global
│   └── package.json
│
└── render.yaml          # Config deploy
```

## 🔧 Variáveis de Ambiente

Copie `.env.example` para `.env` e configure:
```env
DATABASE_URL="postgresql://..."
REDIS_URL="redis://..."
JWT_SECRET="seu-secret-aqui"
OPENAI_API_KEY="sk-proj-..."
NODE_ENV="development"
PORT=3000
```

## 📚 API Endpoints

### Auth
- `POST /auth/signup` - Criar conta
- `POST /auth/login` - Login
- `POST /auth/refresh` - Refresh token

### Rituais
- `GET /ritual/catalog` - Listar rituais
- `GET /ritual/:id` - Detalhes do ritual
- `POST /ritual/:id/start` - Iniciar ritual
- `GET /ritual/active` - Rituais ativos

### IA
- `POST /ai/recommendation` - Recomendação personalizada
- `POST /ai/chat` - Conversar com IA

### Progresso
- `GET /progress/stats` - Estatísticas
- `POST /progress/complete` - Marcar como completo
- `GET /progress/history` - Histórico

## 🚀 Deploy

### Render.com (Recomendado)

1. Conecte seu repositório GitHub ao Render
2. Use o arquivo `render.yaml` (deploy automático)
3. Configure a variável `OPENAI_API_KEY`
4. Deploy! 🎉

### Railway.app (Alternativa)

1. Conecte ao Railway
2. Adicione PostgreSQL e Redis
3. Configure variáveis de ambiente
4. Deploy automático via Git

## 📖 Documentação

- [Backend Completo](./BACKEND-COMPLETO.md)
- [Deploy Railway](./DEPLOY-RAILWAY.txt)
- [Deploy Render](./DEPLOY-COM-OPENAI.txt)

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## 📄 Licença

MIT License - sinta-se livre para usar este projeto!

## 👨‍💻 Autor

**Aldo Oliveira** - [GitHub](https://github.com/aldoolivera83)

---

⚛️ **Mudanças quânticas começam com micro-ações** 💜
