---
title: Fórmulas de classificação
description: Saiba como criar fórmulas para classificar ofertas
feature: Ranking, Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: baf76d3c571c62105c1f0a59e07ca70e61a83cc6
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 3%

---

# Fórmulas de classificação {#create-ranking-formulas}

## Sobre fórmulas de classificação {#about-ranking-formulas}

**As fórmulas de classificação** permitem definir regras que determinarão qual oferta deve ser apresentada primeiro para determinado posicionamento, em vez de levar em conta as pontuações de prioridade das ofertas.

As fórmulas de classificação são expressas em **sintaxe PQL** e podem aproveitar atributos de perfil, dados de contexto e atributos de oferta. Para obter mais informações sobre como usar a sintaxe do PQL, consulte a [documentação dedicada](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=pt-BR).

Depois que uma fórmula de classificação é criada, é possível atribuí-la a uma inserção em uma decisão. Para obter mais informações, consulte [Configurar seleção de ofertas em decisões](../offer-activities/configure-offer-selection.md).

## Criar uma fórmula de classificação {#create-ranking-formula}

Para criar uma fórmula de classificação, siga as etapas abaixo:

1. Acesse o menu **[!UICONTROL Componentes]** e selecione a guia **[!UICONTROL Classificação]**. A guia **[!UICONTROL Fórmulas]** é selecionada por padrão. A lista de fórmulas criadas anteriormente é exibida.

   ![](../assets/rankings-list.png)

1. Clique em **[!UICONTROL Criar classificação]** para criar uma nova fórmula de classificação.

   ![](../assets/ranking-create-formula.png)

1. Especifique o nome, a descrição e a fórmula da fórmula.

   Neste exemplo, queremos aumentar a prioridade de todas as ofertas com o atributo &quot;quente&quot; se o tempo real estiver quente. Para fazer isso, o **contextData.weather=hot** foi passado na chamada de decisão.

   ![](../assets/ranking-syntax.png)

   >[!IMPORTANT]
   >
   >Ao criar uma fórmula de classificação, a retrospectiva para um período anterior não é compatível. Por exemplo, se você especificar um evento de experiência que ocorreu no último mês como um componente da fórmula. Qualquer tentativa de incluir um período de lookback durante a criação de uma fórmula acionará um erro ao salvá-la.

1. Clique em **[!UICONTROL Salvar]**. Sua fórmula de classificação é criada, você pode selecioná-la na lista para obter detalhes e editá-la ou excluí-la.

   Agora ele está pronto para ser usado em uma decisão para classificar ofertas qualificadas para um posicionamento (consulte [Configurar seleção de ofertas em decisões](../offer-activities/configure-offer-selection.md)).

   ![](../assets/ranking-formula-created.png)

## Exemplos de fórmula de classificação {#ranking-formula-examples}

Você pode criar muitas fórmulas de classificação diferentes de acordo com suas necessidades. Abaixo estão alguns exemplos.

<!--
Boost by offer ID

Boost the priority of an offer with the offer ID *xcore:personalized-offer:13d213cd4cb328ec* by 5.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec", offer.rank.priority + 5, offer.rank.priority)
```

Change the offer priority based on a certain profile attribute

Set the offer priority to 30 for offer *xcore:personalized-offer:13d213cd4cb328ec* if the user lives in the city of Bondi.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec" and homeAddress.city.equals("Bondi", false), 30, offer.rank.priority)
```

Boost multiple offers by offer ID based on the presence of a profile's audience membership

Boost the priority of offers based on whether the user is a member of a priority audience, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.get("prioritySegmentId")).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### Aumente as ofertas com determinado atributo de oferta com base no atributo de perfil

Se o perfil estiver na cidade correspondente à oferta, duplique a prioridade para todas as ofertas nessa cidade.

**Fórmula de classificação:**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Impulsione ofertas em que a data final seja anterior a 24 horas a partir de agora

**Fórmula de classificação:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### Aumente as ofertas com determinado atributo de oferta com base nos dados de contexto

Aumente determinadas ofertas com base nos dados de contexto transmitidos na chamada de decisão. Por exemplo, se `contextData.weather=hot` for passado na chamada de decisão, a prioridade de todas as ofertas com `attribute=hot` deverá ser aumentada.

**Fórmula de classificação:**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.get("weather")=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

Observe que, ao usar a API de decisão, os dados de contexto são adicionados ao elemento do perfil no corpo da solicitação, como no exemplo abaixo.

**Trecho do corpo da solicitação:**

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
 }],
```

### Aumente as ofertas com base na propensão dos clientes para comprar o produto oferecido

Você pode aumentar a pontuação de uma oferta com base em uma pontuação de propensão do cliente.

Neste exemplo, o locatário da instância é *_salesvelocity* e o esquema de perfil contém um intervalo de pontuações armazenadas em uma matriz:

![](../assets/ranking-example-schema.png)

Diante disso, para um perfil como:

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

As ofertas conteriam um atributo para *propensityType* que corresponde à categoria das pontuações:

![](../assets/ranking-example-propensityType.png)

Sua fórmula de classificação pode então definir a prioridade de cada oferta para igualar a *propensityScore* dos clientes para esse *propensityType*. Se nenhuma pontuação for encontrada, use a prioridade estática definida na oferta:

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.get("propensityType"), false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
