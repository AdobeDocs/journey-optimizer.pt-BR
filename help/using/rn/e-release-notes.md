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
source-git-commit: 91a687563ecd989c89061996b5906bcc77e82e23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 27%

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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<p>Agora é possível criar regras granulares de limite de frequência e aplicá-las a diferentes tipos de comunicações de marketing por meio de conjuntos de regras. Esse novo recurso permite controlar a frequência com que seus públicos-alvo recebem uma mensagem definindo regras entre canais que excluem automaticamente perfis excessivamente solicitados de mensagens e ações.</p>
<p>O recurso Regras de negócio está disponível no momento como um beta público.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Experience Decisioning** (Disponibilidade limitada)

Da versão beta para esta, as seguintes melhorias foram adicionadas:

* **Experience Decisioning + experiências baseadas em código** - Agora você pode aproveitar o recurso Decisão da experiência para usar itens de decisão em suas campanhas baseadas em código. Observação: o canal de experiência baseado em código e o Experience Decisioning não estão disponíveis para organizações que compraram as ofertas complementares do Adobe Healthcare Shield e do Privacy and Security Shield. [Leia mais](../code-based/get-started-code-based.md)
* **Dados de contexto** - Agora você pode aproveitar os dados de contexto do Adobe Experience Platform em suas regras de decisão e fórmulas de classificação. [Leia mais](../experience-decisioning/context-data.md)
* **Nova permissão** - Uma nova permissão &quot;Gerenciar decisões de experiência&quot; agora está disponível para o recurso Gerenciamento de decisões. Ele permite gerenciar direitos relacionados ao Experience Decisioning. [Leia mais](../experience-decisioning/gs-experience-decisioning.md)
* **Regras de limite** - Agora você pode adicionar várias regras de limitação para um determinado item de decisão no Experience Decisioning. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas. [Leia mais](../experience-decisioning/items.md#capping)
* **Relatórios** - Agora você pode criar painéis de relatórios personalizados para campanhas do Experience Decisioning usando o [!DNL Customer Journey Analytics]. [Leia mais](../experience-decisioning/cja-reporting.md)


**Gestão de decisões**

* **Suporte a várias regras** - Agora você pode adicionar até 10 regras de limitação para uma determinada oferta na Gestão de decisões. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas.
* **Auditorias** - A **Log de alterações** permite que você veja todas as alterações feitas em uma oferta ou em uma decisão que foi removida. As alterações relacionadas a ofertas e decisões agora podem ser vistas no menu **Auditorias**.


**Canal de email**

* **List-unsubscribe** - Após os anúncios recentes do Gmail e do Yahoo para remetentes em massa, o Journey Optimizer é compatível com a opção &quot;post/1-click&quot; List-Unsubscribe.
* **Pontuação de spam** (Beta) — Agora você pode verificar sua pontuação de spam de conteúdo em um relatório de spam dedicado. Usando o SpamAssassin, o Adobe Journey Optimizer agora pode testar seu conteúdo de email e atribuir uma pontuação para indicar se os provedores de ISP o considerarão como spam ou não.
  <!--[Read more](../content-management/spam-report.md)-->


**Públicos-alvo**

* O uso de públicos-alvo e atributos da composição de público-alvo e do upload personalizado (arquivo CSV) agora está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

**Personalização**

* **Fragmento da expressão** - Os fragmentos de expressão agora estão disponíveis para o **Canal no aplicativo**.
  <!--[Read more](../personalization/use-expression-fragments.md)-->

**Jornadas**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Suporte a mTLS** - A autenticação mTLS agora é compatível com ações personalizadas. Não há necessidade de configuração adicional na ação personalizada ou na jornada para ativar o mTLS; isso ocorre automaticamente quando um terminal habilitado para mTLS é detectado.
* **Pesquisar tabelas em eventos** - Agora você pode aproveitar os dados de um conjunto de dados de pesquisa quando uma relação tiver sido definida usando um atributo dentro de uma matriz de objetos. Os valores de pesquisa estarão disponíveis em jornadas (condições, ações personalizadas etc.) e personalização de mensagens.
