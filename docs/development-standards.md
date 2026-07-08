# Padrões de Desenvolvimento

Padrões técnicos aplicados em todos os projetos da Quebrada Network.

## 🌍 Idioma

- **pt-BR** em comentários de código e em todo texto voltado ao jogador/usuário.
- Nomes de variáveis/funções podem seguir convenção técnica em inglês, desde que
  claros e consistentes com o projeto.

## 🔒 Segurança

- **Server-authoritative:** nunca confie em valores vindos do cliente/NUI.
- Valide e sanitize toda entrada externa no servidor.
- **Nunca** exponha webhooks, tokens, chaves ou credenciais no cliente ou no repositório.
- Sinalize proativamente riscos: exposição de webhook, race conditions,
  vulnerabilidades de confiança no cliente.

## 🎮 FiveM / vRP

- **Identidade:** use `vRP.Passport` para identificar o jogador.
- **Persistência:** use `vRP.GetSrvData` / `vRP.SetSrvData`.
- **Banco:** use `oxmysql` para operações relacionais.
- **Arquitetura:** respeite o padrão Tunnel/Proxy do vRP.
- **NUI:** React + Vite; a NUI é camada de apresentação — nunca de decisão.

### Validação obrigatória

- Rode `luac5.4` em todo Lua **antes de entregar**.
- Verifique ausência de erros no console (F8) e no txAdmin.

## ⚡ Performance

- Evite loops de eventos de alta frequência que saturem a fila de saída
  (ex.: atualização contínua de coordenadas/blips).
- Prefira _batching_ e _debounce_ em eventos frequentes.
- Meça antes de otimizar; otimize o gargalo real.

## 🧱 Estilo e manutenção

- Prefira **correções cirúrgicas** a reescritas; reescreva apenas quando justificado.
- Mantenha funções pequenas e com responsabilidade única.
- Código reutilizável e modular; evite duplicação.
- Documente decisões não óbvias no próprio PR.

## 🛠️ Fluxo de edição

- Edições de arquivo via _heredoc_ (Python/bash) com verificação por `grep`.
- Confirme o resultado da edição antes de considerar a tarefa concluída.

## ✅ Definition of Done

Uma entrega está pronta quando:

- [ ] Segue os padrões acima
- [ ] Lua validado com `luac5.4` (quando aplicável)
- [ ] Sem erros de console no teste local
- [ ] Sem segredos expostos
- [ ] Sem race conditions conhecidas
- [ ] Textos ao usuário em pt-BR
- [ ] Pronto para produção (nada de _boilerplate_ ou correção parcial)
