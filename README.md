#  Sistema de Agendamento de Quadras com IA e WhatsApp

Aplicação web completa para gestão de quadras de areia (Beach Tennis, Futevôlei, Vôlei), com suporte a agendamentos de aulas e aluguéis, atendimento automático via WhatsApp Business API.
---

##  Funcionalidades Principais

### Core
- Cadastro e gestão de **quadras** (3 quadras de areia)
- Escolha de **modalidade** (Beach Tennis, Futevôlei, Peteca, Vôlei)
- **Agendamento** de aulas ou aluguéis
- Gestão de **professores** e seus horários
- Visualização da **agenda por quadra e por dia**

###  Integração com WhatsApp Business API
- Recebimento de mensagens via **webhook**
- **Envio automático** de mensagens: confirmação, lembrete e cancelamento

---

## 📊 Diagrama de Fluxo do Sistema

Abaixo está o fluxo geral de funcionamento do sistema:

![Fluxo do Sistema](docs/fluxo_gestao_quadras.png)

---

## 🧱 Tecnologias Utilizadas

| Camada        | Tecnologia                          |
|---------------|-------------------------------------|
| Frontend      | React + TailwindCSS (tema escuro)   |
| Backend       | FastAPI (Python 3.11+)              |
| Banco de Dados| PostgreSQL                          |
| Integração    | API Oficial do WhatsApp (Meta)      |
| Infraestrutura| Vite (desenvolvimento local)        |

---

##  Design do Painel Web

### Tela Principal: Agenda por Quadra
- Estilo **calendário** com horários
- Filtros por **quadra**, **dia** e **modalidade**
- Cores diferenciadas: aula / aluguel / indisponível

### Tela de Novo Agendamento
- Dropdowns para:
  - Modalidade
  - Tipo (aula ou aluguel)
  - Quadra
  - Professor (se aula)
- Campos para:
  - Data e hora
  - Nome do cliente

### Tela de Mensagens
- Histórico de interações com usuários
- Caixa de entrada com filtro por número
- Envio manual de mensagens (opcional)

---
## ⚙️ Como Executar o Projeto Localmente

1. **Clone o repositório**
   ```bash
   git clone https://github.com/seu-usuario/seu-repo.git
   cd seu-repo
   ```

2. **Instale as dependências do frontend**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

3. **Execute o backend com FastAPI**
   ```bash
   cd backend
   uvicorn main:app --reload
   ```

4. Acesse em seu navegador:
   - Frontend: http://localhost:5173  
   - Backend (API): http://localhost:8000/docs  

---


## 👤 Acesso

O sistema será utilizado apenas por **um usuário administrador** com login único.
