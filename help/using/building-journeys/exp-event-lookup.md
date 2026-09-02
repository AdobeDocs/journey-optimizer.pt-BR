---
solution: Journey Optimizer
product: journey optimizer
title: Pesquisa de eventos de experiência no jornada
description: Saiba como usar a pesquisa de Eventos de experiência no jornada
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/kVO36LmCfr9cYVq3EHRy8OpqPCZDq20mXTEA49TIRTI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: fa683eda-48de-4558-af32-2673edcd44fe
topic_v2:
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1717
ht-degree: 4%

---

# Pesquisa de evento de experiência no jornada {#ee-journeys}

>[!BEGINSHADEBOX]

**Nesta página:** conheça padrões escaláveis e práticas recomendadas para usar Eventos de Experiência no jornada para suprimir, qualificar ou personalizar perfis com base em seus atributos de comportamento e evento.

>[!ENDSHADEBOX]

>[!CAUTION]
>
>A partir de 8 de julho de 2025, em novas organizações de clientes, a criação de expressões usando eventos de experiência não será mais suportada no editor de expressão usado em condições de jornada. Como resultado, os eventos de experiência na [fonte de dados da Experience Platform](../datasource/adobe-experience-platform-data-source.md) não poderão ser usados para criar expressões.
>
>A partir de 1º de abril de 2026, o uso de atributos de evento de experiência em expressões do jornada não será mais compatível com organizações que não usaram esse recurso nos últimos 90 dias. Abordagens alternativas e práticas recomendadas para criar expressões/lógica com eventos de experiência são referenciadas abaixo.
>
>Precisa de mais detalhes? [Leia as perguntas frequentes](#faq-ee).

Esta página descreve padrões comuns e abordagens escaláveis para ajudá-lo a aproveitar ao máximo os Eventos de Experiência do [!DNL Adobe Journey Optimizer]. Esses casos de uso são projetados para ajudar você a resolver desafios frequentes, como gerenciar recusas, controlar a frequência da mensagem, personalizar o conteúdo com base no comportamento do usuário e reagir a sinais em tempo real.

Ao utilizar essas estratégias, é possível transformar dados comportamentais em ações significativas — suprimindo, qualificando ou excluindo perfis com base nos eventos acionados ou nos atributos transportados. Quer você esteja criando lógica para limites de compra, acionadores de abandono ou lidando com rejeições, esses exemplos oferecem orientação prática que você pode adaptar às suas necessidades.

Ao avaliar qual abordagem se encaixa melhor, considere os requisitos de latência do seu caso de uso para garantir que suas jornadas permaneçam responsivas e eficazes.

## Supressão de recusa

Para suprimir perfis que recusaram comunicações de marketing, use o gerenciamento de consentimento integrado. As preferências de recusa são capturadas automaticamente nos campos de consentimento do perfil; elas podem ser referenciadas diretamente nas condições de jornada e são aplicadas automaticamente pelo Journey Optimizer durante a entrega da mensagem.

Saiba mais:

* [Gerenciar consentimento](../privacy/opt-out.md)
* [Gerenciamento de opção de não participação de email](../email/email-opt-out.md)
* [Gerenciamento de recusa para mensagens móveis](../mobile/mobile-opt-out.md)


## Supressão baseada em rejeição

Para excluir perfis que tiveram rejeições de email, use a lista de supressão automática de [!DNL Adobe Journey Optimizer] para endereços rejeitados. Esse mecanismo integrado garante que emails inválidos ou inacessíveis sejam excluídos de envios futuros sem exigir lógica personalizada.

Saiba mais:

* [Gerenciar a lista de supressão](../configuration/manage-suppression-list.md)


## Supressão genérica

Para suprimir perfis que demonstraram determinados comportamentos, use públicos-alvo em lote com lógica baseada em eventos para capturar perfis que atendem aos critérios de supressão. Faça referência a esse público-alvo em condições de jornada.

Saiba mais:

* [!DNL Adobe Experience Platform] [Construtor de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Construtor de segmentos - Restrições de tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de públicos-alvo em condições](../building-journeys/conditions.md#using-a-segment)

* [função inAudience()](../building-journeys/functions/functioninaudience.md)


## Exclusão recebida por comunicações

Para impedir o envio de mensagens a perfis que receberam comunicações em uma janela de tempo recente:

* Use públicos-alvo em lote com critérios baseados em tempo e faça referência a eles em condições de jornada.
* Aplicar regras de negócios de limite de frequência para aplicar limites de mensagem diários ou semanais.


Saiba mais sobre como usar os públicos-alvo:

* [!DNL Adobe Experience Platform] [Construtor de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Construtor de segmentos - Restrições de tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de públicos-alvo em condições](../building-journeys/conditions.md#using-a-segment)

* [função inAudience()](../building-journeys/functions/functioninaudience.md)


Consulte também:

* [Limite de frequência por canal e tipo de comunicação](../conflict-prioritization/channel-capping.md)



## Inclusão/exclusão específica à mensagem

Para incluir ou excluir perfis com base no fato de terem recebido uma mensagem específica, crie públicos-alvo em lote que encapsulam essa lógica e os referenciam em condições de jornada.


Saiba mais:

* [!DNL Adobe Experience Platform] [Construtor de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Construtor de segmentos - Restrições de tempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de públicos-alvo em condições](../building-journeys/conditions.md#using-a-segment)

* [função inAudience()](../building-journeys/functions/functioninaudience.md)

## Personalização de abandono de carrinho ou navegação

Para personalizar as comunicações com base no carrinho mais recente ou procurar eventos em vários tipos de carrinho ou exibições de produto:

* Se você tiver acesso ao [[!DNL Adobe Experience Platform] Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configure consultas automatizadas para extrair os dados necessários do evento, manipulá-los para se ajustarem ao caso de uso e gravá-los em um [conjunto de dados habilitado para perfil](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} para ativação.
* Se os dados de abandono puderem ser modelados no perfil com atributos escalares, considere usar atributos Calculados para capturar as informações mais recentes e, em seguida, fazer referência a esses atributos na jornada para criar a comunicação. [Saiba mais em [!DNL Adobe Experience Platform] documentação](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Saída da jornada baseada em comportamento

Para remover perfis do jornada quando eles exibirem um comportamento específico, utilize os critérios de saída para sair do perfil da jornada quando um evento específico for recebido ou o perfil for qualificado para um público-alvo específico.

Saiba mais:

* [Definir as propriedades da jornada - Critérios de saída](journey-properties.md#exit-criteria)

## Qualificação com base em compras com limites de valor

Para acionar jornadas com base em compras e suprimir se o valor estiver acima/abaixo de um limite, defina atributos calculados para somar compras em um período específico. Crie um público-alvo que inclua perfis cujo valor dos gastos atenda a determinados critérios.

Saiba mais:

* [!DNL Adobe Experience Platform] [Visão geral de atributos computados](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Perguntas frequentes {#faq-ee}

Estas perguntas frequentes se concentram na linha do tempo para retirar o uso do evento de experiência nas expressões do jornada e quem é afetado. Para obter orientação sobre abordagens alternativas, consulte os casos de uso e as práticas recomendadas acima.

Precisa de mais detalhes? Use as opções de comentários na parte inferior desta página para levantar sua pergunta ou conectar-se à [[!DNL Adobe Journey Optimizer] comunidade](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}.

+++Quais recursos específicos serão afetados? 

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

A partir de 8 de julho de 2025, novas organizações de clientes não poderão criar expressões usando atributos de evento de experiência. A partir de 1º de abril de 2026, as organizações que não acessaram eventos de experiência por meio de expressões do jornada nos últimos 90 dias não terão mais acesso a esse recurso.

+++

+++Eu tenho uma nova Organização da Adobe. Como posso resolver meu caso de uso que requer dados de evento de experiência? 

Abordagens alternativas e práticas recomendadas envolvendo eventos de experiência estão disponíveis acima para atingir os casos de uso desejados.

+++

+++ E se abordagens alternativas não funcionarem no meu caso de uso?

Se seu caso de uso não puder ser resolvido usando uma das abordagens alternativas listadas acima, entre em contato com o representante da Adobe.

+++

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página descreve padrões alternativos e práticas recomendadas para o uso de dados do Evento de experiência no Adobe Journey Optimizer jornada, no contexto da descontinuação da pesquisa direta de evento de experiência no editor de expressão de jornada.

**Intenções:**

* Suprimir perfis que recusaram a participação usando o gerenciamento de consentimento integrado em vez de expressões de evento de experiência
* Excluir endereços de email rejeitados usando a lista de supressão automática do AJO
* Criar lógica de supressão genérica usando públicos-alvo em lote com critérios baseados em eventos
* Evite a comunicação excessiva aplicando regras de limite de frequência ou condições de público-alvo baseadas em tempo
* Personalize o carrinho abandonado ou procure comunicações usando o AEP Data Distiller ou atributos computados

**Glossário:**

* **Evento de experiência**: um registro imutável com carimbo de data e hora de uma ação ou comportamento do cliente armazenado no Adobe Experience Platform *(específico do produto)*
* **Atributo computado**: um atributo de nível de perfil derivado da agregação ou do resumo dos dados do evento de experiência ao longo do tempo, disponível para uso nas expressões de jornada *(específico do produto)*
* **Lista de supressão**: lista interna de endereços de email da AJO excluída automaticamente de envios futuros devido a devoluções permanentes ou reclamações de spam *(específico do produto)*
* **Limite de frequência**: uma regra de negócios que limita quantas mensagens um perfil pode receber em uma janela de tempo definida *(específico do produto)*
* **Data Distiller**: um recurso do AEP que permite que consultas em lote baseadas em SQL extraiam e transformem dados do evento em conjuntos de dados habilitados para perfil *(específico do produto)*

**Medidas de Proteção:**

* A partir de 8 de julho de 2025, novas organizações de clientes não poderão criar expressões usando atributos de evento de experiência no editor de expressão do jornada.
* A partir de 1º de abril de 2026, as organizações que não usaram atributos de evento de experiência em expressões do jornada nos últimos 90 dias perderão o acesso a esse recurso.
* A pesquisa direta de evento de experiência em condições de jornada está sendo removida; as alternativas incluem públicos em lote, atributos calculados e AEP Data Distiller.
* Os recursos NÃO afetados pela retirada incluem: acionar jornadas com eventos, ouvir eventos em uma jornada, usar dados de contexto de jornada de eventos de acionamento, configurar eventos e detectar eventos de reação.

**Terminologia:**

* Nome canônico: Pesquisa de evento de experiência — Acrônimo: Pesquisa EE — variantes: expressões de evento de experiência, pesquisa de atributo de evento
* Sinônimos: &quot;público-alvo em lote com lógica baseada em eventos&quot; = &quot;segmento baseado em eventos&quot; como um mecanismo de supressão/inclusão
* Não confunda: &quot;pesquisa de evento de experiência no editor de expressão&quot; ≠ &quot;acionar uma jornada com um evento&quot; — o acionamento de jornadas com eventos NÃO está sendo removido

**Perguntas frequentes:**

* **P: Ainda posso acionar uma jornada usando um evento de experiência?** — Sim, o acionamento de jornadas com eventos unitários ou de negócios não é afetado por essa alteração.
* **P: Qual é a substituição recomendada para a pesquisa de evento de experiência em condições de jornada?** — use públicos-alvo em lote criados com a lógica baseada em eventos, atributos computados ou AEP Data Distiller do AEP Segment Builder para transformações complexas.
* **P: Minha organização existente foi afetada agora?** — Novas organizações serão afetadas a partir de 8 de julho de 2025. As organizações existentes são afetadas a partir de 1 de abril de 2026 somente se não tiverem usado o recurso nos últimos 90 dias.
* **P: Como faço para lidar com a personalização de abandono de carrinho sem pesquisa direta de evento?** — use o AEP Data Distiller para extrair e gravar dados do evento em um conjunto de dados habilitado para perfis ou use atributos computados para capturar o estado de abandono mais recente no perfil.
* **P: Quais recursos NÃO são afetados por esta descontinuação?** — o acionamento de jornadas com eventos, a escuta de eventos no jornada, o uso de dados de contexto de evento de acionador em expressões, a configuração de eventos e a detecção de eventos de reação (por exemplo, aberturas de email) não são afetados.

+++
