---
solution: Journey Optimizer
product: journey optimizer
title: Integrar com o Marketo Engage
description: Saiba como usar a ação do Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: integração do marketo, marketo engage
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: d92c280e40419d2e3ec62a7ba85cd492a0867fde
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 4%

---

# Integrar com o Marketo Engage {#integrating-with-marketo-engage}

Embarque em uma jornada de integração perfeita de dados com o Marketo Engage. Uma ação personalizada específica está disponível em suas jornadas para integrar o Adobe Journey Optimizer e o Marketo Engage. Essa ação personalizada oferece suporte à assimilação de dois tipos de dados principais:

* **Pessoas** (Perfis): o Marketo transforma perfis em insights acionáveis.
* **Objetos personalizados**: adapte seus dados com objetos personalizados, como produtos, para uma abordagem de marketing personalizada.

## Pré-requisitos {#prerequisites}

Os seguintes pré-requisitos se aplicam a essa integração:

* A instância do cliente do Marketo Engage deve ser habilitada para IMS
* A instância do Marketo Engage e a instância do Adobe Experience Platform/Journey Optimizer devem estar na mesma organização
* O cliente deve ser provisionado com **MktoSync: acesso ao Serviço de Assimilação**

## Configurar a ação {#configure-marketo-action}


No Journey Optimizer, você deve configurar uma ação personalizada para o Marketo Engage. Siga estas etapas:

1. Selecione **[!UICONTROL Configurações]** na seção de menu ADMINISTRAÇÃO.
1. Na seção **[!UICONTROL Ações]**, clique em **[!UICONTROL Criar Ação]**. O painel de configuração de ação é aberto no lado direito da tela.
1. Insira o Nome, a Descrição e selecione **Adobe Marketo Engage** como **Tipo de ação**

![](assets/engage-customaction-creation.png){width="40%" align="left"}

1. Clique no ícone de **Editar carga** para suas cargas de **Solicitação** e **Resposta**.
1. Para ambos, componha sua carga útil e cole-a no pop-up dedicado.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

1. Inspecionar e configurar valores de payload
Observação: para passar valores dinamicamente, para cada campo, altere **Constante** para **Variável**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. Clique em **Salvar** na tela Configuração de campo e **Salvar** sua ação personalizada.

Agora você pode usar sua ação personalizada na tela de jornada.

## Sintaxe da carga útil {#payload-syntax}

### Pessoa

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**Exemplo de carga para a pessoa**

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

**Exemplo de carga para o objeto personalizado**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## Usar a ação {#engage-using}

Para cada ação configurada, uma atividade de ação do Marketo Engage está disponível na paleta do designer de jornada.

Para usá-lo, siga estas etapas:

1. Arraste a ação personalizada para a tela de jornada.

1. Insira o rótulo e a descrição desta ação.

1. Na seção **Solicitar parâmetros**, clique no ícone **Editar** para cada um dos parâmetros e selecione os valores dinâmicos que você configurou na carga.

![](assets/engage-use-canvas.png){width="70%" align="left"}
