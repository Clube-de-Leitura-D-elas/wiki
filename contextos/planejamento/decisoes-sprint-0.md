---
type: decisoes
title: Decisões da Sprint 0
description: Decisões consolidadas na Sprint 0 que sustentam o escopo do MVP e o roadmap de sprints.
tags: [decisoes, sprint-0, mvp]
status: ativo
timestamp: 2026-08-27
---

# Decisões da Sprint 0

Decisões consolidadas durante a Sprint 0 (11/08–27/08/2026), a partir do [Termo de Abertura](../materiais/termo-de-abertura.md) e do [kickoff](../materiais/kickoff/). Sustentam os [épicos do MVP](./epicos-mvp.md) e o [roadmap](./roadmap.md).

## Plataforma: app mobile em Flutter e painel web de gestão

**Enunciado:** o produto tem duas frentes — um aplicativo mobile em **Flutter**, para leitoras e coordenadoras, e um **painel web** para o trabalho administrativo da gestão —, ambas consumindo o mesmo backend.

**Motivo:** o uso cotidiano do produto acontece no celular; manter grupos e participantes e enxergar o clube inteiro é trabalho administrativo que não faz sentido numa tela pequena. Uma única API serve as duas frentes.

**Data:** 27/08/2026

## Carga inicial de dados via seed

**Enunciado:** a carga inicial de grupos, participantes e coordenações entra por **seed na Sprint 1**; a manutenção durável desses dados passa ao painel de gestão.

**Motivo:** destravar o desenvolvimento e as demos já na primeira semana, sem esperar a primeira versão do painel de gestão.

**Data:** 27/08/2026

## Re-indicação de livro após sorteio

**Enunciado:** depois que o livro de uma leitora é sorteado em um grupo, ela **não faz nova indicação naquele grupo**.

**Motivo:** garantir que o sorteio circule pelos livros de todas as participantes do grupo, em vez de se concentrar em quem já foi sorteada.

**Data:** 27/08/2026

## Notificações com gatilhos modelados desde o início

**Enunciado:** o MVP contempla push **e/ou** avisos no aplicativo; o mix final de canais fica em aberto, mas os **gatilhos de notificação são modelados desde o início** do desenvolvimento para suportar ambos.

**Motivo:** permitir que a definição do mix aconteça tarde, sem retrabalho na modelagem.

**Data:** 27/08/2026
