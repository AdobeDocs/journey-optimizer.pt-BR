---
solution: Journey Optimizer
product: journey optimizer
title: Validação de personalização
description: Saiba mais sobre a validação de personalização e como solucionar problemas.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, validação, erros, personalização
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 155ae8ef14e5482d94e54b15962afa09aa6826fc
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 2%

---

# Validação de personalização {#personalization-validation}

## Mecanismos de validação {#validation-mechanisms}

Na tela do **editor de personalização**, use o botão **Validar** para verificar sua sintaxe de personalização.

>[!NOTE]
> A validação é executada automaticamente quando você clica no botão **Adicionar** para fechar a janela do editor.
>

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Se a sintaxe de personalização não for válida, não será possível fechar a janela do editor de personalização.
>

## Erros comuns {#common-errors}

* **Caminho &quot;XYZ&quot; não encontrado**

Ao tentar referenciar um campo que não está definido no esquema.

Nesse caso, **firstName1** não está definido como atributo no esquema de perfil:

```
{{profile.person.name.firstName1}}
```

* **Incompatibilidade de tipo para a variável &quot;XYZ&quot;. Matriz esperada. Cadeia de caracteres encontrada.**

Ao tentar iterar sobre uma cadeia de caracteres em vez de uma matriz:

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

## Erros específicos relacionados às ofertas {#specific-errors}

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
