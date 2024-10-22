---
title: Gerenciamento de conflitos e priorização
description: Saiba como pré-visualizar e testar o conteúdo.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Disponibilidade limitada"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '1187'
ht-degree: 21%

---


# Gerenciamento de conflitos e priorização {#conflict-prioritization}

>[!AVAILABILITY]
>
>As ferramentas de gerenciamento e priorização de conflitos estão disponíveis atualmente como uma versão beta somente para usuários selecionados.

No Journey Optimizer, gerenciar o volume e o tempo das campanhas e jornadas é essencial para evitar sobrecarregar os clientes com muitas interações. As duas seções a seguir apresentam as principais ferramentas para ajudar você a manter o equilíbrio e priorizar as comunicações de maneira eficaz

## Exibir possíveis conflitos em jornadas e campanhas {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Visualizador de conflitos em campanhas"
>abstract="Essa ferramenta pode ajudar você a determinar a sobreposição com outras jornadas, campanhas ou configurações de canal. Se você quiser identificar sobreposições no público-alvo, data inicial e final, configuração de canais, canal ou conjunto de regras, é possível exibir os possíveis conflitos aqui."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Visualizador de conflitos em jornadas"
>abstract="Essa ferramenta pode ajudar você a determinar a sobreposição com outras jornadas, campanhas ou configurações de canal. Se você quiser identificar sobreposições no público-alvo, data inicial e final, configuração de canais, canal ou conjunto de regras, é possível exibir os possíveis conflitos aqui."

À medida que os profissionais de marketing aumentam o volume de Campanhas e Jornadas no Journey Optimizer, fica cada vez mais difícil para um profissional de marketing saber se estão bombardeando seus clientes com muitas interações de marketing. portanto, é essencial identificar facilmente quando há campanhas e jornadas sobrepostas para garantir que elas estejam alcançando o equilíbrio certo de comunicações de marketing e, ao mesmo tempo, reduzir o risco de fadiga do cliente.

As principais áreas a serem monitoradas quanto a possíveis sobreposições são:

* **Linha do Tempo** (datas de início e término): muitas jornadas estão sendo executadas simultaneamente?
* **Público-alvo**: que porcentagem do meu público-alvo de jornada também faz parte de outras jornadas?
* **Canal**: há outras comunicações agendadas para o mesmo período? Em caso afirmativo, quantas?
* **Conjunto de Regras de Limite**: que tipos de jornadas estou limitando e há sobreposição entre eles?
* **Configuração de Canal**: há outras jornadas ou campanhas usando qualquer configuração de canal que esteja sendo usada na mesma jornada ou campanha que possam impedir a exibição da jornada ou campanha ao usuário final?

### Como o Journey Optimizer detecta conflitos {#detection}

Abaixo está um resumo de como o Journey Optimizer identifica possíveis conflitos para jornadas e campanhas:

* **Escopo de identificação de conflito**: os conflitos são mostrados somente para campanhas e jornadas ativas ou agendadas.
* **jornadas Unitárias**: se a jornada selecionada for unitária, outras jornadas que começam com o mesmo evento serão exibidas, pois esse evento acionará todas essas jornadas.
* **Qualificação de público-alvo e Público-alvo de leitura/Evento comercial** jornadas: se a jornada selecionada for uma qualificação de Público-alvo ou uma jornada de Evento comercial/Público de leitura, todas as outras jornadas do mesmo tipo com um público-alvo válido serão exibidas, pois pode haver sobreposições entre os públicos-alvo.
* **Campanhas**: como todas as campanhas estão direcionando públicos e não há nenhum conceito de eventos, todas as campanhas potencialmente entram em conflito com jornadas acionadas por segmento (começando com uma atividade Ler público).
* **Campanhas online/agendadas**: campanhas online e agendadas podem entrar em conflito devido a uma possível sobreposição de públicos. Para qualquer campanha, todas as campanhas ativas ou programadas são listadas no visualizador de conflitos.

### Exibir conflitos identificados para uma determinada jornada ou campanha {#view}

Ao criar uma jornada ou campanha, o Journey Optimizer permite verificar sempre que há uma possibilidade de sobreposição com outras jornadas ou campanhas. Para fazer isso, siga estes passos:

1. No momento da criação de uma jornada ou campanha, clique no botão **[!UICONTROL Exibir Conflitos Potenciais]** nas propriedades da jornada ou campanha.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >O botão **[!UICONTROL Exibir conflitos potenciais]** ficará disponível para seleção assim que você atribuir qualquer uma das seguintes configurações: **[!UICONTROL Data de início/término]**, **[!UICONTROL Público-alvo]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuração de canal]** e **[!UICONTROL Conjunto de regras]**. Selecione **[!UICONTROL Salvar]** depois de atribuir essas configurações, pois o botão não poderá ser selecionado até que as alterações sejam salvas.

