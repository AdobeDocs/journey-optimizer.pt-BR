---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 2eb1ffff7101362b52ae91f1a7277188664b2954
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 31%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de maio de 2024 {#e-2024}

**Data de lançamento**: 21 a 22 de maio de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.


<table>
<thead>
<tr>
<th><strong>Experience Decisioning - Disponibilidade limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Escolha de experiências simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.</p>
<p>Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada por meio do novo canal de experiência baseado em código, agora acessível nas campanhas do Journey Optimizer. As políticas de decisão do Experience Decisioning estão disponíveis para uso somente em campanhas de experiência baseadas em código.</p>
<p>No momento, o Experience Decisioning está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/gs-experience-decisioning.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Fluxo de trabalho de Warmup de IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se você estiver enviando emails em um novo endereço IP, agora é possível executar facilmente workflows de aquecimento de IP diretamente da interface do usuário. O Adobe Journey Optimizer oferece uma maneira padronizada e eficiente de aquecer seus endereços IP que segue as práticas recomendadas para uma entrega ideal.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/ip-warmup-gs.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regras comerciais - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar regras granulares de limite de frequência e aplicá-las a diferentes tipos de comunicações de marketing por meio de conjuntos de regras. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Dados de personalização estendidos - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível pesquisar e buscar valores de dados em conjuntos de dados do Adobe Experience Platform e usar esses valores para criar condições no Adobe Journey Optimizer. Você pode aproveitar os dados de um conjunto de dados de pesquisa quando uma relação tiver sido definida usando um atributo dentro de uma matriz de objetos. Você pode especificar conjuntos de dados não ativados por perfil para pesquisa. Depois de habilitado, você pode usar um atributo de perfil como uma chave de junção para o conjunto de dados especificado a fim de recuperar mais dados para personalização.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Experience Decisioning**

De beta para LA, as seguintes melhorias foram adicionadas:

* **Experience Decisioning + Experiências baseadas em código (DL)**: agora você pode aproveitar o recurso Decisão da experiência para usar itens de decisão em suas campanhas com base em código. Observação: o canal de experiência baseado em código e o Experience Decisioning não estão disponíveis para organizações que compraram as ofertas complementares do Adobe Healthcare Shield e do Privacy and Security Shield. [Leia mais](../code-based/get-started-code-based.md)
* Agora você pode aproveitar os dados de contexto do Adobe Experience Platform em suas regras de decisão e fórmulas de classificação. [Leia mais](../experience-decisioning/context-data.md)
* Uma nova permissão “Gerenciar a escolha de experiência” agora está disponível para o recurso Gestão de decisões. Ele permite gerenciar direitos relacionados ao Experience Decisioning. [Leia mais](../experience-decisioning/gs-experience-decisioning.md)
* Agora é possível adicionar várias regras de limite para um determinado item de decisão na Escolha de experiências. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas. [Leia mais](../experience-decisioning/items.md#capping)
* Agora é possível criar painéis de relatórios personalizados para campanhas do Experience Decisioning usando o [!DNL Customer Journey Analytics]. [Leia mais](../experience-decisioning/cja-reporting.md)


**Offer Decisioning**

* **Suporte a várias regras** - Agora você pode adicionar até 10 regras de limitação para uma determinada oferta na Gestão de decisões. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas.
* **Auditorias** - A **Log de alterações** permite que você veja todas as alterações feitas em uma oferta ou em uma decisão que foi removida. As alterações relacionadas a ofertas e decisões agora podem ser vistas no menu **Auditorias**.


**Canal de email**

* **List-unsubscribe** - Após os anúncios recentes do Gmail e do Yahoo para remetentes em massa, o Journey Optimizer é compatível com a opção &quot;post/1-click&quot; List-Unsubscribe.
* **Pontuação de spam** (Beta) — Agora você pode verificar sua pontuação de spam de conteúdo em um relatório de spam dedicado. Usando o SpamAssassin, o Adobe Journey Optimizer agora pode testar seu conteúdo de email e atribuir uma pontuação para indicar se os provedores de ISP o considerarão como spam ou não. [Leia mais](../content-management/spam-report.md)


**Públicos-alvo**

* O uso de públicos-alvo e atributos da composição de público-alvo e do upload personalizado (arquivo CSV) agora está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

**Personalização**

* **Fragmento da expressão** - Os fragmentos de expressão agora estão disponíveis para o **Canal no aplicativo**. [Leia mais](../personalization/use-expression-fragments.md)

**Jornadas**

* **Políticas de mesclagem** - As políticas de mesclagem agora podem ser configuradas e usadas em suas jornadas.
* **Suporte a mTLS** - O protocolo mTLS agora é compatível com APIs do Journey Optimizer e ações personalizadas.
* **Pesquisar tabelas em eventos** - Agora você pode aproveitar os dados de um conjunto de dados de pesquisa quando uma relação tiver sido definida usando um atributo dentro de uma matriz de objetos. Os valores de pesquisa estarão disponíveis em jornadas (condições, ações personalizadas etc.) e personalização de mensagens.
