# Convenções de Repositórios

Padrões para nomear, organizar e manter os repositórios da Quebrada Network.

## 🏷️ Nomenclatura

Prefixos por domínio do projeto:

| Prefixo | Uso | Exemplos |
|---------|-----|----------|
| `qn_` / `qnet_` | Recursos e produtos da organização | `qn_radio`, `qn_panel`, `qn_emotes` |
| `qp_` / `qprp_` | Recursos do servidor Quebrada Paulista | `qp_store`, `qp-bank` |
| `qfinance` | Plataforma SaaS QFinance | `qfinance-api`, `qfinance-app` |
| `docs-` | Documentação | `docs-vrp` |

> Padronizar prefixos facilita busca, agrupamento e identificação de propriedade.

## 🌿 Branches

- `main` — estável, pronta para produção.
- `dev` — integração contínua (quando aplicável).
- `feat/<nome>` — novas funcionalidades.
- `fix/<nome>` — correções.
- `refactor/<nome>` — refatorações.

## 🔖 Versionamento

- **SemVer** (`MAJOR.MINOR.PATCH`) para produtos versionados.
- _Tags_ e _releases_ com changelog resumido.

## 📄 Arquivos esperados por repositório

Repositórios não precisam duplicar os arquivos de comunidade — eles herdam
deste repositório `.github`. O que cada repo deve ter:

- `README.md` — descrição, instalação, uso, dependências.
- `CHANGELOG.md` — histórico de mudanças (quando versionado).
- `LICENSE` — apenas se diferente do padrão da organização.
- `.gitignore` — adequado à stack.

## ✅ Qualidade antes do merge

- Lua validado com `luac5.4` (resources FiveM).
- Sem segredos/credenciais/webhooks no histórico.
- Sem race conditions conhecidas.
- Testado localmente sem erros de console.
- Comentários e textos ao usuário em **pt-BR**.

## 🔐 Visibilidade

- Produtos proprietários: repositórios **privados** por padrão.
- O repositório `.github` deve ser **público** para exibir o perfil da organização.
