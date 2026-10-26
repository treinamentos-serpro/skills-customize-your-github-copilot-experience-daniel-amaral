# 📘 Assignment: Local Web Server with Python

## 🎯 Objective

Construa um pequeno mural de recados usando `http.server`, `BaseHTTPRequestHandler` e outros módulos da biblioteca padrão. Pratique como requisições GET e POST transportam dados e como um servidor responde a elas, sem instalar dependências externas.

## 📝 Tasks

### 🛠️ Servir uma Página Inicial

#### Descrição
Execute o servidor inicial e complete a rota `GET /` para exibir uma página HTML com o formulário do mural.

#### Requisitos
O programa concluído deve:

- Iniciar um servidor local na porta `8000`
- Responder a `GET /` com uma página HTML e código HTTP `200`
- Exibir um formulário com campos para nome e recado, enviado para `/messages` usando o método `POST`
- Retornar código HTTP `404` para caminhos que não existem

### 🛠️ Receber Recados pelo Formulário

#### Descrição
Implemente a rota `POST /messages`. Leia o corpo da requisição, interprete os campos enviados pelo formulário e guarde cada recado em uma lista na memória.

#### Requisitos
O programa concluído deve:

- Ler o tamanho do corpo usando o cabeçalho `Content-Length`
- Interpretar os campos codificados com `parse_qs`
- Guardar o nome e o recado na lista `MESSAGES`
- Rejeitar campos vazios com uma resposta HTTP apropriada
- Redirecionar o navegador de volta para `/` após receber um recado válido

### 🛠️ Exibir Recados com Segurança

#### Descrição
Atualize a página inicial para mostrar os recados recebidos. Como o conteúdo vem de usuários, escape os valores antes de incluí-los no HTML.

#### Requisitos
O programa concluído deve:

- Mostrar todos os recados armazenados após uma nova requisição `GET /`
- Usar `html.escape` para exibir nomes e recados sem interpretá-los como HTML
- Responder com o tipo de conteúdo `text/html; charset=utf-8`
- Confirmar o fluxo completo: abrir a página, enviar um recado e vê-lo na lista
