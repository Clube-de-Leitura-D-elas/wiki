# AGENTS.md — wiki

## O que é este repositório

Base de conhecimento do **Clube de Leitura D'elas**. Aqui mora o contexto durável que
humanos e agentes de IA consomem para planejar e executar: specs, decisões, briefs e
arquiteturas.

- `contextos/` — **bundle OKF**: conhecimento durável, organizado por domínio.
- `templates/` — modelos de documento por tipo (fora do bundle).

Os documentos são alto nível: contratos, garantias, comportamentos e o porquê deles —
detalhe de implementação vive no código.

## Padrão: OKF (Open Knowledge Format)

`contextos/` é um bundle [OKF v0.1](templates/okf-spec.md). Na dúvida, a especificação manda.
As regras locais que tornam o corpus consultável:

1. **Todo documento tem frontmatter** com `type`, `status` e `tags`.
2. **Links entre documentos são relativos padrão markdown** (`../dominio/arquivo.md`).
3. **Asset não-markdown** (CSV, imagem) tem um `.md` irmão como dono.

## Frontmatter

```yaml
---
type: spec
title: Título do documento
description: Uma frase que resume o documento (aparece nos index.md).
tags: [tag1, tag2]
status: ativo # rascunho | ativo
timestamp: 2026-08-11
---
```

## Tipos de documento (`type`)

Lista não exaustiva — se nenhum servir, cunhe um descritivo e autoexplicativo:

- `guia` — visões gerais, introduções, referências de contexto.
- `spec` — especificação de produto ou funcionalidade.
- `requisitos`
- `decisoes` — registro de decisões datadas e imutáveis (ver "Decisões" abaixo).
- `glossario` — termos e definições de negócio e produto.
- `fluxo` — fluxo de usuário por persona.
- `modelo-de-dados` — modelo de dados/domínio, contratos de dados, regras de cálculo.
- `arquitetura`

## Tags

As tags são o eixo de consulta transversal do corpus — é por elas que se responde "tudo que
afeta X", independente de em qual pasta o documento mora. Tags podem ser personas,
funcionalidades ou qualquer outro tópico que o documento aborda.

## Organização de pastas

**Livre — do jeito que fizer sentido para quem mantém.** Pasta serve para coesão e ownership;
a visão por persona quem dá são as tags. Duas orientações, não regras:

- Não crie pasta vazia — ela nasce com o primeiro documento.
- `index.md` em subpastas é bem-vindo onde ajudar a navegação, mas não é obrigatório — um
  index desatualizado é pior que nenhum, e o consumidor pode sintetizar um na hora.

Documentos supersedidos/arquivados podem ir para uma subpasta `arquivo/` do domínio, com
`status: supersedido` + `substituido_por:`.

## Nomenclatura

- **kebab-case, português, sem emoji, sem espaços, sem hashes.** Termos de código/produto em
  inglês são aceitos (`rbac-spec.md`).
- **Sem sufixo de versão no nome** (`-v2`, `-v3`). Nova versão = mesmo arquivo.

## Decisões

Decisões consolidadas moram em docs `type: decisoes` (por iniciativa ou por domínio, quando
transversais). Cada entrada tem **enunciado, motivo e data** — e é imutável: para mudar uma
decisão, adiciona-se uma nova, datada, que marca a anterior como substituída.
