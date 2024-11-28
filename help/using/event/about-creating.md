---
solution: Journey Optimizer
product: journey optimizer
title: Configurar um evento unitário
description: Saiba como configurar um evento unitário
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: event, unitário, create, jornada
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: f9f2cd339680d0dbff1812e64c5082ca97a34771
workflow-type: tm+mt
source-wordcount: '1638'
ht-degree: 10%

---

# Configurar um evento unitário {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="Eventos unitários"
>abstract="A configuração do evento permite definir as informações que o Journey Optimizer receberá como eventos. Você pode usar vários eventos (em diferentes etapas de uma jornada), e várias jornadas podem usar o mesmo evento. Os eventos unitários são vinculados a um perfil específico. Eles podem ser baseados em regras ou gerados pelo sistema."

Os eventos unitários são vinculados a um perfil específico. Eles podem ser baseados em regras ou gerados pelo sistema.  Leia mais sobre o evento unitário [esta seção](../event/about-events.md).

Abaixo estão as primeiras etapas para configurar um novo evento:

1. Na seção de menu ADMINISTRAÇÃO, navegue até **[!UICONTROL Configurações]**, e na seção **[!UICONTROL Eventos]**, clique em **[!UICONTROL Gerenciar]**. A lista de eventos é exibida.

   ![](assets/jo-event1.png)

1. Clique em **[!UICONTROL Criar Evento]** para criar um novo evento. O painel de configuração do evento é aberto no lado direito da tela.

   ![](assets/jo-event2.png)

1. Insira o nome do evento. Você também pode adicionar uma descrição.

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >Somente caracteres alfanuméricos e sublinhados são permitidos. O comprimento máximo é de 30 caracteres.

1. No campo **[!UICONTROL Tipo]**, escolha **Unitário**.

   ![](assets/jo-event3bis.png)

