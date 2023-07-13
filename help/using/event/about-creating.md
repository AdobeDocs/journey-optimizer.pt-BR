---
solution: Journey Optimizer
product: journey optimizer
title: Configurar um evento unitário
description: Saiba como configurar um evento unitário
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: event, unitário, create, jornada
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1573'
ht-degree: 16%

---

# Configurar um evento unitário {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="Eventos unitários"
>abstract="A configuração do evento permite definir as informações que o Journey Optimizer receberá como eventos. Você pode usar vários eventos (em diferentes etapas de uma jornada), e várias jornadas podem usar o mesmo evento. Os eventos unitários são vinculados a um perfil específico. Eles podem ser baseados em regras ou gerados pelo sistema."

Os eventos unitários são vinculados a um perfil específico. Eles podem ser baseados em regras ou gerados pelo sistema.  Leia mais sobre evento unitário [nesta seção](../event/about-events.md).

Estas são as primeiras etapas para configurar um novo evento:

1. Na seção de menu ADMINISTRAÇÃO, selecione **[!UICONTROL Configurações]**. No  **[!UICONTROL Eventos]** clique em **[!UICONTROL Gerenciar]**. A lista dos eventos é exibida.

   ![](assets/jo-event1.png)

1. Clique em **[!UICONTROL Criar evento]** para criar um novo evento. O painel de configuração do evento é aberto no lado direito da tela.

   ![](assets/jo-event2.png)

1. Insira o nome do evento. Você também pode adicionar uma descrição.

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >Não use espaços ou caracteres especiais. Não use mais de 30 caracteres.

1. No **[!UICONTROL Tipo]** escolha **Unitário**.

   ![](assets/jo-event3bis.png)

