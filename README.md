# Análise de Caixa Branca — Verificação de Usuário (Java)

Este repositório contém a análise de **caixa branca** realizada sobre o código Java responsável pela verificação de usuários em um banco de dados MySQL.  
A atividade inclui documentação, grafo de fluxo, complexidade ciclomática, caminhos básicos e tabela de testes.

---

## 📌 1. Descrição do Código Analisado

O código analisado pertence à classe `User`, no pacote `login`.  
Ele possui duas funções principais:

- **conectarBD()** → tenta abrir uma conexão com o banco MySQL  
- **verificarUsuario(login, senha)** → monta SQL, cria Statement, executa query e retorna se o usuário existe  

Principais problemas levantados na análise:

- Falta de documentação adequada  
- Conexão com BD não foi estabelecida corretamente (driver incorreto)  
- Conexões não são fechadas  
- NullPointers não tratados  
- SQL vulnerável a injeção  
- Catches vazios  
- Arquitetura incorreta (acesso ao BD deveria estar em um DAO)

---

## 📌 2. Notação do Grafo de Fluxo

A notação do grafo utilizada para cálculo da complexidade ciclomática foi definida com os seguintes nós:

- **A** – Entrada do método verificarUsuario  
- **B** – Chamada conectarBD()  
- **C** – Montagem da SQL  
- **D** – createStatement()  
- **F** – executeQuery() / ResultSet  
- **E** – Catch vazio  
- **G** – Retorno final  

> **A imagem do grafo você adiciona no repositório**, conforme instruído.

---

## 📌 3. Complexidade Ciclomática

Para o grafo fornecido, identificou-se:

- **Nós (N)** = 7  
- **Arestas (E)** = 8  
- **Componentes conectados (P)** = 1  

### 🔢 Cálculo:

\[
M = E - N + 2P
\]

\[
M = 8 - 7 + 2*1 = 3
\]

### ✅ **Complexidade ciclomática = 3**

Isto significa que existem **3 caminhos minimamente independentes** dentro do fluxo do código.

---

## 📌 4. Caminhos Básicos

A partir do grafo, foram identificados os caminhos independentes abaixo:

1. **Caminho 1:**  
   `A → B → D → E → G`

2. **Caminho 2:**  
   `A → C → A → B → D → E → F → G`

3. **Caminho 3:**  
   `A → B → D → F → D → E → G`

> Esses caminhos garantem cobertura total dos ciclos do grafo.

---

## 📌 5. Tabela de Teste (Caixa Branca Estática)

A tabela de teste foi preenchida conforme solicitado na atividade, contendo:

- Validação de documentação  
- Nomenclatura  
- NullPointers  
- Loops  
- Arquitetura  
- Tratamento de exceções  
- Conexões abertas e não fechadas  

> **A imagem da tabela será adicionada por você aqui no repositório.**

---

## 📌 6. Código Fonte

O código original analisado também deve ser incluído no repositório, com comentários e correções realizadas conforme solicitado.

---

## 📌 7. Estrutura Recomendada do Repositório

