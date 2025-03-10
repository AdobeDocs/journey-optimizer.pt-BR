---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar personalização
description: Saiba como trabalhar com o editor de personalização para adicionar personalização.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, sobre, iniciar
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 78c1464ccddec75e4827cbb1877d8fab5ac08b90
workflow-type: tm+mt
source-wordcount: '1410'
ht-degree: 5%

---

# Adicionar personalização {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Sobre o editor de personalização"
>abstract="O editor de personalização permite selecionar, organizar, personalizar e validar todos os dados para criar um conteúdo personalizado."

O editor de personalização é a peça central da personalização em [!DNL Journey Optimizer]. Ele está disponível em todos os contextos em que você precisa definir a personalização, como emails, push e ofertas.

Na interface do editor de personalização, você pode selecionar, organizar, personalizar e validar todos os dados para criar uma personalização personalizada para seu conteúdo.

![](assets/perso_ee1.png)

## Onde posso adicionar personalização

Você pode adicionar personalização em **[!DNL Journey Optimizer]** em todos os campos com o ícone ![adicionar personalização](assets/do-not-localize/add-perso-icon.svg).

### Mensagens

Nas mensagens, a personalização pode ser adicionada em locais diferentes, como o campo **[!UICONTROL Linha de assunto]**.

![](assets/perso_subject.png)

Ele também pode ser adicionado em outras seções do seu conteúdo. Por exemplo, para [notificações por push](../push/push-gs.md), a personalização pode ser adicionada nos campos **Título**, **Corpo**, **Som personalizado**, **Medalhas** e **Dados personalizados**.

### Email Designer

Ao editar o conteúdo de email na [Designer de email](../email/get-started-email-design.md), você pode adicionar personalização em blocos de texto e em URLs usando o ícone na barra de ferramentas contextual.

![](assets/perso_insert.png)

### Ofertas

Você pode adicionar personalização ao usar conteúdo do tipo texto em suas representações de **ofertas**. [Saiba como criar ofertas personalizadas](../offers/offer-library/creating-personalized-offers.md)

### URLs

O Journey Optimizer também permite personalizar **URLs** em sua mensagem.  Os URLs personalizados levam os destinatários para páginas específicas de um site ou para um microsite personalizado, dependendo dos atributos do perfil. A personalização de URL está disponível para estes tipos de links: **Link externo**, **Link de unsubscription** e **Opt-Out**.

+++Consulte exemplos de URLs personalizados

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

+++

![](assets/perso-url.png){width="50%"}

>[!NOTE]
>
>Ao editar um URL personalizado no editor de personalização, as funções auxiliares e a associação de públicos-alvo são desativadas por motivos de segurança.
>
>Não há suporte para espaços nos tokens de personalização usados em urls.

## Fontes do Personalization {#sources}

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização. As fontes disponíveis são:

