# Zabbix + Grafana com Docker e SSL (Let's Encrypt)
Este repositório configura um ambiente de monitoramento com Zabbix 7 e Grafana, protegidos com HTTPS automático usando **nginx-proxy** e **Let's Encrypt**.

## 📦 Componentes

- Zabbix Server + Web + Agent
- PostgreSQL (banco de dados)
- Grafana
- Nginx Proxy (reverse proxy com HTTPS automático)
- Let's Encrypt companion (para gerar certificados SSL válidos)

## 🌐 Acesso

| Serviço       | URL                              | Usuário | Senha   |
|---------------|----------------------------------|---------|---------|
| Zabbix Web    | https://zabbix.seudominio.com.br | Admin   | zabbix  |
| Grafana       | https://grafana.seudominio.com.br| admin   | admin   |

> **Nota:** Substitua `seudominio.com.br` pelo seu domínio real e configure o DNS apontando para seu servidor Docker.

## 🚀 Como usar

### 1. Criar rede compartilhada do proxy (uma vez)

```bash
docker network create nginx-proxy
