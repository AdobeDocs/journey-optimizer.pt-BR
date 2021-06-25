---
title: Validação de personalização
description: Saiba mais sobre a validação de personalização e como solucionar problemas
feature: Personalização
topic: Personalização
role: Data Engineer
level: Intermediate
source-git-commit: 94f3fb815fdeec9853351be9bc41b0579cfc6c5b
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 2%

---


# Validação de personalização {#personalization-validation}

## Mecanismos de validação

Na tela **Editor de expressão**, use o botão **Validar** para verificar a sintaxe de personalização.

>[!NOTE]
> A validação é executada automaticamente ao clicar no botão **Add** para fechar a janela do editor.


![](assets/perso_validation1.png)

>[!IMPORTANT]
> Se a sintaxe de personalização não for válida, não será possível fechar a janela do editor de expressão.


## Erros comuns

* **Caminho &quot;XYZ&quot; não encontrado**

Ao tentar fazer referência a um campo que não está definido no esquema.

Nesse caso, **firstName1** não está definido como atributo no schema de perfil:

```
{{profile.person.name.firstName1}}
```

* **Incompatibilidade de tipo para a variável &quot;XYZ&quot;. Matriz esperada. Sequência de caracteres encontrada.**

Ao tentar iterar sobre uma string em vez de array:

Nesse caso, **product** não é uma matriz:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintaxe de handlebars inválida. Encontrado`‘[XYZ}}’`**

Quando uma sintaxe de handlebars inválida é usada.

As expressões Handlebars são cercadas com **{{expression}**

```
   {{[profile.person.name.firstName}}
```

* **Definição de segmento inválida**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Erros específicos relacionados às ofertas

Os erros relacionados à integração de ofertas em um email ou mensagem de push têm o seguinte padrão:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

A validação é realizada durante a publicação da mensagem ou durante a validação do conteúdo de personalização no editor de expressão.

<table> 
 <thead> 
  <tr> 
   <th> Título do erro<br /> </th> 
   <th> Validação/Resolução <br /> </th> 
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
   <td>A decisão (anteriormente conhecida como atividade de oferta) contém atributos que não são de perfil.</td> 
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
Texto: content<br/>
HTML: conteúdo<br/></td> 
  </tr> 
 </tbody> 
</table>

