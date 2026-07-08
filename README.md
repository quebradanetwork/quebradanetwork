# .github — Quebrada Network

Este é o repositório especial **`.github`** da organização
[Quebrada Network](https://github.com/quebradanetwork). Ele centraliza a
identidade da organização e os arquivos de comunidade padrão, que são
aplicados automaticamente a **todos** os repositórios que não possuírem seus
próprios equivalentes.

> ⚠️ Para que o perfil da organização apareça, este repositório precisa se
> chamar exatamente **`.github`** e ser **público**.

## 📂 Estrutura

```
.github/                     ← repositório (nome fixo: ".github")
├── profile/
│   └── README.md            # Página principal exibida no perfil da organização
│
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug.yml          # Template de bug
│   │   ├── feature.yml      # Template de funcionalidade
│   │   └── config.yml       # Configuração do seletor de issues
│   ├── DISCUSSION_TEMPLATE/
│   │   └── duvidas.yml       # Template de discussões
│   ├── workflows/
│   │   └── update-stats.yml # Gera e commita os cards de estatísticas (SVG)
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── FUNDING.yml
│
├── CODE_OF_CONDUCT.md       # Código de conduta (org-wide)
├── CONTRIBUTING.md          # Guia de contribuição (org-wide)
├── SECURITY.md              # Política de segurança (org-wide)
├── SUPPORT.md               # Canais de suporte (org-wide)
├── LICENSE                  # Licença padrão da organização
│
└── docs/
    ├── branding.md          # Identidade visual e uso da marca
    ├── stack.md             # Stack tecnológica detalhada
    ├── architecture.md      # Padrões de arquitetura
    ├── repositories.md      # Convenções de repositórios
    └── development-standards.md  # Padrões de desenvolvimento
```

## 🚀 Como publicar

1. Crie um repositório **público** chamado `.github` na organização.
2. Envie o conteúdo deste `.zip` para a raiz do repositório.
3. O `profile/README.md` passará a ser exibido na página da organização.
4. Os arquivos de comunidade valerão como padrão para os demais repositórios.

## 🎨 Pendências recomendadas

- [ ] Adicionar `profile/assets/banner.png` (1920×640)
- [ ] Adicionar `profile/assets/logo.png`
- [ ] Rodar o workflow **Atualizar cards de estatísticas** uma vez (aba Actions →
      _Run workflow_) para gerar `profile/stats.svg` e `profile/top-langs.svg`
- [ ] (Opcional) Criar um secret `STATS_PAT` para incluir repositórios privados
- [ ] Revisar domínios e e-mails de contato
- [ ] Ativar **Discussions** na organização (se desejar usar o template)

> 💡 **Estatísticas:** os cards são gerados via
> [`github-readme-stats-action`](https://github.com/stats-organization/github-readme-stats-action)
> e commitados em `profile/` — não dependem de endpoint público em tempo real.
> Configuração em `.github/workflows/update-stats.yml`.

---

<sub>© 2025 Quebrada Network</sub>
