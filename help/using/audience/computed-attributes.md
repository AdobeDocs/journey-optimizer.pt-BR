---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com atributos computados
description: Saiba como trabalhar com atributos computados.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: 12449430f48153ebe3fbb30b782f51de4b11d4ef
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Trabalhar com atributos computados {#computed-attributes}

Os atributos computados permitem resumir eventos comportamentais individuais em atributos de perfil computados disponíveis no Adobe Experience Platform. Esses atributos calculados são baseados em conjuntos de dados de Evento de experiência ativados por perfil assimilados na Adobe Experience Platform e servem como pontos de dados agregados armazenados em perfis de clientes.

Cada atributo calculado é um atributo de perfil que você pode aproveitar para segmentação, personalização e ativação em jornadas e campanhas. Essa simplificação melhora a capacidade de fornecer experiências personalizadas oportunas e significativas aos seus clientes.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Para obter acesso a atributos computados, você precisa ter as permissões apropriadas (**Exibir atributos computados** e **Gerenciar atributos computados**).

## Criar atributos computados {#manage}

Para criar atributos computados, navegue até a guia **[!UICONTROL Atributos computados]** no menu **[!UICONTROL Perfis]**, localizado no lado esquerdo.

Nessa tela, você pode construir atributos calculados criando regras que combinam atributos de evento, funções agregadas, juntamente com um período de pesquisa especificado. Por exemplo, você pode calcular a soma das compras feitas nos últimos três meses, identificar o item mais recente visualizado por um perfil que não fez uma compra na última semana ou calcular o total de pontos de premiação acumulados por cada perfil.

![](assets/computed-attributes.png)

Quando a regra estiver pronta, publique o atributo computado para disponibilizá-lo em outros serviços downstream, incluindo o Journey Optimizer.

Informações detalhadas sobre como criar e gerenciar atributos computados estão disponíveis na [documentação sobre atributos computados](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=pt-BR)

## Adicionar atributos calculados à fonte de dados do Adobe Experience Platform {#source}

Para poder aproveitar os atributos computados no Journey Optimizer, primeiro é necessário adicioná-los à fonte de dados **Experience Platform** do Journey Optimizer.

A fonte de dados da Adobe Experience Platform define a conexão com o Real-Time Customer Profile. Essa fonte de dados foi projetada para recuperar dados de Perfil e dados de Eventos de experiência do Serviço de perfil do cliente em tempo real.

Para adicionar atributos calculados à origem de dados, siga estas etapas:

1. Navegue até o menu do lado esquerdo das **[!UICONTROL Configurações]** e clique no cartão **[!UICONTROL Fontes de dados]**.

1. Selecione a fonte de dados **[!UICONTROL Experience Platform]**.

   ![](assets/computed-attributes-add.png)

1. Adicione o grupo de campos **[!UICONTROL SystemComputedAttributes]** contendo todos os atributos computados criados.

   ![](assets/computed-attributes-fieldgroup.png)

Os atributos computados agora estão disponíveis para uso no Journey Optimizer. [Saiba como usar atributos computados no Journey Optimizer](#use)

Informações detalhadas sobre como adicionar grupos de campos à fonte de dados do Adobe Experience Platform estão disponíveis em [esta seção](../datasource/adobe-experience-platform-data-source.md).

## Usar atributos computados no Journey Optimizer {#use}

>[!NOTE]
>
>Antes de começar, verifique se você adicionou os atributos calculados à fonte de dados do Adobe Experience Platform. [Saiba mais nesta seção](#source).

Os atributos computados oferecem um conjunto versátil de recursos no Jornada otimizer. Você pode usá-los para várias finalidades, como personalizar o conteúdo da mensagem, criar novos públicos ou dividir jornadas com base em um atributo calculado específico. Por exemplo, você pode dividir o caminho de uma jornada com base no total de compras de um perfil nas últimas três semanas, adicionando um único atributo calculado em uma atividade de Condição. Você também pode personalizar um email exibindo o item visualizado mais recentemente para cada perfil.

Como os atributos computados são campos de atributo de perfil criados no esquema de união de perfis, você pode acessá-los no editor de personalização no grupo de campos **SystemComputedAttributes**. A partir daí, você pode adicionar atributos calculados em suas expressões, tratando-os como qualquer outro atributo de perfil para executar as operações desejadas.

![](assets/computed-attributes-ajo.png)
