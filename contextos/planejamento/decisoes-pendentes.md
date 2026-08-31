---
type: guia
title: Decisões pendentes
description: Fila de decisões em aberto levantadas na reunião de entrega da Sprint 0, para deliberação do time e das clientes.
tags: [decisoes, pendencias, produto]
status: ativo
timestamp: 2026-08-27
---

# Decisões pendentes

Fila de decisões em aberto, levantadas na [reunião de entrega de 27/08](../materiais/entrega-sprint-0/index.md). Quando uma pendência é decidida, registra-se a decisão em [Decisões da Sprint 0](./decisoes-sprint-0.md) ou em documento de decisões posterior, e o item aqui é marcado como resolvido, com data e link.

## Para o time

Deliberação prevista na reunião de terça (01/09/2026).

### Coordenadora com acesso ao painel web

A Speaker J puxou com força ("seria interessantíssimo os coordenadores fazerem a gestão do próprio grupo, só do próprio grupo") e Claudine apoiou. O painel foi desenhado só para gestão (4 pessoas hoje); o app já cobre a operação da coordenadora dentro do grupo.

**Se aprovado:** o épico 10 ganha o papel de coordenadora com visão restrita ao próprio grupo — participantes, presenças e pendências —, sem criar grupos nem administrar o clube.

### Solicitação de participação ou visita pelo aplicativo

Contexto: há leitoras que visitam grupos alheios; hoje a visita é negociada por WhatsApp/Instagram. A agenda com encontros de todos os grupos (dados limitados) já está acordada; o que ficou de fora é o fluxo completo: leitora solicita visita a um encontro → coordenadora do grupo-alvo aprova → o local é liberado.

**Impacto se aprovado:** novo tipo de solicitação com aprovador diferente do épico 11 (coordenadora, no app, em vez de gestão no painel) e política de exposição do local do encontro. Escopo já levantado; decidir se entra no MVP e em qual sprint.

### Lista de espera por grupo

Hoje a gestão mantém colunas por região na planilha (São Paulo, Rio de Janeiro, Porto Alegre...). Pergunta da Claudine na reunião: o aplicativo modela fila de espera por grupo, além da fila geral de inscritas?

**Impacto se aprovado:** introduz noção de vagas/capacidade por grupo — hoje fora do escopo por decisão (inativação não abre vaga; abrir vaga é decisão da gestão).

### Terminologia da busca de livros

As clientes se confundiram entre os resultados da API pública e as listas do clube — que, no vocabulário delas, se dividem em "sugeridos" (lista geral mantida pela gestão) e "indicados" (livros que leitoras indicam a um grupo). A lista curada "recomendados pelo clube" já foi decidida; falta alinhar o vocabulário e a separação visual na busca.

### Indicação a partir da página do livro

No protótipo, o botão "indicar" na página de um livro lista todos os grupos da leitora. A Speaker J questionou ("tem que ser o grupo que tu tá"). Decidir: indicação apenas dentro do contexto do grupo, ou a partir do livro com escolha do grupo — validando livro já indicado/lido naquele grupo em ambos os casos.

### Ranking de melhores avaliados na busca

Sugerido na reunião (mostrar os melhores avaliados primeiro, alimentando posts do Instagram). Conflita com a exclusão atual do épico 9 (nota não é pública entre grupos). Decidir: ranking visível no aplicativo ou apenas dado de apoio para a gestão usar nas publicações.

## Para as clientes

### Gráficos do dashboard

A gestão vai pensar em quais indicadores e gráficos importam e responder no grupo do WhatsApp. Em aberto: o que o épico 10 (fase 2) mostra no dashboard.

## Ações relacionadas (não são decisões)

- Pedir à Claudine a planilha de participantes — insumo do seed da Sprint 1 e da migração futura.
- Atualizar o Figma do fluxo de login (splash → login social → "tenho um código") antes de fechar as user stories da Sprint 1.
- AGES III: elaborar o documento de stack e fluxo de deploy para validação com as clientes.
