# Contribuindo com a Quebrada Network

Obrigado pelo interesse em contribuir. Este guia descreve o fluxo e os padrões
esperados nas contribuições aos projetos da organização.

> Este repositório `.github` centraliza os arquivos de comunidade que valem
> para **todos** os repositórios da organização.

## 📌 Antes de começar

1. Leia o [Código de Conduta](./CODE_OF_CONDUCT.md).
2. Verifique as [issues abertas](../../issues) para evitar trabalho duplicado.
3. Para mudanças grandes, abra primeiro uma issue de discussão.

## 🔀 Fluxo de contribuição

1. Faça um _fork_ do repositório.
2. Crie uma branch descritiva a partir da `main`:
   ```bash
   git checkout -b feat/nome-da-feature
   # ou
   git checkout -b fix/descricao-do-bug
   ```
3. Faça commits pequenos e objetivos (veja o padrão abaixo).
4. Abra um Pull Request preenchendo o template.

## ✍️ Padrão de commits

Seguimos o **Conventional Commits**:

```
tipo(escopo): descrição curta no imperativo

[corpo opcional]
```

Tipos aceitos: `feat`, `fix`, `refactor`, `perf`, `docs`, `style`, `chore`, `security`.

Exemplos:

```
feat(qp_store): adiciona hierarquia de staff em três níveis
fix(qn_radio): corrige race condition no BypassProtect
perf(blipsystem): reduz saturação da fila de saída em UpdateCoords
```

## 🧭 Padrões técnicos

Todas as contribuições devem seguir os padrões descritos em
[`docs/development-standards.md`](./docs/development-standards.md). Em resumo:

- **Validação server-authoritative** — nunca confie no cliente.
- **pt-BR** em comentários de código e textos voltados ao jogador/usuário.
- **vRP**: use `vRP.Passport` para identidade e `vRP.GetSrvData` / `SetSrvData`
  para persistência.
- **Lua** validado com `luac5.4` antes de enviar.
- Sem exposição de webhooks, tokens ou credenciais.
- Prefira **correções cirúrgicas** a reescritas — reescreva apenas quando
  realmente justificado.

## ✅ Checklist do PR

- [ ] Segue os padrões de desenvolvimento
- [ ] Testado localmente sem erros de console
- [ ] Sem segredos expostos
- [ ] Documentação atualizada quando necessário

## 🐞 Reportando bugs

Use o template **🐞 Reportar Bug** nas issues, com passos de reprodução e logs.

## ✨ Sugerindo funcionalidades

Use o template **✨ Solicitar Funcionalidade**, explicando o problema que a
proposta resolve.

## 🔒 Segurança

**Não** abra issues públicas para vulnerabilidades. Siga a
[Política de Segurança](./SECURITY.md).
