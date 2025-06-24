---
title: Regras de decisão
description: Saiba como trabalhar com regras de decisão
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: ebefeb59a19e831ec7f86cee690a35fe71e14554
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 20%

---

# Regras de decisão {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Criar regras de decisão"
>abstract="As regras de decisão permitem definir o público-alvo dos itens de decisão aplicando restrições diretamente no nível do item de decisão ou em uma estratégia de seleção específica. Isso permite controlar com precisão quais itens devem ser apresentados a quem."

## Sobre as regras de decisão {#about}

As regras de decisão permitem definir o público-alvo dos itens de decisão aplicando restrições diretamente no nível do item de decisão ou em uma estratégia de seleção específica. Isso permite controlar com precisão quais itens devem ser apresentados a quem.

Por exemplo, vamos considerar um cenário onde você tem itens de decisão com produtos relacionados a Yoga projetados para mulheres. Com as regras de decisão, é possível especificar que esses itens só devem ser exibidos para perfis cujo gênero seja &quot;Feminino&quot; e que tenham indicado um &quot;Ponto de interesse&quot; em &quot;Yoga&quot;.

>[!NOTE]
>
>Além das regras de decisão em nível de estratégia de seleção e item, você também pode definir o público-alvo desejado no nível da campanha. [Saiba mais](../campaigns/create-campaign.md#audience)

A lista de regras de decisão está acessível no menu **[!UICONTROL Configuração de estratégia]**.

![](assets/decision-rules-list.png)

## Criar uma regra de decisão {#create}

Para criar uma regra de decisão, siga estas etapas:

1. Navegue até **[!UICONTROL Configuração da estratégia]** / **[!UICONTROL Regras de decisão]** e clique no botão **[!UICONTROL Criar regra]**.

   >[!NOTE]
   >
   >Você também pode usar dados do Adobe Experience Platform para enriquecer sua lógica de decisão com dados externos. Isso é especialmente útil para atributos que mudam com frequência, como disponibilidade de produtos ou preços em tempo real. Esse recurso está atualmente disponível para todos os clientes como uma versão beta pública. Entre em contato com o representante de sua conta se desejar obter acesso. [Saiba como usar dados do Adobe Experience Platform para a tomada de decisão](../experience-decisioning/aep-data-exd.md)

1. A tela de criação de regras de decisão é aberta. Nomeie a regra e forneça uma descrição.

1. Crie a regra de decisão para atender às suas necessidades usando o Construtor de segmentos do Adobe Experience Platform. Para fazer isso, você pode aproveitar várias fontes de dados, como:
   * Atributos de item de perfil e decisão,
   * Públicos-alvo,
   * Dados de contexto provenientes do Adobe Experience Platform. [Saiba como aproveitar os dados de contexto](context-data.md)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >O Construtor de segmentos fornecido para criar regras de decisão apresenta algumas especificidades em comparação à usada com o serviço de Segmentação do Adobe Experience Platform. No entanto, o processo global descrito na documentação ainda é válido para criar regras de decisões. [Saiba como criar definições de segmento](../audience/creating-a-segment-definition.md)

1. À medida que você adiciona e configura novos campos no espaço de trabalho, o painel **[!UICONTROL Propriedades de público-alvo]** exibe informações sobre os perfis estimados pertencentes ao público-alvo. Clique em **[!UICONTROL Atualizar estimativa]** para atualizar os dados.

   >[!NOTE]
   >
   >As estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto.

1. Quando a regra de decisão estiver pronta, clique em **[!UICONTROL Salvar]**. A regra criada aparece na lista e está disponível para uso em itens de decisão e estratégias de seleção para controlar a apresentação de itens de decisão para perfis.

   >[!NOTE]
   >
   >A profundidade do aninhamento em uma regra de elegibilidade é limitada a 30 níveis. Isso é medido pela contagem dos parênteses de fechamento `)` na cadeia de caracteres do PQL. Uma sequência de regras pode ter até 15 KB para caracteres codificados em UTF-8. É equivalente a 15.000 caracteres ASCII (1 byte cada) ou 3.750-7.500 caracteres não ASCII (2-4 bytes cada). [Saiba mais sobre as medidas de proteção e limitações da decisão](gs-experience-decisioning.md#guardrails)
