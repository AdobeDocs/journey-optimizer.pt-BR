---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 94f6a1ee3a226f22042776b2f8b3ffa99c61cc55
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 23%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de setembro de 2023 {#sept-rn-2023}

**Data de lançamento**: 26 a 27 de setembro de 2023

### Novos recursos{#sept-2023-features}

Essa versão traz os novos recursos listados abaixo.


<table>
<thead>
<tr>
<th><strong>Relatórios de canal consolidado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O recurso Relatório de canal oferece aos analistas e profissionais de marketing uma visão geral abrangente das métricas de tráfego e engajamento no nível do canal. Para acessar o menu 'Relatório', você deve ter a permissão 'Exibir relatórios do canal'.</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Destinos de exportação do conjunto de dados (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A exportação de conjuntos de dados do Journey Optimizer para Destinos de armazenamento na nuvem agora está disponível para o público em geral. Com esse recurso, é possível estabelecer uma conexão ativa com locais de armazenamento na nuvem para exportar o conteúdo dos conjuntos de dados.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Armazenamento de credenciais do aplicativo móvel por sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esse novo recurso permite gerenciar e associar facilmente as credenciais de push a uma sandbox dedicada nas Superfícies do aplicativo.</p>
<p>Para obter mais informações, consulte a <a href="../in-app/inapp-configuration.md">documentação detalhada</a>.</p>
</tr>
</tbody>
</table>

### Melhorias {#sept-2023-improvements}

Esta versão vem com as melhorias listadas abaixo.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personalização**

* Além dos fragmentos visuais, agora é possível criar, salvar e reutilizar fragmentos de expressão da interface do Journey Optimizer por meio do Editor de expressão. Os fragmentos de expressão substituem as expressões salvas anteriormente.
* Agora você pode usar os atributos computados do Adobe Experience Platform para personalização no Journey Optimizer. Os atributos computados são valores agregados que são calculados com base em conjuntos de dados de Evento de experiência habilitados para perfil assimilados na Adobe Experience Platform.

**Alertas**

* Foram introduzidos dois novos tipos de alertas de sistema. Agora você pode ser notificado quando uma ação personalizada ou um segmento de leitura falhar.

**Canal da Web**

* Agora é possível selecionar a quais exibições específicas você deseja aplicar as modificações da página da Web. Uma exibição pode ser definida como um site inteiro ou um grupo de elementos visuais em um site, como a página inicial, o site de produtos inteiro ou o quadro de preferências de entrega em todas as páginas de check-out.
* Ao editar uma página usando o web designer, agora é possível adicionar novas alterações ao conteúdo diretamente do painel Modificações, sem a necessidade de selecionar um componente e editá-lo na interface do designer.
* Ao configurar subdomínios da Web, agora há a opção de adicionar seu próprio subdomínio, além de usar um subdomínio já delegado ao Adobe.

**Jornadas**

* Os recursos de resposta de ação personalizada agora estão disponíveis no mercado. Isso permite aproveitar as respostas de chamada da API em ações personalizadas e orquestrar sua jornada com base nessas respostas. Além disso, foi adicionada uma nova garantia para limitar todas as ações aduaneiras a 5000 chamadas/s por ponto de extremidade.
* Ao duplicar uma jornada, agora é possível definir o nome da cópia da jornada.
* A duração máxima que você pode definir na atividade de espera agora é de 29 dias, em vez de 30.

**Canal de email**

Uma nova opção na configuração da superfície de email permite optar por enviar mensagens transacionais para perfis mesmo se os endereços de email estiverem na lista de supressão do Adobe Journey Optimizer.

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->