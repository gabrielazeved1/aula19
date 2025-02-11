# API FastAPI com SQLAlchemy

## Descrição

Este projeto é uma API desenvolvida utilizando **FastAPI** e **SQLAlchemy** para gerenciar um banco de dados SQLite. A API permite realizar operações CRUD (Criar, Ler, Atualizar, Deletar) em itens.

## Funcionalidades

- **Criar um item**: Permite criar um novo item no banco de dados.
- **Listar itens**: Recupera uma lista de itens com paginação.
- **Obter item por ID**: Recupera um item específico pelo ID.
- **Atualizar item**: Atualiza os dados de um item existente.
- **Deletar item**: Exclui um item do banco de dados.

## Tecnologias Utilizadas

- **FastAPI**: Framework moderno e rápido para a construção de APIs.
- **SQLAlchemy**: ORM para interagir com o banco de dados.
- **SQLite**: Banco de dados relacional utilizado para persistência de dados.

## Pré-requisitos

- Python 3.12 ou superior.

## Instalação

### Usando Poetry

1. Instale as dependências:  
   poetry install

2. Ative o ambiente virtual do Poetry:  
   poetry shell

3. Para rodar a aplicação, execute:  
   uvicorn main:app --reload

A API estará disponível em `http://127.0.0.1:8000`.

## Endpoints

### GET `/`
Retorna uma resposta simples para testar a API.

### POST `/items/`
Cria um novo item.

- **Body**:
  {
    "name": "Nome do Item",
    "price": 10.99,
    "is_offer": true
  }

- **Resposta**:
  {
    "id": 1,
    "name": "Nome do Item",
    "price": 10.99,
    "is_offer": true
  }

### GET `/items/`
Lista os itens com paginação.

- **Parâmetros**:
  - `skip`: Número de itens a serem pulados (padrão: 0).
  - `limit`: Número máximo de itens a serem retornados (padrão: 10).

### GET `/items/{item_id}`
Retorna um item específico pelo ID.

### PUT `/items/{item_id}`
Atualiza os dados de um item.

- **Body**:
  {
    "name": "Novo Nome do Item",
    "price": 15.99,
    "is_offer": false
  }

### DELETE `/items/{item_id}`
Deleta um item pelo ID.

## Autor

Gabriel Azevedo  
Email: g.azevedo0121@gmail.com