1. No **[!UICONTROL Tipo de ID do evento]** selecione o tipo de ID de evento que deseja usar: **Baseado em regras** ou **Gerado pelo sistema**. Leia mais sobre os tipos de ID de evento em [nesta seção](../event/about-events.md#event-id-type).

   ![](assets/jo-event4.png)

1. O número de jornadas que usam esse evento é exibido no **[!UICONTROL Usado em]** campo. Você pode clicar no link **[!UICONTROL Exibir jornadas]** ícone para exibir a lista de jornadas usando esse evento.

1. Defina os campos schema e payload: é aqui que você seleciona as informações do evento (normalmente chamadas de payload) que o jornada espera receber. Você poderá então usar essas informações em sua jornada. Consulte [esta seção](../event/about-creating.md#define-the-payload-fields).

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >Ao selecionar a variável **[!UICONTROL Gerado pelo sistema]** tipo, somente os esquemas que têm o campo de tipo eventID estão disponíveis. Ao selecionar a variável **[!UICONTROL Baseado em regras]** , todos os esquemas de Evento de experiência estarão disponíveis.

1. Para eventos baseados em regras, clique dentro da variável **[!UICONTROL Condição de ID de evento]** campo. Usando o editor de expressões simples, defina a condição que será usada pelo sistema para identificar os eventos que acionarão sua jornada.
   ![](assets/jo-event6.png)

   Em nosso exemplo, escrevemos uma condição com base na cidade do perfil. Isso significa que sempre que o sistema receber um evento que corresponda a essa condição (**[!UICONTROL Cidade]** campo e **[!UICONTROL Paris]** ), ele vai passá-lo para o jornada.

   >[!NOTE]
   >
   >O editor de expressão avançado não está disponível ao definir o **[!UICONTROL Condição de ID de evento]**. No editor de expressões simples, nem todos os operadores estão disponíveis, eles dependem do tipo de dados. Por exemplo, para um tipo de sequência de caracteres de campo, é possível usar &quot;contém&quot; ou &quot;igual a&quot;.

1. Adicione um namespace. Esta etapa é opcional, mas é recomendada, pois a adição de namespace permite que você aproveite as informações armazenadas no Serviço de perfil do cliente em tempo real. Ela define o tipo de chave que o evento tem. Consulte [esta seção](../event/about-creating.md#select-the-namespace).

1. Definir o identificador do perfil: escolha um campo a partir dos campos de carga útil ou defina uma fórmula para identificar a pessoa associada ao evento. Essa chave é configurada automaticamente (mas ainda pode ser editada) se você selecionar um namespace. Na verdade, o jornada escolhe a chave que deve corresponder ao namespace (por exemplo, se você selecionar um namespace de email, a chave de email será selecionada). Consulte [esta seção](../event/about-creating.md#define-the-event-key).

   ![](assets/jo-event7.png)

1. Clique em **[!UICONTROL Salvar]**.

   Agora o evento está configurado e pronto para ser lançado em uma jornada. Etapas de configuração adicionais são necessárias para receber eventos. Consulte [esta página](../event/additional-steps-to-send-events-to-journey.md).

## Definir os campos de carga {#define-the-payload-fields}

A definição de carga útil permite escolher as informações que o sistema espera receber do evento em sua jornada e a chave para identificar qual pessoa está associada ao evento. A carga é baseada na definição do campo XDM do Experience Cloud. Para obter mais informações sobre o XDM, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

1. Selecione um esquema XDM na lista e clique no botão **[!UICONTROL Campos]** ou no campo **[!UICONTROL Editar]** ícone.

   ![](assets/journey8.png)

   Todos os campos definidos no esquema são exibidos. A lista de campos varia de um esquema para outro. Você pode pesquisar um campo específico ou usar os filtros para exibir todos os nós e campos ou apenas os campos selecionados. De acordo com a definição do esquema, alguns campos podem ser obrigatórios e pré-selecionados. Não é possível desmarcá-los. Todos os campos obrigatórios para o evento ser recebido corretamente pelas jornadas são selecionados por padrão.

   >[!NOTE]
   >
   >Para eventos gerados pelo sistema, verifique se você adicionou o grupo de campos &quot;orquestração&quot; ao esquema XDM. Isso garantirá que seu esquema contenha todas as informações necessárias para trabalhar com [!DNL Journey Optimizer].

   ![](assets/journey9.png)

1. Selecione os campos que você espera receber do evento. Esses são os campos que o usuário empresarial utilizará na jornada. Eles também devem incluir a chave que será usada para identificar a pessoa associada ao evento (consulte [nesta seção](../event/about-creating.md#define-the-event-key)).

   >[!NOTE]
   >
   >Para eventos gerados pelo sistema, a variável **[!UICONTROL eventID]** campo é adicionado automaticamente na lista de campos selecionados para que [!DNL Journey Optimizer] pode identificar o evento. O sistema que envia o evento não deve gerar uma ID, mas usar a disponível na pré-visualização de carga. Consulte [esta seção](../event/about-creating.md#preview-the-payload).

1. Quando terminar de selecionar os campos necessários, clique em **[!UICONTROL Ok]** ou pressione **[!UICONTROL Enter]**.

   O número de campos selecionados aparece na variável **[!UICONTROL Campos]** campo.

   ![](assets/journey12.png)

## Selecionar o namespace {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="Namespace de identidade"
>abstract="Selecione a chave para identificar o perfil do cliente associado ao evento."

O namespace permite definir o tipo de chave usada para identificar a pessoa associada ao evento. Sua configuração é opcional. Ela é necessária se você quiser recuperar, em suas jornadas, informações adicionais provenientes da [Perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}. A definição do namespace não é necessária se você estiver usando apenas dados provenientes de um sistema de terceiros por meio de uma fonte de dados personalizada.

Você pode usar um dos predefinidos ou criar um novo usando o serviço de namespace de identidade. Consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=pt-BR){target="_blank"}.

Se você selecionar um esquema que tenha uma identidade primária, a variável **[!UICONTROL Identificador do profiler]** e **[!UICONTROL Namespace]** Os campos são pré-preenchidos. Se não houver identidade definida, selecionamos _identityMap > id_ como chave primária. Em seguida, é necessário selecionar um namespace e a chave será pré-preenchida (abaixo de **[!UICONTROL Namespace]** campo) usando _identityMap > id_.

Ao selecionar campos, os campos de identidade principais são marcados.

![](assets/primary-identity.png)

Selecione um namespace na lista suspensa.

![](assets/journey17.png)

Somente um namespace é permitido por jornada. Se você usar vários eventos na mesma jornada, eles precisarão usar o mesmo namespace. Consulte [esta página](../building-journeys/journey.md).

>[!NOTE]
>
>Você só pode selecionar um namespace de identidade com base em pessoas. Se você tiver definido um namespace para uma tabela de pesquisa (por exemplo: Namespace de ProductID para uma pesquisa de Produto), ele não estará disponível na **Namespace** lista suspensa.

## Definir o identificador do perfil {#define-the-event-key}

A chave é o campo, ou combinação de campos, que faz parte dos dados de payload do evento e que permite que o sistema identifique a pessoa associada ao evento. A chave pode ser, por exemplo, a ID do Experience Cloud, uma ID do CRM ou um endereço de email.

Para usar os dados armazenados no banco de dados do Perfil do cliente em tempo real do Adobe, a chave do evento deve ser a informação definida como a identidade de um perfil na [Serviço de perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}.

O identificador de perfil permite que o sistema execute a reconciliação entre o evento e o perfil do indivíduo. Se você selecionar um esquema que tenha uma identidade primária, a variável **[!UICONTROL Identificador de perfil]** e **[!UICONTROL Namespace]** Os campos são pré-preenchidos. Se não houver identidade definida, a variável _identityMap > id_ é a chave primária. Em seguida, selecione um namespace e a chave é automaticamente preenchida usando _identityMap > id_.

Ao selecionar campos, os campos de identidade principais são marcados.

![](assets/primary-identity.png)

Se você precisar usar uma chave diferente, como uma ID do CRM ou um endereço de email, precisará adicioná-lo manualmente, conforme explicado abaixo:

1. Clique dentro do **[!UICONTROL Identificador de perfil]** ou no ícone de lápis.

   ![](assets/journey16.png)

1. Selecione o campo escolhido como a chave na lista de campos de carga. Você também pode alternar para o editor de expressão avançado para criar chaves mais complexas (por exemplo, uma concatenação de dois campos dos eventos).

   ![](assets/journey20.png)

Quando o evento é recebido, o valor da chave permite que o sistema identifique a pessoa associada ao evento. Associado a um namespace (consulte [nesta seção](../event/about-creating.md#select-the-namespace)), a chave pode ser usada para executar consultas no Adobe Experience Platform. Consulte [esta página](../building-journeys/about-journey-activities.md#orchestration-activities).
A chave também é usada para verificar se uma pessoa está em uma jornada. De fato, uma pessoa não pode estar em dois lugares diferentes na mesma jornada. Como resultado, o sistema não permite que a mesma chave, por exemplo, a chave CRMID=3224, esteja em locais diferentes na mesma jornada.

Você também tem acesso às funções avançadas de expressão (**[!UICONTROL Modo avançado]**) se quiser executar manipulações adicionais. Essas funções permitem manipular os valores usados para realizar consultas específicas, como alterar formatos e executar concatenações de campo, levando em conta apenas uma parte de um campo (por exemplo, os 10 primeiros caracteres). Consulte esta [página](../building-journeys/expression/expressionadvanced.md).

## Visualizar o conteúdo {#preview-the-payload}

A pré-visualização de carga permite validar a definição de carga útil.

>[!NOTE]
>
>Para eventos gerados pelo sistema, ao criar um evento, antes de visualizar a pré-visualização de carga, salve o evento e abra-o novamente. Essa etapa é necessária para gerar uma ID de evento na carga.

1. Clique em **[!UICONTROL Exibir carga]** ícone para visualizar o conteúdo esperado pelo sistema.

   ![](assets/journey13.png)

   Você pode observar que os campos selecionados são exibidos.

   ![](assets/journey14.png)

1. Verifique a visualização para validar a definição de carga.

1. Em seguida, é possível compartilhar a pré-visualização do conteúdo com a pessoa responsável pelo envio do evento. Essa carga pode ajudá-los a projetar a configuração de um push de evento para [!DNL Journey Optimizer]. Consulte [esta página](../event/additional-steps-to-send-events-to-journey.md).
