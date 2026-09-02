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
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 1%

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
      <strong>Nome:</strong> Medication D<br>
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

## Referência rápida {#quick-reference}

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

>[!BEGINTABS]

>[!TAB Visão geral]

**TL;DR**

Esta página demonstra um caso de uso de personalização completo: iteração em matrizes de perfis aninhadas (planos de integridade contendo receitas) com filtragem condicional para exibir apenas as receitas nos estados &quot;pronto&quot; ou &quot;recuperação&quot; em um email.

**Intenções**

* Veja um exemplo de saída renderizada de um email personalizado de plano de integridade
* Compreender o modelo HTML usando blocos `{{#each}}` e `{%#if%}` aninhados para iteração de matriz condicional
* Entenda a estrutura de dados de perfil necessária: uma matriz `plans` em que cada plano contém uma matriz `prescriptions` com campos `state`

>[!TAB Glossário]

* **Iteração aninhada**: usar `{{#each}}` loops dentro de outros `{{#each}}` loops para atravessar estruturas de matriz de vários níveis nos dados do perfil (por exemplo, planos → receitas).
* **Estado de prescrição**: um campo em cada objeto de prescrição indicando seu status de ciclo de vida neste caso de uso. Os valores usados são &quot;pronto&quot;, &quot;rechamar&quot; e &quot;selecionado&quot;. *(caso de uso específico)*
* **`{%#if%}`/`{%/if%}`**: Sintaxe de bloco condicional usada em modelos de mensagem para filtrar itens de matriz durante a iteração (distinta da sintaxe Handlebars `{{#if}}` com duas curvas).

>[!TAB Terminologia]

* **Nome canônico:** iteração de matriz aninhada — variantes: loops aninhados, cada um aninhado, iteração de vários níveis
* **Não confunda:** `{{#each}}` / `{{/each}}` (Sintaxe de iteração de Handlebars, chaves duplas) ≠ `{%#if%}` / `{%/if%}` (sintaxe condicional, chaves percentuais) — ambos são usados juntos neste modelo
* **Não confundir:** &quot;pronto&quot; (receita disponível para retirada) ≠ &quot;recall&quot; (a receita foi retirada) ≠ &quot;retirado&quot; (a receita já foi coletada — excluída da saída pelo filtro condicional)

>[!TAB Perguntas frequentes]

**P: Quais estados de prescrição são incluídos na saída de email?**

Somente as receitas com o estado &quot;pronto&quot; ou &quot;recuperação&quot; são exibidas. As prescrições com o estado &quot;selecionado&quot; são excluídas pelo filtro condicional `{%#if prescription.state = "ready" or prescription.state = "recall"%}`.

**P: Qual estrutura de dados de perfil é necessária para este caso de uso?**

Um perfil com uma matriz `plans`, em que cada objeto de plano contém uma matriz `prescriptions`. Cada objeto de receita deve ter campos `prescription_id`, `name` e `state`.

**P: Como os planos e as receitas são iterados no modelo?**

O loop `{{#each profile.plans as |plan|}}` externo repete cada plano de integridade. Dentro dele, `{{#each plan.prescriptions as |prescription|}}` repete as prescrições de cada plano e um bloco condicional filtra somente para os estados &quot;pronto&quot; ou &quot;recuperação&quot;.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 4b68d597 -->
