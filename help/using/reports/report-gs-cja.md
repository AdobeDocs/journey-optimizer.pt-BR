---
solution: Journey Optimizer
product: journey optimizer
title: Experiência de relatório atualizada
description: Introdução ao relatório de tempo total
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bfd88d2a-e7b8-4e3b-85a1-4a14b0ba56dc
source-git-commit: a9349cedc4da2a8e76e53f9e2b5185270cda2558
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 32%

---

# Introdução ao relatório de tempo total {#channel-report-gs-cja}

>[!CONTEXTUALHELP]
>id="cja_connections_enable_cja"
>title="Habilitar o Customer Journey Analytics"
>abstract="Para analisar esse relatório no Customer Journey Analytics, entre em contato com a administração para verificar se sua organização adquiriu o Customer Journey Analytics e se a integração está configurada corretamente."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Customer Journey Analytics"

Os relatórios do Journey Optimizer vêm com uma interoperabilidade aprimorada com os recursos do Customer Journey Analytics, padronizando os relatórios em ambas as plataformas e melhorando a consistência e a confiabilidade dos dados. Essa integração perfeita entre o Journey Optimizer e o Customer Journey Analytics fornece uma visão mais clara das métricas de desempenho, permitindo que os usuários tomem decisões mais conscientes.

O acesso a esses recursos de relatórios depende do contexto e das áreas do produto:

* **Jornadas** - Se quiser direcionar uma ou mais jornadas no contexto de uma jornada, no menu **[!UICONTROL Jornadas]**, acesse sua jornada e clique no botão **[!UICONTROL Exibir relatório]**.

  Na lista de jornadas existentes, você também pode selecionar **[!UICONTROL Relatório]** no menu avançado da jornada selecionada. [Saiba mais sobre o relatório de Jornadas](journey-global-report-cja.md)

  ![](assets/gs-cja-report-3.png)

* **Campanhas** - Se quiser direcionar uma campanha, no menu **[!UICONTROL Campanhas]**, acesse sua campanha e clique no botão **[!UICONTROL Relatórios]** e depois **[!UICONTROL Exibir relatório de todos os tempos]**.

  Na lista de campanhas existentes, você também pode selecionar **[!UICONTROL Relatório]** no menu avançado da campanha selecionada. [Saiba mais sobre o relatório de Campanha](campaign-global-report-cja.md)

  ![](assets/gs-cja-report-2.png)

* **Global** - Se quiser direcionar métricas para todas as campanhas e jornadas do seu ambiente, acesse o relatório **Visão geral** navegando até o menu **[!UICONTROL Relatórios]** na seção **[!UICONTROL Gerenciamento de Jornadas]**. [Saiba mais sobre o relatório de Visão geral](channel-report-cja.md)

  ![](assets/gs-cja-report-1.png)

>[!IMPORTANT]
>
>Os relatórios no Adobe Journey Optimizer estão padronizados para UTC. A capacidade de personalizar o fuso horário dos relatórios será introduzida em uma versão futura.

## Pré-requisitos {#prerequisites}

* Se você tiver **não** o Customer Journey Analytics ou se for proprietário dele, mas **não** tiver acesso a qualquer perfil de produto do Customer Journey Analytics, as permissões serão gerenciadas no Journey Optimizer. Nesse caso, você precisa da permissão **[!UICONTROL Exibir relatórios de canal]** ou funções relacionadas. [Saiba mais](../administration/permissions.md)

* Se você **possui** o Customer Journey Analytics e tem acesso a um perfil de produto do Customer Journey Analytics, é necessário:

   * Permissões de **[!UICONTROL Criação de público]** e **[!UICONTROL Exibição de público]** para o Customer Journey Analytics. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/technotes/access-control){target="_blank"}

   * Permissão **[!UICONTROL Gerenciar perfis]** para o Adobe Journey Optimizer. [Saiba mais](../administration/permissions.md)

* Suas exibições de dados do Customer Journey Analytics precisam ser configuradas com a seguinte configuração: **Definir como exibição de dados padrão no Adobe Journey Optimizer**. [Saiba mais sobre visualizações de dados](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}


## Todos os relatórios de tempo por canal

Relatórios globais o tempo todo estão disponíveis para todos os seus canais. Selecione o relatório do canal que precisa para obter mais detalhes.

### Canais de saída

Selecione um canal de saída para descobrir os **relatórios globais contínuos** associados.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="email" src="../channels/assets/do-not-localize/email.png">
<div align="center"><p><strong>Canal de email</strong></p><p><a href="campaign-global-report-cja-email.md"><strong>Relatório de campanha</strong></a></p><p><a href="journey-global-report-cja-email.md"><strong>Relatório de jornada</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><p><strong>Canal de SMS</strong></p><p><a href="campaign-global-report-cja-sms.md"><strong>Relatório de campanha</strong></a></p><p><a href="journey-global-report-cja-sms.md"><strong>Relatório de jornada</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-push.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><p><strong>Canal de push</strong></p><p><a href="campaign-global-report-cja-push.md"><strong>Relatório de campanha</strong></a></p><p><a href="journey-global-report-cja-push.md"><strong>Relatório de jornada</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-direct.md"><img alt="Correspondência direta" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><p><strong>Canal de correspondência direta</strong></p><p><a href="campaign-global-report-cja-direct.md"><strong>Relatório de campanha</strong></a></p><p><a href="journey-global-report-cja-direct.md"><strong>Relatório de jornada</strong></a></p></div></td>
</tr></table>

### Experiências de entrada

Selecione uma experiência de entrada para descobrir os **relatórios globais de todos os tempos** associados.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="No aplicativo" src="../channels/assets/do-not-localize/inapp.jpg">
<div align="center"><p><strong>Canal no aplicativo</strong></p><p><a href="campaign-global-report-cja-inapp.md"><strong>Relatório de campanha</strong></a></p><p><a href="journey-global-report-cja-inapp.md"><strong>Relatório de jornada</strong></a></p></div></td>
<td><p><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></p>
<div align="center"><p><strong>Canal da web</strong></p><p><a href="campaign-global-report-cja-web.md"><strong>Relatório de campanha</strong></a></p><p><a href="journey-global-report-cja-web.md"><strong>Relatório de jornada</strong></a></p></div></td>
<td><img alt="Experiência baseada em código" src="../channels/assets/do-not-localize/code.png">
<div align="center"><p><strong>Experiências baseadas em código</strong></p><p><a href="campaign-global-report-cja-code.md"><strong>Relatório de campanha</strong></a></p><p><a href="campaign-global-report-cja-code.md"><strong>Relatório de jornada</strong></a></p></div></td>
<td><img alt="Cartões de conteúdo" src="../channels/assets/do-not-localize/cards.png">
<div align="center"><p><strong>Cartões de conteúdo</strong></p><p><a href="campaign-global-report-cja-content.md"><strong>Relatório de campanha</strong></a></p><p><a href="journey-global-report-cja-content.md"><strong>Relatório de jornada</strong></a></p></div></td>
</tr></table>

## Vídeo tutorial{#video}

O vídeo abaixo mostra como usar os relatórios aprimorados do Journey Optimizer com o Customer Journey Analytics.

>[!VIDEO](https://video.tv.adobe.com/v/3443156?captions=por_br)