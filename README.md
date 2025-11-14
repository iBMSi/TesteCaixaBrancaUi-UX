# Análise de Caixa Branca — Verificação de Usuário (Java)

Este repositório contém a análise de **caixa branca** realizada sobre o código Java responsável pela verificação de usuários em um banco de dados MySQL.  
A atividade inclui documentação, grafo de fluxo, complexidade ciclomática, caminhos básicos e tabela de testes.

---

## 1. Código Analisado e Respondido

## O código foi devidamente documentado? 

Não, o programa mostra uma série de linhas de código em Java, porém não está documentado, isto é, alguém sem conhecimento do programa e da linguagem não consegue entender o que o código está fazendo pois não há comentários dizendo o que o código está fazendo em partes. Algumas partes estão comentadas instruindo o que esta acontecendo, porém nem todo código está documentado dificultando o entendimento do código todo

## As variáveis e constantes possuem nomenclatura?

Sim, as variáveis e constantes presentes no código possuem nomenclatura. Em Java ao criar as variáveis é necessário as nomear, sendo assim quando tais variáveis foram declaradas foram atribuídas nomenclaturas.

## Existem legibilidade e organização no código?

Sim o código está organizado 	em bibliotecas, classes variáveis e métodos assim como a linguagem Java necessita, sendo assim ao ter ciência dos comandos utilizados no código é possível analisa-lo de forma legível 

## Todos os NullPointers foram tratados?

Não, há um tratamento em um Try, porém o catch não realiza uma ação de tratamento como impedir ou corrigir, ele apenas informa a “Exception e”

##As conexões utilizadas foram fechadas?

Após feito uma análise do código é possível perceber que as conexões com o banco de dados não foram estabelecidas sendo assim, as conexões não foram fechadas.


## 2. Notação do Grafo de Fluxo

<img width="871" height="881" alt="image" src="https://github.com/user-attachments/assets/e9f2f4ce-cbbb-4faf-99a7-c76a60d2db64" />


---

## 3. Complexidade Ciclomática

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

## 4. Caminhos Básicos

A partir do grafo, foram identificados os caminhos independentes abaixo:

1. **Caminho 1:**  
   `A → B → D → E → G`

2. **Caminho 2:**  
   `A → C → A → B → D → E → F → G`

3. **Caminho 3:**  
   `A → B → D → F → D → E → G`

> Esses caminhos garantem cobertura total dos ciclos do grafo.

---

## 5. Tabela de Teste (Caixa Branca Estática)
<img width="1464" height="791" alt="image" src="https://github.com/user-attachments/assets/b3af31a6-c9a3-46f7-a81e-e3494caea964" />

---

## 6. Código Fonte

<img width="678" height="547" alt="image" src="https://github.com/user-attachments/assets/6d0d1cc1-aeb2-4910-bf93-70d50159913c" />


---

## 7. Estrutura Recomendada do Repositório