1. No campo **[!UICONTROL Tipo de ID de evento]**, selecione o tipo de ID de evento que deseja usar: **Baseado em Regras** ou **Gerado pelo Sistema**. Leia mais sobre os tipos de ID de evento em [esta seção](../event/about-events.md#event-id-type).

   ![](assets/jo-event4.png)

1. O número de jornadas que usam este evento é exibido no campo **[!UICONTROL Usado em]**. Você pode clicar no ícone **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas que usam esse evento.

1. Defina os campos schema e payload: é aqui que você seleciona as informações do evento (normalmente chamadas de payload) que o jornada espera receber. Você poderá então usar essas informações em sua jornada. Consulte [esta seção](../event/about-creating.md#define-the-payload-fields).

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >Ao selecionar o tipo **[!UICONTROL Gerado pelo Sistema]**, somente esquemas com o campo de tipo eventID estarão disponíveis. Quando você seleciona o tipo **[!UICONTROL Baseado em regras]**, todos os esquemas de Evento de experiência ficam disponíveis.

1. Para eventos baseados em regras, clique dentro do campo **[!UICONTROL Condição de ID de evento]**. Usando o editor de expressão simples ou avançado, defina a condição que será usada pelo sistema para identificar os eventos que acionarão sua jornada.

   ![](assets/jo-event6.png)

   Em nosso exemplo, escrevemos uma condição com base na cidade do perfil. Isso significa que sempre que o sistema receber um evento que corresponda a essa condição (campo **[!UICONTROL Cidade]** e valor **[!UICONTROL Paris]**), ele o transmitirá para o jornada.

   >[!NOTE]
   >
   >No editor de expressões simples, nem todos os operadores estão disponíveis, eles dependem do tipo de dados. Por exemplo, para um tipo de sequência de caracteres de campo, é possível usar &quot;contém&quot; ou &quot;igual a&quot;.
   >
   >Se você modificar seu esquema com novos valores de enumeração depois de criar o evento, será necessário seguir estas etapas para aplicar as alterações ao evento existente: desmarque o campo de enumeração dos campos de evento, confirme a seleção e selecione o campo de enumeração novamente. O novo valor de enumeração agora é exibido.

1. Adicione um tipo de identidade. Esta etapa é opcional, mas é recomendada, pois a adição de um tipo de identidade permite aproveitar as informações armazenadas no Serviço de perfil do cliente em tempo real. Ela define o tipo de chave que o evento tem. Saiba mais [nesta seção](../event/about-creating.md#select-the-namespace).

1. Definir o identificador do perfil: escolha um campo a partir dos campos de carga útil ou defina uma fórmula para identificar a pessoa associada ao evento. Essa chave é configurada automaticamente (mas ainda pode ser editada) se você selecionar um tipo de identidade. Na verdade, o jornada escolhe a chave que deve corresponder ao tipo de identidade (por exemplo, se você selecionar um tipo de identidade de email, a chave de email será selecionada). Saiba mais [nesta seção](../event/about-creating.md#define-the-event-key).

   ![](assets/jo-event7.png)

1. Clique em **[!UICONTROL Salvar]**.

   Agora o evento está configurado e pronto para ser lançado em uma jornada. Etapas de configuração adicionais são necessárias para receber eventos. Consulte [esta página](../event/additional-steps-to-send-events-to-journey.md).

## Definir os campos de carga {#define-the-payload-fields}

A definição de carga útil permite escolher as informações que o sistema espera receber do evento em sua jornada e a chave para identificar qual pessoa está associada ao evento. A carga é baseada na definição do campo XDM do Experience Cloud. Para obter mais informações sobre o XDM, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

1. Selecione um esquema XDM na lista e clique no campo **[!UICONTROL Campos]** ou no ícone **[!UICONTROL Editar]**.

   ![](assets/journey8.png)

   Todos os campos definidos no esquema são exibidos. A lista de campos varia de um esquema para outro. Você pode pesquisar um campo específico ou usar os filtros para exibir todos os nós e campos ou apenas os campos selecionados. De acordo com a definição do esquema, alguns campos podem ser obrigatórios e pré-selecionados. Não é possível desmarcá-los. Todos os campos obrigatórios para o evento ser recebido corretamente pelas jornadas são selecionados por padrão.

   >[!NOTE]
   >
   >Para eventos gerados pelo sistema, verifique se você adicionou o grupo de campos &quot;orquestração&quot; ao esquema XDM. Isso garantirá que seu esquema contenha todas as informações necessárias para trabalhar com [!DNL Journey Optimizer].

   ![](assets/journey9.png)

1. Selecione os campos que você espera receber do evento. Esses são os campos que o usuário empresarial utilizará na jornada. Eles também devem incluir a chave que será usada para identificar a pessoa associada ao evento (consulte [esta seção](../event/about-creating.md#define-the-event-key)).

   >[!NOTE]
   >
   >Para eventos gerados pelo sistema, o campo **[!UICONTROL eventID]** é adicionado automaticamente à lista de campos selecionados para que [!DNL Journey Optimizer] possa identificar o evento. O sistema que envia o evento não deve gerar uma ID, mas usar a disponível na pré-visualização de carga. Consulte [esta seção](../event/about-creating.md#preview-the-payload).

1. Quando terminar de selecionar os campos necessários, clique em **[!UICONTROL Ok]** ou pressione **[!UICONTROL Enter]**.

   O número de campos selecionados aparece no campo **[!UICONTROL Campos]**.

   ![](assets/journey12.png)

## Selecione o tipo de identidade {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="Tipo de identidade"
>abstract="Selecione a chave para identificar o perfil do cliente associado ao evento."

O tipo de identidade (anteriormente conhecido como &quot;namespace&quot;) permite definir o tipo de chave usada para identificar a pessoa associada ao evento. Sua configuração é opcional. Ela é necessária se você quiser recuperar, em suas jornadas, informações adicionais provenientes do [Perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}. A definição do tipo de identidade não é necessária se você estiver usando apenas dados provenientes de um sistema de terceiros por meio de uma fonte de dados personalizada.

Você pode criar um tipo de identidade existente ou criar um novo usando o Serviço de identidade da Adobe Experience Platform. Saiba mais na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=pt-BR){target="_blank"}.

Se você selecionar um esquema que tenha uma identidade primária, os campos **[!UICONTROL Identificador do profiler]** e **[!UICONTROL Tipo de identidade]** serão preenchidos previamente. Se não houver identidade definida, selecionamos _identityMap > id_ como a chave primária. Em seguida, é necessário selecionar um tipo de identidade e a chave será preenchida previamente (abaixo do campo **[!UICONTROL Tipo de identidade]**) usando _identityMap > id_.

Ao selecionar campos, os campos de identidade principais são marcados.

![](assets/primary-identity.png)

Selecione um tipo de identidade na lista suspensa.

![](assets/journey17.png)

Somente um tipo de identidade é permitido por jornada. Se você usar vários eventos na mesma jornada, eles precisarão usar o mesmo tipo de identidade. Consulte [esta página](../building-journeys/journey.md).

>[!NOTE]
>
>Você só pode selecionar um tipo de identidade com base em pessoas. Se você tiver definido um tipo de identidade para uma tabela de pesquisa (por exemplo: tipo de identidade ProductID para uma pesquisa de Produto), ele não estará disponível na lista suspensa **Tipo de identidade**.

## Definir o identificador do perfil {#define-the-event-key}

A chave é o campo, ou combinação de campos, que faz parte dos dados de payload do evento e que permite que o sistema identifique a pessoa associada ao evento. A chave pode ser, por exemplo, a ID do Experience Cloud, uma ID do CRM ou um endereço de email.

Para usar os dados armazenados no banco de dados do Perfil do Cliente em Tempo Real do Adobe, a chave do evento deve ser a informação definida como a identidade de um perfil no [Serviço de Perfil do Cliente em Tempo Real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}.

O identificador de perfil permite que o sistema execute a reconciliação entre o evento e o perfil do indivíduo. Se você selecionar um esquema que tenha uma identidade primária, os campos **[!UICONTROL Identificador de perfil]** e **[!UICONTROL Tipo de identidade]** serão preenchidos previamente. Se não houver identidade definida, _identityMap > id_ será a chave primária. Em seguida, você deve selecionar um tipo de identidade e a chave é automaticamente preenchida usando _identityMap > id_.

Ao selecionar campos, os campos de identidade principais são marcados.

![](assets/primary-identity.png)

Se você precisar usar uma chave diferente, como uma ID do CRM ou um endereço de email, precisará adicioná-lo manualmente, conforme explicado abaixo:

1. Clique dentro do campo **[!UICONTROL Identificador de perfil]** ou no ícone de lápis.

   ![](assets/journey16.png)

1. Selecione o campo escolhido como a chave na lista de campos de carga.

Quando o evento é recebido, o valor da chave permite que o sistema identifique a pessoa associada ao evento. Associada a um [tipo de identidade](../event/about-creating.md#select-the-namespace), a chave pode ser usada para executar consultas no Adobe Experience Platform. Consulte [esta página](../building-journeys/about-journey-activities.md#orchestration-activities).
A chave também é usada para verificar se uma pessoa está em uma jornada. De fato, uma pessoa não pode estar em dois lugares diferentes na mesma jornada. Como resultado, o sistema não permite que a mesma chave, por exemplo, a chave CRMID=3224, esteja em locais diferentes na mesma jornada.

## Editor de expressão avançado {#adv-exp-editor}

Ao definir a condição da ID de evento ou o identificador de perfil, você pode alternar para o editor de expressão avançado para criar chaves mais complexas (por exemplo, uma concatenação de dois campos dos eventos).

![](assets/journey20.png)

Você tem acesso às funções de expressão avançadas a partir do botão **[!UICONTROL Modo avançado]** se quiser executar manipulações adicionais. Essas funções permitem manipular os valores usados para realizar consultas específicas, como alterar formatos e executar concatenações de campo, levando em conta apenas uma parte de um campo (por exemplo, os 10 primeiros caracteres). Consulte esta [página](../building-journeys/expression/expressionadvanced.md).


## Visualizar o conteúdo {#preview-the-payload}

A pré-visualização de carga permite validar a definição de carga útil.

>[!NOTE]
>
>Para eventos gerados pelo sistema, ao criar um evento, antes de visualizar a pré-visualização de carga, salve o evento e abra-o novamente. Essa etapa é necessária para gerar uma ID de evento na carga.

1. Clique no ícone **[!UICONTROL Exibir carga]** para visualizar a carga útil esperada pelo sistema.

   ![](assets/journey13.png)

   Você pode observar que os campos selecionados são exibidos.

   ![](assets/journey14.png)

1. Verifique a visualização para validar a definição de carga.

1. Em seguida, é possível compartilhar a pré-visualização do conteúdo com a pessoa responsável pelo envio do evento. Esta carga pode ajudá-los a criar a configuração de envio de evento para [!DNL Journey Optimizer]. Consulte [esta página](../event/additional-steps-to-send-events-to-journey.md).
