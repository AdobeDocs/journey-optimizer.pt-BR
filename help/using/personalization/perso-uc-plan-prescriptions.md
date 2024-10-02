---
title: Exemplos de Personalization de modelo
description: Exemplos do Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
source-git-commit: c7ecfdbc9c97c49c77f3c4fb8bcb1656e04819a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# Email de receitas do plano de saúde {#plan-prescription}

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

>[!TAB Modelo de HTML]

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
