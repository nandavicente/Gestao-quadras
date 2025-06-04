#  Sistema de Agendamento de Quadras com IA e WhatsApp

Aplicação web completa para gestão de quadras de areia (Beach Tennis, Futevôlei, Vôlei), com suporte a agendamentos de aulas e aluguéis, atendimento automático via WhatsApp Business API e integração com IA (GPT-4) para interpretação e resposta de mensagens.

---

##  Funcionalidades Principais

### Core
- Cadastro e gestão de **quadras** (3 quadras de areia)
- Escolha de **modalidade** (Beach Tennis, Futevôlei, Vôlei)
- **Agendamento** de aulas ou aluguéis
- Gestão de **professores** e seus horários
- Visualização da **agenda por quadra e por dia**

###  Integração com WhatsApp Business API
- Recebimento de mensagens via **webhook**
- Resposta automática por IA e tentativa de **agendamento direto**
- **Envio automático** de mensagens: confirmação, lembrete e cancelamento

###  IA para Atendimento Inteligente
- Utilização do **GPT-4 (OpenAI API)** para interpretar comandos como:
  > “Quero alugar uma quadra pra beach tennis amanhã às 19h”

---

## 🧱 Tecnologias Utilizadas

| Camada      | Tecnologia                         |
|-------------|------------------------------------|
| Backend     | Python + FastAPI                   |
| Frontend    | React + TailwindCSS + shadcn/ui    |
| Banco de Dados | PostgreSQL (ou SQLite para testes) |
| IA          | OpenAI API (GPT-4)                 |
| Integração  | Meta WhatsApp Business API         |
| Deploy      | Railway (ou Render)                |

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

##  Executando Localmente

### Pré-requisitos
- Python 3.10+
- Node.js 18+
- PostgreSQL (ou SQLite para testes)
- Conta na [OpenAI](https://platform.openai.com/) e [Meta for Developers](https://developers.facebook.com/)

### Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
