# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Crie uma API REST em Python usando FastAPI. Pratique a criação de endpoints HTTP, a validação de dados com Pydantic e o uso de códigos de status para representar resultados e erros.

## 📝 Tasks

### 🛠️ Create the FastAPI App and List Books

#### Descrição
Configure o ambiente, execute o aplicativo inicial e crie um endpoint para listar os livros do catálogo.

Instale as dependências e inicie o servidor de desenvolvimento:

```bash
python -m pip install "fastapi[standard]"
fastapi dev starter-code.py
```

#### Requisitos
O programa concluído deve:

- Criar um endpoint `GET /books` que retorne a lista de livros
- Retornar cada livro com `id`, `title` e `author`
- Permitir que a documentação interativa da API seja acessada em `/docs`

### 🛠️ Retrieve and Create Books

#### Descrição
Adicione endpoints para buscar um livro pelo identificador e cadastrar novos livros no catálogo.

#### Requisitos
O programa concluído deve:

- Criar `GET /books/{book_id}` para retornar o livro solicitado
- Retornar o código HTTP `404` quando o identificador não corresponder a um livro
- Criar `POST /books` para receber e validar `title` e `author` usando um modelo Pydantic
- Atribuir um identificador ao novo livro, armazená-lo e retorná-lo na resposta

### 🛠️ Delete Books and Handle Errors

#### Descrição
Implemente a remoção de livros e use respostas HTTP apropriadas quando uma operação não puder ser concluída.

#### Requisitos
O programa concluído deve:

- Criar `DELETE /books/{book_id}` para remover um livro existente
- Retornar o código HTTP `404` ao tentar remover um livro inexistente
- Confirmar a remoção com uma resposta HTTP apropriada
- Permitir testar as operações de listar, buscar, criar e remover em `/docs`