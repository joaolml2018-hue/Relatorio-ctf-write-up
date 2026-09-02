Relatório CTF
# Desafio CTF: Cookies

**Nome:** João Lucas Marques de Lima

---

## 📜 Descrição do Desafio

O desafio explorava o uso e a manipulação de cookies pelo navegador. A proposta era analisar a forma como a aplicação web armazenava e utilizava essas informações no lado do cliente para controlar o acesso ou o comportamento da página.

---

## 🔍 Análise e Resolução

### 1. Inspeção da Aplicação
Ao acessar o desafio, foi feita a inspeção do ambiente da aplicação web utilizando as ferramentas de desenvolvedor do navegador (**Developer Tools** / *Inspecionar Elemento*).

### 2. Análise dos Cookies
Navegando até a aba **Application** (ou *Armazenamento*) e selecionando a seção **Cookies**, identificou-se a lista de dados armazenados localmente para a origem do site. 

Entre as entradas disponíveis, localizou-se um cookie cujo valor definido era `"nao"`.

### 3. Modificação do Parâmetro
Como o controle de acesso ou estado estava condicionado a esse valor no lado do cliente:
1. O valor do cookie foi alterado diretamente na interface do navegador de `"nao"` para `"sim"`.
2. A página foi recarregada (refresh) para enviar o novo valor no cabeçalho HTTP da requisição.

Ao reprocessar a requisição com o parâmetro alterado, a aplicação modificou seu comportamento e exibiu a flag na tela.

---

## 🛠️ Resumo do Processo

`Inspecionar elemento` ➔ `Application` ➔ `Cookies` ➔ `Alterar "nao" para "sim"` ➔ `Recarregar a página` ➔ `FLAG`

---

## 🚩 Flag

```text
FLAG{C00K1E_M0NST3R_MUNCH}