1. A janela **[!UICONTROL Conflitos potenciais]** é aberta, permitindo visualizar todos os elementos que estão sobrepondo a jornada/campanha atual.

   Você pode abrir uma jornada ou campanha sobreposta diretamente nesta tela selecionando o nome dela.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >As campanhas recém-publicadas podem levar até 5 minutos para serem exibidas no visualizador de conflitos, devido ao armazenamento em cache implementado

Para refinar ainda mais sua pesquisa por possíveis sobreposições, você pode filtrar sua lista de campanhas e jornadas com base nos campos relevantes. Para fazer isso, selecione o ícone de filtro na visualização de inventário. [Saiba como trabalhar com filtros](../start/search-filter-categorize.md#filter-lists)

### Resolver conflitos {#resolve}

Estas são algumas dicas para reduzir os possíveis conflitos depois de identificados:

* Ajuste as **datas de início/término** para evitar campanhas ou jornadas sobrepostas.
* Refine **direcionamento de público** para minimizar a sobreposição entre as jornadas.
* Implemente **limites de frequência** para evitar que os clientes recebam muitas comunicações.
* Reduza o número de **jornadas ativas** para gerenciar a experiência do cliente com mais eficiência.
* Defina **prioridades** em ações de entrada para garantir que a ação mais importante seja exibida para os clientes.

Ao aproveitar esses recursos, você pode garantir que seus esforços de marketing estejam alinhados e que você mantenha o equilíbrio certo em sua estratégia de comunicação.

## Atribuir pontuações de prioridade a jornadas e campanhas {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Prioridade"
>abstract="Atribua uma pontuação de prioridade à jornada, variando de 0 a 100. Um número mais alto indica uma prioridade mais alta. O valor de prioridade inserido aqui é herdado por qualquer ação de entrada (como in-app) contida nesta jornada. Para situações em que essa mesma configuração de canais de entrada é usada em outras campanhas ou jornadas, a ação de entrada com a pontuação de prioridade mais alta é mostrada ao destinatário. Se várias jornadas ou campanhas tiverem a mesma pontuação, o elemento que foi modificado mais recentemente será escolhido."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Prioridade"
>abstract="Atribua uma pontuação de prioridade à campanha, variando de 0 a 100. Um número mais alto indica uma prioridade mais alta. Para situações em que essa mesma configuração de canais de entrada (como in-app) é usada em outras campanhas ou jornadas, a ação de entrada com a pontuação de prioridade mais alta é mostrada ao destinatário. Se várias jornadas ou campanhas tiverem a mesma pontuação, o elemento que foi modificado mais recentemente será escolhido."

O Journey Optimizer permite atribuir uma pontuação de prioridade a uma jornada ou campanha. A prioridade é essencial para priorizar uma jornada, campanha ou ação quando há uma restrição imposta (como um limite de frequência). Em situações em que um cliente se qualifica para muitas jornadas, campanhas ou comunicações e você deseja ser seletivo quanto ao que ele deve informar e receber, você deve utilizar esse campo.

>[!NOTE]
>
>A pontuação de prioridade está disponível para canais de entrada: canais da Web, no aplicativo e baseados em código. No jornada, a pontuação de prioridade está disponível somente para os canais **no aplicativo** e **baseados em código**.

Atribuir uma pontuação de prioridade é fundamental para a comunicação de entrada, como Web, Dispositivo móvel e No aplicativo. Se você tiver várias campanhas usando a mesma configuração de canal (por exemplo, um banner na parte superior da página da Web), isso pode ser problemático, pois somente o conteúdo de uma campanha pode ser exibido. A pontuação de prioridade é onde você insere sua preferência para qual campanha deve ser exibida quando o recipient pode se qualificar para mais de uma campanha.

Para atribuir uma pontuação de prioridade a uma jornada ou campanha, insira um valor numérico (de 0 a 100) no campo **[!UICONTROL Pontuação de prioridade]** localizado nas propriedades da jornada ou campanha. Observe que quanto maior o número, maior a prioridade. Se você estava criando esta campanha e queria garantir que o conteúdo dela fosse exibido, atribuiria a ela uma pontuação de 100.

![](assets/priority-score.png)

Para situações em que duas campanhas têm a mesma pontuação de prioridade, a campanha que foi ativada primeiro será exibida.
