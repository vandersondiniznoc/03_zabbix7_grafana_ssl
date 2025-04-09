# Zabbix + Grafana com Docker e SSL (Let's Encrypt)
Este repositório configura um ambiente de monitoramento com **Zabbix 7** e **Grafana**, protegidos com HTTPS automático usando **nginx-proxy** e **Let's Encrypt**.

## 🌆 Acesso Rápido

| Serviço       | URL                              | Usuário | Senha   |
|---------------|----------------------------------|---------|---------|
| Zabbix Web    | https://zabbix.seudominio.com.br | Admin   | zabbix  |
| Grafana       | https://grafana.seudominio.com.br| admin   | admin   |

> Substitua `seudominio.com.br` pelo seu domínio real. Certifique-se que o DNS esteja corretamente apontando para o IP do servidor Docker.

---

## 🚀 Como usar

### 1. Subir os serviços

```bash
docker compose up -d
```

O Docker irá criar automaticamente a rede `nginx-proxy` e os certificados SSL serão gerados via Let's Encrypt.

### 2. Verificar

- Acesse os serviços nos links HTTPS informados.
- O certificado SSL estará ativo se o DNS e as portas estiverem corretamente configurados.

---

## 👉 Requisitos

- Docker e Docker Compose instalados
- Domínio apontando para seu IP
- Portas **80** e **443** liberadas no firewall

---

## 📂 Volumes utilizados

- `postgres-data`: dados do banco PostgreSQL
- `grafana-storage`: dados persistentes do Grafana
- `certs`: certificados SSL gerados automaticamente

---

Altere o IP do Zabbix Agent na interface WEB 

## 📜 Créditos

- [Zabbix Docker](https://hub.docker.com/u/zabbix)
- [Grafana Docker](https://hub.docker.com/r/grafana/grafana)
- [nginx-proxy](https://github.com/nginx-proxy/nginx-proxy)
- [Let's Encrypt Companion](https://github.com/nginx-proxy/acme-companion)

