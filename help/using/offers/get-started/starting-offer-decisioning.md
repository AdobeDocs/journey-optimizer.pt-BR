---
title: Introdução ao Gerenciamento de decisões
description: Saiba como o Adobe Journey Otimizer pode ajudar você a enviar aos clientes a oferta certa na hora certa
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Sobre o Gerenciamento de decisões {#about-decision-management}

Use [!DNL Journey Optimizer] para oferecer a melhor oferta e experiência aos clientes em todos os pontos de contato na hora certa. Depois de projetado, direcione seus públicos-alvo com ofertas personalizadas.

O gerenciamento de decisões facilita a personalização com uma biblioteca central de ofertas de marketing e um mecanismo de decisão que aplica regras e restrições a perfis ricos e em tempo real criados pela Adobe Experience Platform para ajudar você a enviar aos clientes a oferta certa na hora certa.

A capacidade de gerenciamento de decisões consiste em dois componentes principais:

* O **Biblioteca de ofertas centralizada** que é a interface onde você cria e gerencia os diferentes elementos que compõem suas ofertas e define suas regras e restrições.
* O **Mecanismo de decisão da oferta** O que aproveita os dados da Adobe Experience Platform e os perfis do cliente em tempo real, juntamente com a Biblioteca de ofertas, para selecionar o momento certo, os clientes e os canais para os quais as ofertas serão entregues.

![](../assets/architecture.png)

Os benefícios incluem:

* Melhor desempenho da campanha fornecendo ofertas personalizadas em vários canais,
* Fluxos de trabalho aprimorados: em vez de criar várias entregas ou campanhas, as equipes de marketing podem melhorar os fluxos de trabalho criando um único delivery e variar as ofertas em diferentes partes do template,
* Controle o número de vezes que uma oferta é exibida em campanhas e clientes.

➡️ [Saiba mais sobre o Gerenciamento de decisões nesses vídeos](#video)


>[!NOTE]
>
>Se você for um [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target=&quot;_blank&quot;} usuário aproveitando a variável **Offer Decisioning** serviço de aplicativos, todos os recursos de Gerenciamento de decisões descritos nesta seção também se aplicam a você.

## Sobre ofertas e decisões {#about-offers-and-decisions}

Um **Oferta** O é composto de conteúdo, regras de elegibilidade e restrições que definem as condições em que é apresentado aos clientes.

Ele é criado usando o **Biblioteca de ofertas**, que fornece um catálogo de ofertas central, onde você pode associar regras e restrições de elegibilidade a vários conteúdos para criar e publicar ofertas (consulte [Interface do usuário da Biblioteca de ofertas](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Depois que a Biblioteca de ofertas tiver sido enriquecida com ofertas, você poderá integrar suas ofertas em **decisões**.

As decisões são contêineres para suas ofertas que aproveitarão o Mecanismo de decisão da oferta para escolher a melhor oferta a ser entregue, dependendo do target do delivery.

## Casos de uso comuns {#common-use-cases}

Os recursos de gerenciamento de decisões e a integração com a Adobe Experience Platform permitem cobrir vários casos de uso para ajudá-lo a aumentar a participação e a conversão dos clientes.

* Exiba em seu site as ofertas da página inicial que corresponderão ao ponto de interesse do cliente visitante, com base nos dados da Adobe Experience Platform.

   ![](../assets/website.png)

* Se os clientes se aproximarem de uma de suas lojas, enviem notificações por push lembrando as ofertas disponíveis de acordo com seus atributos (nível de fidelidade, gênero, compras anteriores...).

   ![](../assets/push_sample.png)

* O Gerenciamento de decisões também ajuda você a aprimorar a experiência dos clientes ao entrar em contato com a equipe de suporte. As APIs de gerenciamento de decisão permitem exibir no portal de agentes da central de atendimento informações sobre as melhores ofertas resgatadas e as melhores ofertas do cliente.

   ![](../../assets/do-not-localize/call-center.png)

## Conceder acesso ao gerenciamento de decisões {#granting-acess-to-decision-management}

As permissões para acessar e usar os recursos de decisão são gerenciadas com o [Adobe Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Para conceder acesso à funcionalidade de Gerenciamento de decisões, é necessário criar um **[!UICONTROL Product profile]** e atribuir as permissões correspondentes aos usuários. Saiba mais sobre como gerenciar [!DNL Journey Optimizer] usuários e permissões em [esta seção](../../administration/permissions.md).

As permissões específicas do Gerenciamento de decisões estão listadas em [esta seção](../../administration/high-low-permissions.md#decisions-permissions).

## Glossário {#glossary}

Você pode encontrar abaixo a lista dos principais conceitos com os quais você trabalhará ao usar o Gerenciamento de decisões.

* **Limitação** ou **Limite de frequência**: A limitação é usada como uma restrição para definir quantas vezes uma oferta é apresentada. Há dois tipos de limites, quantas vezes uma oferta pode ser proposta em todo o público-alvo combinado, também conhecido como &quot;Total limites&quot; e quantas vezes uma oferta pode ser proposta ao mesmo usuário final, também conhecido como &quot;Limite de perfil&quot;.

* **Coleções**: Coleções são subconjuntos de ofertas com base em condições predefinidas definidas por um profissional de marketing, como a categoria da oferta.

* **Decisão**: Uma decisão contém a lógica que informa a seleção de uma oferta.

* **Regra de decisão**: As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a qualificação.

* **Oferta elegível**: Uma oferta qualificada atende às restrições definidas upstream que podem ser oferecidas de forma consistente a um perfil.

* **Gerenciamento de decisões**: Permite criar e fornecer experiências de ofertas personalizadas de usuários finais em canais e aplicativos usando lógica de negócios e regras de decisão.

* **Ofertas de fallback**: Uma oferta de fallback é a oferta padrão exibida quando um usuário final não está qualificado para nenhuma das ofertas personalizadas na coleção.

* **Oferta**: Uma oferta é uma mensagem de marketing que pode ter regras associadas a ela que especificam quem está qualificado para ver a oferta.

* **Biblioteca de ofertas**: A biblioteca de ofertas é uma biblioteca central usada para gerenciar ofertas personalizadas e de fallback, regras de decisão e decisões.

* **Ofertas personalizadas**: Uma oferta personalizada é uma mensagem de marketing personalizável com base em regras e restrições de elegibilidade.

* **Posicionamentos**: Uma disposição é o local e ou contexto em que uma oferta é exibida para um usuário final.

* **Prioridade**: A prioridade é usada para classificar ofertas que atendem a todas as restrições, como qualificação, calendário e limite.

* **Representações**: Uma representação são informações usadas por um canal, como localização ou idioma para exibir uma oferta.

## Vídeos tutoriais{#video}

>[!NOTE]
>
>Esses vídeos se aplicam ao serviço de aplicativo Offer Decisioning criado na Adobe Experience Platform e não são específicos de [!DNL Adobe Journey Optimizer]. No entanto, fornecem orientações genéricas para utilizar a gestão de decisões no contexto da [!DNL Journey Optimizer].

### O que é o Gerenciamento de decisões? {#what-is-offer-decisioning}

O vídeo abaixo apresenta os principais recursos, arquitetura e casos de uso do Gerenciamento de decisão:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Definir e gerenciar ofertas {#use-offer-decisioning}

O vídeo abaixo mostra como usar o Gerenciamento de decisões para definir e gerenciar suas ofertas e aproveitar os dados do cliente em tempo real.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


