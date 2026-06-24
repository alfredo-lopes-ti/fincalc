# FinCalc 🧮

> Calculadora financeira full-stack com autenticação, histórico de cálculos e dashboard analítico.

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Node](https://img.shields.io/badge/Node.js-20+-339933?logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-18+-20232A?logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15+-316192?logo=postgresql&logoColor=white)

---

## Sobre o projeto

O **FinCalc** é uma aplicação web completa para cálculos financeiros pessoais e empresariais. O usuário se autentica, realiza cálculos (juros simples, compostos, financiamentos, ROI, etc.), e pode consultar o histórico com filtros e exportação.

O projeto foi desenvolvido como portfólio técnico demonstrando arquitetura full-stack production-ready.

---

## Funcionalidades

- [x] Autenticação com JWT (login, registro, refresh token)
- [x] Cálculos: juros simples e compostos, amortização, ROI, margem
- [x] Histórico persistido por usuário no banco de dados
- [ ] Dashboard com gráficos (Recharts)
- [ ] Exportação de histórico em CSV/PDF
- [ ] Deploy automatizado (Railway + Vercel)

---

## Stack Técnica

| Camada     | Tecnologia                          |
|------------|-------------------------------------|
| Backend    | Node.js · TypeScript · Express      |
| Banco      | PostgreSQL · Prisma ORM             |
| Auth       | JWT · bcrypt                        |
| Frontend   | React · Vite · TypeScript           |
| Deploy     | Railway (API) · Vercel (Frontend)   |

---

## Estrutura do Projeto

```
fincalc/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── routes/
│   │   ├── services/
│   │   └── server.ts
│   ├── prisma/
│   │   └── schema.prisma
│   └── package.json
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── services/
    │   └── main.tsx
    └── package.json
```

---

## Como executar localmente

### Pré-requisitos
- Node.js 20+
- PostgreSQL 15+

### Backend

```bash
cd backend
cp .env.example .env
# Configure DATABASE_URL e JWT_SECRET no .env
npm install
npx prisma migrate dev
npm run dev
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

A API rodará em `http://localhost:3333` e o frontend em `http://localhost:5173`.

---

## Endpoints da API

| Método | Rota                   | Descrição                  |
|--------|------------------------|----------------------------|
| POST   | /auth/register         | Cadastro de usuário        |
| POST   | /auth/login            | Login e geração de token   |
| GET    | /calculations          | Histórico do usuário       |
| POST   | /calculations          | Novo cálculo               |
| DELETE | /calculations/:id      | Remover cálculo            |

---

## Autor

**Alfredo Lopes** — [@alfredo-lopes-ti](https://github.com/alfredo-lopes-ti)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-alfredolopes--ti-0077B5?logo=linkedin)](https://linkedin.com/in/alfredolopes-ti)
