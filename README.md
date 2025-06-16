# fc-docker-node

Este projeto é uma aplicação simples utilizando **Node.js + Express + MySQL + Nginx**, demonstrando integração entre containers Docker.

---

## 🚀 Pré-requisitos

- [Docker](https://www.docker.com/products/docker-desktop/) instalado
- [Docker Compose](https://docs.docker.com/compose/) instalado

---

## 🐳 Executando com Docker Compose

1. Clone este repositório:

```bash
git clone https://github.com/jonasmzsouza/fc-docker-node.git
cd fc-docker-node
```

2. Suba os containers:

```bash
docker compose up --build -d
```
Aguarde até que todos os serviços estejam prontos. O container app esperará o MySQL estar saudável antes de iniciar.

3. Acesse a aplicação via navegador:

- http://localhost:8080

A cada atualização da página, um novo nome "Jonas" é inserido no banco e listado na tela.

---

## ❌ Finalizando

Para parar e remover os containers:

```bash
docker compose down
```

---

## 📁 Estrutura do Projeto

```bash
.
├── docker-compose.yml
├── node/
│   ├── Dockerfile
│   └── index.js
├── nginx/
│   └── nginx.conf
└── mysql/ (criado automaticamente pelo volume)
```

---

## 🔧 Tecnologias utilizadas
- Node.js 22 (Express)
- MySQL 8.0
- Nginx (proxy reverso)
- Docker + Docker Compose

---

## 📃 Licença

Este projeto é de uso livre para fins educacionais.