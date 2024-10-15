---

# 💳 DigitalBank API - Gestão de Cartões e Transações

Bem-vindo à **DigitalBank API**! 🚀 Esta API é uma solução simples e poderosa para gestão de cartões, processamento de transações e consultas financeiras. Ideal para fintechs e bancos, oferecendo funcionalidades essenciais de forma segura e eficaz.

## 📑 Funcionalidades Principais:

### 1. **Gerenciamento de Cartões** 🏦
   - **Criar um novo cartão**: Solicite um novo cartão, seja de crédito ou débito.
   - **Consultar detalhes do cartão**: Veja saldo atual, limite disponível e data de validade.
   - **Bloquear ou desbloquear cartão**: Bloqueie ou desbloqueie o cartão temporariamente.
   - **Cancelar cartão**: Encerre o uso de um cartão.

### 2. **Processamento de Transações** 💸
   - **Autorizar transações**: Valide e processe uma compra ou pagamento.
   - **Estornar transações**: Reversão de compras realizadas.
   - **Consultar histórico de transações**: Acesse todas as compras e estornos realizados.

### 3. **Consultas Financeiras** 📊
   - **Consultar saldo disponível**: Veja o saldo ou limite disponível no cartão.
   - **Consultar faturas**: Acompanhe faturas de cartões de crédito abertas e passadas.
   - **Histórico de pagamentos**: Veja os pagamentos já realizados e pendentes.

---

## 🔄 **Estrutura dos Endpoints:**

### 1. **Gerenciamento de Cartões** 💳
   - **POST** `/cartoes` — Cria um novo cartão.
   - **GET** `/cartoes/{id}` — Consulta detalhes de um cartão específico.
   - **PATCH** `/cartoes/{id}/bloquear` — Bloqueia um cartão.
   - **PATCH** `/cartoes/{id}/desbloquear` — Desbloqueia um cartão.
   - **DELETE** `/cartoes/{id}` — Cancela um cartão.

### 2. **Processamento de Transações** 💰
   - **POST** `/transacoes` — Autoriza uma nova transação.
   - **POST** `/transacoes/{id}/estorno` — Estorna uma transação específica.
   - **GET** `/transacoes/{id}` — Consulta detalhes de uma transação.
   - **GET** `/cartoes/{id}/transacoes` — Lista todas as transações de um cartão.

### 3. **Consultas Financeiras** 💼
   - **GET** `/cartoes/{id}/saldo` — Consulta saldo ou limite disponível.
   - **GET** `/cartoes/{id}/faturas` — Consulta faturas de um cartão de crédito.
   - **GET** `/cartoes/{id}/pagamentos` — Lista os pagamentos realizados e pendentes.

---

## 🌟 Exemplo de Uso:

### **1. Criar um Cartão:**
   - Solicite a criação de um novo cartão com o endpoint `POST /cartoes` e os dados a seguir:
   
   ```json
   {
     "tipo": "crédito",
     "nome_cliente": "João Silva",
     "limite": 5000.00
   }
   ```

### **2. Autorizar uma Transação:**
   - Realize uma compra com o endpoint `POST /transacoes`:
   
   ```json
   {
     "id_cartao": 1,
     "valor": 150.75,
     "descricao": "Compra em Supermercado",
     "data": "2024-10-15"
   }
   ```

### **3. Consultar Saldo:**
   - Veja o saldo disponível com `GET /cartoes/{id}/saldo`:
   
   ```json
   {
     "id_cartao": 1,
     "saldo_disponivel": 3500.00,
     "limite_total": 5000.00
   }
   ```

---

## ⚙️ **Tecnologias Utilizadas**:

   - **Backend**: Java Quarkus 🧑‍💻
   - **Banco de Dados**: MySQL 🗄️
   - **Autenticação**: OAuth2 ou JWT 🔒

---

## 📌 Como Rodar o Projeto:

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/digitalbank-api.git
   ```

2. Instale as dependências:
   ```bash
   ./mvnw clean install
   ```

3. Rode a aplicação:
   ```bash
   ./mvnw quarkus:dev
   ```

---

## 🤝 Contribuições
Sinta-se à vontade para contribuir com novas funcionalidades ou melhorias! Abra um PR e vamos juntos melhorar a DigitalBank API! 😄

---
