---
solution: Journey Optimizer
product: journey optimizer
title: Guia de projeto integrado | ADOBE JOURNEY OPTIMIZER
description: Planeje e gerencie um projeto de integração do Adobe Journey Optimizer em funções de administrador, dados, desenvolvedor e profissional de marketing.
feature: Get Started
topic: Content Management
role: Admin
level: Intermediate
keywords: otimizador de jornada, integração, projeto de integração, implantação, plano de implementação, administrador, csm, parceiro de implementação, lista de verificação em fases
source-git-commit: 6a653e1dbb00f68ff689ea3e0dc0b15abda1e21e
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# Guia de projeto integrado {#onboarding-hub}

>[!BEGINSHADEBOX]

**Nesta página:** Planeje e coordene uma implantação completa do Adobe Journey Optimizer com uma lista de verificação em fases que abrange as funções de administrador, engenheiro de dados, desenvolvedor e profissional de marketing.

>[!ENDSHADEBOX]

Esta página é para **administradores do sistema e parceiros de implementação** que coordenam uma implantação completa do Journey Optimizer. Ela fornece uma lista de verificação em fases que abrange todas as funções, com links para os guias detalhados específicos da função.

>[!NOTE]
>
>Se você for um indivíduo iniciando com uma função específica, vá para [Introdução ao Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md).

## Fase 1 — Configuração do ambiente (Administrador) {#phase-1}

Conclua essas tarefas fundamentais primeiro para que as outras funções possam começar seu trabalho:

* [ ] Provisionar sandboxes (desenvolvimento, preparo, produção)
* [ ] Configurar funções e permissões de usuário no Adobe Admin Console
* [ ] Configurar perfis de produto e controle de acesso no nível do objeto
* [ ] Delegar subdomínios e configurar pools de IP
* [ ] Definir configurações de canal (email, SMS, push, web, no aplicativo, correspondência direta)
* [ ] Configurar listas de supressão e políticas de consentimento

➡️ Veja todos os detalhes: [Introdução para administradores](path/administrator.md)

## Fase 2 — Base de dados (engenheiro de dados) {#phase-2}

Crie a camada de dados que capacita perfis, públicos-alvo e acionadores de jornada:

* [ ] Definir namespaces de identidade
* [ ] Criar esquemas XDM (perfil, eventos de experiência, relacional)
* [ ] Configurar e habilitar conjuntos de dados para o Perfil de Cliente em Tempo Real
* [ ] Configurar a assimilação de dados (em lote e transmissão)
* [ ] Criar atributos computados
* [ ] Configurar fontes de dados e eventos do jornada

➡️ Veja todos os detalhes: [Introdução para engenheiros de dados](path/data-engineer.md)

## Fase 3 — Integrações técnicas (Desenvolvedor) {#phase-3}

Conecte seus aplicativos para que o jornada possa ser executado em dados em tempo real:

* [ ] Integrar o Mobile SDK (iOS/Android) com configuração por push
* [ ] Implementar o Web SDK para experiências da Web e push da Web
* [ ] Implementar o envio de eventos de aplicativos
* [ ] Criar pontos de extremidade de ação personalizados para integrações de sistema externas
* [ ] Validar usando o Adobe Experience Platform Assurance

➡️ Veja todos os detalhes: [Introdução para desenvolvedores](path/developer.md)

## Fase 4 — Primeiras experiências (profissional de marketing) {#phase-4}

Coloque a base para funcionar iniciando suas primeiras jornadas e campanhas:

* [ ] Criar a primeira audiência (definição de segmento ou carregamento CSV)
* [ ] Criar uma jornada de teste com ação de email
* [ ] Configurar modelos e fragmentos de conteúdo
* [ ] Publicar e monitorar uma campanha
* [ ] Revisar relatórios ao vivo

➡️ Veja todos os detalhes: [Introdução para profissionais de marketing](path/marketer.md)

## Lista de verificação de integração (imprimível) {#checklist}

| Fase | Proprietário | Status |
|-------|-------|--------|
| Configuração do ambiente | Administrador | |
| Base de dados | Engenheiro de dados | |
| Integrações técnicas | Desenvolvedor | |
| Primeiras experiências | Profissional de marketing | |

## Recursos relacionados {#related-resources}

* [Funções e responsabilidades](quick-start.md) — como as quatro funções funcionam juntas e a ordem de implementação recomendada.
* [Tutoriais do Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — vídeos passo a passo e apresentações guiadas para cada função.
* [Introdução ao gerenciamento de dados](../data/gs-data.md) — Como os dados são assimilados, unificados e ativados.
