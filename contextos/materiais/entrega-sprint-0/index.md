---
type: reuniao
title: Entrega Sprint 0 — Clube de Leitura D'elas
description: Validação do protótipo e planejamento do semestre na entrega da Sprint 0, com presença da equipe AGES e das clientes do clube.
tags: [sprint-0, prototipo, validação, produto]
status: ativo
timestamp: 2026-08-27
---

# Entrega Sprint 0 — Clube de Leitura D'elas

Reunião de entrega/validação da **Sprint 0**, realizada em **27 de agosto de 2026**, na qual a equipe de desenvolvimento apresentou à stakeholder a visão do produto, as decisões de tecnologia e os **protótipos de tela** do aplicativo, bem como o planejamento das próximas sprints.

Resumo gerado por IA com base apenas na transcrição. Leve com um grão de sal.

## Participantes

A transcrição foi diarizada e os speakers mapeados manualmente:

| Speaker | Nome     | Papel                                          |
| ------- | -------- | ---------------------------------------------- |
| A       | Bruno    | Equipe de desenvolvimento (apresentação/visão) |
| D       | Davi     | Equipe de desenvolvimento (fluxos/telas)       |
| E       | Natan    | Equipe de desenvolvimento (técnico / POC)      |
| F       | Botega   | Equipe de desenvolvimento (técnico)            |
| B       | Alessandra | Cliente — professora PUC e integrante do clube |
| C       | Claudine | Cliente — fundadora e gestora do clube         |
| G, H, J | —      | Clientes/gestoras (não identificados)          |
| —        | Daniel   | Equipe de desenvolvimento (speaker literal)    |

> **Nota:** `Speaker G`, `Speaker H` e `Speaker J` ainda não foram mapeados para nomes. `Daniel` é citado pelo nome no próprio transcrito.

## Contexto da reunião

- Sprint 0 foi dedicada a **debater funcionalidades** entre a equipe, **decidir tecnologias** e desenhar **protótipos de tela** (Figma).
- Equipe optou por **aplicativo mobile** (não web responsiva) por interesse do time e aderência à solução.
- Fluxo da leitora: descobre o clube (Instagram/indicação) → preenche **Google Forms** → aprovada pela gestão → recebe código de ativação → baixa o app e vincula os dados já preenchidos (evitar duplo cadastro).

## Decisões e discussões-chave

### Inscrição fora do app (Google Forms mantido)
- Manter o **Forms** para a entrada evita que a candidata baixe o app antes de ser aprovada e **preserva a rapidez do Instagram** (link na bio).
- Aprovação/ativação via **painel web** da gestão; disparo de e-mail com código de ativação.
- Discussão sobre simplificar o Forms (não duplicar perguntas que voltam preenchidas no app).

### Painel web (gestão) + app mobile
- App mobile foca em **leitora/coordenadora**; gestão pesada (ver todos os grupos, participantes, encontros, inscrições) ficou num **painel web** para tela maior.
- Existe discussão sobre **coordenadora** também acessar gestão do próprio grupo.

### Rede social postergada
- Itens avançados de rede social (curtir, repostar, comentários) foram **postergados** por complexidade e moderação.
- Mantida a **avaliação de livros** (notas/estrelas e comentários), próxima de uma "rede social" e útil como ranking para o Instagram.

### Código de ativação / login
- Para simplificar para pessoas de **mais idade**, previu-se **código de ativação** em vez de login/senha.
- Cliente (Alessandra) sugeriu juntar tela de login e código de ativação numa só (pessoa que já está dentro usa login; nova usa código).
- **POC** demonstrada (Natan): automação Forms → banco (`pending users` → `aprovado`), disparo de e-mail com código, vínculo ao fazer login.

### Data/brasileira de presença e sorteio
- Lista de presença no encontro; sorteio apenas entre presentes; excluir já sorteados e ausentes.
- Confirmação de presença com **prazo de 48h** para desmarcar; cobrança para quem confirma e falta.
- Discussão sobre **local público vs residencial**, custos e lista de espera.

### Visita a outros grupos e grupos
- Leitora pode solicitar **visita/entrada** em outros grupos (fila de espera, aprovação da coordenadora).
- Dados de outros grupos divulgados de forma limitada (data, livro, contato da coordenadora), evitando expor local.

### Akum candados no banco
- `pending_users` → `users`; migração dos ~**1.000 participantes** já existentes (planilha com todos os dados) para o banco, com disparo em escala.
- Falta política de dados/termo de uso para publicação nas lojas.

## Tecnologias e produção
- **Supabase** (banco + automações de e-mail/push) — tier free no início.
- **Fastlane** para deploy (Google Play $25 única / Apple $99 anual).
- Cliente pede **deploy em produção já** (não POC): orçamento de host, contas de dev, primeiro deploy até a próxima apresentação.
- Discussão sobre uso de **dados reais** na produção vs. dados simulados (CPF/endereço fake) até aprovação nas lojas.

## Planejamento
- **5 sprints** no semestre (Sprint 0 já feita); funcionalidades distribuídas por sprint; **user stories** e critérios de aceitação a detalhar no **Linear**.
- Client focusing on **user stories** por sprint para validação por aceitação.

## Arquivos relacionados
- [Gravação da reunião (Opus)](./gravacao.opus) — Áudio completo (~1h11)
- [Transcrição](./transcricao.txt) — Registro textual da conversa