---
solution: Journey Optimizer
product: journey optimizer
title: Criar condições
description: Saiba como criar condições
feature: Personalization, Rules
topic: Personalization
role: Developer
level: Intermediate
keywords: expressão, editor, condicional, regras
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1255
ht-degree: 6%

---

# Trabalhar com regras condicionais {#conditions}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como criar regras condicionais de atributos de perfil, eventos contextuais e públicos-alvo no editor de personalização e como salvá-las na biblioteca para reutilização no seu conteúdo.

>[!ENDSHADEBOX]

As regras condicionais são conjuntos de regras que definem qual conteúdo deve ser exibido em suas mensagens, dependendo de vários critérios, como atributos de perfis, associação de público-alvo ou eventos contextuais.

As regras condicionais são criadas usando o editor de personalização e podem ser armazenadas se você quiser reutilizá-las no conteúdo. [Saiba como salvar uma regra condicional na biblioteca](#save)

>[!NOTE]
>
>As pessoas precisarão da permissão [Gerenciar itens de biblioteca](../administration/ootb-product-profiles.md) para salvar ou excluir regras condicionais. As condições salvas estão disponíveis para uso por todos os usuários em uma organização.

## Acessar o construtor de regras condicionais {#access}

As regras condicionais são criadas no menu **[!UICONTROL Condições]**, no editor de personalização, que pode ser acessado:

* No Designer de email, ao ativar o conteúdo dinâmico para um componente no corpo do email. [Saiba como adicionar conteúdo dinâmico a emails](dynamic-content.md#emails)

  ![](assets/conditions-access-email.png)

* Em qualquer campo onde você possa adicionar personalização usando o [editor de personalização](personalization-build-expressions.md).

  ![](assets/conditions-access-editor.png)

## Criar uma regra condicional {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="Criar condição"
>abstract="Combine atributos de perfil, eventos contextuais ou públicos-alvos para criar regras que definem qual conteúdo deve ser exibido nas mensagens."

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="Criar condição"
>abstract="Combine atributos de perfil, eventos contextuais ou públicos-alvos para criar regras que definem qual conteúdo deve ser exibido nas mensagens."

As etapas para criar uma regra condicional são as seguintes:

1. Acesse o menu **[!UICONTROL Condições]** do editor de personalização ou do Designer de email e clique em **[!UICONTROL Criar novo]**.

1. Crie a regra condicional de acordo com suas necessidades. Para fazer isso, arraste e solte e organize os atributos desejados do menu esquerdo na tela de desenho.

   As etapas para combinar atributos na tela são semelhantes à experiência de construção de segmentos. Para obter mais informações sobre como trabalhar com a tela do construtor de regras, consulte [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=pt-BR#rule-builder-canvas).

   ![](assets/conditions-create.png)

   Os atributos são organizados em três guias:

   * **[!UICONTROL Perfil]**:
      * **[!UICONTROL Públicos-alvo]** lista todos os atributos de público-alvo (ou seja, status, versão etc.) para o [serviço de Segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"},
      * **[!UICONTROL Perfis individuais XDM]** lista todos os atributos de perfil associados ao [esquema do Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"} definido no Adobe Experience Platform.
   * **[!UICONTROL Contextual]**: quando a mensagem é usada em uma jornada, os campos de jornada contextual ficam disponíveis por meio desta guia.
   * **[!UICONTROL Públicos-alvo]**: lista todos os públicos-alvo gerados pelas definições de segmento criadas no [serviço de Segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"}.

1. Quando a regra condicional estiver pronta, você poderá adicioná-la à mensagem para criar conteúdo dinâmico. [Saiba como adicionar conteúdo dinâmico](dynamic-content.md)

   Você também pode salvar a regra para permitir mais reutilização. [Saiba como salvar uma condição](#save)

## Salvar uma regra condicional {#save}

Se houver regras de condição que serão reutilizadas com frequência, você poderá salvá-las na biblioteca de condições. Todas as regras salvas são compartilhadas e podem ser acessadas e usadas por indivíduos em sua organização.

>[!NOTE]
>
>Regras condicionais que usam atributos contextuais do jornada não podem ser salvas na biblioteca.

1. Na tela de edição de condição, clique no botão **[!UICONTROL Salvar condição]**.

1. Dê um nome e uma descrição (opcional) à regra e clique em **[!UICONTROL Adicionar]**.

   ![](assets/conditions-name-description.png)

1. A regra condicional é salva na biblioteca. Agora você pode usá-lo para criar conteúdo dinâmico em suas mensagens. [Saiba como adicionar conteúdo dinâmico](dynamic-content.md)


>[!CAUTION]
>
>Ao nomear variantes de conteúdo condicional, use somente caracteres alfanuméricos (A-Z, a-z, 0-9). O uso de caracteres especiais (como `<`, `>`, `=`, `{`, `}`, etc.) em nomes de variantes pode fazer com que o editor de modelo quebre ou oculte componentes.

## Editar e excluir regras condicionais salvas {#edit-delete}

É possível excluir uma regra condicional a qualquer momento usando o botão de reticências.

![](assets/conditions-open.png)

Regras condicionais salvas na biblioteca não podem ser modificadas. No entanto, você ainda pode usá-las para criar novas regras. Para fazer isso, abra a regra condicional, faça as alterações desejadas e salve-a na biblioteca. [Saiba como salvar uma condição na biblioteca](#save)

## Referência rápida {#quick-reference}

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

>[!BEGINTABS]

>[!TAB Visão geral]

**TL;DR**

Esta página explica como criar regras condicionais de atributos de perfil, eventos contextuais e públicos-alvo no editor de personalização e como salvá-los na biblioteca para reutilização no conteúdo da mensagem.

**Intenções**

* Acesse o construtor de regras condicionais pelo editor de personalização ou pelo Email Designer
* Criar uma regra condicional combinando atributos de perfil, associação de público-alvo e campos de jornada contextual
* Adicionar uma regra condicional a uma mensagem para criar conteúdo dinâmico
* Salvar uma regra condicional na biblioteca de condições para reutilização em toda a organização
* Editar ou excluir uma regra condicional salva

>[!TAB Glossário]

* **Regra condicional**: um conjunto de regras que define qual conteúdo deve ser exibido nas mensagens, com base em critérios como atributos de perfil, associação de público ou eventos contextuais. *(específico do produto)*
* **Biblioteca de condições**: um repositório compartilhado em uma organização onde regras condicionais salvas são armazenadas e acessíveis a todos os usuários. *(específico do produto)*
* **Conteúdo dinâmico**: conteúdo de mensagem cuja exibição é regida por regras condicionais. *(específico do produto)*
* **Campos contextuais**: campos específicos de Jornada disponíveis no construtor de regras quando uma mensagem é usada em uma jornada; regras que usam esses campos não podem ser salvas na biblioteca.
* **Perfis individuais XDM**: os atributos de perfil associados ao esquema Experience Data Model (XDM) definido no Adobe Experience Platform, disponíveis como critérios de regra.

>[!TAB Terminologia]

* **Nome canônico:** regra condicional — variantes: condição, condições, regra de conteúdo condicional
* **Sinônimos:** &quot;regra condicional&quot; = &quot;condição&quot; (conforme rotulado na interface do usuário)
* **Não confunda:** a guia &quot;Perfil&quot; (contém os atributos de Públicos-alvo e as subseções de perfis individuais XDM) ≠ a guia &quot;Públicos-alvo&quot; (lista todos os públicos-alvo gerados a partir das definições de segmento no serviço de Segmentação do AEP)
* **Não confunda:** &quot;salvar uma condição&quot; (armazenar uma regra na biblioteca compartilhada) ≠ &quot;criar uma condição&quot; (criar uma nova regra no editor)

>[!TAB Medidas de proteção e limitações]

* As regras condicionais que usam atributos contextuais de jornada não podem ser salvas na biblioteca de condições.
* Somente usuários com a permissão **Gerenciar itens de biblioteca** podem salvar ou excluir regras condicionais da biblioteca.
* As condições salvas são compartilhadas e acessíveis a todos os usuários na organização.
* Regras condicionais salvas na biblioteca não podem ser modificadas diretamente; abra a regra, faça as alterações desejadas e salve-a na biblioteca.
* Os nomes de variantes devem usar somente caracteres alfanuméricos (A-Z, a-z, 0-9); caracteres especiais como `<`, `>`, `=`, `{`, `}` podem fazer com que o editor de modelo quebre ou oculte componentes.

>[!TAB Perguntas frequentes]

**P: Quais critérios posso usar para criar uma regra condicional?**

Atributos de perfil, associação de público-alvo e campos de jornada contextual (quando a mensagem é usada em uma jornada).

**P: Posso salvar uma regra condicional que use atributos contextuais de jornada?**

Não. As regras condicionais que usam atributos contextuais de jornada não podem ser salvas na biblioteca de condições.

**P: Quem pode salvar ou excluir regras condicionais na biblioteca?**

Somente usuários com a permissão **Gerenciar itens de biblioteca** podem salvar ou excluir regras condicionais.

**P: Posso modificar uma regra condicional que já está salva na biblioteca?**

As regras condicionais salvas na biblioteca não podem ser modificadas diretamente. É possível abrir uma regra salva, fazer as alterações desejadas e salvá-la na biblioteca.

**P: Há restrições para nomear variantes de conteúdo condicional?**

Sim. Os nomes de variantes devem conter somente caracteres alfanuméricos (A-Z, a-z, 0-9). Caracteres especiais como `<`, `>`, `=`, `{`, `}` podem fazer com que o editor de modelo quebre ou oculte componentes.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: f375658d -->
