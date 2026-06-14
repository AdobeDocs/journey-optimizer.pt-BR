---
title: Exemplos de Personalization de modelo
description: Exemplos do Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: cb09dcb7-3367-4b63-b02c-8a1356eb876eid: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: 378c98d4dc9552de3eed68eda59d9917c2b56347
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# Email de receitas do plano de saúde {#plan-prescription}

>[!BEGINSHADEBOX]

**Nesta página:** Siga um caso de uso de personalização que repete as matrizes de perfis aninhadas com regras condicionais para criar uma lista de receitas de email de plano de integridade prontas para retirada ou rechamada.

>[!ENDSHADEBOX]

Um perfil contém planos de integridade e cada plano inclui receitas. As prescrições têm vários estados, como &quot;pronto&quot;, &quot;recuperação&quot; ou &quot;recolhido&quot;.

Nesse caso de uso, queremos enviar um único email para cada perfil, incluindo todas as receitas que estão prontas para coleta ou para recall. Clique em cada guia abaixo para obter mais informações sobre a sintaxe a ser usada para implementar esse caso de uso.

>[!BEGINTABS]

>[!TAB Mensagem renderizada]

<p>Oi, John Doe.</p>
<p>Estas são as receitas que estão prontas para coleta ou foram recuperadas:</p>

**Plano de Integridade A**

<ul>

<li>
      <strong>ID de prescrição:</strong> pres1<br>
      <strong>Nome:</strong> Medicação A<br>
      <strong>Estado:</strong> pronto
   </li>

<li>
      <strong>ID de prescrição:</strong> pres2<br>
      <strong>Nome:</strong> Medicação B<br>
      <strong>Estado:</strong> rechamada
   </li>

</ul>

**Plano de Integridade B**

<ul>

<li>
      <strong>ID de prescrição:</strong> pres4<br>
      <strong>Nome:</strong> Medicação D<br>
      <strong>Estado:</strong> pronto
   </li>

</ul>

>[!TAB Modelo do HTML]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB Dados do perfil]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]
