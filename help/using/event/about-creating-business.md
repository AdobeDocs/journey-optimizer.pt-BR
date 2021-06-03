---
title: Configurar um evento comercial
description: Saiba como criar um evento comercial
source-git-commit: 4464ea7169424c1ec6212394b8bda79a9bec1913
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 14%

---

# Configurar um evento comercial {#configure-a-business-event}

![](../assets/do-not-localize/badge.png)

Ao contrário de eventos unitários, os eventos de negócios não estão vinculados a um perfil específico. O tipo de ID de evento sempre se baseia em regras. Leia mais sobre eventos comerciais em [esta seção](../event/about-events.md).

As jornadas baseadas em segmentos de leitura podem ser acionadas uma única vez, por um programador regularmente ou por um evento de negócios, quando o evento ocorre.

Os eventos comerciais podem ser &quot;um produto está de volta ao estoque&quot;, &quot;o preço das ações de uma empresa atinge um determinado valor&quot;, etc.

## Observações importantes

* O schema de eventos deve conter uma identidade primária.
* Os eventos comerciais só podem ser descartados como a primeira etapa de uma jornada.
* Ao soltar um evento comercial como a primeira etapa de uma jornada, o tipo de agendador da jornada será &quot;evento comercial&quot;.
* Somente uma atividade de segmento de leitura pode ser solta após um evento comercial. Ele é adicionado automaticamente como a próxima etapa.
* Os eventos comerciais não podem ser acionados com mais frequência do que uma hora.
* Depois que um evento comercial é acionado, haverá um atraso para que o segmento seja exportado de 15 minutos para até uma hora.
* Ao testar um evento comercial, você deve passar os parâmetros do evento e o identificador do perfil de teste que inserirá a jornada em teste. Além disso, ao testar uma jornada baseada em eventos empresariais, você só pode acionar a entrada de perfil único. Consulte [esta seção](../building-journeys/testing-the-journey.md#test-business). No modo de teste, não há modo de &quot;Visualização de código&quot; disponível.
* O que acontece com os indivíduos que estão atualmente na jornada se um novo evento comercial chegar? Ele se comporta da mesma forma que quando os indivíduos ainda estão em uma jornada recorrente quando ocorre uma nova recorrência. Seu caminho está encerrado. Como resultado, os profissionais de marketing devem prestar atenção para evitar a criação de jornadas muito longas se esperarem eventos comerciais frequentes.

## Introdução a eventos comerciais

Estas são as primeiras etapas para configurar um evento comercial:

1. Na seção ADMINISTRATION , navegue até **[!UICONTROL Configurations]** e clique em **[!UICONTROL Events]**. A lista dos eventos é exibida.

   ![](../assets/jo-event1.png)

1. Clique em **[!UICONTROL Add]** para criar um novo evento. O painel de configuração do evento é aberto no lado direito da tela.

   ![](../assets/jo-event2.png)

1. Insira o nome do evento. Você também pode adicionar uma descrição.

   ![](../assets/jo-event3-business.png)

   >[!NOTE]
   >
   >Não use espaços ou caracteres especiais. Não use mais de 30 caracteres.

1. No campo **[!UICONTROL Type]**, escolha **Negócios**.

   ![](../assets/jo-event3bis-business.png)

1. O número de jornadas que usam esse evento é exibido no campo **[!UICONTROL Used in]**. Você pode clicar no ícone **[!UICONTROL View journeys]** para exibir a lista de jornadas usando esse evento.

1. Defina os campos schema e payload: é aqui que você seleciona as informações do evento (normalmente chamadas de carga útil) que o jornada espera receber. Você poderá então usar essas informações em sua jornada. Consulte [esta seção](../event/about-creating-business.md#define-the-payload-fields).

   ![](../assets/jo-event5-business.png)

   Apenas estão disponíveis esquemas de séries cronológicas. Os esquemas Eventos de experiência, Eventos de decisão e Eventos de etapa de Jornada não estão disponíveis. O schema de eventos deve conter uma identidade primária.

   ![](../assets/test-profiles-4.png)

1. Clique dentro do campo **[!UICONTROL Event ID condition]**. Usando o editor de expressões simples, defina a condição que será usada pelo sistema para identificar os eventos que acionarão sua jornada.
   ![](../assets/jo-event6-business.png)

   Em nosso exemplo, escrevemos uma condição com base na ID do produto. Isso significa que sempre que o sistema receber um evento que corresponda a essa condição, ele o passará para o jornada.

1. Clique em **[!UICONTROL Save]**.

   ![](../assets/journey7-business.png)

   Agora o evento está configurado e pronto para ser lançado em uma jornada. Etapas de configuração adicionais são necessárias para receber eventos. Consulte [esta página](../event/additional-steps-to-send-events-to-journey-orchestration.md).

## Defina os campos de carga {#define-the-payload-fields}

A definição de carga permite escolher as informações que o sistema espera receber do evento em sua jornada e a chave para identificar qual pessoa está associada ao evento. A carga é baseada na definição do campo Experience Cloud XDM. Para obter mais informações sobre XDM, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR).

1. Selecione um esquema XDM na lista e clique no campo **[!UICONTROL Payload]** ou no ícone **[!UICONTROL Edit]**.

   ![](../assets/journey8-business.png)

   Todos os campos definidos no schema são exibidos. A lista de campos varia de um schema para outro. Você pode pesquisar um campo específico ou usar os filtros para exibir todos os nós e campos ou somente os campos selecionados. De acordo com a definição do schema, alguns campos podem ser obrigatórios e pré-selecionados. Não é possível desmarcá-los. Todos os campos obrigatórios para o evento ser recebido corretamente pelo jornada são selecionados por padrão.

   ![](../assets/journey9-business.png)

1. Selecione os campos que você espera receber do evento. Esses são os campos que o usuário empresarial aproveitará na jornada.

   ![](../assets/journey10-business.png)

1. Quando terminar de selecionar os campos necessários, clique em **[!UICONTROL Save]** ou pressione **[!UICONTROL Enter]**.

   O número de campos selecionados aparece no campo **[!UICONTROL Payload]**.

   ![](../assets/journey12-business.png)

## Visualizar a carga {#preview-the-payload}

A pré-visualização de carga permite validar a definição da carga útil.

1. Clique no ícone **[!UICONTROL View Payload]** para visualizar a carga esperada pelo sistema.

   ![](../assets/journey13-business.png)

   Observe que os campos selecionados são exibidos.

   ![](../assets/journey14-business.png)

1. Verifique a pré-visualização para validar a definição da carga útil.

1. Em seguida, você pode compartilhar a pré-visualização de carga com a pessoa responsável pelo envio do evento. Essa carga útil pode ajudá-lo a projetar a configuração de um evento que leva para [!DNL Journey Optimizer]. Consulte [esta página](../event/additional-steps-to-send-events-to-journey-orchestration.md).
