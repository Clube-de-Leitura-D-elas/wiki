---
type: reuniao
title: Kickoff — Clube de Leitura D'elas
description: Reunião inaugural do projeto com definição de escopo, personas e próximos passos.
tags: [kickoff, governanca, produto]
status: ativo
timestamp: 2026-08-11
---

# Kickoff — Clube de Leitura D'elas

Reunião de abertura do projeto, realizada em **11 de agosto de 2024**.

Resumo gerado por IA com base apenas na transcrição. Leve com um grão de sal.

## Participantes

| Nome                                 | Papel                                                         |
| ------------------------------------ | ------------------------------------------------------------- |
| Claudine                             | Fundadora e gestora do Clube D'elas                           |
| Simone                               | Conselheira e coordenadora                                    |
| Carolina                             | Conselheira e coordenadora                                    |
| Josiane                              | Coordenadora (Grupo 31 — Zona Sul), ponte técnica (TI/SERPRO) |
| Bruno, Daniel, Davi, Natan, Teixeira | Equipe de desenvolvimento (alunos PUC)                        |

## O Clube D'elas

- Fundado em **maio de 2023**
- **42 grupos** ativos (agosto/2024), ~**1000 mulheres** participantes
- Objetivo: resgatar o hábito da **leitura no público feminino**, de forma voluntária e sem fins lucrativos
- Grupos **presenciais**, ~30–40 integrantes cada
- Cada integrante indica **1 livro** (ficção/literatura). O livro é sorteado na reunião e a pessoa que o indicou vira **anfitriã** do próximo encontro
- Intervalo entre encontros: **30–45 dias**
- Crescimento orgânico via Instagram (~5.000 seguidores), sem investimento em anúncios
- Em processo de formalização como **fundação**

## Dores e problemas identificados

### 1. Comunicação fragmentada

Tudo roda em WhatsApp: grupos por clube, grupo de coordenadoras, grupo de gestão. Listas de confirmação são copiadas manualmente (umas por cima das outras). Informações se perdem com facilidade.

### 2. Inscrições desconectadas

Candidatas preenchem **Google Forms** → dados caem numa planilha → equipe de apoio repassa contatos manualmente para coordenadoras. Quem cuida das inscrições não é a coordenadora; a comunicação é indireta e gera retrabalho.

### 3. Agenda trabalhosa e frágil

- Mantida no **Canva**, centralizada na Claudine
- Coordenadoras não preenchem; ela precisa cobrar **uma por uma**
- Instagram não permite editar um post fixo com datas que mudam
- Oportunidades perdidas com **editoras e autoras** que consultam a agenda e encontram dados incompletos

### 4. Sorteio manual

Hoje: papelzinho ou número de WhatsApp. Livros já sorteados precisam ser excluídos manualmente. Só participam as presentes, mas isso nem sempre é registrado de forma confiável.

### 5. Pós-encontro sem padrão

Fotos, textos e marcações para Instagram dependem de cobrança manual da Claudine. Não há lembrete automático para a anfitriã. A divulgação é inconsistente entre grupos.

### 6. Falta de histórico estruturado

- Coordenadoras mantêm planilhas manuais de presença
- Não há registro consolidado de encontros por grupo
- Participantes podem ficar meses ou anos sem ir a encontro e ninguém percebe
- Não há avaliação dos livros lidos

## Personas identificadas

| Persona                            | Descrição                                                                                     | Necessidades-chave                                                                      |
| ---------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **Candidata**                      | Descobre o clube pelo Instagram, preenche formulário, aguarda vaga                            | Inscrição simples, sem obrigação de baixar app antes de ser aceita                      |
| **Leitora**                        | Participa de 1+ grupos, indica livro, confirma presença, pode ser sorteada como anfitriã      | Ver livros do grupo, confirmar presença, indicar/trocar livro, consultar agenda         |
| **Coordenadora**                   | Ponto focal do grupo, impulsiona sorteio, cobra anfitriã, gerencia comunicação                | Gerenciar lista do grupo, sortear livro, registrar presença (check-in), delegar funções |
| **Anfitriã** _(status temporário)_ | Leitora cujo livro foi sorteado; organiza aquele encontro específico                          | Informar data/local, receber confirmações, receber lembrete de tarefas pós-encontro     |
| **Gestão**                         | Claudine + equipe de apoio: abertura de grupos, aprovação de coordenadoras, Instagram, agenda | Visão global de todos os grupos, agenda unificada, aprovação de novos grupos            |

