---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 645db980155993155a10d27f4ff59967b000442f
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 19%

---

# Notas de versão {#release-notes}

[!DNL Adobe Journey Optimizer] O fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nessas notas de versão.

As notas de versão anteriores estão disponíveis em [esta página](release-notes-2022.md). Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Cadastre-se para a [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais diretamente para sua caixa de entrada a cada trimestre.


## Versão de janeiro de 2023 {#jan-2023-release}

### Novos recursos{#jan-2023-features}


<table>
<thead>
<tr>
<th><strong>Higiene de dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Experience Platform fornece um conjunto de recursos de higiene de dados que permitem gerenciar seus dados armazenados por meio de exclusões programáticas de registros e conjuntos de dados do consumidor. Esse recurso agora está disponível para o Adobe Journey Optimizer. </p>
<p>Você pode gerenciar seus armazenamentos de dados para garantir que as informações sejam usadas conforme esperado, sejam atualizadas quando a correção de necessidades de dados estiver incorreta e excluídas quando as políticas organizacionais o considerarem necessário.</p>
<p><strong>Cuidado</strong> - Os recursos de Higiene de dados estão disponíveis atualmente apenas para organizações que compraram a variável <strong>Escudo da Saúde</strong> e <strong>Privacy e Security Shield</strong> ofertas complementares.</p><p>Para obter mais informações, consulte a <a href="../privacy/data-hygiene.md">documentação detalhada</a>.

</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create standalone content templates that can be leveraged across journeys and campaigns for quick reuse.</p> 
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

### Melhorias {#jan-2023-improvements}

**Jornadas**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* Ao adicionar uma **Qualificação do segmento** ou **Ler segmento** em uma jornada, o namespace agora é pré-preenchido, por padrão, com o último namespace usado. Consulte a [Qualificação do segmento](../building-journeys/segment-qualification-events.md#about-segment-qualification) e [Ler segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity) seções.

* Na tela jornada , um novo botão está disponível na barra de ferramentas, que permite baixar uma captura de tela da jornada.

**Email Designer**

* Agora você pode exportar o conteúdo de email do **Exportar HTML** menu. Os arquivos exportados estão disponíveis em um arquivo de arquivamento (.ZIP).

**Administração**

* Uma nova subseção fornece recomendações sobre a criação da variável **Responder para (email)** endereço e assegurar uma gestão adequada das respostas. [Saiba mais](../email/email-settings.md#reply-to-email)

* Ao criar ou editar **pools de IP**, os registros PTR associados agora são exibidos na lista de IP e ao passar o cursor do mouse sobre os endereços IP selecionados. [Saiba mais](../configuration/ip-pools.md#create-ip-pool)

* Depois que um pool de IP é selecionado em uma superfície de canal, as informações de registro PTR agora ficam visíveis ao passar o mouse sobre os endereços IP. [Saiba mais](../email/email-settings.md#subdomains-and-ip-pools)

* A interface do usuário para edição [Registros PTR](../configuration/ptr-records.md#edit-ptr-record) e [campos de execução](../configuration/primary-email-addresses.md) foi atualizada.

* A interface do usuário para criar e editar subdomínios foi aprimorada. [Saiba mais](../configuration/delegate-subdomain.md)

* A lista de supressão **Uploads recentes** foi atualizada. [Saiba mais](../configuration/manage-suppression-list.md#recent-uploads)

**Campanhas**

* Um exemplo de solicitação de cURL que permite a execução de campanhas acionadas por API agora é gerado automaticamente e disponibilizado na tela da campanha. [Saiba mais](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalização**

* Novas funções de ajuda estão disponíveis: formatCurrency, charCodeAt, stringToDate, toString, formatNumber e toHexString. Além disso, a função toDateTimeOnly agora aceita tipos de campos string, date, long e int. [Saiba mais](../personalization/functions/functions.md)
