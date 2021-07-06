---
title: '&Carimbo de uso de personalização; dois pontos; email de abandono do carrinho'
description: Saiba como personalizar uma mensagem usando funções auxiliares
feature: Personalização
topic: Personalização
role: Data Engineer
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 4%

---


# Caso de uso de personalização: email de abandono do carrinho {#personalization-use-case-helper-functions}

Neste exemplo, você personalizará o corpo de uma mensagem de email. Essa mensagem direciona os clientes que deixaram itens em seu carrinho de compras, mas não concluíram a compra.

Você usará esses tipos de funções de ajuda:

* A função de string `upperCase`, para inserir o nome do cliente em letras maiúsculas. [Saiba mais](functions/string.md#upper).
* A ajuda `each` para listar os itens que estão no carrinho. [Saiba mais](functions/helpers.md#each).
* O `if` auxiliar para inserir uma nota específica do produto se o produto relacionado estiver no carrinho. [Saiba mais](functions/helpers.md#if-function).

<!-- **Context**: personalization based on contextual data from the journey -->

Antes de começar, certifique-se de saber como configurar esses elementos:
* Uma mensagem de email. [Saiba mais](../create-message.md)
* O corpo de um email. [Saiba mais](../create-email-content.md).
* Um evento unitário. [Saiba mais](../event/about-events.md).
* Uma jornada que começa com um evento. [Saiba mais](../building-journeys/using-the-journey-designer.md).

Siga estas etapas:
1. [Criar uma mensagem](#configure-email) de email.
2. [Insira o nome do cliente em letras maiúsculas](#uppercase-function).
3. [Crie o evento inicial e a jornada](#create-context).
4. [Adicione o conteúdo do carrinho ao email](#each-helper).
5. [Insira uma nota](#if-helper) específica do produto.
6. [Testar e publicar a jornada](#test-and-publish).

## Etapa 1: Criar o email{#configure-email}

1. Crie ou modifique uma mensagem de email e clique em **[!UICONTROL Email Designer]**.
   ![](../assets/personalization-uc-helpers-1.png)

2. Na paleta esquerda da página inicial do Designer de email, arraste e solte três componentes da estrutura no corpo da mensagem.

3. Arraste e solte um componente de conteúdo HTML em cada novo componente de estrutura.

   ![](../assets/personalization-uc-helpers-2.png)

## Etapa 2: Inserir o nome do cliente em maiúsculas {#uppercase-function}

1. Na página inicial do Designer de email, clique no componente HTML onde deseja adicionar o nome do cliente.
2. Na barra de ferramentas contextual, clique em **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

3. Na janela **[!UICONTROL Edit HTML]**, adicione a função de string `upperCase`:
   1. Na lista, selecione **[!UICONTROL Helper functions]**.
   2. Use o campo de pesquisa para localizar &quot;maiúsculas&quot;.
   3. Nos resultados da pesquisa, adicione a função `upperCase` . Para fazer isso, clique no sinal de adição (+) ao lado de `{%= upperCase(string) %}: string`.

      O editor de expressão mostra esta expressão:

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](../assets/personalization-uc-helpers-4.png)

4. Remova o espaço reservado &quot;string&quot; da expressão.
5. Adicione o token de nome:
   1. Na lista, selecione **[!UICONTROL Profile]**.
   2. Selecione **[!UICONTROL Profile]** > **[!UICONTROL Person]** > **[!UICONTROL Full name]**.
   3. Adicione o token **[!UICONTROL First name]** à expressão.

      O editor de expressão mostra esta expressão:

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](../assets/personalization-uc-helpers-5.png)

      Saiba mais sobre o tipo de dados do nome da pessoa [Documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target=&quot;_blank&quot;}.

6. Clique em **[!UICONTROL Validate]** e depois em **[!UICONTROL Save]**.

   ![](../assets/personalization-uc-helpers-6.png)
7. Salve a mensagem.

## Etapa 3: Crie o evento inicial e a jornada relacionada {#create-context}

O conteúdo do carrinho é uma informação contextual da jornada. Portanto, é necessário adicionar um evento inicial e o email a uma jornada antes de adicionar informações específicas do carrinho ao email.

1. Crie um evento cujo esquema inclua a matriz `productListItems`.
2. Defina todos os campos dessa matriz como campos de carga para esse evento.

   Saiba mais sobre o tipo de dados do item da lista de produtos [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target=&quot;_blank&quot;}.

3. Crie uma jornada que comece com esse evento.
4. Adicione a mensagem à jornada.
5. Encerre a jornada com uma atividade final.

   Como você ainda não publicou a mensagem, não é possível testar nem publicar a jornada.

   ![](../assets/personalization-uc-helpers-7.png)

6. Clique em **[!UICONTROL OK]**.

   Uma mensagem informa que o contexto da jornada foi passado para a mensagem.

   ![](../assets/personalization-uc-helpers-8.png)

## Etapa 4: Inserir a lista de itens do carrinho {#each-helper}

1. Reabra a mensagem.

   ![](../assets/personalization-uc-helpers-18.png)

2. Na página inicial do Designer de email, clique no componente HTML onde deseja listar o conteúdo do carrinho.
3. Na barra de ferramentas contextual, clique em **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

4. Na janela **[!UICONTROL Edit HTML]**, adicione o auxiliar `each`:
   1. Na lista, selecione **[!UICONTROL Helper functions]**.
   2. Use o campo de pesquisa para localizar &quot;cada&quot;.
   3. Nos resultados da pesquisa, adicione o auxiliar `each`.

      O editor de expressão mostra esta expressão:

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](../assets/personalization-uc-helpers-9.png)

5. Adicione a matriz `productListItems` à expressão:

   1. Remova o espaço reservado &quot;someArray&quot; da expressão.
   2. Na lista, selecione **[!UICONTROL Context]**.

      A opção **[!UICONTROL Context]** está disponível somente após o contexto da jornada ter sido passado para a mensagem.

   3. Selecione **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]*** e expanda o nó **[!UICONTROL productListItems]**.

      Neste exemplo, *event_name* representa o nome do seu evento.

   4. Adicione o token **[!UICONTROL Product]** à expressão.

      O editor de expressão mostra esta expressão:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```
      Neste exemplo, *event_ID* representa a ID do seu evento.

      ![](../assets/personalization-uc-helpers-10.png)

   5. Modifique a expressão:
      1. Remova a string &quot;.product&quot;.
      2. Substitua o espaço reservado &quot;variável&quot; por &quot;produto&quot;.

      Este exemplo mostra a expressão modificada:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```
6. Cole esse código entre a tag de abertura `{{#each}}` e a tag de fechamento `{/each}}`:

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>$#priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```

7. Adicione os tokens de personalização para o nome do item, a quantidade e o preço:

   1. Remova o espaço reservado &quot;#name&quot; da tabela HTML.
   2. Nos resultados da pesquisa anterior, adicione o token **[!UICONTROL Name]** à expressão.

   Repita estas etapas duas vezes:
   * Substitua o espaço reservado &quot;#quantity&quot; pelo token **[!UICONTROL Quantity]**.
   * Substitua o espaço reservado &quot;#priceTotal&quot; pelo token **[!UICONTROL Total price]**.

   Este exemplo mostra a expressão modificada:

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
               <td><b>{{context.journey.events.event_ID.productListItems.name}}</b></td>
               <td><b>{{context.journey.events.event_ID.productListItems.quantity}}</b></td>
               <td><b>${{context.journey.events.event_ID.productListItems.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```
8. Clique em **[!UICONTROL Validate]** e depois em **[!UICONTROL Save]**.
   ![](../assets/personalization-uc-helpers-11.png)

## Etapa 5: Inserir uma nota específica do produto {#if-helper}

1. Na página inicial do Designer de email, clique no componente HTML onde deseja inserir a nota.
2. Na barra de ferramentas contextual, clique em **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

3. Na janela **[!UICONTROL Edit HTML]**, adicione o auxiliar `if`:
   1. Na lista, selecione **[!UICONTROL Helper functions]**.
   2. Use o campo de pesquisa para localizar &quot;if&quot;.
   3. Nos resultados da pesquisa, adicione o auxiliar `if`.

      O editor de expressão mostra esta expressão:

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-12.png)

4. Remova essa condição da expressão:

   ```handlebars
   {%else if condition2%} render_2
   ```

   Este exemplo mostra a expressão modificada:

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

5. Adicione o token de nome de produto à condição:
   1. Remova o espaço reservado &quot;condition1&quot; da expressão.
   2. Na lista, selecione **[!UICONTROL Context]**.
   3. Selecione **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]*** e expanda o nó **[!UICONTROL productListItems]**.

      Neste exemplo, *event_name* representa o nome do seu evento.

   4. Adicione o token **[!UICONTROL Name]** à expressão.

      O editor de expressão mostra esta expressão:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-13.png)

6. Modifique a expressão:
   1. No Editor de expressão, especifique o nome do produto após o token `name`.

      Use essa sintaxe, onde *product_name* representa o nome do seu produto:

      ```javascript
      = "product_name"
      ```

      Neste exemplo, o nome do produto é &quot;Jaqueta de Juno&quot;:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   2. Substitua o espaço reservado &quot;render_1&quot; pelo texto da nota.

      Exemplo:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```
   3. Remova o espaço reservado &quot;default_render&quot; da expressão.
7. Clique em **[!UICONTROL Validate]** e depois em **[!UICONTROL Save]**.

   ![](../assets/personalization-uc-helpers-14.png)

8. Salve e publique a mensagem.

## Etapa 6: Testar e publicar a jornada {#test-and-publish}

1. Abra a jornada. Se a jornada já estiver aberta, atualize a página.
2. Ative a opção **[!UICONTROL Test]** e clique em **[!UICONTROL Trigger an event]**.

   Você pode ativar o modo de teste somente depois de publicar a mensagem.

   ![](../assets/personalization-uc-helpers-15.png)

3. Na janela **[!UICONTROL Event configuration]**, insira os valores de entrada e clique em **[!UICONTROL Send]**.

   O modo de teste funciona somente com perfis de teste.

   ![](../assets/personalization-uc-helpers-16.png)

   O email é enviado para o endereço do perfil de teste.

   Neste exemplo, o email contém a nota sobre a Jaqueta de Juno porque este produto está no carrinho:

   ![](../assets/personalization-uc-helpers-17.png)

4. Verifique se não há erro e publique a jornada.


## Tópicos relacionados

### Funções de handlebars

* [Auxiliares](functions/helpers.md)

* [Funções de string](functions/string.md)

### Casos de uso

* [Personalização com informações, contexto e oferta do perfil](personalization-use-case.md)

* [Personalização com oferta baseada em decisões](../offers/offers-e2e.md)

## Tutorial em vídeo{#helper-functions-video}

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)