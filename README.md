# financeiro-deploy

Repositório de deploy do sistema financeiro (backend + frontend + banco de dados).

## Pré-requisitos

- Docker e Docker Compose instalados no servidor
- Git instalado

## Como subir o projeto

### 1. Clone os três repositórios na mesma pasta

```bash
mkdir financeiro && cd financeiro
git clone https://github.com/Sdioni30/financeiro-backend.git
git clone https://github.com/Sdioni30/financeiro-frontend.git
git clone https://github.com/Sdioni30/financeiro-deploy.git
```

### 2. Configure as variáveis de ambiente

```bash
cd financeiro-deploy
cp .env.example .env
# edite o .env com seus valores reais
```

### 3. Suba os containers

```bash
docker compose up -d --build
```

### 4. Acesse

- Frontend: `http://SEU_IP`
- API: `http://SEU_IP:8080`
- Swagger: `http://SEU_IP:8080/swagger-ui.html`

## Atualizar para nova versão

```bash
git -C ../financeiro-backend pull
git -C ../financeiro-frontend pull
docker compose up -d --build
```
