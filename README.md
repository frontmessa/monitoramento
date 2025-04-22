# Monitoramento da Qualidade do Ar

Projeto para monitorar e exibir dados sobre a qualidade do ar em tempo real, com foco em cidades inteligentes e sustentabilidade.

## Tecnologias Utilizadas

- Java 17 + Spring Boot
- Docker & Docker Compose
- MongoDB
- GitHub Actions (CI/CD)
- Git + GitHub
- GitHub Secrets & Push Protection
- Git Filter-Repo (limpeza de histórico)
- Ambiente de produção via Docker Compose (`stage/prod`)

## Como Executar Localmente

1. **Clone o repositório:**

```bash
git clone https://github.com/seuusuario/monitoramento.git
cd monitoramento
Configure o .env:

Crie um arquivo .env com as variáveis necessárias (exemplo abaixo):

env
Copiar
Editar
MONGO_INITDB_ROOT_USERNAME=admin
MONGO_INITDB_ROOT_PASSWORD=senha123
⚠️ O arquivo .env está no .gitignore para segurança.

Execute com Docker Compose:

bash

docker-compose -f docker-compose.stage.yml up --build -d
Acesse: http://localhost:8080

 CI/CD com GitHub Actions
Este projeto possui integração contínua automatizada. O pipeline realiza:

Build e testes da aplicação

Lint e validações

Deploy em ambiente de produção com Docker 

Arquivo do workflow: .github/workflows/main.yml
