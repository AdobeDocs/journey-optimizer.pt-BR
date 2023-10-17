---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 100%

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
<th><strong>Relatórios de canal consolidados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O recurso Relatório de canal oferece aos analistas e profissionais de marketing uma visão geral abrangente das métricas de tráfego e engajamento no nível do canal. Para acessar o menu “Relatório”, é necessário ter a permissão “Exibir relatórios de canal”.</p>
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
<p>A exportação de conjuntos de dados do Journey Optimizer para destinos de armazenamento na nuvem agora está disponível. Com esse recurso, é possível estabelecer uma conexão ativa com locais de armazenamento na nuvem para exportar o conteúdo dos conjuntos de dados.</p>
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

<table>
<thead>
<tr>
<th><strong>Atributos computados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os atributos computados permitem resumir facilmente os dados do evento em atributos de perfil por meio de uma interface intuitiva para segmentação, personalização e ativação aprimoradas com base em comportamento. Com esse recurso, você pode criar atributos computados de maneira independente, gerenciá-los e usá-los na segmentação, nos destinos do Perfil do cliente em tempo real ou no Journey Optimizer.<br/><br/>
Além disso, os atributos computados simplificam os fluxos de trabalho de jornada e segmentação, ajudando a fornecer experiências relevantes perfeitamente. Saiba mais na <a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=pt-BR">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
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

**Alertas**

* Foi introduzido um novo tipo de alerta de sistema. Agora é possível receber uma notificação quando houver uma falha em um público-alvo de leitura.

**Canal da Web**

* Agora, os aplicativos de página única (SPA) podem ser criados no editor visual do designer da Web, o que permite selecionar em quais exibições específicas você deseja aplicar as modificações da página da Web. Uma exibição pode ser definida como um site inteiro ou um grupo de elementos visuais de um site, como a página inicial, a totalidade do site de produtos ou o quadro de preferências de entrega em todas as páginas de check-out. É necessária a configuração do desenvolvedor uma única vez para definir as exibições na implementação do SDK da Web da Adobe Experience Platform. Isso permite criar e executar as campanhas da Web do Adobe Journey Optimizer em SPAs.

* Ao editar uma página usando o designer da Web, agora é possível adicionar novas alterações ao conteúdo diretamente do painel **Modificações**, sem a necessidade de selecionar um componente e editá-lo na interface do designer.
* Ao configurar subdomínios da Web, agora há a opção de adicionar seu próprio subdomínio, além de usar um subdomínio já delegado à Adobe.

**Jornadas**

* O suporte a respostas de ação personalizadas agora é GA. Isso permite aproveitar as respostas de chamada da API em ações personalizadas e orquestrar sua jornada com base nessas respostas. Além disso, foi adicionada uma nova medida de proteção para limitar todas as ações personalizadas a 5000 chamadas/s por ponto de acesso.
* Agora é possível definir o nome da cópia da jornada ao duplicá-la.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**Canal de email**

Uma nova opção na configuração da superfície de email permite optar por enviar mensagens transacionais para perfis mesmo que os endereços de email estejam na lista de supressão do Adobe Journey Optimizer.

**Canal SMS**

Dois novos campos, **Mensagem de aceitação** e **Mensagem de ajuda**, foram adicionados à tela de configuração da API, permitindo personalizar respostas para palavras-chave de entrada. Observe que isso só está disponível para o provedor de SMS Sinch.

**Relatórios**

Agora é possível exportar os relatórios do Journey Optimizer como arquivos CSV. [Saiba mais](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->
