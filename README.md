# ⚽ Automação Copa do Mundo → Google Calendar

Workflow em N8N que consome a API oficial da FIFA, trata os dados em JavaScript e cria automaticamente os jogos da fase de grupos na Google Agenda.

## 📖 Contexto

Buscar manualmente os jogos da Copa do Mundo todos os dias é repetitivo e pouco eficiente.

Este projeto automatiza:

- Consumo da API oficial da FIFA
- Tratamento e padronização dos dados
- Criação automática de eventos na Google Agenda

## 🏗 Arquitetura

Fluxo:

1. HTTP Request → Consome API da FIFA
2. Code (JavaScript) → Filtra fase de grupos e ajusta timezone
3. Google Calendar Node → Cria eventos automaticamente

Ambiente executado via Docker.

## 🛠 Stack

- N8N
- Docker
- API pública da FIFA
- Google Calendar API
- JavaScript (data transformation)

## 🚀 Como executar

### 1. Subir o N8N via Docker

docker run -it --rm \
  -p 5678:5678 \
  n8nio/n8n

### 2. Importar o workflow
- Acesse http://localhost:5678
- Import Workflow
- Selecione o arquivo JSON deste repositório

### 3. Configurar credencial Google
- Criar credencial OAuth no N8N
- Selecionar no node "Google Calendar"

### 4. Executar manualmente

## 🔐 Configuração

É necessário:

- Criar credencial OAuth Google
- Informar o ID da agenda no node

- ## 📌 Resultado

- 72 jogos da fase de grupos criados automaticamente
- Padronização de informações
- Custo de execução: R$ 0,00

A agenda pode ser acessada através deste link:

🔗 [Adicionar à Google Agenda](https://calendar.google.com/calendar/u/0?cid=NWQxODA2MTZjMTIxYmMwNGYxZTBlOTRhOGRhNzcyOTUwZWNjYjQxNTIyZTJkN2RiZDRmMjJhMjJhNTQ4NjliMEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t)
