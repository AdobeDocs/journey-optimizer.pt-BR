---
solution: Journey Optimizer
product: journey optimizer
title: Crie sua Targeting dimension
description: Saiba como mapear um esquema relacional para o perfil do cliente
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: 0b92d0e806c47b0d87ba53b7c7f1d56ee4453abb
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# Configurar uma Targeting dimension {#configuration}

Com as **[!UICONTROL Campanhas orquestradas]**, você pode projetar e fornecer comunicações direcionadas no nível da entidade, aproveitando os recursos de esquema relacional da Adobe Experience Platform. A Experience Platform usa esquemas para descrever a estrutura dos dados de forma consistente e reutilizável. Quando os dados são assimilados na Experience Platform, eles são estruturados de acordo com um esquema XDM.

Embora a segmentação de **[!UICONTROL Campanhas orquestradas]** funcione principalmente em esquemas relacionais, a entrega de mensagens real sempre ocorre no nível **Perfil**.

Ao configurar o direcionamento, você define dois aspectos principais:

* **Esquemas de Tabela de Destino**

  Você especifica quais esquemas relacionais são elegíveis para o direcionamento. Por padrão, o esquema chamado `Recipient` é usado, mas você pode configurar alternativas como `Visitors`, `Customers`, etc.

  >[!IMPORTANT]
  >
  > O esquema de destino deve ter uma relação 1:1 com o esquema `Profile`. Por exemplo, você não pode usar `Purchases` como esquema de destino, pois ele geralmente representa uma relação um para muitos.

* **Vinculação de perfis**

  O sistema deve entender como o esquema de destino mapeia para o esquema `Profile`. Isso é feito por meio de um campo de identidade compartilhado — um que existe tanto no esquema de destino quanto no esquema `Profile` e está configurado como um namespace de identidade.

## Crie sua Targeting dimension {#targeting-dimension}

Comece configurando a orquestração de campanhas, mapeando um esquema relacional para o perfil do cliente.

1. Em **[!UICONTROL Administration]**, acesse o menu **[!UICONTROL Configurations]** e selecione **[!UICONTROL Campaign Target Dimension]**.

   ![](assets/target-dimension-1.png)

1. Clique em **[!UICONTROL Criar]** para começar a criar sua **[!UICONTROL Targeting dimension]**.

1. Escolha seu [Esquema](gs-schemas.md) configurado anteriormente &#x200B;no menu suspenso.

   Embora todos os esquemas relacionais estejam visíveis, somente os esquemas com uma relação de identidade direta com o **Perfil** estão qualificados para seleção.

1. Selecione o **[!UICONTROL Valor de identidade]** que representa a entidade que você deseja direcionar.

   Neste exemplo, o perfil do cliente está vinculado a várias assinaturas, cada uma representada por um único `crmID` no esquema `Recipient`. Ao configurar o **[!UICONTROL Dimension de Destino]** para usar o esquema `Recipient` e sua identidade `crmID`, você poderá enviar mensagens no nível de assinatura, em vez de no perfil principal do cliente, garantindo que cada contrato ou linha receba sua própria mensagem personalizada.

   [Saiba mais na documentação da Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Clique em **[!UICONTROL Salvar]** para concluir a instalação. Observe que uma vez criada, uma **[!UICONTROL Dimensão de destino]** não pode ser removida nem editada.

Após configurar o **[!UICONTROL Dimension de Destino]**, prossiga para criar e configurar sua **[!UICONTROL Configuração de Canal]** e defina os **[!UICONTROL Detalhes de Execução]** correspondentes.