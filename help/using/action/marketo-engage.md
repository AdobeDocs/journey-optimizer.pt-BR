---
solution: Journey Optimizer
product: journey optimizer
title: Integrar com o Marketo Engage
description: Saiba como usar a ação do Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: integração do marketo, marketo engage
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
TQID: https://experienceleague.adobe.com/-aRINahKmp9bI1tyW-XA-LzZOFeoEPXpWoH8JydG6Rk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 3%

---

# Integrar com o Marketo Engage {#integrating-with-marketo-engage}

>[!BEGINSHADEBOX]

**Nesta página:** Configure e use a ação personalizada do Marketo Engage para sincronizar dados de pessoas e objetos personalizados de suas jornadas com a Marketo Engage.

>[!ENDSHADEBOX]

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
   ![](assets/engage-customaction-creation.png){width="40%"}
1. Clique no ícone de **Editar carga** para suas cargas de **Solicitação** e **Resposta**.
1. Para ambos, componha sua carga útil e cole-a no pop-up dedicado.
   ![](assets/engage-customaction-payload.png){width="70%"}
1. Inspecionar e configurar valores de payload

   Observação: para passar valores dinamicamente, para cada campo, altere **Constante** para **Variável**.

   ![](assets/engage-customaction-payload-fields.png){width="70%"}

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

![](assets/engage-use-canvas.png){width="70%"}
