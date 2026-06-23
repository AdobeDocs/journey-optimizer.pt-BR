---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com atributos computados
description: Saiba como trabalhar com atributos computados.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
TQID: https://experienceleague.adobe.com/bH8UDdjWsh1Kle1ltVP2ltgXcNJDfVIdTuFdGWSZv6Y
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1012
ht-degree: 1%

---

# Trabalhar com atributos computados {#computed-attributes}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como criar atributos computados que agregam eventos comportamentais em atributos de perfil e usá-los para segmentação, personalização e lógica de jornada no Adobe Journey Optimizer.

>[!ENDSHADEBOX]

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

- **TL;DR:** Saiba como criar atributos computados no Adobe Experience Platform e aproveitá-los no Journey Optimizer para segmentação, personalização e lógica de jornada.

**Intenções:**
- Entenda o que são atributos calculados e como eles diferem dos atributos de perfil padrão
- Criar atributos computados combinando atributos de evento, funções agregadas e um período de lookback
- Adicione o grupo de campos SystemComputedAttributes à fonte de dados do Experience Platform no AJO
- Usar atributos computados em condições de jornada, criação de público e personalização de mensagens

**Glossário:**
- **Atributo computado**: um atributo de perfil derivado de dados de eventos comportamentais agregados, armazenado em perfis de clientes *(específico do produto)*
- **Período de pesquisa**: a janela de tempo aplicada ao calcular a regra de agregação de um atributo calculado (por exemplo, &quot;últimos 3 meses&quot;) *(específico do produto)*
- **Grupo de campos SystemComputedAttributes**: o grupo de campos na fonte de dados Experience Platform da AJO que expõe todos os atributos computados publicados para uso no jornada e na personalização *(específico do produto)*
- **Esquema de união de perfil**: o esquema mesclado que combina todos os fragmentos de perfil de uma determinada identidade, onde os atributos computados são armazenados

**Medidas de Proteção:**
- Requer **Exibir atributos computados** e **Gerenciar atributos computados** permissões para acessar o recurso
- Os atributos computados devem ser **publicados** no AEP antes de se tornarem disponíveis no downstream no Journey Optimizer
- Os atributos computados devem ser adicionados explicitamente à **fonte de dados do Experience Platform** no AJO para que possam ser usados em jornadas ou personalização
- Os atributos computados são baseados em conjuntos de dados de Evento de experiência habilitados para perfil assimilados na Adobe Experience Platform

**Terminologia:**
- Nome canônico: Adobe Journey Optimizer — Acrônimo: AJO — variantes: Journey Optimizer, A-JO
- Nome canônico: Adobe Experience Platform — Acrônimo: AEP
- Sinônimos: &quot;atributos computados&quot; = &quot;atributos de perfil computados&quot;
- Não confunda: &quot;atributos computados&quot; (recurso agregado específico do AEP/AJO) ≠ &quot;atributos de perfil&quot; genéricos

**Perguntas frequentes:**
- **P: O que são atributos computados?** — Dados de evento comportamentais agregados (por exemplo, total de compras, último item visualizado) armazenados como atributos de perfil no AEP e utilizáveis no AJO.
- **P: Preciso de permissões especiais?** — Sim: são necessários os atributos &quot;Exibir computados&quot; e &quot;Gerenciar atributos computados&quot;.
- **P: Como disponibilizar atributos computados no Journey Optimizer?** — Adicione o grupo de campos `SystemComputedAttributes` à fonte de dados do Experience Platform em Configurações > Fontes de dados.
- **P: Onde posso usar atributos computados no AJO?** — Em Atividades de condição (divisão de jornada), criação de público-alvo e editor de personalização.
- **P: O que é um período de pesquisa?** — A janela de tempo usada para determinar o escopo da regra de agregação, por exemplo, &quot;soma das compras das últimas 3 semanas&quot;.
- **P: Posso usar atributos computados em jornadas em tempo real?** — Sim, depois de publicados e adicionados à fonte de dados, eles podem ser acessados como qualquer outro atributo de perfil.

+++
