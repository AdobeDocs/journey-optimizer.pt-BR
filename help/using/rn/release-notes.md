---
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ac3c49c16a2496b3d5bc9b803589644b69c6565c
workflow-type: ht
source-wordcount: '487'
ht-degree: 100%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target=&quot;_blank&quot;}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [Informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Versão de junho de 2022 {#june-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Enviar SMS para seus usuários (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar, personalizar e enviar SMS no Journey Optimizer por meio de uma integração com o <b>Sinch</b> ou <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>No momento, o canal SMS está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.</p>
<p>Saiba como criar e enviar um SMS nesta <a href="../messages/create-sms.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Encontre imagens impactantes mais rapidamente com a integração do Adobe Stock</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O plug-in de integração do Designer de email do Adobe Stock e Adobe Journey Optimizer fornece aos clientes uma maneira fácil de navegar, licenciar e salvar imagens para uso na criação de mensagens. </br> A nova opção <b>Localizar fotos semelhantes do Stock</b> também permite localizar fotos do Stock que correspondam ao conteúdo, cor e composição de suas imagens. </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>Para obter mais informações, consulte a <a href="../design/stock.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar Email Cco em todos os seus emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar o recurso Email Cco (com cópia oculta) para armazenar emails enviados pelo Adobe Journey Optimizer. Ative essa opção nas predefinições de email para que cada email enviado seja copiado de forma oculta para o endereço do Cco.</p>
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>Para obter mais informações, consulte a <a href="../configuration/bcc-email.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copiar objetos entre sandboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível transferir as experiências de uma sandbox do Journey Optimizer para outra, por exemplo, criando uma sandbox de produção a partir de uma sandbox de não produção. Esse novo recurso copia uma jornada inteira de um ambiente para outro, incluindo todos os objetos dos quais ela depende para ser executada corretamente. Além das Jornadas, também é possível copiar outros componentes, como Ofertas, Mensagens, Esquemas, Conjuntos de dados, Fontes de dados, Eventos e Ações.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/copy-to-sandbox.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Melhorias

**Gestão de decisões**

* **Compatibilidade com arquivos HTML e JSON** - agora, é possível arrastar e soltar arquivos HTML e JSON externos da biblioteca de ativos da Adobe Experience Cloud para o conteúdo de representação da oferta. [Saiba mais](../offers/offer-library/add-representations.md#html-json)


**Email**

* **Salvar como modelo** - agora, você pode salvar um conteúdo de email como modelo e reutilizá-lo ao criar outras mensagens. [Saiba mais](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**Administração**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **Visualizar parâmetros de URL de rastreamento** - ao configurar uma predefinição de mensagem, se você definir parâmetros de rastreamento de URL, uma visualização dinâmica do URL de rastreamento resultante será exibida. [Saiba mais](../configuration/email-settings.md#url-tracking)

* **Edição de predefinição de mensagem** - Agora, ao atualizar uma predefinição de mensagem, o tempo de processamento pode levar até 3 horas. [Saiba mais](../configuration/message-presets.md#edit-message-preset)

* **Edição de pool de IPs** - Agora, ao atualizar um pool de IPs, o tempo de processamento pode levar até 3 horas. [Saiba mais](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
