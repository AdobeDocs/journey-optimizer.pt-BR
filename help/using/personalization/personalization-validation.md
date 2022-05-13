---
title: Validação de personalização
description: Saiba mais sobre a validação de personalização e como solucionar problemas.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---

# Validação de personalização {#personalization-validation}

## Mecanismos de validação {#validation-mechanisms}

No **Editor de expressão** use a **Validar** para verificar a sintaxe de personalização.

>[!NOTE]
> A validação é executada automaticamente ao clicar no botão **Adicionar** para fechar a janela do editor.

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Se a sintaxe de personalização não for válida, não será possível fechar a janela do editor de expressão.

## Erros comuns {#common-errors}

* **Caminho &quot;XYZ&quot; não encontrado**

Ao tentar fazer referência a um campo que não está definido no esquema.

Nesse caso **firstName1** não é definido como atributo no schema de perfil:

```
{{profile.person.name.firstName1}}
```

* **Incompatibilidade de tipo para a variável &quot;XYZ&quot;. Matriz esperada. Sequência de caracteres encontrada.**

Ao tentar iterar sobre uma string em vez de array:

Nesse caso **produto** não é uma matriz:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintaxe de handlebars inválida. Encontrado`‘[XYZ}}’`**

Quando uma sintaxe de handlebars inválida é usada.

As expressões Handlebars são cercadas por **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Definição de segmento inválida**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Erros específicos relacionados às ofertas {#specific-errors}

Os erros relacionados à integração de ofertas em um email ou mensagem de push têm o seguinte padrão:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

A validação é realizada durante a publicação da mensagem ou durante a validação do conteúdo de personalização no editor de expressão.

<table> 
 <thead> 
  <tr> 
   <th> Título do erro<br /> </th> 
   <th> Validação / Resolução <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Recurso com id placementID e tipo OfferPlacement não encontrado <br/>
Recurso com id activityID e tipo OfferActivity não encontrado<br/></td> 
   <td>Verifique se ActivityID e/ou PlacementID estão disponíveis</td> 
  </tr> 
   <tr> 
   <td>O recurso não pôde ser validado.</td> 
   <td>O componentType na Disposição deve corresponder à oferta offerType</td> 
  </tr> 
   <tr> 
   <td>O URL público não está presente em offerId.</td> 
   <td>As Ofertas de imagem (todas Personalizadas e de fallback associadas à decisão e ao par de disposições) devem ter o URL público preenchido (deliveryURL não deve estar vazio).</td> 
  </tr> 
  <tr> 
   <td>A decisão contém atributos que não são de perfil.</td> 
   <td>O uso do Modelo de ofertas deve conter somente os atributos do perfil.</td> 
  </tr> 
  <tr> 
   <td>Ocorreu um erro ao obter o uso de decisão.</td> 
   <td>Esse erro pode ocorrer quando a API está tentando buscar o modelo de oferta.</td> 
  </tr>
  <tr> 
   <td>O atributo de oferta Atributo de Oferta é inválido.</td> 
   <td>Verifique se o atributo de oferta referenciado no drp de oferta é válido. A seguir estão os atributos válidos: <br/>
Imagem: deliveryURL, linkURL<br/>
Texto: conteúdo<br/>
HTML: conteúdo<br/></td> 
  </tr> 
 </tbody> 
</table>
