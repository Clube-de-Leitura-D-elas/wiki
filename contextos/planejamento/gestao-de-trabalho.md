---
type: convencao
title: Gestão de trabalho no Linear
description: Como o trabalho é estruturado no Linear — hierarquia de issues, regras de decomposição e templates.
tags: [linear, processo, planejamento]
status: rascunho
timestamp: 2026-09-01
---

# Gestão de trabalho no Linear

O board deve ser autoexplicativo: quem pega uma task precisa entender o que fazer e quando
está pronto sem precisar buscar contexto em outros canais. Este documento define a estrutura
das issues e o que se espera de cada nível.

## Hierarquia

O trabalho é organizado em três níveis: épico, história de usuário (US) e task técnica.

Um épico agrupa uma funcionalidade completa. Descreve o problema a resolver e a visão da
solução; detalhes de especificação ficam na wiki, e o épico aponta para eles.

Uma US pertence a um épico e descreve o trabalho do ponto de vista de quem usa o sistema:
quem é o usuário, o que ele precisa e por quê. Toda US tem critérios de aceite verificáveis.
US são redigidas por AGES IV.

Uma task técnica, quando existir, pertence a uma US e descreve o trabalho de implementação:
o quê, onde e o critério de pronto. A task referencia a US pai e não repete seus critérios
de aceite.

Bugs, dívida técnica e setup de ambiente não pertencem a essa hierarquia. Essas issues
recebem uma label de tema e seguem o fluxo normal do board, sem pai obrigatório.

## Decomposição

A decomposição não é obrigatória. Uma US que pode ser implementada em uma única issue não
gera tasks: a própria US é executada. Tasks técnicas existem quando o trabalho é grande
demais para um PR ou quando será dividido entre mais de uma pessoa.

## O que não vai em issue

Decisões, pendências e discussões ficam na wiki. A issue contém apenas o que é necessário
para executá-la e, quando relevante, um link para a especificação.

## Fluxo de trabalho

Uma US entra no board para execução somente com contexto e critérios de aceite completos. O limite de
trabalho em andamento é de uma task por pessoa: para começar outra, é preciso concluir ou
devolver a atual.
