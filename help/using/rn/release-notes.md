---
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 8766f64c4ea7985c6c9d6e4ba022ef6b1fc0dbed
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 24%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target=&quot;_blank&quot;}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [Informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Versão de julho de 2022 {#july-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Novo fluxo de mensagens em linha</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer fornece um novo fluxo para a criação de mensagens no Jornada. As mensagens em linha salvarão os usuários tempo significativo e simplificarão o processo do fluxo de trabalho para criar e entregar um email, uma notificação por push ou um SMS no Journey Optimizer. Ao remover mensagens como uma etapa separada e, em vez disso, torná-las editáveis em linha como parte de uma ação na Tela de Jornada, os usuários precisarão clicar em menos botões e navegar em menos telas para criar e editar seu conteúdo.</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>Para obter mais informações, consulte a <a href="../messages/get-started-content.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Controle de acesso baseado em atributos (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível identificar campos de esquema com rótulos que definem escopos organizacionais ou de uso de dados. Os administradores podem usar a interface Permissões para definir políticas de acesso que cubram campos de esquema XDM e gerenciar melhor o acesso dado aos usuários ou grupos de usuários (usuários internos, externos ou de terceiros), e gerenciar o acesso a tipos específicos de dados (ou seja, dados pessoais confidenciais/SPD).</p>
<p>O uso do controle de acesso baseado em atributos está atualmente restrito aos usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../administration/attribute-based-access.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trabalhos de decisão em lote</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode executar tarefas de decisão em lote a partir da interface do usuário, de modo que não precise que um desenvolvedor execute tarefas de api em lote e possa reduzir o tempo necessário para o marketing. Essa nova interface permite criar tarefas e gerenciar trabalhos atuais/anteriores.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Para obter mais informações, consulte a <a href="../offers/batch-delivery.md">documentação detalhada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Use automaticamente a oferta com melhor desempenho em suas decisões (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar sistemas de modelos de otimização personalizados no Gerenciamento de decisões. Esse novo tipo de modelo permite otimizar e personalizar ofertas com base em segmentos e oferecer desempenho.</p>
<p>O uso de modelos de AI de otimização personalizada está atualmente restrito a usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obter mais informações, consulte a <a href="../offers/ranking/personalized-optimization-model.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* **Encerramento de uma jornada** - Na tela da jornada, a variável **End** foi removida da paleta. Tags finais agora são adicionadas por padrão no final de cada caminho e não podem ser removidas. Essa melhoria permite melhores relatórios sobre onde um cliente saiu da jornada, sem nenhuma ação necessária do profissional de jornada. Consulte a [documentação](../building-journeys/journey-end.md) e [vídeo de recurso](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.

**Mensagens**

* As predefinições de mensagem agora são **superfícies dos canais**. [Saiba mais](../configuration/channel-surfaces.md)

**Administração**

* **Edição de registro PTR** - Agora, ao atualizar um registro PTR, o tempo de processamento levará apenas 3 horas. [Saiba mais](../configuration/ptr-records.md#processing)

* **Interface do usuário do Lista de permissões** - Agora é possível usar a interface do usuário do Journey Optimizer para adicionar novos domínios ou endereços de email à lista de permissões. [Saiba mais](../configuration/allow-list.md)

* **Atualização lógica da lista de permissões** - Agora a lógica de lista de permissões se aplica assim que o recurso é ativado, mesmo que a lista esteja vazia. [Saiba mais](../configuration/allow-list.md#logic)

* **Parâmetros de rastreamento de URL** - Agora você pode usar o Editor de expressão para configurar parâmetros de rastreamento de URL em suas superfícies de email (ou seja, predefinições). [Saiba mais](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **Tamanho do público-alvo** - Um novo componente de estimativa de tamanho de público-alvo agora é exibido na interface do usuário ao criar uma regra de decisão, ao selecionar um segmento ou uma regra para definir uma qualificação de oferta ou ao adicionar um segmento ou uma regra a um escopo de decisão.