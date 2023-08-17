---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 100%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de julho de 2023 {#july-rn-2023}

**Data de lançamento**: 26-27 de julho

### Novos recursos{#july-2023-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Composição de público-alvo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar fluxos de trabalho de composição para combinar públicos já existentes do Adobe Experience Platform em uma tela visual e aproveitar várias atividades (divisão, enriquecer...) para criar novos públicos. Os públicos-alvo recém-criados são salvos na Adobe Experience Platform junto com os públicos-alvo existentes e podem ser aproveitados nas campanhas do Journey Optimizer para direcionar clientes.</p>
<p>Para obter mais informações, consulte a <a href="../audience/get-started-audience-orchestration.md">documentação detalhada</a>.</p>
<p>A composição de público-alvo vem totalmente integrada ao novo menu “Públicos-alvo” da Adobe Experience Platform, que serve como um portal centralizado para públicos-alvo. Agora é possível usar uma página de navegação que inclui um novo painel com tendências de segmento e sobreposições para encontrar novos insights e explorar ferramentas organizacionais para organização em pastas e marcação. Incorporados nessa experiência estão controles de governança para rotulagem de público-alvo padronizada, bem como recursos de gerenciamento do ciclo de vida do público-alvo para gerenciar fluxos de trabalho de ativação. Com essa nova experiência de gerenciamento, agora é possível gerenciar públicos-alvo de maneira fácil e segura em um único local. Para obter mais informações, consulte a <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=pt-BR" target="_blank">Documentação da Adobe Experience Platform</a>.</p></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Converter conteúdo de HTML para o designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível importar e converter qualquer conteúdo de HTML no editor de email do Journey Optimizer. Os blocos de conteúdo são identificados automaticamente e disponibilizados no designer de email: use seus recursos de design eficientes para atualizá-los e personalizá-los.</p>
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Usar tags no Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Além de campanhas e jornadas, agora é possível atribuir Tags unificadas da Adobe Experience Platform às suas páginas de destino, modelos de conteúdo, fragmentos e listas de assinatura. Isso permite classificá-los facilmente e melhorar a pesquisa e a navegação em todas as listas. </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Para obter mais informações, consulte a <a href="../start/search-filter-categorize.md#tags">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>APIs de modelos de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar e gerenciar modelos de conteúdo do Adobe Journey Optimizer usando APIs dedicadas, proporcionando uma integração perfeita com seu sistema de conteúdo já existente.</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### Melhorias {#july-2023-improvements}

Esta versão vem com as melhorias listadas abaixo.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* Foi introduzido um novo tipo de alerta de sistema. Agora você pode ser notificado quando houver falha em uma ação personalizada.
-->

**Campanhas**

* Eventos contextuais relacionados a campanhas agora estão disponíveis para uso no menu “Atributos contextuais” do editor de personalização.


**Públicos-alvo**

Foram feitos aprimoramentos no seletor de público-alvo em jornadas ou campanhas, com a adição de novas colunas que exibem a origem e a frequência de atualização dos públicos-alvo.

Com o lançamento do portal Composição de público-alvo, a Adobe Experience Platform e o Adobe Journey Optimizer atualizaram oa utilização de “públicos-alvo” e “segmentos” no sistema e na documentação.

* Público-alvo: um conjunto de pessoas, contas, famílias ou outras entidades que compartilham características e comportamentos comuns.
* Definição de segmento: na Adobe Experience Platform, as regras usadas para descrever as principais características ou comportamentos de um público-alvo. Esse termo era anteriormente conhecido apenas como “segmento”.

Como resultado, na na interface do Adobe Journey Optimizer e da Adobe Experience Platform, “Segmentos” será substituído por “Públicos-alvo” para refletir esse novo caminho de criação e gerenciamento de público-alvo.

**APIs**

Autenticação de APIs do Adobe Journey Optimizer: o método JWT para gerar tokens de acesso foi descontinuado. Todas as novas integrações devem ser criadas usando o método de autenticação OAuth de servidor para servidor. A Adobe também recomenda migrar as integrações já existentes para o método OAuth. [Saiba mais](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**Outras alterações**

A exportação de conjuntos de dados do Journey Optimizer para Destinos de armazenamento na nuvem agora está disponível para todos os clientes como um beta público. Com esse recurso, é possível estabelecer uma conexão ativa com locais de armazenamento na nuvem para exportar o conteúdo dos conjuntos de dados. [Saiba mais](../data/export-datasets.md)




