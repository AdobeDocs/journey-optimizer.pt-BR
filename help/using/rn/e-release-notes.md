---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão anteriores do Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: bef5bc9f86d1e11e6b1ed5853fc0b57a6e47d4ac
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 22%

---

# Notas de versão anteriores {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês no [notas de versão](release-notes.md).

As notas de versão anteriores abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados no [notas de versão](release-notes.md), na data de lançamento.


## Notas de versão antecipadas de julho de 2023 {#july-rn-2023}

**Data de lançamento**: 26 a 27 de julho

### Novos recursos{#july-2023-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Composição de público</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar workflows de composição para combinar públicos-alvo existentes do Adobe Experience Platform em uma tela visual e aproveitar várias atividades (dividir, enriquecer...) para criar novos públicos-alvo. Os públicos-alvo recém-criados são salvos no Adobe Experience Platform junto com os públicos-alvo existentes e podem ser aproveitados nas campanhas do Journey Optimizer para direcionar os clientes.</p>
<img src="../audience/assets/audiences-publish.png"/>
<p>Para obter mais informações, consulte a <a href="../audience/get-started-audience-orchestration.md">documentação detalhada</a>.</p>
<p>A composição de público-alvo vem totalmente integrada ao novo menu "Públicos-alvo" do Adobe Experience Platform, que serve como um portal centralizado para públicos-alvo. Agora você pode usar uma página de navegação que inclui um novo painel com tendências e sobreposições de segmentos para encontrar novos insights e explorar ferramentas organizacionais para pastas e marcação. Incorporados nessa experiência estão controles de governança para rotulagem de público-alvo padronizada, bem como recursos de gerenciamento do ciclo de vida do público-alvo para gerenciar workflows de ativação. Com essa nova experiência de gerenciamento, agora é possível gerenciar públicos-alvo de maneira fácil e segura em um único local. Para obter mais informações, consulte <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html" target="_blank">Documentação do Adobe Experience Platform</a>.</p></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Canal de correspondência direta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Adobe Journey Optimizer está expandindo seus recursos entre canais adicionando suporte para canal de mala direta. A correspondência direta é um canal offline que permite personalizar e gerar os arquivos de extração necessários para os provedores de correspondência direta enviarem emails para seus clientes.</p>
<!--img src="assets/do-not-localize/web-authoring.gif"/>
<p>For more information, refer to the <a href="../web/get-started-web.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Converter conteúdo de HTML para o designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode importar e converter qualquer conteúdo de HTML no editor de email do Journey Optimizer. Os blocos de conteúdo são identificados automaticamente e disponibilizados no designer de email: use seus poderosos recursos de design para atualizá-los e personalizá-los!</p>
<!--img src="../audience/assets/audiences-publish.png"/-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Usar tags na Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode atribuir Tags unificadas do Adobe Experience Platform a suas páginas de aterrissagem, modelos, fragmentos de conteúdo e listas de assinaturas, além de campanhas e jornadas. Isso permite classificá-los facilmente e melhorar a pesquisa e a navegação em todas as listas. No momento, esse recurso está disponível na disponibilidade geral.</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Para obter mais informações, consulte a <a href="../start/search-filter-categorize.md#tags">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


### Melhorias {#july-2023-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

Foram feitos aprimoramentos no seletor de público em jornadas ou campanhas, com a adição de novas colunas que exibem a origem e a frequência de atualização dos públicos.

Com o lançamento do portal Composição de público-alvo, a Adobe Experience Platform e a Adobe Journey Optimizer atualizaram o uso de &quot;públicos-alvo&quot; e &quot;segmentos&quot; no sistema e na documentação.

* Público-alvo: um conjunto de pessoas, contas, famílias ou outras entidades que compartilham características e comportamentos comuns.
* Definição de segmento: na Adobe Experience Platform, as regras usadas para descrever as principais características ou comportamentos de um público-alvo. Esse termo era anteriormente conhecido apenas como “segmento”.

Como resultado, na na interface do Adobe Journey Optimizer e da Adobe Experience Platform, “Segmentos” será substituído por “Públicos-alvo” para refletir esse novo caminho de criação e gerenciamento de público-alvo.


**Jornadas**

* Agora é possível aproveitar as respostas de chamada da API em ações personalizadas e orquestrar sua jornada com base nessas respostas.


**Campanhas**

* Eventos contextuais relacionados a campanhas agora estão disponíveis para uso no menu &quot;Contextual attributes&quot; do editor de personalização.

