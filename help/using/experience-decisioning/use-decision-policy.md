---
title: Usar políticas de decisão em mensagens
description: Saiba como usar políticas de decisões em suas mensagens.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
source-git-commit: 2960ed9c9f7a65cbd7122424c2438a461ee8beab
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 1%

---

# Usar políticas de decisão em mensagens {#create-decision}

Depois que uma política de decisão é criada, a política e os atributos vinculados aos itens de decisão retornados podem ser usados no conteúdo para personalização. Para fazer isso, o código associado à política de decisão deve primeiro ser inserido no conteúdo. Depois de concluído, você poderá aproveitar seus atributos para personalização.

## Inserir o código de política de decisão {#insert-code}

>[!BEGINTABS]

>[!TAB Experiência baseada em código]

1. Abra o editor de personalização e acesse o menu **[!UICONTROL Políticas de decisão]**.

1. Selecione **[!UICONTROL Inserir política]** para adicionar o código correspondente à política de decisão.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Se o botão de inserção de código não for exibido, uma política de decisão pode já ter sido configurada para o componente principal.

1. O código da política de decisão é adicionado. Essa sequência será repetida o número de vezes que você deseja que a política de decisão seja retornada. Por exemplo, se você optar por retornar dois itens ao [criar a decisão](#add-decision), a mesma sequência será repetida duas vezes.

>[!TAB Email]

1. Abra o editor de personalização e acesse o menu de **[!UICONTROL Política de decisão]**.

1. Selecione **[!UICONTROL Inserir sintaxe]** para adicionar o código correspondente à política de decisão.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Se o botão de inserção de código não for exibido, uma política de decisão pode já ter sido configurada para o componente principal.

1. Se nenhum posicionamento tiver sido associado ao componente anteriormente, selecione um na lista e clique em **[!UICONTROL Atribuir]**.

   ![](assets/decision-policy-placement.png)

>[!ENDTABS]

Quando o código da política de decisão for adicionado, essa sequência será repetida o número de vezes que você deseja que a política de decisão seja retornada. Por exemplo, se você optar por retornar dois itens ao [criar a decisão](#add-decision), a mesma sequência será repetida duas vezes.

## Aproveitar atributos de itens de decisão {#attributes}

Agora você pode adicionar todos os atributos de decisão desejados dentro desse código. Os atributos disponíveis são armazenados no esquema do catálogo **[!UICONTROL Ofertas]**. Os atributos personalizados são armazenados na pasta **`_<imsOrg`>** e os atributos padrão na pasta **`_experience`**. [Saiba mais sobre o esquema do catálogo de Ofertas](catalogs.md)

![](assets/decision-code-based-decision-attributes.png)

>[!NOTE]
>
>Para o rastreamento de itens da política de decisão, o atributo `trackingToken` precisa ser adicionado da seguinte forma para o conteúdo da política de decisão:
>&#x200B;>`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

Para adicionar um atributo, clique no ícone &quot;+&quot; ao lado dele. Você pode adicionar quantos atributos desejar ao código.

![](assets/decision-code-based-add-decision-attributes.png)

Certifique-se de envolver o loop `#each` dentro de um par de colchetes `[ ]` e adicionar uma vírgula antes de fechar `/each`.

![](assets/decision-code-based-wrap-code.png)

Você também pode adicionar qualquer outro atributo disponível no editor de personalização, como atributos de perfil.

![](assets/decision-code-based-decision-profile-attribute.png)

## Aproveitar fragmentos {#fragments}

Se a política de decisão contiver itens de decisão, incluindo fragmentos, você poderá aproveitar esses fragmentos no código de política de decisão. [Saiba mais sobre fragmentos](../content-management/fragments.md)

>[!AVAILABILITY]
>
>No momento, esse recurso só está disponível para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o representante da Adobe.

Por exemplo, digamos que você queira exibir conteúdos diferentes para vários modelos de dispositivos móveis. Certifique-se de ter adicionado fragmentos correspondentes a esses dispositivos ao item de decisão que você está usando na política de decisão. [Saiba como](items.md#attributes).

![](assets/item-fragments.png){width=70%}

Depois de concluído, você pode usar um dos seguintes métodos:

>[!BEGINTABS]

>[!TAB Inserir o código diretamente]

Basta copiar e colar o bloco de código abaixo no código de política de decisão. Substitua `variable` pela ID do fragmento e `placement` pela chave de referência do fragmento:

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB Siga as etapas detalhadas]

1. Navegue até as **[!UICONTROL funções auxiliares]** e adicione a **função Let** `{% let variable = expression %} {{variable}}` ao painel de código, onde você pode declarar a variável para o fragmento.

   ![](assets/decision-let-function.png)

1. Use a função **de** Mapa **>** Obter`{%= get(map, string) %}` para criar sua expressão. O mapa é o fragmento referenciado no item de decisão e a sequência pode ser o modelo de dispositivo inserido no item de decisão como a **[!UICONTROL Chave de referência do fragmento]**.

   ![](assets/decision-map-function.png)

1. Você também pode usar um atributo contextual que contenha essa ID de modelo de dispositivo.

   ![](assets/decision-contextual-attribute.png)

1. Adicione a variável escolhida para o fragmento como a ID do fragmento.

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

A ID do fragmento e a chave de referência serão selecionadas na seção **[!UICONTROL Fragmentos]** do item de decisão.

>[!WARNING]
>
>Se a chave do fragmento estiver incorreta ou se o conteúdo do fragmento não for válido, a renderização falhará, causando erro na chamada do Edge.

### Medidas de proteção ao usar fragmentos {#fragments-guardrails}

**Atributos de item de decisão e de contexto**

Por padrão, os atributos de item de decisão e o atributo contextual não têm suporte em fragmentos [!DNL Journey Optimizer]. No entanto, você pode usar variáveis globais, conforme descrito abaixo.

Digamos que você queira usar a variável *sport* no fragmento.

1. Faça referência a essa variável no fragmento, por exemplo:

   ```
   Elevate your practice with new {{sport}} gear!
   ```

1. Defina a variável com a função **Let** no bloco de política de decisão. No exemplo abaixo, *sport* é definido com o atributo de item de decisão:

   ```
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

**Validação do conteúdo do fragmento do item de decisão**

* Devido à natureza dinâmica desses fragmentos, quando usados em uma campanha, a validação da mensagem durante a criação do conteúdo da campanha é ignorada para fragmentos referenciados em itens de decisão.

* A validação do conteúdo do fragmento ocorre somente durante a criação e a publicação do fragmento.

* No caso de fragmentos JSON, a validade do objeto JSON não é garantida. Verifique se o conteúdo do fragmento de expressão é um JSON válido para que ele possa ser usado em itens de decisão.

No tempo de execução, o conteúdo da campanha (incluindo o conteúdo de fragmentos de itens de decisão) é validado. No caso de uma falha de validação, a campanha não será renderizada.

## Próximas etapas {#final-steps}

Quando o conteúdo estiver pronto, revise e publique sua campanha ou jornada:

* [Publicar uma jornada](../building-journeys/publishing-the-journey.md)
* [Revisar como ativar uma campanha](../campaigns/review-activate-campaign.md)
* [Publicar e ativar uma experiência baseada em código](../code-based/publish-code-based.md)

Para experiências baseadas em código, assim que o desenvolvedor fizer uma chamada de API ou SDK para buscar conteúdo para a superfície definida na configuração do canal, as alterações serão aplicadas à página da Web ou aplicativo.

>[!NOTE]
>
>Atualmente não é possível simular o conteúdo da interface do usuário em uma campanha ou jornada de [experiência baseada em código](../code-based/create-code-based.md) usando decisões. Uma solução alternativa está disponível em [esta seção](../code-based/code-based-decisioning-implementations.md).

Para ver o desempenho de suas decisões, você pode criar [painéis de relatórios personalizados do Customer Journey Analytics](cja-reporting.md).

