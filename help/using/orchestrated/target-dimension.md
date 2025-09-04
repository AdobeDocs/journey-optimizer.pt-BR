---
solution: Journey Optimizer
product: journey optimizer
title: Crie sua Targeting dimension
description: Saiba como mapear um esquema relacional para o perfil do cliente
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

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

## Definir a configuração do canal {#channel-configuration}

Após configurar seu **[!UICONTROL Target Dimension]**, é necessário definir sua **[!UICONTROL Configuração de Canal]** de email ou SMS e definir os **[!UICONTROL Detalhes de Execução]** apropriados. Isso permite definir :

* **O nível de entrega de mensagens**: por exemplo, enviar uma mensagem por destinatário, como um único email por indivíduo.

* **O endereço de execução**: o campo de contato específico a ser usado para envio, como um endereço de email ou número de telefone.

Para definir a configuração do canal:

1. Comece criando e configurando sua **[!UICONTROL Configuração de canal]**.

   Você também pode atualizar uma **[!UICONTROL Configuração de canal]** existente.

   ➡️ [Siga as etapas detalhadas nesta página](../email/surface-personalization.md)

1. Na seção **[!UICONTROL Detalhes da execução]** da sua **[!UICONTROL Configuração do canal]**, acesse a guia **[!UICONTROL Campanhas orquestradas]**.

   ![](assets/target-dimension-3.png)

1. Clique em **[!UICONTROL Habilitado]** para torná-lo compatível com as campanhas Orquestradas.

1. Escolha seu método de delivery:

   * **[!UICONTROL Dimension de Destino]**: enviar para a entidade principal, por exemplo, destinatário.

   * **[!UICONTROL Target + Secondary Dimension]**: enviar usando entidades primárias e secundárias, por exemplo, recipient + contrato.

1. Selecione no menu suspenso seu [Dimension de Destino](#targeting-dimension) criado anteriormente.

   ![](assets/target-dimension-4.png)

1. Se você selecionou **[!UICONTROL Target + Secondary Dimension]** como método de entrega, escolha um **[!UICONTROL Secondary Dimension]** para definir o contexto de entrega de mensagem.

1. Na seção **[!UICONTROL Endereço de Execução]**, escolha qual **[!UICONTROL Source]** deve ser usada para buscar o endereço de entrega, como o endereço de email ou o número de telefone:

   * **[!UICONTROL Perfil]**: selecione essa opção se o endereço de entrega, por exemplo, email, for armazenado diretamente no perfil principal do cliente.

     Útil ao enviar mensagens ao cliente principal, não a uma entidade associada específica.

   * **[!UICONTROL Dimension de Destino]**: escolha essa opção se o endereço de entrega estiver armazenado na entidade primária, por exemplo, um destinatário.

     Útil quando cada recipient tem seu próprio endereço de entrega, como um email ou número de telefone diferente.

   * **[!UICONTROL Dimension Secundário]**: ao usar **[!UICONTROL Target + Dimension Secundário]** como método de entrega, selecione o **[!UICONTROL Dimension Secundário]** relevante que você configurou anteriormente.

     Por exemplo, se a dimensão secundária representar uma reserva ou assinatura, o endereço de execução, como um email, poderá ser retirado desse nível. Isso é útil nos casos em que os perfis usam um detalhe de contato diferente ao reservar ou assinar um serviço.

1. No campo **[!UICONTROL Endereço de entrega]**, clique em ![ícone de edição](assets/do-not-localize/edit.svg) para escolher o campo específico a ser usado para a entrega de mensagens.

   ![](assets/target-dimension-4.png)

1. Depois de configurado, clique em **[!UICONTROL Enviar]**.

Seu canal agora está pronto para uso com **Campanhas orquestradas** e as mensagens serão entregues de acordo com o target dimension selecionado.
