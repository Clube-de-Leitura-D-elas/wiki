---
type: spec
title: Épicos do MVP
description: Escopo do MVP em onze épicos, com objetivo, o que cada um abrange e o que não abrange.
tags: [mvp, epicos, escopo]
status: ativo
timestamp: 2026-08-27
---

# Épicos do MVP

Baseado no [Termo de Abertura](../materiais/termo-de-abertura.md) e no [kickoff de 11/08](../materiais/kickoff/), refinado na Sprint 0 e ajustado após a [reunião de entrega de 27/08](../materiais/entrega-sprint-0/index.md). As decisões que sustentam este escopo estão registradas em [Decisões da Sprint 0](./decisoes-sprint-0.md); as em aberto, em [Decisões pendentes](./decisoes-pendentes.md).

## Direção do MVP

O MVP prioriza o funcionamento operacional dos encontros para **leitoras e coordenadoras**, reduzindo a dependência de listas e cobranças manuais no WhatsApp.

A gestão terá um painel web próprio para o trabalho administrativo, construído em duas fases: primeiro a manutenção de grupos e participantes, depois a visão consolidada do clube (épico 10). O fluxo de entrada de novas participantes — quem ainda não é do clube — pode continuar, inicialmente, no Instagram e Google Forms, seguido de ativação da conta no aplicativo; leitoras já ativas podem buscar outros grupos e solicitar entrada pelo próprio aplicativo (épico 11).

### Ciclo principal contemplado

> A leitora acessa seus grupos, indica um livro, acompanha e confirma presença no encontro. A coordenação registra a presença efetiva, realiza o sorteio e define a próxima anfitriã. Depois do encontro, as pendências e informações do próximo encontro ficam registradas.

## Épicos prioritários

### 1. Acesso e perfis

**Objetivo:** permitir que participantes já aprovadas ativem e acessem sua conta no aplicativo, mantendo uma identidade única mesmo que participem de vários grupos.

**Abrange:**

- fluxo único de entrada: splash, tela de login com foco em login social (Google/Apple) e botão dedicado para inserir o código de ativação;
- ativação e vínculo da identidade social aos dados da inscrição pelo código;
- entrada apenas com o código, email e senha, para quem não usa provedor social;
- perfil básico da participante e edição dos próprios dados;
- indicação de dados pendentes na primeira entrada;
- identificação das permissões da usuária.

**Não abrange:** inscrição aberta e aprovação de candidatas; o painel de gestão é tratado no épico 10.

### 2. Grupos

**Objetivo:** organizar os grupos de leitura, as participantes e as responsabilidades de coordenação que contextualizam os demais fluxos.

**Abrange:**

- lista de grupos dos quais a leitora participa;
- página do grupo com participantes, coordenadoras, próximo encontro e resumo do histórico;
- vínculo de uma participante a um ou mais grupos;
- atribuição de coordenadora por grupo;
- permissões operacionais da coordenadora naquele grupo.

**Não abrange:** criação e encerramento de grupos (ficam no painel de gestão) e descoberta pública de grupos; a descoberta entre leitoras ativas é tratada no épico 11.

### 3. Indicação de livros

**Objetivo:** substituir a lista manual de indicações e preparar um sorteio confiável.

**Abrange:**

- uma indicação ativa por leitora em cada grupo;
- cadastro e consulta de livros indicados no grupo;
- alteração da indicação enquanto ela não tiver sido sorteada;
- registro de livros já sorteados/lidos no grupo;
- bloqueio de livros já lidos no sorteio daquele grupo;
- estado visível para a leitora sobre a sua indicação;
- busca com separação clara entre os livros recomendados pelo clube e os resultados da API pública;
- consulta, em leitura, à lista de livros recomendados pelo clube.

**Não abrange:** catálogo editorial completo, links afiliados, recomendações automatizadas; manutenção da lista de recomendados no aplicativo (a curadoria é da gestão, pelo painel — épico 10); a avaliação de livros lidos é tratada no épico 9.

### 4. Encontros

**Objetivo:** centralizar a agenda dos grupos e tornar visíveis as informações necessárias para participação em cada encontro.

**Abrange:**

