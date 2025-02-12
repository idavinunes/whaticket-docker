# 📦 Whaticket SaaS - Docker

Projeto Whaticket SaaS totalmente containerizado utilizando **Docker** e **Docker Compose**, facilitando a implantação e configuração do ambiente.

## 🚀 Como Instalar

### 1️⃣ Clone o repositório
```sh
git clone https://github.com/idavinunes/whaticket-docker.git
cd whaticket-docker
```

### 2️⃣ Construa as Imagens Docker
```sh
docker compose build
```
Esse comando criará as imagens e os contêineres necessários para rodar o projeto.

---

## 🖥️ Configuração da Rede

1. **Abra o Portainer** e **crie uma rede** com o nome de sua preferência.
2. **Edite os arquivos de configuração** do projeto para garantir que a rede criada esteja definida corretamente no `docker-compose.yaml`.

---

## 🌍 Acesso Externo (Cloudflare Zero Trust)
Atualmente, o projeto **ainda não está configurado para funcionar com o Traefik**, mas você pode utilizar o **Cloudflare Zero Trust** para expor os serviços externamente via **tunnel**.

### 📌 Como configurar o Cloudflare Tunnel:
1. **Crie um subdomínio** no Cloudflare para cada serviço.
2. **Aponte os domínios para os serviços internos**, conforme o exemplo:
   - **Frontend**: `whafront.axisnetworks.com.br` → `http://whaticket_frontend:3250`
   - **Backend**: `whapi.axisnetworks.com.br` → `http://whaticket_backend:3001`

---

## 🔦 Banco de Dados
A migração do banco de dados ocorre automaticamente, então nenhuma ação extra é necessária.

---

## 🔑 Acesso ao Sistema
Após a instalação, utilize as credenciais padrão:

- **Usuário:** `admin@admin.com`
- **Senha:** `123456`

---

## 📌 Tecnologias Utilizadas
- **Docker** e **Docker Compose**
- **Cloudflare Zero Trust**
- **Node.js** (Backend)
- **React.js** (Frontend)
- **PostgreSQL** (Banco de Dados)
- **Redis** (Cache e Filas)

---

## 💌 Contato e Contribuição
Caso tenha dúvidas ou queira contribuir, abra um **issue** ou envie um **pull request**.

---

## 🐜 Licença
Este projeto está sob a licença **MIT**.

---

🚀 **Agora é só rodar e começar a utilizar o Whaticket SaaS!** 🎉