* **[!UICONTROL Atributos do perfil]**: lista todas as referências associadas ao esquema de perfil descrito na [documentação do Modelo de Dados (XDM) do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.
* **[!UICONTROL Públicos-alvo]** : lista todos os públicos-alvo criados no serviço de Segmentação do Adobe Experience Platform. Mais informações sobre segmentação disponíveis [aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"}.
* **[!UICONTROL Decisões de oferta]** : lista todas as ofertas associadas a uma disposição específica. Selecione o posicionamento e insira as ofertas no conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Atributos contextuais]**: quando uma atividade de ação de canal (email, push, SMS) é usada em uma jornada ou campanha, os atributos contextuais relacionados a eventos e propriedades ficam disponíveis para personalização. Um exemplo de personalização que utiliza atributos contextuais é apresentado em [esta seção](personalization-use-case.md).

>[!NOTE]
>
>Se você estiver direcionando um público-alvo com atributos de enriquecimento gerados usando um fluxo de trabalho de composição, poderá aproveitar esses atributos de enriquecimento para personalizar sua mensagem. [Saiba como usar atributos de enriquecimento de públicos-alvo](../audience/about-audiences.md#enrichment)

## Adicionar personalização {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Preenchimento automático"
>abstract="Ativar essa opção permite que o sistema sugira e conclua automaticamente o código à medida que você digita. Esse recurso está disponível somente para formatos de HTML e Texto e é compatível com atributos de Perfil e Contexto. Se desativado por meio do botão de alternância, o editor fornecerá preenchimento automático do código HTML nativo."

O espaço de trabalho central é onde você cria sua sintaxe de personalização. Para usar um atributo para personalizar sua mensagem, localize-o no painel de navegação esquerdo e clique no botão `+` para adicioná-lo à expressão.

O menu de reticências ao lado do ícone `+` permite obter mais detalhes para cada atributo e adicionar os atributos usados com mais frequência aos favoritos. Os atributos adicionados aos favoritos podem ser acessados pelo menu **[!UICONTROL Favoritos]**, no painel de navegação esquerdo.

Além disso, você pode definir um texto de fallback padrão que será exibido se um atributo de perfil do tipo string estiver vazio. Para fazer isso, clique no botão de reticências ao lado do atributo e selecione **[!UICONTROL Inserir com texto alternativo]**. Escreva o texto que deve ser exibido por padrão se o valor do atributo estiver vazio para um perfil e clique em **[!UICONTROL Adicionar]**.

![](assets/attribute-details.png)

No exemplo a seguir, o editor de personalização permite selecionar os perfis que fazem aniversário hoje e, em seguida, concluir a personalização inserindo uma oferta específica correspondente a este dia.

![](assets/perso_ee2.png)

## Ferramentas para edição de expressão

O espaço de trabalho central fornece várias ferramentas para ajudar você a escrever sua expressão de personalização.

![](assets/perso-workspace.png)

As opções disponíveis são:

1. **[!UICONTROL Localizar]** / **[!UICONTROL Localizar e substituir]**: pesquise pela expressão e substitua automaticamente partes do código.
1. **[!UICONTROL Desfazer]** / **[!UICONTROL Refazer]**: Desfazer / Refazer a última operação.
1. **[!UICONTROL Preenchimento automático]**: sugere e conclui automaticamente o código à medida que você digita. Esse recurso está disponível somente para formatos de HTML e Texto e é compatível com atributos de Perfil e Contexto. Se desativado por meio do botão de alternância, o editor fornecerá preenchimento automático do código HTML nativo.

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL Text]**: identifique o formato do seu código. Isso permite que o sistema adapte a validação e o recurso de preenchimento automático com base no idioma selecionado.
1. **[!UICONTROL Validar]**: verifique a sintaxe da sua expressão. Saiba mais [nesta seção](../personalization/personalization-build-expressions.md).
1. **[!UICONTROL Salvar como fragmento]**: salve sua expressão como um fragmento de expressão. Saiba mais [nesta seção](../content-management/save-fragments.md#save-as-expression-fragment)
1. **[!UICONTROL Tamanho da fonte]**: ajusta o tamanho da fonte do conteúdo dentro do editor para melhorar a leitura.
1. **[!UICONTROL Quebra de texto]**: habilita ou desabilita a quebra automática de linha, permitindo que expressões longas sejam exibidas em uma única linha ou quebra automática no editor. As opções incluem:
   * **Desativado** (Padrão) - Sem quebra automática de linha. As linhas longas se estendem além da exibição do editor e exigem rolagem horizontal.
   * **Em** - Quebra linhas na largura do editor.
   * **Coluna de quebra automática de linha** - Quebra as linhas quando os caracteres de linha atingem 80 caracteres.
   * **Limitado** - Quebra as linhas na largura do editor ou em 80 caracteres, o que for menor.

No painel de navegação, recursos adicionais estão disponíveis para ajudar você a criar sua expressão de personalização.

![](assets/perso-features.png)

* **[!UICONTROL Funções auxiliares]** - As funções auxiliares permitem executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-las no contexto da personalização. [Saiba mais sobre funções auxiliares disponíveis](functions/functions.md)

* **[!UICONTROL Favoritos]** - Os atributos adicionados aos favoritos são exibidos nesta lista. Isso permite acessar rapidamente os itens usados com mais frequência. Para adicionar um atributo aos favoritos, clique no menu de reticências e escolha **[!UICONTROL Adicionar aos favoritos]**.

* **[!UICONTROL Condições]** - Aproveite as regras condicionais criadas na biblioteca para adicionar conteúdo dinâmico às suas mensagens. Isso permite criar várias variantes da mensagem com base em condições. [Saiba como criar conteúdo dinâmico](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL Fragmentos]** - Aproveite fragmentos de expressão que foram criados ou salvos na sandbox atual. Um fragmento é um componente reutilizável que pode ser referenciado em [!DNL Journey Optimizer] campanhas e jornadas. Essa funcionalidade permite pré-construir vários blocos de conteúdo personalizado que podem ser usados por usuários de marketing para reunir conteúdo rapidamente em um processo de design aprimorado. [Saiba como usar fragmentos de expressão para personalização](../personalization/use-expression-fragments.md)

Quando a expressão de personalização estiver pronta, será necessário validá-la pelo editor de personalização. Saiba mais [nesta seção](../personalization/personalization-build-expressions.md).

## Mecanismos de validação {#validation-mechanisms}

A validação da sua expressão é executada automaticamente quando você clica no botão **Adicionar** para fechar a janela do editor. Você também pode usar o botão **Validar** para verificar sua sintaxe de personalização.

![](assets/perso_validation1.png)

Expanda a seção abaixo para ver erros comuns que podem ocorrer ao validar a personalização.

+++Erros comuns

* **Caminho &quot;XYZ&quot; não encontrado**

Ao tentar referenciar um campo que não está definido no esquema.

Nesse caso, **firstName1** não está definido como atributo no esquema de perfil:

```
{{profile.person.name.firstName1}}
```

* **Incompatibilidade de tipo para a variável &quot;XYZ&quot;. Matriz esperada. Cadeia de caracteres encontrada.**

Ao tentar iterar sobre uma cadeia de caracteres em vez de uma matriz.

Neste caso, o **produto** não é uma matriz:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintaxe de manipuladores inválida. Encontrado`‘[XYZ}}’`**

Quando a sintaxe de manipuladores inválidos é usada.

Expressões Handlebars cercadas por **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Definição de segmento inválida**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

+++

Para ofertas, podem ocorrer erros específicos. Expanda a seção abaixo para obter mais detalhes:

+++ Erros específicos relacionados às ofertas

Os erros relacionados à integração de ofertas em uma mensagem de email ou push têm o seguinte padrão:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

A validação é executada durante a validação do conteúdo de personalização no editor de personalização.

<table> 
 <thead> 
  <tr> 
   <th> Título de erro <br /> </th> 
   <th> Validação/Resolução <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Recurso com id placementID e tipo OfferPlacement não encontrado <br/>
Recurso com id activityID e tipo OfferActivity não encontrado<br/></td> 
   <td>Verificar se ActivityID e/ou PlacementID estão disponíveis</td> 
  </tr> 
   <tr> 
   <td>O recurso não pôde ser validado.</td> 
   <td>O componentType no Posicionamento deve corresponder à oferta offerType</td> 
  </tr> 
   <tr> 
   <td>O URL público não está presente em offerId.</td> 
   <td>As Ofertas de imagem (todas as Personalizadas e substitutas associadas ao par de decisão e posicionamento) devem ter o URL público preenchido (deliveryURL não deve estar vazio).</td> 
  </tr> 
  <tr> 
   <td>A decisão contém atributos que não são de perfil.</td> 
   <td>O uso do modelo de ofertas deve conter somente os atributos do perfil.</td> 
  </tr> 
  <tr> 
   <td>Ocorreu um erro ao buscar o uso de decisão.</td> 
   <td>Esse erro pode ocorrer quando a API está tentando buscar o modelo de oferta.</td> 
  </tr>
  <tr> 
   <td>Atributo de oferta atributo de oferta inválido.</td> 
   <td>Verifique se o atributo de oferta referenciado na queda da oferta é válido. A seguir estão os atributos válidos: <br/>
Imagem: deliveryURL, linkURL<br/>
Texto: conteúdo<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>

+++
