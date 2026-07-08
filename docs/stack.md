# Stack Tecnológica

Visão detalhada das tecnologias utilizadas nos projetos da Quebrada Network.

## 🎮 FiveM

| Camada | Tecnologia |
|--------|-----------|
| Runtime / lógica | **Lua** (server & client) |
| Framework | **vRP** (fork ImagicTheCat / PascalCase) |
| Arquitetura | Tunnel / Proxy |
| Banco de dados | **oxmysql** sobre MySQL |
| Interfaces (NUI) | **React** + **Vite** |
| Validação | `luac5.4` antes da entrega |

## 🌐 Web

| Camada | Tecnologia |
|--------|-----------|
| Frontend | **Next.js**, **React**, **Vite**, TypeScript |
| Backend | **NestJS**, **Node.js**, **PHP**, **Laravel** |
| ORM | **Prisma** |
| APIs | REST |
| Integrações | Discord (webhooks / bots) |

## ☁️ SaaS — QFinance

| Camada | Tecnologia |
|--------|-----------|
| Frontend | Next.js + Recharts (dashboards) |
| Backend | NestJS / Node.js |
| ORM | Prisma |
| Mobile | Build Android **AAB** + Digital Asset Links |
| Domínio | plataforma de microcrédito e cobrança (pt-BR) |

## 📡 Infraestrutura & Monitoramento

| Camada | Tecnologia |
|--------|-----------|
| Séries temporais | **TimescaleDB** |
| API de coleta | **Fastify** |
| Dashboard | **Next.js** |
| Alertas | Discord / webhooks |
| Observabilidade | políticas de retenção, páginas de status |

## 🛠️ DevOps

- **Linux** (servidores de produção)
- **Docker**
- **Git** / GitHub
- **Nginx** (proxy reverso)
- **Redis** (cache / filas, quando aplicável)

## 🔤 Convenções

- **pt-BR** em comentários e textos ao usuário.
- Edições de arquivo via _heredoc_ com verificação por `grep`.
- Validação de Lua com `luac5.4` antes de qualquer entrega.
