# 🧾 Debita ai

> Controle coletivo de despesas domésticas para grupos como famílias, casais e repúblicas.

---

## 📌 Visão Geral

**Conta Junto** é uma aplicação web que permite a organização e divisão justa de contas entre pessoas que vivem na mesma casa. O sistema ajuda a registrar despesas, dividir valores (de forma igual ou personalizada), acompanhar pagamentos e manter a transparência nos gastos do grupo.

Ideal para famílias, casais ou repúblicas que desejam evitar confusões com as finanças do lar.

---

## 🎯 Objetivo

Facilitar a organização de contas compartilhadas, promovendo clareza e colaboração entre os membros de um grupo doméstico. O sistema ajuda a evitar atrasos, esquecimentos ou desigualdade no pagamento de despesas coletivas.

---

## 👤 Personas

- **Carla (32 anos)** – Casada, usa planilhas para controlar contas, mas quer algo mais intuitivo.
- **Pedro (24 anos)** – Mora com amigos em república, precisa dividir tudo com clareza.
- **Dona Helena (59 anos)** – Mora com os filhos e quer uma forma simples de saber se está tudo certo.

---

## 🧱 Stack Tecnológica

| Camada       | Tecnologia               |
|--------------|---------------------------|
| Frontend     | React (Vite) + TailwindCSS |
| Backend      | Node.js + Express          |
| Autenticação | JWT (JSON Web Token)       |
| Banco de dados | PostgreSQL              |
| Deploy       | Hostinger (VPS ou FTP)     |

---

## 🧩 Estrutura de Banco (MVP)

### users
- `id`, `name`, `email`, `password_hash`

### groups
- `id`, `name`

### group_users
- `id`, `user_id`, `group_id`, `role`

### expenses
- `id`, `title`, `group_id`, `total_value`, `due_date`

### expense_shares
- `id`, `expense_id`, `user_id`, `value`, `paid_status`

---

## ✅ Funcionalidades do MVP

- Registro e login com JWT
- Criação de grupos e entrada via link ou ID
- Cadastro de despesas com divisão proporcional ou igual
- Listagem de despesas com status de pagamento por membro
- Resumo mensal de gastos e pendências
- Proteção de rotas com autenticação
- Interface clara e acessível

---

## 🛠️ Como Rodar Localmente

### 1. Backend (Node.js + PostgreSQL)

```
cd backend
npm install
cp .env.example .env
# Configure suas variáveis de ambiente

npm run migrate
npm run dev
```
### 2. Frontend (React)

```
cd frontend
npm install
npm run dev
# Certifique-se de que o backend está rodando e que as URLs estão corretas no .env.
```

---

## 🚀 Funcionalidades Futuras (Pós-MVP)

- Dashboard com gráficos de gastos por mês e membro
- Upload de comprovantes de pagamento
- Exportação de despesas (PDF ou Excel)
- Notificações por email para vencimentos
- Cálculo automático de saldo entre membros
- Modo escuro
- Chat entre membros
- Versão mobile com React Native

---

## 🔗 Recursos
- 🗂️ Trello do Projeto
- 🎨 Wireframes no Figma
- 💬 Documentação técnica

---

## 🧑‍💻 Autor
Conta Junto está sendo desenvolvido por Kauã Vicente Domingos.
Este projeto é um estudo prático completo com foco em impacto social e organização de código real para portfólio profissional.
