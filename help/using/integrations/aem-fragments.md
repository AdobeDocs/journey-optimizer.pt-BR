---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de conteúdo do AEM
description: Saiba como acessar e gerenciar fragmentos de conteúdo do AEM
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: d9f2dbd5433ec9a89b4ef5a6d1caf6ff81c90a81
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# Trabalhar com fragmentos de conteúdo do Adobe Experience Manager {#aem-fragments}

A integração entre o Adobe Experience Manager e o Journey Optimizer segue esse fluxo de dados:

1. **[Criar e criar](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**: o conteúdo é criado e configurado no Adobe Experience Manager como Fragmentos de Conteúdo.

1. **[Marcação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**: os fragmentos de conteúdo devem ser marcados com a marca específica da Journey Optimizer (`ajo-enabled:{OrgId}/{SandboxName}`).

1. **[Publicar](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**: os fragmentos de conteúdo são publicados no Adobe Experience Manager, tornando-os disponíveis para o Journey Optimizer.

1. **[Acesso](#aem-add)**: o Journey Optimizer busca e exibe os Fragmentos de conteúdo disponíveis da instância de publicação do Adobe Experience Manager em tempo real.

1. **[Integração](#aem-add)**: os Fragmentos de conteúdo são selecionados e integrados em campanhas ou jornadas.

Quando um fragmento de conteúdo é publicado no Adobe Experience Manager, um evento é enviado para atualizar o conteúdo no lado do Journey Optimizer. Se a atualização for bem-sucedida, o Fragmento de conteúdo ficará disponível em aproximadamente 5 minutos para jornadas unitárias e no próximo lote de processamento para casos de uso em lote. Quando a atualização estiver disponível no Journey Optimizer, o conteúdo publicado mais recente será usado em todas as campanhas e jornadas aplicáveis.

## Criar e atribuir uma tag no Experience Manager

Antes de usar o fragmento de conteúdo no Journey Optimizer, é necessário criar uma tag especificamente para o Journey Optimizer:

1. Acesse seu ambiente **Experience Manager**.

1. No menu **Ferramentas**, selecione **Marcação**.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Clique em **Criar Marca**.

1. Verifique se a ID segue a seguinte sintaxe: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Clique em **Criar**.

1. Defina seu Modelo de fragmento de conteúdo conforme detalhado na [documentação do Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} e atribua a tag do Journey Optimizer recém-criada.

Essa conexão em tempo real garante que o conteúdo esteja sempre atualizado, mas também significa que quaisquer alterações nos fragmentos publicados afetarão imediatamente as campanhas e jornadas ativas.

Agora você pode começar a criar e configurar o fragmento de conteúdo para uso posterior no Journey Optimizer. Saiba mais em [documentação do Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Adicionar fragmentos de conteúdo do Experience Manager {#aem-add}

Depois de criar e personalizar os fragmentos de conteúdo do AEM, você pode importá-los para a campanha ou jornada do otimizador de Jornadas.

1. Crie sua [Campanha](../campaigns/create-campaign.md) ou [Jornada](../building-journeys/journey-gs.md).

1. Para acessar o fragmento de conteúdo do AEM, clique no ![ícone do Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) em qualquer campo de texto ou abra o código-fonte por meio de um componente de conteúdo do HTML.

   ![](assets/aem_campaign_2.png)

1. No menu **[!UICONTROL Fragmento de Conteúdo do AEM]** no painel esquerdo, clique em **[!UICONTROL Abrir seletor de CF do AEM]**.

   ![](assets/aem_campaign_3.png)

1. Selecione um **[!UICONTROL Fragmento de conteúdo]** na lista disponível para importar para o conteúdo do Journey Optimizer.

1. Clique em **[!UICONTROL Mostrar filtros]** para ajustar a lista de Fragmentos de conteúdo.

   Por padrão, o filtro de Fragmento de conteúdo é predefinido para exibir somente conteúdo aprovado.

   ![](assets/aem_campaign_4.png)

1. Depois de selecionar seu **[!UICONTROL Fragmento do conteúdo]**, clique em **[!UICONTROL Selecionar]** para abri-lo.

   ![](assets/aem_campaign_5.png)

1. Clique em **[!UICONTROL Exibir fragmento]** para exibir as informações do fragmento. Observe que abrir o menu **[!UICONTROL Informações do fragmento]** coloca o editor no modo somente leitura.

   Selecione **[!UICONTROL Visualizar]** no menu à direita para exibir seu fragmento no Adobe Experience Manager.

   ![](assets/aem_campaign_7.png)

1. Clique no ícone ![Mais ações](assets/do-not-localize/Smock_MoreSmallList_18_N.svg) para acessar o menu avançado do Fragmento:

   * **[!UICONTROL Trocar fragmento]**
   * **[!UICONTROL Explorar referências]**
   * **[!UICONTROL Abrir no AEM]**

   ![](assets/aem_campaign_8.png)

1. Escolha os campos desejados em seu **[!UICONTROL Fragmento]** para adicionar ao conteúdo.
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Para habilitar a personalização em tempo real, todos os espaços reservados usados em um **[!UICONTROL Fragmento de conteúdo]** devem ser declarados explicitamente pelo usuário como parâmetros na marca auxiliar do fragmento. Você pode mapear esses espaços reservados para atributos de perfil, atributos contextuais, cadeias de caracteres estáticas ou variáveis predefinidas usando os seguintes métodos:

   1. **Mapeamento de Perfil ou de Atributo Contextual**: atribua o espaço reservado a um perfil ou atributo contextual, por exemplo: name = profile.person.name.firstName.

   1. **Mapeamento de Cadeia de Caracteres Estática**: atribua um valor de cadeia de caracteres fixo colocando-o entre aspas duplas; por exemplo: name = &quot;John&quot;.

   1. **Mapeamento de Variáveis**: faça referência a uma variável declarada anteriormente na mesma HTML, por exemplo, name = &#39;variableName&#39;.
Nesse caso, verifique se **_variableName_** está declarado antes de adicionar a ID do fragmento, usando a seguinte sintaxe:

      ```html
      {% let variableName = attribute name %} 
      ```

   No exemplo abaixo, o espaço reservado **_name_** é mapeado para o atributo **_profile.person.name.firstName_** dentro do fragmento.

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**. Agora você pode testar e verificar o conteúdo da sua mensagem conforme detalhado em [esta seção](../content-management/preview.md).
Depois de executar os testes e validar o conteúdo, você pode [enviar a campanha](../campaigns/review-activate-campaign.md) ou [publicar a jornada](../building-journeys/publish-journey.md) para o público-alvo.

O Adobe Experience Manager permite identificar as campanhas ou jornadas do Journey Optimizer em que um fragmento de conteúdo está sendo usado. Saiba mais em [documentação do Adobe Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references).

