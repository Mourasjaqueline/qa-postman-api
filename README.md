# 🔗 Automação de Testes de API com Postman

## 📌 Sobre o Projeto



Este repositório contém a automação de testes para a API pública **JSONPlaceholder**.

Os testes foram implementados utilizando **Postman** e são executados automaticamente através do **Newman**, integrado ao **GitHub Actions** para execução contínua.

URL: https://jsonplaceholder.typicode.com/
---

## 🧪 Estratégia de Testes

Os testes foram desenvolvidos para validar o comportamento dos principais endpoints da API.

Os cenários implementados incluem:

* Validação de criação de recursos
* Validação de listagem de dados
* Validação de status code das requisições
* Verificação da integridade do corpo da resposta

---

## 📋 Endpoints Testados

### POST /albums

Objetivo: validar a criação de um novo álbum.

Validações realizadas:

* Status Code **201**
* Verificação do campo **title** retornado na resposta

---

### GET /comments

Objetivo: validar a listagem de comentários.

Validações realizadas:

* Status Code **200**
* Verificação de que a resposta contém um **array de dados**

---

## 🛠️ Tecnologias Utilizadas

* **Postman**
* **Newman**
* **Node.js**
* **GitHub Actions (CI/CD)**

---

## 📂 Estrutura do Projeto

```
postman
│
└── jsonplaceholder_api_tests.postman_collection.json

.github
└── workflows
```

---

## ⚙️ Pré-requisitos

Para executar os testes localmente é necessário possuir instalado:

* Node.js
* Newman

---

## 🚀 Como Executar o Projeto

Instalar o Newman:

```bash
npm install -g newman
```

Executar a collection:

```bash
newman run jsonplaceholder_api_tests.postman_collection.json
```

---

## 🔄 Integração Contínua (CI)

Este repositório possui pipeline configurada no **GitHub Actions**.

A cada **push** ou **pull request**, a pipeline executa automaticamente:

1. Checkout do repositório
2. Configuração do ambiente Node.js
3. Instalação do Newman
4. Execução da collection Postman

---

## 📊 Evidências da Execução

Durante a execução da pipeline são gerados:

* Resultados da execução dos testes
* Status das requisições
* Tempo de resposta das APIs
* Quantidade de testes executados, aprovados e falhos

Os resultados podem ser visualizados diretamente na aba **Actions** do repositório.

---

## 👩‍💻 Autora

**Jaqueline Moura**
