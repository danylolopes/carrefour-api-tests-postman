# Testes de API – Postman (ServeRest)

Projeto de automação de testes de API desenvolvido em **Postman**, utilizando a API pública **ServeRest**, criado para fins de **avaliação técnica** e **demonstração de boas práticas em testes de API**.

---

## 🎯 Objetivo do Projeto

Validar endpoints REST de **Usuários** e **Autenticação**, garantindo:

- Funcionamento correto dos fluxos principais (POS)
- Tratamento adequado de erros e validações (NEG)
- Validação de payloads
- Validação de códigos de status HTTP
- Validação de mensagens de resposta
- Execução automatizada via Collection Runner

---

## 🛠️ O que é necessário para executar o projeto

Antes de executar os testes, você **PRECISA** ter:

### 🔹 Ferramentas
- **Postman** instalado (desktop ou web)  
  👉 https://www.postman.com/downloads/

### 🔹 Acesso
- Conexão com a internet
- API pública **ServeRest** disponível  
  👉 https://serverest.dev

### 🔹 Arquivos do projeto
- Collection Postman (`.postman_collection.json`)
- Environment Postman (`.postman_environment.json`)

Esses arquivos estão localizados na pasta `/postman` do repositório.


---

## ▶️ Como Executar os Testes (PASSO A PASSO)

### 1️⃣ Importar os arquivos no Postman

1. Abra o **Postman**
2. Clique em **Import**
3. Importe os dois arquivos abaixo:
   - `Carrefour_API_Tests_ServeRest.postman_collection.json`
   - `serverest.postman_environment.json`
4. No canto superior direito, selecione o environment **serverest**

---

### 2️⃣ Conferir o Environment (SEGURANÇA)

O environment já vem configurado.

⚠️ **Antes de executar, confirme:**

- O campo `TOKEN` está **vazio**
- `email` e `password` são apenas valores de exemplo
- Nenhum dado sensível é versionado

Exemplo esperado:

base_url = https://serverest.dev
email = test@example.com
password = 123456
TOKEN =


👉 O token JWT é gerado **automaticamente** durante a execução do login.

---

### 3️⃣ Executar os testes manualmente (opcional)

Você pode executar qualquer request individualmente:

1. Abra a collection **Carrefour API Tests – ServeRest**
2. Selecione um request
3. Clique em **Send**
4. Verifique:
   - Status Code
   - Body da resposta
   - Aba **Test Results**

---

### 4️⃣ Executar todos os testes automaticamente (RECOMENDADO)

1. Clique com o botão direito na collection  
   **Carrefour API Tests – ServeRest**
2. Selecione **Run collection**
3. Configure:
   - Environment: `serverest`
   - Iterations: `1`
4. Clique em **Run**

✔️ O Collection Runner executará automaticamente:
- Cenários positivos
- Cenários negativos
- Validações de status HTTP
- Validações de payload
- Fluxo completo CRUD de usuários

---

## 🧪 Escopo de Testes

### ✔️ Usuários – Cenários Positivos
- Criar usuário
- Login
- Listar usuários
- Buscar usuário por ID
- Atualizar usuário
- Excluir usuário
- Validar comportamento após exclusão

### ❌ Usuários – Cenários Negativos
- Criar usuário com e-mail inválido
- Criar usuário com campo obrigatório ausente
- Criar usuário com e-mail duplicado
- Buscar usuário com ID inválido
- Buscar usuário inexistente
- Atualizar usuário com payload inválido
- Excluir usuário inexistente

### 🔐 Autenticação – Cenários Negativos
- Login com senha inválida
- Login com usuário inexistente

---

## 📌 Boas Práticas Aplicadas

- Separação clara entre cenários POS e NEG
- Uso de variáveis de environment
- Testes independentes e reexecutáveis
- Validação de status HTTP e mensagens
- Organização no padrão corporativo
- Projeto seguro (sem tokens ou dados sensíveis versionados)

---

## 📄 Observações Finais

Este projeto foi desenvolvido com foco em **qualidade de software**, **clareza**, **organização** e **aderência a padrões técnicos**, sendo adequado para avaliação em **processo seletivo**.

---


## 📁 Estrutura do Projeto

```text
postman/
├── Carrefour_API_Tests_ServeRest.postman_collection.json
├── serverest.postman_environment.json

README.md



