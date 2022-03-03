---
title: Criar fórmulas de classificação
description: Saiba como criar fórmulas para classificar ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: 14ab70aa32f4f7978b8c72b3981d3b55f56fd08b
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 1%

---

# Criar fórmulas de classificação {#create-ranking-formulas}

## Sobre fórmulas de classificação {#about-ranking-formulas}

**Fórmulas de classificação** permite definir regras que determinam qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas.

As fórmulas de classificação são expressas em **Sintaxe PQL** e podem aproveitar atributos de perfil, dados de contexto e atributos de oferta. Para obter mais informações sobre como usar a sintaxe PQL, consulte [documentação dedicada](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

Depois que uma fórmula de classificação é criada, você pode atribuí-la a uma disposição em uma decisão. Para obter mais informações, consulte [Configurar seleção de ofertas em decisões](../offer-activities/configure-offer-selection.md).

## Criar uma fórmula de classificação {#create-ranking-formula}

Para criar uma fórmula de classificação, siga as etapas abaixo:

1. Acesse o **[!UICONTROL Components]** , em seguida, selecione o **[!UICONTROL Rankings]** guia . A lista de classificações criadas anteriormente é exibida.

   ![](../assets/rankings-list.png)

1. Clique em **[!UICONTROL Create ranking]** para criar uma nova fórmula de classificação.

   ![](../assets/ranking-create-formula.png)

1. Especifique o nome da fórmula de classificação, a descrição e a fórmula.

   Neste exemplo, queremos aumentar a prioridade de todas as ofertas com o atributo &quot;quente&quot; se o tempo real estiver quente. Para fazer isso, o **contextData.weather=hot** foi passada na chamada de decisão.

   ![](../assets/ranking-syntax.png)

1. Clique em **[!UICONTROL Save]**. Sua fórmula de classificação é criada, você pode selecioná-la na lista para obter detalhes e editá-la ou excluí-la.

   Agora ele está pronto para ser usado em uma decisão para classificar ofertas elegíveis para uma disposição (consulte [Configurar seleção de ofertas em decisões](../offer-activities/configure-offer-selection.md)).

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

Boost multiple offers by offer ID based on the presence of a profile's segment membership

Boost the priority of offers based on whether the user is a member of a priority segment, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.prioritySegmentId).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### Aumentar ofertas com determinado atributo de oferta com base no atributo de perfil

Se o perfil estiver na cidade correspondente à oferta, então duplique a prioridade para todas as ofertas nessa cidade.

**Fórmula de classificação:**

```
if( offer.characteristics.city = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Aumente as ofertas em que a data final será menos de 24 horas a partir de agora

**Fórmula de classificação:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### Aumente as ofertas com determinado atributo de oferta com base nos dados de contexto

Impulsione determinadas ofertas com base nos dados de contexto que estão sendo transmitidos na chamada de decisão. Por exemplo, se a variável `contextData.weather=hot` é passada na chamada de decisão, a prioridade de todas as ofertas com `attribute=hot` deve ser potenciado.

**Fórmula de classificação:**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

Observe que, ao usar a API de decisão, os dados de contexto são adicionados ao elemento de perfil no corpo da solicitação, como no exemplo abaixo.

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

### Aumente as ofertas com base na propensão do cliente para comprar o produto que está sendo oferecido

Se houver duas instâncias de *CustomerAI* cálculo da propensão de compra *TravelInsurance* e *extraBaggauge* para uma companhia aérea, a seguinte fórmula de classificação aumentará a prioridade (em 50 pontos) da oferta específica para seguro ou bagagem se a pontuação de propensão do cliente para comprar esse produto for maior que 90.

Mas porque cada *CustomerAI* A instância cria seu próprio objeto no esquema de perfil unificado, não é possível selecionar dinamicamente a pontuação com base no tipo de propensão da oferta. Assim você tem que encadear a `if` instruções para verificar primeiro o tipo de propensão da oferta e, em seguida, extrair a pontuação do campo de perfil apropriado.

**Fórmula de classificação:**

```
if ( offer.characteristics.propensityType = "extraBaggagePropensity" and _salesvelocity.CustomerAI.extraBaggagePropensity.score > 90, offer.rank.priority + 50,
    (
        if ( offer.characteristics.propensityType = "travelInsurancePropensity" and _salesvelocity.CustomerAI.insurancePropensity.score > 90, offer.rank.priority + 50, offer.rank.priority )
    )
)
```

Uma solução melhor é armazenar as pontuações em uma matriz do perfil. O exemplo a seguir funcionará em uma variedade de diferentes pontuações de propensão usando apenas uma fórmula de classificação simples. A expectativa é que você tenha um esquema de perfil com uma matriz de pontuações. Neste exemplo, o locatário da instância é *_salesvelocity* e o schema de perfis contém o seguinte:

![](../assets/ranking-example-schema.png)

Considerando isso, para um perfil como:

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

Sua fórmula de classificação pode definir a prioridade de cada oferta para ser igual aos clientes *pontuação de propensão* para *propensityType*. Se nenhuma pontuação for encontrada, use a prioridade estática definida na oferta:

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.propensityType, false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
