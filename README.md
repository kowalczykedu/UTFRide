# 🎓 UTF Angular Template

Template da disciplina de **Angular** (UTFPR): uma aplicação web com **Angular
20+ e BaaS** (sem backend próprio), desenvolvida em equipe com **Gitflow**. Ele
traz o método completo — comandos, agentes, workflows e guias — para você
desenvolver seu projeto com **UTF-SDD**, um **SDD por Portões** (*Gated
Spec-Driven Development*): a IA escreve o código; **você decide nos portões**,
quem revisa nunca é quem escreveu, e todo artefato é evidência para a
apresentação final.

## 🚀 Como começar

1. Clique em **Use this template → Create a new repository** (não faça fork).
   O repositório criado é seu.
2. Clone o seu repositório e abra-o na sua IDE agêntica. **Claude Code, Cursor,
   Antigravity e OpenCode já vêm configurados** — inclusive a trava que impede os
   revisores de editar arquivo. Veja *Um método, quatro ferramentas*, abaixo.
3. Leia `docs/checklist.md` — é a **ficha da disciplina**: as regras do projeto,
   os Indicadores de Desempenho (IDs) e as entregas.
4. Siga o fluxo, um comando por fase:

| Fase | Comando | Produz |
| --- | --- | --- |
| Requisitos | `/utf-prd` | `docs/prd.md` — o QUE o produto faz |
| Backlog | `/utf-backlog` | Issues no GitHub + Kanban no Projects |
| Design | `/utf-design` | `docs/design-tokens.md` + protótipo navegável — tokens, Mobile-First e identidade PWA |
| Arquitetura | `/utf-architecture` | `docs/architecture.md` — onde as coisas moram |
| Scaffold | `/utf-setup` | o app Angular, nascendo verde |
| Cada história | `/utf-issue <n>` → `/utf-task` | spec, plano e código, tarefa a tarefa |
| Aprender | `/utf-tutor` | a explicação didática de cada passo |

### Um método, quatro ferramentas

O conteúdo de verdade — constituição, fluxos e subagentes — vive uma vez só, em
`.agents/`. Cada ferramenta tem apenas uma casca de poucas linhas que aponta para
lá, com a sintaxe de permissão dela. Trocar de ferramenta no meio do semestre não
reescreve nada: o miolo é o mesmo.

| Ferramenta | Regras | Comandos | Subagentes |
| --- | --- | --- | --- |
| Claude Code | `CLAUDE.md` | `.claude/commands/` | `.claude/agents/` |
| Cursor | `.cursor/rules/` | `.cursor/commands/` | `.cursor/agents/` |
| Antigravity | `.agents/rules/` | `.agents/workflows/` | `.agents/agents/` |
| OpenCode | `AGENTS.md` | `.opencode/command/` | `.opencode/agents/` |

Nas quatro, os revisores e o tutor nascem **sem poder de escrita**; só o
implementador escreve. A trava tem forças diferentes, e vale saber qual você tem:

- **Claude Code, Cursor e Antigravity** negam a ferramenta de edição, mas precisam
  liberar o terminal para o revisor rodar `git diff`. Quem tem terminal poderia, em
  tese, escrever com `sed` ou redirecionamento — o que fecha isso ali é a proibição
  escrita no prompt do agente.
- **O OpenCode fecha por configuração:** é o único que libera comandos específicos em
  vez de ligar ou desligar o terminal inteiro. E **funciona com modelos gratuitos**,
  o que faz dele o caminho de custo zero mais completo da disciplina. Ajuste a lista
  de comandos de teste em `.opencode/agents/` à stack do seu `docs/architecture.md`:
  comando que não estiver liberado não roda, e o parecer sai incompleto sem avisar.

> Se o seu OpenCode não listar os agentes ou os comandos, é diferença de versão nos
> nomes das pastas: renomeie `.opencode/agents/` para `.opencode/agent/` e
> `.opencode/command/` para `.opencode/commands/`. O conteúdo é o mesmo.

O passo a passo detalhado está em [`docs/tutorial-sdd.md`](docs/tutorial-sdd.md);
o porquê de cada regra, em [`docs/guia-sdd.md`](docs/guia-sdd.md).

Pré-requisitos das integrações: **`gh` autenticado (`gh auth login`, escopos
`repo`, `workflow` e `project`) ou MCP do GitHub** — sem isso, backlog, etiquetas
e PRs não saem. **MCPs recomendados** (ID32 — configure na sua IDE): **Figma**
(o protótipo vira contexto do agente), **Supabase** (na E3) e **Context7**
(versões atuais de ferramentas antes de decidir).

---

> ✂️ **Daqui para baixo é a vitrine do SEU projeto.** Apague tudo acima desta
> linha (incluindo ela) quando o projeto tiver nome, e preencha o que segue.

# [Nome da aplicação]

[Breve descrição: o tema do semestre e o escopo/identidade da SUA equipe.]

## Autores

- [Nome completo — GitHub]

## Documentação Técnica

- [PRD](docs/prd.md) · [Architecture/SSD](docs/architecture.md) · [Checklist](docs/checklist.md)
- **Protótipo (Stitch/Figma):** [link público]

## Modelagem de Dados (Diagrama ER)

```mermaid
erDiagram
```

## Stack

- **Frontend:** Angular [versão]
- **Framework CSS:** [Tailwind, PrimeNG, …]
- **Dados:** json-server (MVP/E2) → [Supabase, PocketBase, …] (E3)
- **Bibliotecas:** [lista]

## Em produção

- **Aplicação:** [URL no Vercel/Render]

## Instruções de Execução

[Passos para configurar e rodar localmente — gerado/refinado no `/utf-setup`.]

## Telas da Aplicação

[Imagens de algumas telas.]
