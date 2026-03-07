# Testes Automatizados de API - JSONPlaceholder


Este projeto contém a automação de testes para a API pública JSONPlaceholder, desenvolvida como parte de um desafio técnico para QA. A solução utiliza Postman para a criação dos testes e GitHub Actions integrado com Newman para a execução contínua (CI).


# 📌 Sobre a API

A API utilizada neste projeto é a: https://jsonplaceholder.typicode.com.  Ela é uma API pública usada para testes e prototipação de aplicações.

## 📋 Endpoints Testados
O projeto cobre os seguintes cenários:

**POST /albums**

Objetivo: Validar a criação de um novo álbum.

Testes realizados: * Validação do Status Code 201.

Validação do corpo da resposta (se o título enviado é o mesmo retornado).

**GET /comments**

**Objetivo:** Validar a listagem de comentários.

**Testes realizados:**

Validação do Status Code 200.

Confirmação de que a resposta é um Array e contém dados.


## 🛠️ Tecnologias Utilizadas

Postman – criação dos testes de API

Newman – execução das collections via CLI

GitHub Actions – execução automatizada da pipeline

Node.js – ambiente de execução


## ⚙️ Como Rodar os Testes

Localmente (Via Newman)
Se você deseja rodar os testes na sua máquina, instale o Newman e execute o comando abaixo na raiz do projeto:

Bash
# Instalar o newman globalmente
npm install -g newman

# Rodar a collection
newman run "jsonplaceholder_api_tests.postman_collection.json"
Via GitHub Actions (CI)

Este repositório está configurado para rodar os testes automaticamente em cada push ou pull_request na branch main.

Vá até a aba Actions neste repositório.

Selecione o workflow Postman API Tests.

Verifique o histórico de execuções e os detalhes de cada teste.


## 📈 Estrutura do Pipeline
O workflow do GitHub Actions segue este fluxo:

**Checkout:** Baixa o código no runner do GitHub.

**Ambiente:** Configura o Node.js v20.

**Dependências:** Instala o Newman.

Execução: Roda a coleção e gera o relatório no console.



## Autora
Jaqueline Moura