- visualização do próximo encontro por grupo;
- agenda com os encontros dos grupos em que a leitora participa e, com dados limitados (grupo, data, livro), os encontros dos demais grupos do clube;
- informações do encontro: grupo, livro, anfitriã, data, horário, local e observações;
- criação e edição das informações por pessoas autorizadas;
- confirmação de presença para o próximo encontro, com cancelamento possível até o prazo do encontro — padrão de 48 horas, configurável pela anfitriã ou coordenadora na criação;
- visão das confirmações pela coordenação e anfitriã;
- consulta de encontros anteriores.

**Não abrange:** solicitação de visita ou participação num encontro de outro grupo pelo aplicativo (fluxo escopado no backlog, pendente de decisão — ver [Decisões pendentes](./decisoes-pendentes.md)); agenda pública para quem não é do clube; controle de vagas; integração com calendários externos.

### 5. Lista de presença

**Objetivo:** registrar quem efetivamente compareceu, separando confirmação prévia de presença real e dando base confiável para o sorteio e o histórico.

**Abrange:**

- lista de participantes do grupo no dia do encontro;
- registro manual de presença pela coordenadora ou pela anfitriã daquele encontro;
- distinção entre quem confirmou e quem compareceu;
- histórico de presença por encontro e por leitora;
- delegação temporária da operação do encontro para outra leitora, quando a coordenadora estiver ausente;
- base para acompanhamento de ausências consecutivas.

**Não abrange:** QR Code na primeira versão, desligamento automático por faltas ou tratamento detalhado de justificativas.

### 6. Sorteio

**Objetivo:** realizar o sorteio de forma transparente, aplicando as regras do clube e registrando seu resultado.

**Abrange:**

- sorteio apenas entre participantes com presença efetivamente registrada;
- exclusão automática de livros já sorteados no grupo;
- possibilidade de a coordenadora retirar, antes do sorteio, uma participante que avisou não poder assumir como anfitriã;
- registro da leitora e do livro sorteados;
- definição da anfitriã temporária do próximo encontro;
- criação do próximo encontro em rascunho, aguardando as demais informações;
- histórico de sorteios.

**Não abrange:** votação, pesos de probabilidade, sorteio remoto assíncrono ou integração de compra de livros.

### 7. Pós-encontro

**Objetivo:** registrar o resultado do encontro e acompanhar as pendências necessárias para que o próximo aconteça de forma organizada.

**Abrange:**

- tarefas associadas à anfitriã do próximo encontro;
- preenchimento e confirmação de data, local e informações do próximo encontro;
- checklist de pendências, como foto do convite do encontro (pré), fotos do encontro (pós) e texto;
- download das fotos do encontro, para reaproveitamento na divulgação;
- visibilidade das pendências para anfitriã, coordenação e gestão autorizada;
- histórico consolidado de encontro, presença, livro discutido, livro seguinte e anfitriã seguinte.

**Não abrange:** editor de posts, publicação automática no Instagram, geração ou otimização de legenda pronta para post (futuro) ou gestão sofisticada de fotos.

### 8. Notificações

**Objetivo:** reduzir cobranças manuais e lembrar cada pessoa das ações relevantes no ciclo do encontro.

**Abrange:**

- avisos dentro do aplicativo;
- lembretes de encontro próximo e confirmação de presença;
- avisos de pendência de data ou local;
- lembretes de tarefas da anfitriã;
- aviso do resultado do sorteio e de alterações relevantes no encontro;
- estado de leitura das notificações.

**Restrição de modelagem:** os gatilhos de notificação devem suportar, desde o início do desenvolvimento, tanto push quanto avisos no aplicativo; o mix final de canais pode ser definido depois, sem retrabalho.

### 9. Avaliação de livros

**Objetivo:** permitir que a leitora registre o que achou do livro lido, transformando o histórico do grupo em memória viva em vez de só uma lista de títulos.

**Abrange:**

- avaliação do livro discutido, com nota e comentário, por leitora;
- uma avaliação por leitora em cada livro lido no grupo, editável enquanto a janela estiver aberta;
- visualização das avaliações do grupo sobre um livro lido;
- nota consolidada do livro no grupo;
- avaliação vinculada ao encontro em que o livro foi discutido, alimentando o histórico.

