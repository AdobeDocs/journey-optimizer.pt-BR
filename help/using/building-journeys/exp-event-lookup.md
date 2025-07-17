---
solution: Journey Optimizer
product: journey optimizer
title: Pesquisa de eventos de experiência no jornada
description: Saiba como usar a pesquisa de Eventos de experiência no jornada
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
source-git-commit: a587b8754e94781b7735f3d7d5abb9b9767a74a5
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 5%

---

# Pesquisa de evento de experiência no jornada {#ee-journeys}

>[!CAUTION]
>
>A partir de 8 de julho de 2025, em novas organizações de clientes, a criação de expressões usando eventos de experiência não será mais suportada no editor de expressão usado em condições de jornada. Como resultado, os eventos de experiência na [fonte de dados da Experience Platform](../datasource/adobe-experience-platform-data-source.md) não poderão ser usados para criar expressões. Abordagens alternativas e práticas recomendadas para criar expressões/lógica com eventos de experiência são referenciadas abaixo.
>
>Precisa de mais detalhes? [Leia as perguntas frequentes](#faq-ee).

Esta página descreve padrões comuns e abordagens escaláveis para ajudá-lo a aproveitar ao máximo os eventos de experiência no Adobe Journey Optimizer. Esses casos de uso são projetados para ajudar você a resolver desafios frequentes, como gerenciar recusas, controlar a frequência da mensagem, personalizar o conteúdo com base no comportamento do usuário e reagir a sinais em tempo real.

Ao utilizar essas estratégias, é possível transformar dados comportamentais em ações significativas — suprimindo, qualificando ou excluindo perfis com base nos eventos acionados ou nos atributos transportados. Quer você esteja criando lógica para limites de compra, acionadores de abandono ou lidando com rejeições, esses exemplos oferecem orientação prática que você pode adaptar às suas necessidades.

Ao avaliar qual abordagem se encaixa melhor, considere os requisitos de latência do seu caso de uso para garantir que suas jornadas permaneçam responsivas e eficazes.

## Supressão de recusa

Para suprimir perfis que recusaram comunicações de marketing, use o gerenciamento de consentimento integrado. As preferências de recusa são capturadas automaticamente nos campos de consentimento do perfil; elas podem ser referenciadas diretamente nas condições de jornada e são aplicadas automaticamente pelo Journey Optimizer durante a entrega da mensagem.

Saiba mais:

* [Gerenciar consentimento](../privacy/opt-out.md)
* [Gerenciamento de opção de não participação de email](../email/email-opt-out.md)
* [Gerenciamento de recusa para mensagens de texto](../sms/sms-opt-out.md)


## Supressão baseada em rejeição

Para excluir perfis que tiveram rejeições de email, use a lista de supressão automática do Adobe Journey Optimizer para endereços rejeitados. Esse mecanismo integrado garante que emails inválidos ou inacessíveis sejam excluídos de envios futuros sem exigir lógica personalizada.

Saiba mais:

* [Gerenciar a lista de supressão](../configuration/manage-suppression-list.md)


## Supressão genérica

Para suprimir perfis que demonstraram determinados comportamentos, use públicos-alvo em lote com lógica baseada em eventos para capturar perfis que atendem aos critérios de supressão. Faça referência a esse público-alvo em condições de jornada.

Saiba mais:

* [Construtor de segmentos do Adobe Experience Platform - Eventos](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [Construtor de segmentos do Adobe Experience Platform - Restrições de tempo](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de públicos-alvo em condições](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [função inAudience()](../building-journeys/functions/functioninaudience.md)


## Exclusão recebida por comunicações

Para impedir o envio de mensagens a perfis que receberam comunicações em uma janela de tempo recente:

* Use públicos-alvo em lote com critérios baseados em tempo e faça referência a eles em condições de jornada.
* Aplicar regras de negócios de limite de frequência para aplicar limites de mensagem diários ou semanais.


Saiba mais sobre como usar os públicos-alvo:

* [Construtor de segmentos do Adobe Experience Platform - Eventos](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [Construtor de segmentos do Adobe Experience Platform - Restrições de tempo](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de públicos-alvo em condições](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [função inAudience()](../building-journeys/functions/functioninaudience.md)


Consulte também:

* [Limite de frequência por canal e tipo de comunicação](../conflict-prioritization/channel-capping.md)



## Inclusão/exclusão específica à mensagem

Para incluir ou excluir perfis com base no fato de terem recebido uma mensagem específica, crie públicos-alvo em lote que encapsulam essa lógica e os referenciam em condições de jornada.


Saiba mais:

* [Construtor de segmentos do Adobe Experience Platform - Eventos](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [Construtor de segmentos do Adobe Experience Platform - Restrições de tempo](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de públicos-alvo em condições](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [função inAudience()](../building-journeys/functions/functioninaudience.md)

## Personalização de abandono de carrinho ou navegação

Para personalizar as comunicações com base no carrinho mais recente ou procurar eventos em vários tipos de carrinho ou exibições de produto:

* Se você tiver acesso ao [Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/pt-br/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configure consultas automatizadas para extrair os dados necessários do evento, manipulá-los para se ajustarem ao caso de uso e gravá-los em um conjunto de dados habilitado para perfil para ativação.
* Se os dados de abandono puderem ser modelados no perfil com atributos escalares, considere usar atributos Calculados para capturar as informações mais recentes e, em seguida, fazer referência a esses atributos na jornada para criar a comunicação. [Saiba mais na documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Saída da jornada baseada em comportamento

Para remover perfis do jornada quando eles exibirem um comportamento específico, utilize os critérios de saída para sair do perfil da jornada quando um evento específico for recebido ou o perfil for qualificado para um público-alvo específico.

Saiba mais:

* [Definir as propriedades da jornada - Critérios de saída](journey-properties.md#exit-criteria)

## Qualificação com base em compras com limites de valor

Para acionar jornadas com base em compras e suprimir se o valor estiver acima/abaixo de um limite, defina atributos calculados para somar compras em um período específico. Crie um público-alvo que inclua perfis cujo valor dos gastos atenda a determinados critérios.

Saiba mais:

* Adobe Experience Platform [Visão geral dos atributos computados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Perguntas frequentes {#faq-ee}

Não há mais suporte para o uso de eventos de experiência em expressões/condições de jornada. Os impactos estão listados nas Perguntas frequentes abaixo:

+++Quais recursos específicos foram afetados?

Somente a pesquisa de eventos de experiência no editor de expressão é afetada. Os seguintes recursos **não** foram afetados e permanecem os mesmos:

* Observação dos eventos de experiência associados a um perfil específico na interface do usuário do perfil

* Uso de eventos de experiência em regras de atributos computados e acesso aos atributos computados em uma jornada

* Acionamento de uma jornada com um evento unitário ou de negócios

* Uso dos dados de contexto de jornada dos eventos que acionam a jornada nos editores de expressão e personalização

* Acompanhamento de um evento em uma jornada

* Configurar eventos para acionar uma jornada

* Detecção de eventos de reação do usuário final a comunicações de marketing (por exemplo, abertura de email)

+++

+++Minha organização atual da Adobe é afetada por essa atualização?

Sua organização da Adobe só será afetada se você ainda não estiver usando a pesquisa de evento de experiência. Se você já estiver utilizando os eventos de experiência na [fonte de dados do Experience Platform](../datasource/adobe-experience-platform-data-source.md), sua organização da Adobe continuará a ser compatível com a pesquisa de evento de experiência.

+++

+++Tenho uma nova Organização da Adobe. Como posso resolver meu caso de uso que requer dados de evento de experiência?

Abordagens alternativas e práticas recomendadas envolvendo eventos de experiência estão disponíveis acima para atingir os casos de uso desejados.

+++

+++ E se abordagens alternativas não funcionarem no meu caso de uso?

Se seu caso de uso não puder ser resolvido usando uma das abordagens alternativas listadas acima, entre em contato com o representante da Adobe.

+++
