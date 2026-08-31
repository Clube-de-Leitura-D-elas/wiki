---
type: spec
title: Roadmap 2026/2
description: Épicos e histórias de usuário do MVP distribuídos da Sprint 1 à Sprint 4, com entrega final em 18/11/2026.
tags: [roadmap, sprints, mvp]
status: ativo
timestamp: 2026-08-27
---

# Roadmap 2026/2

Distribuição dos [épicos do MVP](./epicos-mvp.md) pelas sprints de desenvolvimento, da Sprint 1 (início em 27/08/2026) à Sprint 4, encerrando na entrega final de 18/11/2026. A Sprint 0 — planejamento, mockup no Figma e validação com as clientes — correu de 11/08 a 27/08/2026; as decisões dela estão registradas em [Decisões da Sprint 0](./decisoes-sprint-0.md).

Ajustado após a [reunião de entrega de 27/08](../materiais/entrega-sprint-0/index.md): login social como fluxo primário, agenda com encontros de todos os grupos, inativação de participantes, janela de cancelamento de presença, lista de livros recomendados e deploy em produção postergado (ambiente de teste com contas do time até a validação do plano de produção).

Organização: **sprint → épico (funcionalidade) → histórias de usuário**.

## Princípios da divisão

- **Cada sprint entrega uma dor resolvida**, demonstrável na entrega: a Sprint 1 dá identidade à leitora no app; a Sprint 2 mata a lista de indicações e a cobrança de presença no WhatsApp; a Sprint 3 mata a planilha do sorteio e fecha o ciclo do encontro; a Sprint 4 dá memória, avisos e a visão do clube inteiro.
- **O ciclo dos encontros tem ponto de partida manual:** a coordenadora cria o primeiro encontro; a partir daí o app conduz (confirmação → presença → sorteio → próximo encontro em rascunho). Assim, as interdependências entre indicações, encontros, presença, sorteio e pós-encontro viram sequência de construção, não círculo.
- **Duas frentes de produto** — app Flutter e painel web de gestão — consomem o mesmo backend: contratos de API definidos desde a Sprint 1 para as frentes não divergirem.
- **Válvulas de escape nomeadas:** se uma sprint apertar, o time sabe exatamente o que pode deslizar sem quebrar a narrativa das entregas.

## Visão geral

| Épico | S1 | S2 | S3 | S4 |
| --- | --- | --- | --- | --- |
| 1. Acesso e perfis | completo | | | |
| 2. Grupos | essencial | enriquecimento | | |
| 3. Indicação de livros | | completo | | |
| 4. Encontros | | completo | | |
| 5. Lista de presença | | | completo | |
| 6. Sorteio | | | completo | |
| 7. Pós-encontro | | | essencial | fechamento |
| 8. Notificações | | | | completo |
| 9. Avaliação de livros | | | | completo |
| 10. Dashboard de gestão | fase 1 | | | fase 2 |
| 11. Descoberta e entrada | | | completo | |

---

## Sprint 1 — Fundações e espinha dorsal

**Período:** 27/08 → 14/09 · **Narrativa:** a leitora existe no app e a gestão mantém a base do clube.

**Épico 1 — Acesso e perfis**

- Como leitora aprovada, quero entrar com login social e inserir meu código de ativação, para acessar o aplicativo pela primeira vez.
- Como leitora, quero entrar apenas com meu código de ativação, para usar o aplicativo mesmo sem provedor social.
- Como leitora, quero visualizar e editar meus dados de perfil — com aviso de pendências na primeira entrada —, para completar meu cadastro.
- As permissões de cada usuária (leitora, coordenadora, gestão) devem ser identificadas no acesso e refletidas no que cada uma pode fazer.

**Épico 2 — Grupos (essencial)**

- Como leitora, quero ver e alternar entre os grupos dos quais participo, para acessar o contexto de cada um.
- Como leitora, quero ver a página do meu grupo com participantes e coordenadoras, para conhecer quem faz parte. *(A página ganha próximo encontro e indicações na Sprint 2, e histórico consolidado na Sprint 4.)*

**Épico 10 — Dashboard de gestão (fase 1: manutenção da base)**

- Como gestão, quero autenticar-me no painel web, com acesso restrito a perfis de gestão, para trabalhar com segurança.
- Como gestão, quero criar, editar e listar grupos, para manter a estrutura do clube.
- Como gestão, quero listar, ver detalhes e editar participantes — inclusive vincular a grupos, atribuir coordenadoras e remover de grupos —, para refletir a organização real do clube.
- Como gestão, quero conceder ou revogar acesso ao painel, para controlar quem administra.

