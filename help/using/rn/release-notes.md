---
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 65c2ba7e0931f449a29d1e7ff01d6d68fccca448
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 36%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target=&quot;_blank&quot;}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [Informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Versão de maio de 2022 {#may-2022-release}

### Novos recursos

<!--table>
<thead>
<tr>
<th><strong>Message Frequency Rules</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now set cross-channel business rules that will automatically exclude over-solicited profiles from messages and actions.</p>
<img src="assets/frequency-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/frequency-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Availability date: <strong>May, 31</strong></p>
<p>You can now use the Email BCC (blind carbon copy) capability to store emails sent by Adobe Journey Optimizer. Enable this option in your email presets so that every email sent is blind-copied to your BCC address.</p>
<img src="assets/bcc-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/email-settings.md#bcc-email">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Gerenciamento de decisões - Modelo de otimização automática de classificação AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar sistemas de modelo treinados no Gerenciamento de decisões. Esse novo recurso classifica as ofertas para exibição em um determinado perfil.</p>
<img src="assets/optimization.gif"/>
<p>Para obter mais informações, consulte a <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Logs de auditoria do Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível monitorar ações executadas por usuários nos recursos do Adobe Journey Optimizer.</p>
<img src="assets/audit-rn.gif"/>
<p>Para obter mais informações, consulte a <a href="../reports/audit-logs.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Personalização**

* **Nova função auxiliar para ocultação de caracteres** - O `mask` A função auxiliar permite substituir uma parte de uma string por caracteres &quot;X&quot;. [Saiba mais](../personalization/functions/string.md#mask)

**Páginas de aterrissagem**

* **Landing pages sem um formulário** - Agora é possível criar e publicar uma landing page que não contenha um formulário e não exija nenhuma ação dos visitantes.
* **Templates de landing page** - Agora é possível salvar uma landing page como template e reutilizá-la ao criar outras landing pages. [Saiba mais](../landing-pages/lp-templates.md)
* **Voltar à página principal** - Agora é possível adicionar um link para a página primária a partir de qualquer subpágina na mesma página de aterrissagem.
* **Suporte a JavaScript personalizado** - Agora é possível adicionar JavaScript personalizado ao conteúdo da página de aterrissagem para executar estilos avançados ou adicionar comportamentos personalizados às páginas de aterrissagem.	[Saiba mais](../landing-pages/lp-custom-js.md)

<!--**Decision management**

* **HTML and JSON files support** - You can now drag and drop external HTML and JSON files from the AEM repository into the offer representation content.-->

**Jornadas**

* **Ler segmento** - jornadas de segmento de Leitura única agora são movidas para o status Finished 30 dias após a execução da jornada. Para segmentos de Leitura agendados, é de 30 dias após a execução da última ocorrência. [Leia mais](../building-journeys/read-segment.md)
* **Editor de expressão** - O [limite](../building-journeys/functions/functionlimit.md) foi adicionada para permitir que você limite o número de itens de uma lista. O [sort](../building-journeys/functions/functionsort.md) agora permite classificar um objeto de lista. O suporte a listObject também foi adicionado ao [disctinct](../building-journeys/functions/functiondistinct.md) e [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) funções.
