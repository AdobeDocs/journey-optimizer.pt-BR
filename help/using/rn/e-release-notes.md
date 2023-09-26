---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 5edd643f7e93ade8d12515c83dc6321c96fe3c77
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 21%

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

<table>
<thead>
<tr>
<th><strong>Atributos computados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os atributos computados permitem resumir facilmente os dados do evento em atributos de perfil por meio de uma interface de usuário intuitiva para segmentação, personalização e ativação avançadas com base em comportamento. Com esse recurso, você pode criar atributos computados de maneira automatizada, gerenciá-los e usá-los na segmentação, destinos de Perfil do cliente em tempo real ou Journey Optimizer. <br/>
Além disso, os atributos computados simplificam a segmentação e os fluxos de trabalho de jornada para ajudá-lo a fornecer experiências relevantes de maneira contínua. Saiba mais na <a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html">documentação detalhada</a>.</p>
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

* Foi introduzido um novo tipo de alerta de sistema. Agora você pode ser notificado quando um público-alvo de leitura falhar.

**Canal da Web**

* Agora, os aplicativos de página única (SPA) podem ser criados no editor visual do web designer, o que permite selecionar em quais exibições específicas você deseja aplicar as modificações da página da Web. Uma exibição pode ser definida como um site inteiro ou um grupo de elementos visuais em um site, como a página inicial, o site de produtos inteiro ou o quadro de preferências de entrega em todas as páginas de check-out. Para criar e executar campanhas da Web do Adobe Journey Optimizer no SPA, é necessária a configuração única do desenvolvedor para definir as exibições na implementação do SDK da Web da Adobe Experience Platform.

* Ao editar uma página usando o web designer, agora é possível adicionar novas alterações ao seu conteúdo diretamente do **Modificações** painel - sem a necessidade de selecionar um componente e editá-lo na interface do designer.
* Ao configurar subdomínios da Web, agora há a opção de adicionar seu próprio subdomínio, além de usar um subdomínio já delegado ao Adobe.

**Jornadas**

* O suporte a respostas de ação personalizadas agora está disponível. Isso permite aproveitar as respostas de chamada da API em ações personalizadas e orquestrar sua jornada com base nessas respostas. Além disso, foi adicionada uma nova garantia para limitar todas as ações aduaneiras a 5000 chamadas/s por ponto de extremidade.
* Ao duplicar uma jornada, agora é possível definir o nome da cópia da jornada.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**Canal de email**

Uma nova opção na configuração da superfície de email permite optar por enviar mensagens transacionais para perfis mesmo se os endereços de email estiverem na lista de supressão do Adobe Journey Optimizer.

**Canal SMS**

Dois novos campos, **Mensagem de Opt-in** e **Mensagem de ajuda**, foram adicionados à tela Configuração de API, permitindo que os usuários personalizem respostas para palavras-chave de entrada. Observe que isso só está disponível para o provedor de SMS Sinch.

**Relatórios**

Agora você pode exportar relatórios do Journey Optimizer como um arquivo CSV. [Saiba mais](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->