---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com atributos computados
description: Saiba como trabalhar com atributos computados.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: d87f33c80cc85b1d1a87150687f6d7c9a268a016
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 1%

---

# Trabalhar com atributos computados {#computed-attributes}

Os atributos computados resumem eventos comportamentais individuais em atributos de perfil computados disponíveis no Adobe Experience Platform. Esses atributos são baseados em conjuntos de dados de Evento de experiência ativados por perfil assimilados na Adobe Experience Platform e servem como pontos de dados agregados armazenados em perfis de clientes.

Cada atributo calculado é um atributo de perfil que você pode aproveitar para segmentação, personalização e ativação em jornadas e campanhas. Essa simplificação melhora a capacidade de fornecer experiências personalizadas oportunas e significativas aos seus clientes.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Para acessar atributos computados, verifique se você tem as permissões apropriadas (**Exibir atributos computados** e **Gerenciar atributos computados**).

## Criar atributos computados {#manage}

Para criar atributos computados, navegue até a guia **[!UICONTROL Atributos computados]** no menu **[!UICONTROL Perfis]**, localizado no lado esquerdo.

Nessa tela, você pode construir atributos calculados criando regras que combinam atributos de evento, funções agregadas, juntamente com um período de pesquisa especificado. Por exemplo, você pode calcular a soma das compras feitas nos últimos três meses, identificar o item mais recente visualizado por um perfil que não fez uma compra na última semana ou calcular o total de pontos de premiação acumulados por cada perfil.

![](assets/computed-attributes.png)

Quando a regra estiver pronta, publique o atributo computado para disponibilizá-lo em outros serviços downstream, incluindo o Journey Optimizer.

Informações detalhadas sobre a criação e o gerenciamento de atributos computados estão disponíveis na [documentação sobre atributos computados](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=pt-BR)

## Adicionar atributos calculados à fonte de dados do Adobe Experience Platform {#source}

Para aproveitar os atributos computados no Journey Optimizer, adicione-os à fonte de dados do Journey Optimizer **Experience Platform**.

A fonte de dados do Adobe Experience Platform define a conexão com o Perfil do cliente em tempo real da Adobe. Essa fonte de dados recupera dados do Perfil e dados de Eventos de experiência do Serviço de perfil do cliente em tempo real.

Para adicionar atributos calculados à origem de dados, siga estas etapas:

1. Navegue até o menu esquerdo **[!UICONTROL Configurações]** e clique no cartão **[!UICONTROL Fontes de dados]**.

1. Selecione a fonte de dados **[!UICONTROL Experience Platform]**.

   ![](assets/computed-attributes-add.png)

1. Adicione o grupo de campos **[!UICONTROL SystemComputedAttributes]** contendo todos os atributos computados criados.

   ![](assets/computed-attributes-fieldgroup.png)

Os atributos computados agora estão disponíveis para uso no Journey Optimizer. [Saiba como usar atributos computados no Journey Optimizer](#use)

Informações detalhadas sobre a adição de grupos de campos à fonte de dados do Adobe Experience Platform estão disponíveis em [esta seção](../datasource/adobe-experience-platform-data-source.md).

## Usar atributos computados no Journey Optimizer {#use}

>[!NOTE]
>
>Antes de iniciar, verifique se você adicionou os atributos calculados à fonte de dados do Adobe Experience Platform. [Saiba mais nesta seção](#source).

Os atributos computados fornecem recursos versáteis dentro da Journey Optimizer. Use-os para várias finalidades, como personalizar o conteúdo da mensagem, criar novos públicos ou dividir jornadas com base em um atributo calculado específico. Por exemplo, divida o caminho de uma jornada com base no total de compras de um perfil nas últimas três semanas adicionando um único atributo calculado em uma atividade de Condição. Você também pode personalizar um email exibindo o item visualizado mais recentemente para cada perfil.

Como os atributos computados são campos de atributo de perfil criados no esquema de união de perfis, acesse-os do editor de personalização no grupo de campos **SystemComputedAttributes**. A partir daí, adicione atributos calculados em suas expressões, tratando-os como qualquer outro atributo de perfil para executar as operações desejadas.

![](assets/computed-attributes-ajo.png)
