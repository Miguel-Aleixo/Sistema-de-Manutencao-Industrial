# 🏭 Sistema de Manutenção Industrial (Electron + Angular + Nest + PostgreSQL)

Este projeto é uma aplicação **Desktop** focada na gestão de manutenção industrial, permitindo controlar máquinas, técnicos e ordens de serviço, além de manter um histórico de intervenções. A interface é construída em **Angular** e empacotada com o **Electron** para execução local, enquanto a lógica de negócio e persistência são tratadas por um backend interno feito em **Nest.js**, utilizando **PostgreSQL** com **Prisma ORM**.

---

## 🎯 Objetivo

O sistema auxilia equipes de manutenção a registrar e acompanhar manutenções preventivas e corretivas, gerenciar ordens de serviço e manter rastreabilidade histórica.

---

## 🚀 Tecnologias Utilizadas

| Camada | Tecnologia |
|-------|------------|
| **Frontend (UI)** | Angular + Angular Material |
| **Backend (API Interna)** | Nest.js (Node.js) |
| **ORM & Mapeamento** | Prisma ORM |
| **Banco de Dados** | PostgreSQL |
| **Aplicação Desktop** | Electron |
| **Linguagem Principal** | TypeScript |

---

## 📦 Funcionalidades

### Máquinas
- Cadastrar e editar máquinas
- Registrar setor e status
- Ativar / Inativar equipamentos

### Técnicos
- Cadastro com nível (Júnior / Pleno / Sênior)
- Especialização por área de trabalho

### Ordens de Serviço (OS)
- Criar OS vinculada a técnico e máquina
- Atualizar status (`ABERTA`, `EM_ANDAMENTO`, `FINALIZADA`)
- Registrar data de abertura e fechamento

### Histórico
- Entrada automática a cada mudança significativa
- Visualização por máquina ou técnico

---

## 🗂 Estrutura do Projeto (Prevista)

/app
/frontend (Angular)
/src
/app
/modules
/shared
main.ts
/backend (Nest.js)
/src
/modules
maquinas
tecnicos
ordens
historico
/common
main.ts
/electron
main.js
prisma/schema.prisma
package.json

yaml
Copiar código

---

## 🗃 Modelagem de Dados

Máquina(id, nome, setor, status, dataCadastro)
Técnico(id, nome, nível, especialidade)
OrdemServico(id, maquinaId, tecnicoId, descricao, status, dataAbertura, dataFechamento)
Histórico(id, ordemId, evento, data)

yaml
Copiar código

---

## 💻 Rodando o projeto (quando estiver implementado)

```bash
# instalar dependências
npm install

# configurar migrations do banco
npx prisma migrate dev

# iniciar backend
npm run start:backend

# iniciar frontend
npm run start:frontend

# iniciar app desktop
npm run electron:start
📸 Demonstração (adicionar depois)
Prints ou vídeo da aplicação funcionando
 ```

## 📝 Licença
Projeto livre para estudos e apresentação em portfólio.
