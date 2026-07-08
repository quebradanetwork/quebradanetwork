# Padrões de Arquitetura

Princípios de arquitetura seguidos nos projetos da Quebrada Network.

## 🧩 Princípios gerais

- **Server-authoritative** — toda decisão sensível ocorre no servidor. O cliente
  nunca é fonte de verdade.
- **Modularidade** — sistemas desacoplados, com responsabilidades bem definidas.
- **Correções cirúrgicas** — preferir ajustes pontuais a reescritas, exceto
  quando a reescrita for claramente justificada.
- **Persistência consistente** — um único caminho previsível para ler/gravar dados.

## 🎮 FiveM (vRP)

### Identidade e persistência

- **Identidade:** `vRP.Passport` como identificador do jogador.
- **Persistência:** `vRP.GetSrvData` / `vRP.SetSrvData`.
- **Banco:** `oxmysql` para operações relacionais.

### Comunicação

- Arquitetura **Tunnel / Proxy** do vRP para client ↔ server.
- Exports bem definidos entre resources; evitar acoplamento implícito.

### Cuidados recorrentes

- **Race conditions** em exports (ex.: chamadas a `BypassProtect`) — garantir
  ordem e estado antes de agir.
- **Saturação de fila de saída** — evitar loops de eventos de alta frequência
  (ex.: atualizações de coordenadas/blips) que saturem o _outbound queue_.
- **Confiança no cliente** — validar no servidor qualquer valor vindo da NUI/cliente.

## 🌐 Web / SaaS

- **Camadas separadas:** apresentação (Next.js/React) ↔ API (NestJS/PHP) ↔ dados (Prisma/MySQL).
- **APIs REST** com contratos claros e validação de entrada.
- **Autenticação e autorização** explícitas em cada rota sensível.
- **Segredos** sempre fora do código (variáveis de ambiente).

## 📡 Observabilidade

- Métricas em série temporal (**TimescaleDB**).
- Coleta via **Fastify**; visualização em **Next.js**.
- **Alertas** via Discord/webhooks; políticas de retenção definidas.

## 🔒 Segurança por padrão

- Nunca expor webhooks, tokens ou credenciais no cliente ou no repositório.
- Validar e sanitizar toda entrada externa.
- Registrar e tratar erros sem vazar detalhes sensíveis.
