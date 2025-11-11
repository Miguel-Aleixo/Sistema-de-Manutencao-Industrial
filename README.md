# 🏭 Sistema de Manutenção Industrial (Desktop + Web Core)

Aplicação desktop capaz de gerenciar ordens de serviço, máquinas, técnicos e históricos de manutenção industrial.  
A interface é construída em **Angular**, empacotada com **Electron** para execução local, e o backend utiliza **Node.js + Prisma + PostgreSQL**.

Este projeto segue padrões adotados em ambientes industriais e empresas de médio e grande porte, com módulos bem definidos e arquitetura escalável.

---

## 🚀 Tecnologias Utilizadas

| Camada | Tecnologia |
|-------|------------|
| **Frontend (UI)** | Angular + Angular Material |
| **Desktop Runtime** | Electron |
| **Backend (API Local)** | Node.js + Nest.js |
| **ORM / Query Layer** | Prisma ORM |
| **Banco de Dados** | PostgreSQL |
| **Arquitetura** | Camadas separadas para UI, API e Persistência |

---

## 🎯 Objetivo

Fornecer uma solução para gerenciamento de manutenção, permitindo:

- Controle de máquinas e seus dados operacionais.
- Registro de manutenções preventivas e corretivas.
- Criação, atualização e finalização de Ordens de Serviço (OS).
- Acompanhamento de técnicos envolvidos.
- Histórico detalhado de eventos por máquina ou técnico.

---

## 📌 Funcionalidades Planejadas

| Módulo | Funcionalidades |
|-------|----------------|
| Máquinas | Cadastrar, listar, editar, inativar |
| Técnicos | Registrar, categorizar por nível e especialidade |
| Ordens de Serviço (OS) | Criar, atualizar status, vincular máquina e técnico, registrar tempo |
| Histórico | Consultar linha do tempo de manutenções e finalizações |

---

## 📊 Modelagem Inicial (Entidades)

Máquina (id, nome, setor, status, dataCadastro)
Técnico (id, nome, nível, especialidade)
OrdemServico (id, maquinaId, tecnicoId, descricao, status, dataAbertura, dataFechamento)
Historico (id, ordemId, evento, data)

yaml
Copiar código

---

## 🗂 Estrutura do Projeto

/app
/frontend (Angular + Material)
/backend
server.js (ou main.ts se Nest)
/src
/routes
/controllers
/services
/prisma
/electron
main.js
prisma/schema.prisma
package.json

yaml
Copiar código

---

## 🔧 Comandos (quando implementado)

```bash
npm install
npx prisma migrate dev
npm run build:frontend
npm run electron:start
✔️ Status do Projeto
 Planejamento

 Modelagem Prisma

 Backend com PostgreSQL

 Angular + Material

 Integração Electron

 Módulos CRUD

 Build final

📝 Licença
Projeto aberto para estudo e portfólio.
