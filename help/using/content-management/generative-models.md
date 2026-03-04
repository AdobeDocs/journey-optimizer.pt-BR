---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar marca
description: Saiba como criar e gerenciar modelos geradores
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 9ef6b02c-0a17-4b46-bcd3-8e922eef059a
source-git-commit: 7873c333cbe5002695a11d1edaaf9e15f74a6d3f
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Criar e gerenciar modelos geradores {#generative-models}

Expanda os recursos de criação de imagens de IA com modelos integrados, modelos personalizados de Firefly e provedores de geração de imagens de terceiros para atender às suas necessidades específicas e melhorar o alinhamento da marca.

Escolha o modelo certo para suas necessidades:

- O **[!UICONTROL Adobe model]**, desenvolvido pela Firefly Image Model 4, é fornecido imediatamente e está pronto para uso para geração imediata de imagem sem configuração adicional.
- O **[!UICONTROL Partner model]**, desenvolvido pelo Gemini 2.5 Flash, oferece recursos especializados para casos de uso específicos.
- **[!UICONTROL Os modelos personalizados]** são modelos específicos da marca treinados em seus próprios ativos e adicionados pela sua organização.

  Saiba mais sobre **[!UICONTROL Modelos personalizados]** em [Documentação do Adobe Firefly](https://helpx.adobe.com/br/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html)

Após a configuração, você pode selecionar qualquer um dos modelos geradores ao criar imagens em seu conteúdo. [Saiba mais sobre a geração de imagens](generative-image.md).

## Gerenciar modelos gerativos

Gerencie seus modelos geradores de um local centralizado. Exiba todos os modelos disponíveis, filtre e pesquise para encontrar modelos específicos e defina as configurações para suas marcas.

1. No menu **[!UICONTROL Marcas]**, selecione a guia **[!UICONTROL Modelos gerativos]**.

   ![](assets/gen-model-manage-1.png){zoomable="yes"}

1. Clique no ícone ![](assets/do-not-localize/Smock_Filter_18_N.svg) para acessar o menu de filtro. Filtrar modelos por **[!UICONTROL Tipo]** ou **[!UICONTROL Status]**.

   ![](assets/gen-model-manage-2.png){zoomable="yes"}

1. Use a barra de pesquisa para localizar um modelo generativo específico por nome.

1. Clique no ícone ![](assets/do-not-localize/Smock_More_18_N.svg) para acessar o menu avançado, no qual você pode habilitar, desabilitar ou excluir seu modelo.

   Observe que somente **[!UICONTROL Modelos personalizados]** podem ser excluídos.

   ![](assets/gen-model-manage-6.png){zoomable="yes"}

1. Clique em **[!UICONTROL Adicionar modelo]** para criar um novo modelo generativo do zero.

Agora é possível selecionar qualquer um dos modelos gerativos ao criar imagens em seu conteúdo. [Saiba mais sobre a geração de imagens](generative-image.md).

## Adicionar um modelo generativo

>[!IMPORTANT]
>
>A criação de modelos personalizados do Firefly requer um contrato do Firefly ETLA.

Os modelos personalizados do Firefly são modelos de IA específicos da marca treinados em seus próprios ativos, permitindo gerar imagens que se alinham precisamente à identidade, ao estilo e às diretrizes visuais da marca.

Ao criar provedores de modelos personalizados do Firefly, você pode expandir seus recursos de IA para além dos modelos padrão e garantir que o conteúdo gerado reflita de forma consistente a estética e os requisitos exclusivos de sua marca.

➡️ [Saiba como treinar seu modelo personalizado](https://helpx.adobe.com/br/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html)

1. No menu **[!UICONTROL Marcas]**, acesse a guia **[!UICONTROL Modelos Gerativos]** e clique em **[!UICONTROL Adicionar modelo]**.

   ![](assets/gen-model-manage-4.png){zoomable="yes"}

1. Insira um **[!UICONTROL Nome]** para seu modelo.

1. Insira sua **[!UICONTROL ID do Modelo]**.

   +++ Encontrar a ID do modelo do Firefly

   1. Acesse o site da Firefly e navegue até seus modelos treinados.
   1. Acesse o menu [Visualizar e testar](https://helpx.adobe.com/br/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html#preview-and-test).
   1. Na URL, localize o valor depois de `customModelId=`. Copie esse valor para usar como ID do modelo.

   Para obter mais informações, consulte a [documentação de modelos personalizados do Firefly](https://helpx.adobe.com/br/firefly/web/work-with-enterprise-features/train-custom-models/manage-custom-models.html).

   ![](assets/gen-model-manage-10.png){zoomable="yes"}

   +++

   </br>

   ![](assets/gen-model-manage-5.png){zoomable="yes"}

1. Opcionalmente, insira uma **[!UICONTROL Descrição]** para ajudar a identificar o modelo.

1. Clique em **[!UICONTROL Testar conexão]** para verificar a configuração do modelo.

1. Depois que o teste de conexão for bem-sucedido, clique em **[!UICONTROL Salvar]** para salvar sua configuração de modelo.

   ![](assets/gen-model-manage-7.png){zoomable="yes"}

1. Depois de salvar, o modelo personalizado é adicionado à lista de modelos. Você pode desativá-la ou excluí-la a qualquer momento.

   ![](assets/gen-model-manage-8.png){zoomable="yes"}

<!--
1. Once the connection test is successful, choose whether to enable the model for selected brands.

1. Enable or disable the option to connect the model to all brands.

    If disabled, select which brands this model should be applied to.
-->

Após a configuração, é possível selecionar qualquer um dos modelos gerativos personalizados ao criar imagens em seu conteúdo. [Saiba mais sobre a geração de imagens](generative-image.md).

![](assets/gen-model-manage-9.png){zoomable="yes"}