**Não abrange:** avaliação de livros ainda não lidos pelo grupo; avaliação por quem não participa do grupo; nota pública entre grupos diferentes; moderação de comentários; ranking de livros do clube.

### 10. Dashboard web de gestão

**Objetivo:** dar à gestão um painel web, fora do app Flutter, para o trabalho administrativo que não faz sentido num celular — manter grupos e participantes e enxergar o clube inteiro num lugar só.

**Abrange:**

- aplicação web separada do app mobile, com autenticação restrita a perfis de gestão;
- dashboard com indicadores e gráficos do clube e cartões de pendência operacional;
- calendário com os encontros de todos os grupos, filtrável por grupo e por cidade;
- grupos: criar, editar, listar, ver detalhes e encerrar;
- participantes: listar, ver detalhes, editar, conceder ou revogar acesso ao painel, inativar num grupo — status ativo/inativo que preserva o histórico; inativação não abre vaga —, remover quando necessário e decidir solicitações de entrada;
- livros recomendados: manutenção da lista curada pelo clube, que o aplicativo expõe em leitura;
- configurações: parâmetros de funcionamento do clube;
- consulta ao histórico de um grupo a partir do painel.

**Não abrange:** inscrição de quem ainda não é do clube (continua no formulário externo operado pela cliente; é distinto da solicitação de entrada em grupo, feita por quem já é do clube e decidida aqui); operação do encontro, que é da coordenadora dentro do app (registro de presença, sorteio e tarefas da anfitriã); avaliação de livros, que acontece no app; edição de conteúdo produzido pelas leitoras, como indicações e avaliações.

### 11. Descoberta e entrada em grupos

**Objetivo:** permitir que uma leitora já ativa no aplicativo encontre outros grupos do clube e peça para participar, com a decisão sendo tomada pela gestão.

**Abrange:**

- busca e consulta de grupos existentes pela leitora;
- solicitação de entrada num grupo;
- acompanhamento do status da própria solicitação;
- aprovação ou recusa da solicitação pela gestão, dentro do módulo Participantes do painel web;
- vínculo criado automaticamente quando a solicitação é aprovada.

**Não abrange:** inscrição de quem ainda não é do clube (continua no formulário externo); entrada automática sem aprovação; convite de leitora para leitora; aprovação das solicitações pela coordenadora do grupo dentro do aplicativo (hoje a aprovação é da gestão no painel; mudança em discussão — ver [Decisões pendentes](./decisoes-pendentes.md)).

## Relação entre os épicos

```text
Acesso e perfis
        ↓
      Grupos  ←──  Descoberta e entrada em grupos
      ↙     ↘
Indicação     Encontros
 de livros        ↓
            Lista de presença
               ↓
            Sorteio
               ↓
          Pós-encontro ──→  Avaliação de livros
               ↓
        Próximo encontro

Notificações atravessam todo o fluxo.
O Dashboard de gestão mantém a base (grupos e participantes)
e dá à gestão a visão do clube inteiro.
```

## Épicos de menor prioridade

### Inscrição de novas participantes

Fluxo para quem ainda não é do clube manifestar interesse e se candidatar, incluindo formulário, lista de espera, aprovação e convite de ativação. Permanece no Instagram e Google Forms. É distinto da descoberta de grupos entre leitoras já ativas, que é o épico 11.

A migração das participantes existentes (~1.000 pessoas, a partir da planilha fornecida pela gestão) e o disparo em massa dos códigos de ativação são uma **operação única**, a executar quando o aplicativo estiver em condições de uso — não é funcionalidade do MVP. A mesma planilha alimenta o seed inicial da Sprint 1.

### Sugerir a criação de um novo grupo

Fluxo para manifestar demanda em uma região, cidade ou tema e, eventualmente, candidatar-se à coordenação. É distinto da inscrição em um grupo já existente e depende de avaliação da gestão.

### Rede social

Funcionalidades de comunidade, como mural, perfis públicos, interações entre participantes e comunicação transversal entre grupos. Por ser um produto amplo em si, fica fora do núcleo operacional inicial; WhatsApp e Instagram continuam atendendo essa necessidade no curto prazo.
