---
title: Aproveitar fragmentos em políticas de decisão
description: Saiba como aproveitar fragmentos em políticas de decisão
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
TQID: https://experienceleague.adobe.com/5Vpngi03UnC9YPlB5tdTRcd0NoT7iglH2pRDkmeZKOg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1114
ht-degree: 0%

---

# Aproveitar fragmentos em políticas de decisão {#fragments}

Os itens de decisão são compatíveis com dois tipos de conteúdo de fragmento que podem ser aproveitados ao criar mensagens em uma política de decisão:

* **Fragmentos de conteúdo do Journey Optimizer** — fragmentos de expressão reutilizáveis criados no Journey Optimizer e adicionados à seção **[!UICONTROL Fragmentos]** do item de decisão. [Saiba mais sobre os fragmentos de conteúdo do AJO](../content-management/fragments.md)
* **Fragmentos de conteúdo do AEM** — conteúdo criado no Adobe Experience Manager, mapeado para os atributos do item de decisão e selecionado no editor de personalização por nome de chave. [Saiba como vincular um Fragmento de conteúdo do AEM a um item de decisão](items.md#aem-fragments)

## Fragmentos de conteúdo do Journey Optimizer {#ajo-fragments}

Se a política de decisão contiver itens de decisão, incluindo fragmentos de conteúdo do AJO, você poderá aproveitar esses fragmentos ao criar uma mensagem na política de decisão em todos os canais nos quais a Decisão está disponível (experiência baseada em código, email, push, SMS e jornadas).

Por exemplo, digamos que você queira exibir conteúdos diferentes para vários modelos de dispositivos móveis. Adicione os fragmentos especificados, cada um pertencente a um modelo de telefone diferente, ao item de decisão que você está usando na política de decisão. [Saiba como adicionar fragmentos a um item de decisão](items.md#attributes).

![Seção de fragmentos de um item de decisão mostrando referências de fragmento e chaves de posicionamento.](assets/item-fragments.png){width=70%}

Depois de concluído, você pode usar um dos seguintes métodos:

>[!BEGINTABS]

>[!TAB Inserir o código diretamente]

Basta copiar e colar o bloco de código abaixo no código de política de decisão. Substitua `variable` pela ID do fragmento e `placement` pela chave de referência do fragmento:

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable required=false}}
```

>[!TAB Siga as etapas detalhadas]

1. Navegue até as **[!UICONTROL funções auxiliares]** e adicione a **função Let** `{% let variable = expression %} {{variable}}` ao painel de código, onde você pode declarar a variável para o fragmento.

   ![Editor de código de política de decisão mostrando a função Let helper adicionada ao painel de código.](assets/decision-let-function.png)

1. Use a função `{%= get(map, string) %}` de **Mapa** > **Obter** para criar sua expressão. O mapa é o fragmento referenciado no item de decisão. A cadeia de caracteres pode ser o modelo de dispositivo inserido no item de decisão como a **[!UICONTROL Chave de referência do fragmento]**.

   ![As funções Map e Get são usadas para fazer referência ao mapa de fragmentos e à chave de referência do fragmento.](assets/decision-map-function.png)

1. Você também pode usar um atributo contextual que contenha essa ID de modelo de dispositivo.

   ![Atributo contextual selecionado para o identificador de modelo de dispositivo.](assets/decision-contextual-attribute.png)

1. Adicione a variável escolhida para o fragmento como a ID do fragmento.

   ![Variável de ID de fragmento definida a partir do item de decisão no código de política de decisão.](assets/decision-fragment-id.png)

>[!ENDTABS]

A ID do fragmento e a chave de referência serão selecionadas na seção **[!UICONTROL Fragmentos]** do item de decisão.

>[!WARNING]
>
>Se a chave do fragmento estiver incorreta ou se o conteúdo do fragmento não for válido, a renderização poderá falhar e causar um erro na chamada do Edge.
>
>Para evitar falhas quando um fragmento estiver temporariamente indisponível, o sinalizador `required=false` é usado para que o fragmento seja ignorado. [Saiba mais sobre fragmentos temporariamente indisponíveis](#temporary-unavailable-fragments)

### Uso e medidas de proteção {#fragments-guardrails}

As seguintes medidas de proteção se aplicam especificamente aos **fragmentos de conteúdo do AJO** usados em itens de decisão.

+++Simular fragmentos de conteúdo e expressão em emails

Para o canal de **Email**, os fragmentos de expressão associados a um item de decisão são exibidos corretamente quando você **[!UICONTROL Envia prova]** ou quando a campanha é ativada. No entanto, **[!UICONTROL Simular conteúdo]** não exibe o fragmento de expressão do item de decisão.

+++

+++Fragmentos visuais e itens de decisão em emails

Você não pode atribuir um **[!UICONTROL Fragmento visual]** a um item de decisão. Somente **fragmentos de expressão** são suportados neste contexto.

+++

+++Atributos de item de decisão e contexto

Atributos de item de decisão e atributos contextuais não são suportados por padrão em fragmentos [!DNL Journey Optimizer]. No entanto, você pode usar variáveis globais, conforme descrito abaixo.

Digamos que você queira usar a variável *sport* no fragmento.

1. Faça referência a essa variável no fragmento, por exemplo:

   ```text
   Elevate your practice with new {{sport}} gear!
   ```

1. Defina a variável com a função **Let** no bloco de política de decisão. No exemplo abaixo, *sport* é definido com o atributo de item de decisão:

   ```handlebars
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

