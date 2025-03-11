### API de Gerenciamento de Jogadores ⚽

![FastAPI Jogadores](https://github.com/daaniMatrix2/FastApi_jogadores/raw/main/fastapi.jpg)

Este projeto é uma API desenvolvida com FastAPI para cadastrar, atualizar, excluir e buscar jogadores. 
Ele suporta tanto Path Parameters quanto Query Parameters.

🚀 Como Executar o Projeto

1. Clone o repositório
  git clone https://github.com/daaniMatrix2/FastApi_jogadores

2. Crie um ambiente virtual e ative-o
  python -m venv venv
  source venv/bin/activate  # Para Linux/macOS
  venv\Scripts\activate  # Para Windows

3. Instale as dependências
  pip install fastapi uvicorn pydantic

4. Execute o servidor
  uvicorn api:app --reload --port 8001

5. Acesse a documentação automática da API:
  http://127.0.0.1:8001/docs (Swagger UI)
  http://127.0.0.1:8001/redoc (ReDoc)


### 📌 Endpoints Disponíveis

🔹 Listar todos os jogadores

GET /

Resposta:

{
  "1": { "nome": "Rony", "idade": 21, "time": "Palmeiras" },
  "2": { "nome": "Harry", "idade": 24, "time": "São Paulo" }
}

🔹 Cadastrar um novo jogador (Path Parameter)

POST /cadastra-jogador/{jogador_id}

Body:

{
  "nome": "Messi",
  "idade": 35,
  "time": "Inter Miami"
}

🔹 Deletar um jogador (Path Parameter)

DELETE /exclusao-jogador/{jogador_id}

### Resposta:

{"Mensagem": "Jogador excluído com sucesso!"}

🔹 Atualizar um jogador (Path Parameter)

PUT /atualiza-jogador/{jogador_id}

Body: (dados opcionais)

{
  "nome": "Cristiano Ronaldo",
  "time": "Al Nassr"
}

🔹 Buscar jogador por ID (Path Parameter)

GET /get-jogador/{id_jogador}

🔹 Buscar jogador por time (Query Parameter)

GET /get-jogador-time?time=Palmeiras

Resposta:

{
  "nome": "Rony",
  "idade": 21,
  "time": "Palmeiras"
}

### 📌 Tecnologias Utilizadas

✅ FastAPI - Framework para APIs rápidas em Python
✅ Uvicorn - Servidor ASGI para rodar a API
✅ Pydantic - Validação de dados

Autor
Daniel do Nascimento! 

