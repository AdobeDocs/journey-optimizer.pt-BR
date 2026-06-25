---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a perfis no Journey Optimizer
description: Saiba como criar e gerenciar perfis no Adobe Journey Optimizer
feature: Profiles
role: User
level: Beginner
exl-id: be3936e4-8185-4031-9daf-95eea58077d0
TQID: https://experienceleague.adobe.com/QpLGV-y5qbtmksC-99GU5PtaV-mUA-imew8JDj7-weA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: c6441f0097a75690c0546e492c39c6bb59711a16
workflow-type: tm+mt
source-wordcount: 778
ht-degree: 24%

---

# Introdução a perfis {#profiles-gs}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como o Perfil de Cliente em Tempo Real no Adobe Journey Optimizer unifica os dados do cliente de fontes online, offline e de terceiros em uma única exibição e como acessar o painel de perfis.

>[!ENDSHADEBOX]

## Sobre perfis

Aproveite o Perfil do cliente em tempo real no [!DNL Adobe Journey Optimizer] para ter uma visão holística de cada cliente individual ao combinar dados de vários canais, incluindo online, offline, CRM e de terceiros. **Perfis** permitem consolidar os dados do cliente em uma visualização unificada, oferecendo uma conta acionável com carimbo de data e hora de cada interação com o cliente.

➡️ [Conheça este recurso no vídeo](#video)

**Perfil do Cliente em Tempo Real&#x200B;** - Integre atributos do cliente e eventos de fontes online, offline e de pseudônimos em um único perfil unificado. &#x200B;Use o perfil para envolver os clientes com experiências personalizadas em tempo real em vários pontos de contato. &#x200B;

**Assimilação de dados** - Conecte-se a várias fontes de dados para assimilar dados comportamentais, transacionais, financeiros e operacionais. Assimile dados em tempo real ou por meio de uploads em lote para manter os perfis atualizados constantemente. Os perfis não são criados diretamente na interface [!DNL Journey Optimizer] — eles são criados ou atualizados automaticamente no Adobe Experience Platform quando os dados são assimilados.

>[!NOTE]
>
>Ao assimilar dados, os emails fazem distinção entre maiúsculas e minúsculas. Isso significa que perfis duplicados podem ser criados (por exemplo, um perfil para John.Greene@luma.com, outro perfil para john.greene@luma.com) e usados ao direcionar o destinatário correspondente em suas jornadas e campanhas do [!DNL Journey Optimizer].

**Gráfico de identidade** - Combine dados de diferentes fontes usando identidades de clientes, como IDs de fidelidade ou IDs de sistema de CRM. &#x200B;Crie uma visualização abrangente do cliente, mapeando os relacionamentos entre diferentes identidades nos conjuntos de dados de uma marca. &#x200B;

**Envolvimento do cliente** - Use o perfil do cliente em tempo real para fornecer experiências contextuais e personalizadas, como ofertas e mensagens direcionadas. &#x200B;Envolva os clientes em vários canais, incluindo campanhas de marketing, suporte ao cliente e atualizações transacionais. &#x200B;

**Compartilhamento de dados** - Compartilhe perfis de clientes com os principais provedores de armazenamento na nuvem, como Amazon Web Services, Microsoft Azure e Google Cloud. Use perfis compartilhados para emissão de relatórios, arquivamento de dados ou análise mais profunda com ferramentas de business intelligence.

## Perfis ativáveis e uso de licença {#engageable-profiles}

Um **Perfil Engajável** é um registro de informações que representam um indivíduo armazenado no Serviço de Perfil e envolvido por jornadas ou campanhas. É a métrica de licença principal para [!DNL Adobe Journey Optimizer].

Principais características:

* **Janela contínua de 12 meses**: a contagem reflete perfis exclusivos que você tentou ativar nos últimos 12 meses usando os recursos de criação, decisão, entrega, experimentação ou orquestração do Journey Optimizer.
* **Contado uma vez por sandbox**: um perfil que insere várias jornadas ou campanhas em uma sandbox conta como um único Perfil Acionável para essa sandbox.
* **Com base em seu Público-alvo endereçável**: perfis envolventes são calculados a partir de seu Público-alvo endereçável. A contagem representa o público-alvo engajado nos últimos 12 meses usando qualquer um dos recursos do Journey Optimizer, de seu Público-alvo endereçável total.
* **Comportamento da métrica**: a contagem de perfis ativáveis:
   * Pode aumentar quando novos perfis são envolvidos por meio de jornadas ou campanhas
   * Não pode diminuir a menos que não haja engajamento com determinados perfis por mais de 12 meses
   * Pode diminuir quando perfis com pseudônimos são compilados em perfis conhecidos

>[!TIP]
>
>Ao direcionar perfis pseudônimos (visitantes não autenticados) com canais de entrada, como experiências na Web, no aplicativo ou experiências baseadas em código, considere definir um Tempo de vida (TTL) para exclusão automática de perfil para gerenciar a contagem de Perfis acionáveis e os custos associados. [Saiba mais sobre as medidas de proteção do canal de entrada](../start/guardrails.md#profile-management-inbound)

Monitore a contagem de Perfis Ativáveis da sua organização a qualquer momento em **[!UICONTROL Administração]** > **[!UICONTROL Uso da Licença]**. Se você observar um pico repentino na contagem, consulte a [seção Solução de problemas](license-usage.md#troubleshooting-engageable-profiles) para obter orientação detalhada. [Saiba mais sobre o painel de Uso da Licença](license-usage.md)

>[!MORELIKETHIS]
>
>* [Introdução à gestão de dados no Journey Optimizer](../data/gs-data.md)
>* [Documentação de Perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=pt-BR){target="_blank"}
>* [Medidas de proteção padrão para dados e segmentação do Perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"}
>* &#x200B;[Documentação de assimilação de dados](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home){target="_blank"}

## Painel de perfis

Para acessar perfis, navegue até o menu **[!UICONTROL Cliente]** / **[!UICONTROL Perfis]** no painel de navegação esquerdo.

>[!NOTE]
>
>Se sua organização for nova no [!DNL Adobe Journey Optimizer] e ainda não tem conjuntos de dados de Perfil ativos ou políticas de mesclagem criadas, o painel **Perfis** não está visível. Em vez disso, a guia **Visão geral** exibe links para a documentação da Adobe Experience Platform para ajudar você a começar a usar o Perfil do cliente em tempo real. Para saber como trabalhar com o **painel de Perfil** e obter informações detalhadas sobre as métricas exibidas no painel, consulte [esta seção](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR){target="_blank"}.

É possível reunir fragmentos de dados de várias fontes e combiná-los para obter uma visualização completa de cada cliente individual. Ao reunir esses dados, as políticas de mesclagem são as regras usadas para determinar como os dados são priorizados e quais dados são combinados para criar a exibição unificada. Saiba mais sobre **Políticas de mesclagem** nesta [documentação](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=pt-BR){target="_blank"}.

![](assets/profiles-home.png)

## Vídeo tutorial {#video}

Saiba como a Adobe Experience Platform monta e atualiza Perfis de clientes em tempo real e como você pode acessar e usar esses perfis.

>[!VIDEO](https://video.tv.adobe.com/v/27251?quality=12)