**Fundação técnica**

- Repositórios, CI/CD e ambientes de **teste** das três frentes (app Flutter, painel web, backend/API), com contas próprias do time; o deploy em produção fica postergado até a validação, com as clientes, do documento de stack e fluxo de deploy elaborado pela AGES III.
- Contratos de API compartilhados entre app e painel definidos no início da sprint.
- Seed da carga inicial (grupos, participantes, coordenações e a lista inicial de livros recomendados, a partir da planilha fornecida pela gestão) na primeira semana, para destravar desenvolvimento e demo.

**Mínimo para funcionar (roteiro protegido da demo)**

1. Gestão entra no painel web e cadastra/edita um grupo e suas participantes.
2. Leitora entra com login social (ou código de ativação) e ativa o vínculo.
3. Leitora entra, vê seus grupos, alterna entre eles e abre a página de um grupo.

**Válvulas de escape**

- Reenvio de código de ativação em versão simples (sem fluxo elaborado de recuperação de conta).
- CRUD do painel sem firulas: criar, editar e listar; detalhes e refinamentos podem esperar.

---

## Sprint 2 — Coração operacional

**Período:** 14/09 → 30/09 · **Narrativa:** morre a lista de indicações e a cobrança de presença no WhatsApp.

**Épico 3 — Indicação de livros**

- Como leitora, quero cadastrar, consultar e alterar minha indicação de livro no grupo enquanto ela não for sorteada, para concorrer ao sorteio com o livro certo.
- Como sistema, livros já sorteados/lidos no grupo devem ficar registrados e bloqueados para nova indicação e novo sorteio naquele grupo. *(Regra decidida: leitora cujo livro foi sorteado não indica novamente naquele grupo.)*
- Como leitora, quero ver o estado da minha indicação (ativa, alterável, já sorteada, sem direito a nova indicação no grupo), para saber onde estou.

**Épico 4 — Encontros**

- Como coordenadora, quero criar e editar encontros do grupo com livro, anfitriã, data, horário, local e observações, para organizar a agenda. *(É o ponto de partida manual do ciclo.)*
- Como leitora, quero ver o próximo encontro do grupo e consultar encontros anteriores, para me planejar e relembrar.
- Como leitora, quero confirmar presença no próximo encontro — cancelável até o prazo do encontro (padrão de 48 horas, configurável na criação) —, para avisar a coordenação.
- Como coordenadora ou anfitriã, quero ver quem confirmou presença, para organizar o encontro.
- Como leitora, quero uma agenda com os encontros dos meus grupos e, com dados limitados, os encontros dos demais grupos do clube, para me planejar e conhecer outras rodas.

**Épico 10 — Dashboard de gestão (manutenção de livros recomendados)**

- Como gestão, quero manter a lista de livros recomendados pelo clube, para que o aplicativo a exponha em leitura.

**Enriquecimento da Sprint 1**

- Página do grupo ganha próximo encontro e indicações ativas.

**Roteiro de demo**

1. Coordenadora cria o encontro do mês (livro, data, local).
2. Leitora indica um livro e confirma presença.
3. Coordenadora vê quem confirmou.

**Válvulas de escape**

- Os encontros de demais grupos na agenda (dados limitados): podem deslizar para a Sprint 4; o essencial é a agenda dos grupos da própria leitora.

---

## Sprint 3 — Fechamento do ciclo

**Período:** 30/09 → 26/10 (a sprint mais longa) · **Narrativa:** morre a planilha do sorteio; o ciclo do encontro fecha ponta a ponta.

**Épico 5 — Lista de presença**

- Como coordenadora ou anfitriã do encontro, quero registrar a presença efetiva de cada participante no dia do encontro, para distinguir quem confirmou de quem compareceu.
- Como coordenadora, quero consultar o histórico de presença por encontro e por leitora, para acompanhar ausências consecutivas. *(Base para o alerta de três faltas.)*
- Como coordenadora ausente, quero delegar temporariamente a operação do encontro a outra leitora. *(válvula)*

**Épico 6 — Sorteio**

