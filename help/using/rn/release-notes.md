---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: ht
source-wordcount: '233'
ht-degree: 100%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target=&quot;_blank&quot;}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [Informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.


## Versão de outubro de 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Melhorias {#oct-2022-improvements}

**Jornadas**

* A opção de **Forçar a reentrada na recorrência** foi adicionada em parâmetros de programação de segmentos de leitura recorrentes. Essa opção permite fazer com que todos os perfis ainda presentes na jornada saiam automaticamente na próxima execução. Quando a opção estiver desativada, os perfis devem concluir a jornada antes de entrar novamente em outra ocorrência. [Saiba mais](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Administração**

* Uma mensagem foi adicionada à interface para avisar que as configurações de subdomínio, subdomínio de página de destino, registro PTR e pool de IP são comuns a todas as sandboxes e, portanto, qualquer modificação em uma dessas configurações também afetará as sandboxes de produção.
* As etapas para fazer upload da lista de supressão como um arquivo CSV da interface foram modificadas. [Saiba mais](../configuration/manage-suppression-list.md#download-suppression-list)

**Campanhas**

* Agora é possível arquivar campanhas concluídas e interrompidas. [Saiba mais](../campaigns/modify-stop-campaign.md#archive)