> **Sobreposição:** leitora, coordenadora e anfitriã coexistem na mesma pessoa física. Uma mulher pode ser leitora em 3 grupos, coordenadora em 1, e anfitriã em outro — tudo ao mesmo tempo.

## Decisões de escopo e arquitetura

### App nativo mobile (Android + iOS)

- Inicialmente considerou-se **web responsivo**, mas a família da Claudine (área de TI) argumentou que app nativo é mais prático para o usuário final
- **Decisão:** aplicativo mobile com distribuição via Google Play e App Store
- Para funcionalidades de gestão mais pesadas, um perfil com acesso expandido dentro do mesmo app atende — sem necessidade de uma segunda plataforma no MVP

### MVP: foco em leitora + coordenadora

- A gestão pode continuar operando com as ferramentas atuais no curto prazo
- O MVP cobre o **miolo**: leitora e coordenadora
- Gestoras acessam as mesmas funcionalidades mas com **permissões ampliadas** (ex.: visão de todos os grupos)
- Candidata continua entrando via Instagram/Forms; ao ser aprovada, recebe token/link para ativar conta no app (**evitar duplo cadastro**)

### Funcionalidades planejadas para o MVP

1. **Cadastro e autenticação** — com carga inicial a partir dos dados existentes (planilhas + censo)
2. **Indicação de livros** — cada leitora indica 1 livro por grupo; pode trocar enquanto não sorteado
3. **Sorteio** — automático, apenas com as presentes (check-in), excluindo livros já lidos no grupo
4. **Agenda integrada** — calendário de encontros por grupo, alimentada pela anfitriã/coordenadora
5. **Confirmação de presença** — para o próximo encontro
6. **Check-in presencial** — QR Code escaneado pela coordenadora no dia do encontro
7. **Lembretes e notificações** — tarefas pós-encontro para anfitriã (fotos, texto, dados do próximo livro)
8. **Histórico do grupo** — encontros passados, presenças, livros lidos

### Ideias para evolução futura (pós-MVP)

- Perfil de **editora/autor**: notificação automática quando livro da editora for sorteado
- **Avaliação dos livros** (estrelas)
- **Mensagem de aniversário** automática
- **Link de compra com afiliado** Amazon (monetização para o clube)
- **Loja de produtos** do clube (bolsas, etc.)

## Regras de negócio relevantes

- Grupos são de **ficção/literatura**; existem grupos temáticos (política, clássicos, filosofia)
- Encontros são **presenciais** — havendo demanda para grupos online, isso seria tratado separadamente
- Livro já sorteado **não volta** ao sorteio daquele grupo
- Enquanto o livro da pessoa não foi sorteado, ela pode **trocar** a indicação
- O sorteio é feito **apenas entre as presentes** na reunião
- A anfitriã que não puder organizar deve avisar previamente e sai do sorteio (exceção)
- Participantes que faltam **3 encontros consecutivos** podem ser desligadas do grupo
- As tarefas pós-encontro da anfitriã são: informar livro sorteado + data + local do próximo encontro, e encaminhar fotos e texto para divulgação no Instagram
- Coordenadora pode **delegar** função de check-in/sorteio para outra leitora se não puder comparecer

## Custos previstos

| Item                     | Valor                   |
| ------------------------ | ----------------------- |
| Google Play (publicação) | **USD 25** (taxa única) |
| Apple App Store (anual)  | **USD 100** (por ano)   |

O clube pretende arcar com os custos via fundação e parcerias (Amazon Afiliados, editoras).

## Próximos passos

1. **Equipe de desenvolvimento**: criar protótipo navegável no **Figma** + jornada do usuário
2. **Próxima reunião**: **27 de agosto de 2024** — validação do protótipo com as stakeholders
3. **Sugestão da Josiane**: incluir desenho de jornada do usuário junto com o protótipo para facilitar a validação das funcionalidades cobertas pelo MVP

## Arquivos relacionados

- [Gravação da reunião (Opus)](./kickoff.opus) — Áudio completo (~1h05)
- [Transcrição](./transcricao.txt) — Registro textual da conversa