- Como coordenadora, quero sortear entre as participantes presentes — podendo retirar, antes, quem avisou que não pode assumir —, para escolher a próxima anfitriã e o próximo livro com transparência.
- Como sistema, o sorteio deve excluir automaticamente livros já sorteados no grupo.
- Como sistema, o resultado deve registrar leitora e livro sorteados e criar o próximo encontro em rascunho, aguardando data, horário e local.
- Como leitora, quero ver o resultado do sorteio, para saber quem será a próxima anfitriã e qual o próximo livro.

**Épico 7 — Pós-encontro (essencial)**

- Como anfitriã ou coordenadora, quero preencher e confirmar data, horário e local do próximo encontro em rascunho, para oficializá-lo.
- Como anfitriã, quero ver meu checklist de tarefas e pendências (foto do convite, divulgação, fotos, texto). *(válvula: pode deslizar para a Sprint 4)*
- Como coordenação ou gestão autorizada, quero ver as pendências do próximo encontro, para acompanhar o que falta.

**Épico 11 — Descoberta e entrada em grupos**

- Como leitora, quero buscar e consultar os grupos do clube, para conhecer outras rodas de leitura.
- Como leitora, quero solicitar entrada num grupo e acompanhar o status da minha solicitação, para saber se fui aprovada.
- Como gestão, quero aprovar ou recusar solicitações de entrada no módulo Participantes do painel, com o vínculo criado automaticamente na aprovação.

**Roteiro de demo**

1. Coordenadora abre a lista de presença e registra quem compareceu.
2. Coordenadora sorteia entre as presentes: leitora e livro sorteados, próximo encontro criado em rascunho.
3. Anfitriã preenche data e local: encontro oficializado.
4. Leitora busca outro grupo e solicita entrada; gestão aprova no painel; o vínculo nasce sozinho.

**Válvulas de escape**

- Delegação temporária da operação do encontro: pode deslizar para a Sprint 4.
- Checklist de pendências do pós-encontro: pode deslizar para a Sprint 4 (o essencial — rascunho + data/local — não desliza).

---

## Sprint 4 — Memória, visão e respiro

**Período:** 26/10 → 18/11 · **Narrativa:** o grupo ganha memória viva e a gestão enxerga o clube inteiro num lugar só.

**Épico 9 — Avaliação de livros** *(se a Sprint 3 sobrar capacidade, é o primeiro candidato a adiantar)*

- Como leitora, quero avaliar com nota e comentário o livro discutido no encontro, para registrar o que achei.
- Como leitora, quero editar minha avaliação enquanto a janela estiver aberta, para ajustar minha opinião.
- Como leitora, quero ver as avaliações do grupo sobre um livro lido e a nota consolidada, para reviver a memória do grupo.

**Épico 8 — Notificações** *(gatilhos modelados desde o início do desenvolvimento, para suportar o mix de canais que for validado)*

- Como leitora, quero receber avisos de encontro próximo, de confirmação de presença, de pendência de data ou local e do resultado do sorteio, para não depender de cobrança no WhatsApp.
- Como anfitriã, quero receber lembretes das minhas tarefas e pendências, para cumprir meu papel.
- Como leitora, quero acompanhar o estado de leitura das notificações, para saber o que já vi.

**Épico 7 — Pós-encontro (fechamento)**

- Checklist de pendências completo, com visibilidade para anfitriã, coordenação e gestão autorizada — incluindo download das fotos do encontro —, caso não tenha fechado na Sprint 3.

**Histórico consolidado**

- Como leitora, quero ver o histórico consolidado do grupo — encontros, presenças, livros, anfitriãs e avaliações —, para reviver a trajetória.

**Épico 10 — Dashboard de gestão (fase 2: visão do clube)**

- Como gestão, quero indicadores e gráficos do clube, para enxergar o todo.
- Como gestão, quero cartões de pendência operacional, para agir sobre o que está atrasado.
- Como gestão, quero um calendário com os encontros de todos os grupos, filtrável por grupo e cidade, para planejar.
- Como gestão, quero encerrar grupos, consultar o histórico de um grupo e configurar parâmetros do clube, para manter a organização.

**Buffer**

- Débitos técnicos, polimento de UX alinhado ao Figma e preparação da entrega final.

**Roteiro de demo**

1. Leitora avalia o livro do último encontro; o grupo vê a nota consolidada.
2. Notificações chegam: lembrete de encontro, pendência da anfitriã, resultado do sorteio.
3. Gestão abre o painel: indicadores, calendário, pendências — o clube inteiro num lugar só.
4. Histórico consolidado do grupo na tela.
