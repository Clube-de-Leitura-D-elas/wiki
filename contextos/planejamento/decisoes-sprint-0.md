---
type: decisoes
title: Decisões da Sprint 0
description: Decisões consolidadas na Sprint 0 que sustentam o escopo do MVP e o roadmap de sprints.
tags: [decisoes, sprint-0, mvp]
status: ativo
timestamp: 2026-08-26
---

# Decisões da Sprint 0

Decisões consolidadas durante a Sprint 0 (11/08–27/08/2026), a partir do [Termo de Abertura](../materiais/termo-de-abertura.md) e do [kickoff](../materiais/kickoff/), incluindo as decisões da [reunião de entrega de 27/08](../materiais/entrega-sprint-0/index.md). Sustentam os [épicos do MVP](./epicos-mvp.md) e o [roadmap](./roadmap.md); as pendências em aberto estão em [Decisões pendentes](./decisoes-pendentes.md).

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

## Decisões da reunião de entrega (27/08/2026)

### Login social como fluxo primário de acesso

**Enunciado:** o acesso ao aplicativo segue um fluxo único: splash, tela de login com foco em login social (Google/Apple) e botão dedicado para inserir o código de ativação, que ativa a conta e vincula a identidade aos dados da inscrição — inclusive quando o e-mail do provedor divergir do e-mail do formulário.

**Motivo:** na reunião de entrega, a cliente sugeriu fundir login e ativação numa só tela, evitando caminhos diferentes para quem já é do clube e para quem está chegando; o código permanece como ponte de identidade com o formulário.

**Data:** 27/08/2026 (reunião de entrega)

### Confirmação de presença com janela de cancelamento

**Enunciado:** a confirmação de presença pode ser cancelada até o prazo do encontro — padrão de 48 horas, configurável pela anfitriã ou coordenadora na criação. Após o prazo, o cancelamento deixa de estar disponível; a ausência após confirmação fica registrada no histórico (confirmação × comparecimento).

**Motivo:** encontros em residência envolvem rateio e compras; quem confirma e falta após o prazo gera custo. A cobrança em si continua sendo processo humano — o sistema registra o histórico.

**Data:** 27/08/2026 (reunião de entrega)

### Inativação de participante em vez de remoção

**Enunciado:** a saída de uma participante de um grupo é registrada como inativação (status ativo/inativo no vínculo), preservando o histórico dela; inativação não reabre vaga automaticamente — abrir vaga é decisão da gestão. Remoção permanece como ação restrita do painel.

**Motivo:** a cliente pediu preservar o histórico de quem sai temporariamente (licenças, mudanças) e pode voltar; e o controle de vagas deve permanecer manual, nas mãos da gestão.

**Data:** 27/08/2026 (reunião de entrega)

### Agenda com encontros de todos os grupos

**Enunciado:** a agenda do aplicativo exibe os encontros de todos os grupos do clube, participando a leitora deles ou não; encontros de grupos alheios aparecem com dados limitados (grupo, data, livro), sem local e sem dados sensíveis.

**Motivo:** a gestão já publica hoje a agenda de todos os grupos no Instagram e há leitoras que visitam outros grupos; o aplicativo centraliza essa consulta. O fluxo de solicitar visita pelo app ficou no backlog (ver [Decisões pendentes](./decisoes-pendentes.md)).

**Data:** 27/08/2026 (reunião de entrega)

### Lista de livros recomendados pelo clube, curada pela gestão

**Enunciado:** o aplicativo expõe, em leitura, a lista de livros recomendados pelo clube, separada dos resultados da busca via API pública; a lista é curada pela gestão — carga inicial via seed, manutenção pelo painel web.

**Motivo:** a busca via API pública gerou confusão entre livros "do mundo" e livros do clube; a gestão mantém hoje uma lista própria de sugestões que quer ver distinta no aplicativo.

**Data:** 27/08/2026 (reunião de entrega)

### Deploy em produção postergado; desenvolvimento em ambiente de teste

**Enunciado:** o desenvolvimento segue com deploy em ambiente de teste, usando contas próprias do time; o deploy em produção acontece após a validação, com as clientes, do documento de stack e fluxo de deploy elaborado pela AGES III — incluindo pré-requisitos de produção (contas de desenvolvedor, orçamento de hospedagem, termo de uso e política de dados).

**Motivo:** a cliente pediu produção imediata; o time decidiu não depender de acessos e decisões das clientes para destravar o desenvolvimento, entregando o plano de produção como documento a validar.

**Data:** 27/08/2026 (reunião de entrega)