+++

+++Validação do conteúdo do fragmento do item de decisão

* Devido à natureza dinâmica desses fragmentos, quando usados em uma campanha, a validação da mensagem durante a criação do conteúdo da campanha é ignorada para fragmentos referenciados em itens de decisão.

* A validação do conteúdo do fragmento ocorre somente durante a criação e a publicação do fragmento.

* Para fragmentos de expressão do tipo JSON, o conteúdo é validado sintaticamente ao salvar o fragmento. Os erros de validação são exibidos como alertas.

No tempo de execução, o conteúdo da campanha (incluindo o conteúdo de fragmentos de itens de decisão) é validado. No caso de uma falha de validação, a campanha não será renderizada.

+++

+++Fragmentos indisponíveis temporariamente são ignorados {#temporary-unavailable-fragments}

Quando jornadas ou campanhas fazem referência a fragmentos anexados a itens de decisão, pode haver pequenos atrasos de sincronização antes que os fragmentos atualizados estejam disponíveis no Edge.

Para evitar falhas quando um fragmento estiver temporariamente indisponível, os fragmentos agora têm o sinalizador `required` definido como `false` por padrão, para que sejam ignorados em vez de causar falha na jornada ou na campanha.

Isso significa que, se o fragmento estiver temporariamente indisponível no Edge, ele será simplesmente ignorado. Se o fragmento estiver disponível, ele será renderizado normalmente.

**Exemplo**

Se sua política de decisão se qualificar para duas ofertas e cada uma tiver um fragmento — por exemplo, &quot;20% de desconto&quot; e &quot;30% de desconto&quot; — e o segundo fragmento estiver temporariamente indisponível, com `required=false` o sistema renderiza a oferta disponível (20% de desconto) e ignora o outro fragmento (30% de desconto) em vez de falhar na jornada ou campanha. Isso aumenta a confiabilidade quando o conteúdo ainda está sincronizando.

+++

>[!NOTE]
>
>Você ainda pode marcar um fragmento como obrigatório definindo o sinalizador `required` como `true`. No entanto, se um fragmento estiver temporariamente ausente, isso poderá causar falha na renderização da jornada ou da campanha.

## Fragmentos de conteúdo do AEM {#aem-fragments-decisioning}

>[!AVAILABILITY]
>
>Esse recurso está disponível em Disponibilidade limitada para canais de saída com suporte à Decisão. Para solicitar acesso, entre em contato com o representante da Adobe.

Antes de aproveitar os fragmentos de conteúdo do AEM em uma política de decisão, verifique se você tem:

* Criou seu fragmento de conteúdo no Adobe Experience Manager e o marcou com `ajo-enabled:{OrgId}/{SandboxName}` para que ele possa ser descoberto pelo Journey Optimizer. [Saiba como criar e atribuir uma marca](../integrations/aem-fragments.md#create-tag)
* Vinculou o fragmento à seção **[!UICONTROL Fragmentos do AEM]** do item de oferta atribuindo a ele um nome de referência exclusivo. [Saiba como vincular um Fragmento de conteúdo do AEM a um item de decisão](items.md#attributes)

No editor de personalização, todos os Fragmentos de conteúdo do AEM associados aos itens de decisão selecionados pela política estão disponíveis. Uma pasta é exibida por nome de chave do fragmento.

Neste exemplo, a política de decisão inclui dois itens de decisão que têm fragmentos de AEM vinculados a eles por meio de seu nome de referência.

![](assets/aem-fragment-select.png)

1. Clique no botão + para adicionar o fragmento desejado à expressão.

   Como um único nome de referência pode ter vários fragmentos vinculados a ele em diferentes itens de oferta, o Decisioning determina o melhor a ser entregue a cada cliente com base nos critérios de classificação da política de decisão.

1. Depois que o fragmento for selecionado, você poderá aproveitar seus atributos, como URLs de imagem, campos de texto ou outro conteúdo, e usar o Decisioning para exibir o conteúdo correto ao cliente certo na hora certa.

   ![](assets/aem-fragment-attribute.png)

1. Antes de ativar sua campanha ou jornada, você pode usar **[!UICONTROL Simular conteúdo]** para visualizar como os valores de campo do Fragmento de conteúdo do AEM serão renderizados para um perfil de teste específico. [Saiba mais sobre como simular conteúdo](../content-management/preview-test.md)
