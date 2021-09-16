---
solution: Journey Orchestration
title: Sobre a configuração de ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 967772bcf7413c4c916d045375a84807581ea6ae
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 6%

---

# Configurar uma ação {#configure-an-action}

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, é aqui que você configura a conexão com o jornada. A ação personalizada definida pelos usuários técnicos estará disponível na paleta esquerda da jornada, na categoria **[!UICONTROL Action]** (consulte [esta página](../building-journeys/about-journey-activities.md#action-activities). Estes são alguns exemplos de sistemas aos quais você pode se conectar com ações personalizadas: Epsilon, Facebook, Adobe.io, Firebase, etc.
As limitações são listadas em [this page](../limitations.md).

Estas são as principais etapas necessárias para configurar uma ação personalizada:

1. Na seção do menu ADMINISTRATION , selecione **[!UICONTROL Configurations]**. Na seção **[!UICONTROL Actions]**, clique em **[!UICONTROL Manage]**. Clique em **[!UICONTROL Create Action]** para criar uma nova ação. O painel de configuração de ação é aberto no lado direito da tela.

   ![](../assets/custom2.png)

1. Insira um nome para a ação.

   >[!NOTE]
   >
   >Não use espaços ou caracteres especiais. Não use mais de 30 caracteres.

1. Adicione uma descrição à ação. Esta etapa é opcional.
1. O número de jornadas que usam essa ação é exibido no campo **[!UICONTROL Used in]**. Você pode clicar no botão **[!UICONTROL View journeys]** para exibir a lista de jornadas usando esta ação.
1. Defina os diferentes parâmetros **[!UICONTROL URL Configuration]**. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure a seção **[!UICONTROL Authentication]**. Essa configuração é igual à das fontes de dados.  Consulte [esta seção](../datasource/external-data-sources.md#section_wjp_nl5_nhb).
1. Defina o **[!UICONTROL Action parameters]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Clique em **[!UICONTROL Save]**.

   A ação personalizada agora está configurada e pronta para ser usada em suas jornadas. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando uma ação personalizada é usada em uma jornada, a maioria dos parâmetros é somente leitura. Você só pode modificar os campos **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** e a seção **[!UICONTROL Authentication]**.

## Configurar o URL {#url-configuration}

Ao configurar uma ação personalizada, você precisa definir os seguintes parâmetros **[!UICONTROL URL Configuration]**:

![](../assets/journeyurlconfiguration.png)

1. No campo **[!UICONTROL URL]** , especifique o URL do serviço externo:

   * Se o URL for estático, insira o URL neste campo.

   * Se o URL incluir um caminho dinâmico, insira apenas a parte estática do URL, ou seja, o esquema, o host, a porta e, opcionalmente, uma parte estática do caminho.

      Exemplo: `https://xxx.yyy.com:8080/somethingstatic/`

      Você especificará o caminho dinâmico do URL ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >Por motivos de segurança, recomendamos que você use o esquema HTTPS para o URL. Não permitimos o uso de endereços Adobe que não são públicos e o uso de endereços IP.

1. Selecione a chamada **[!UICONTROL Method]**: pode ser **[!UICONTROL POST]** ou **[!UICONTROL PUT]**.
1. Na seção **[!UICONTROL Headers]** , defina os cabeçalhos HTTP da mensagem de solicitação a ser enviada ao serviço externo:
   1. Para adicionar um campo de cabeçalho, clique em **[!UICONTROL Add a header field]**.
   1. Insira a chave do campo de cabeçalho.
   1. Para definir um valor dinâmico para o par de valores chave, selecione **[!UICONTROL Variable]**. Caso contrário, selecione **[!UICONTROL Constant]**.

      Por exemplo, para um carimbo de data e hora, é possível definir um valor dinâmico.

   1. Se você selecionou **[!UICONTROL Constant]**, insira o valor constante.

      Se tiver selecionado **[!UICONTROL Variable]**, você especificará essa variável ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

      ![](../assets/journeyurlconfiguration2.png)

   1. Para excluir um campo de cabeçalho, aponte para o campo de cabeçalho e clique no ícone **[!UICONTROL Delete]**.
   Os campos de cabeçalho **[!UICONTROL Content-Type]** e **[!UICONTROL Charset]** são definidos por padrão. Não é possível modificar ou excluir esses campos.

   Após adicionar a ação personalizada a uma jornada, você ainda poderá adicionar campos de cabeçalho a ela se a jornada estiver em status de rascunho. Se não quiser que a jornada seja afetada por alterações de configuração, duplique a ação personalizada e adicione os campos de cabeçalho à nova ação personalizada.

   >[!NOTE]
   >
   >Os cabeçalhos são validados de acordo com as regras de análise de campo. [Saiba mais](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## Definir os parâmetros de ação {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

Na seção **[!UICONTROL Action parameters]**, cole um exemplo da carga JSON para enviar ao serviço externo.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Os nomes de campo no payload não podem conter um &quot;.&quot; caractere. Eles não podem começar com um caractere &quot;$&quot;.

Você poderá definir o tipo de parâmetro (por exemplo: string, número inteiro, etc.).

Você também terá uma escolha entre especificar se um parâmetro é uma constante ou variável:

* Constante significa que o valor do parâmetro é definido no painel de configuração da ação por uma pessoa técnica. O valor será sempre o mesmo em jornadas. Ele não variará e o profissional de marketing não a verá ao usar a ação personalizada na jornada. Pode ser, por exemplo, uma ID que o sistema de terceiros espera. Nesse caso, o campo à direita da constante/variável de alternância é o valor transmitido.
* Variável significa que o valor do parâmetro varia. O profissional de marketing que usa essa ação personalizada em uma jornada poderá transmitir o valor desejado ou especificar onde recuperar o valor desse parâmetro (por exemplo, do evento, da Adobe Experience Platform etc.). Nesse caso, o campo à direita da constante/variável de alternância é o rótulo que o profissional de marketing verá na jornada para nomear esse parâmetro.

![](../assets/customactionpayloadmessage2.png)
