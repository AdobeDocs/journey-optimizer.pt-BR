---
solution: Journey Orchestration
title: Sobre a configuração de ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Ações
topic: Administração
role: Administrator
level: Intermediate
source-git-commit: 265e15f3b56dfac7a5c35bf6817a5ff2da1d744a
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 9%

---

# Configurar uma ação {#configure-an-action}

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, é aqui que você configura a conexão com o jornada. A ação personalizada definida pelos usuários técnicos estará disponível na paleta esquerda da jornada, na categoria **[!UICONTROL Action]** (consulte [esta página](../building-journeys/about-journey-activities.md#action-activities). Estes são alguns exemplos de sistemas aos quais você pode se conectar com ações personalizadas: Epsilon, Facebook, Adobe.io, Firebase, etc.
As limitações são listadas em [this page](../building-journeys/limitations.md).

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

1. Adicione o **[!UICONTROL URL]** do serviço externo.

   >[!NOTE]
   >
   >Recomendamos o uso de HTTPS por motivos de segurança. Não permitimos o uso de endereços Adobe que não são públicos e o uso de endereços IP.

1. Selecione a chamada **[!UICONTROL Method]**: pode ser **[!UICONTROL POST]** ou **[!UICONTROL PUT]**.
1. Na seção **[!UICONTROL Headers]**, clique em **[!UICONTROL Add a header field]** para definir um novo par de chave/valor. Eles correspondem aos cabeçalhos HTTP da solicitação feita para o serviço externo. Para excluir pares de chave/valor, coloque o cursor no campo de cabeçalho e clique no ícone **[!UICONTROL Delete]**.

   **[!UICONTROL Content-Type]** e  **[!UICONTROL Charset]** são definidas por padrão e não podem ser excluídas ou substituídas.

   >[!NOTE]
   >
   >Os cabeçalhos são validados de acordo com as seguintes [regras de análise](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## Defina os parâmetros de ação {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

Na seção **[!UICONTROL Action parameters]**, cole um exemplo da carga JSON para enviar ao serviço externo.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Os nomes de campo no payload não podem conter um &quot;.&quot; caractere.

Você poderá definir o tipo de parâmetro (por exemplo: string, número inteiro, etc.).

Você também terá uma escolha entre especificar se um parâmetro é uma constante ou variável:

* Constante significa que o valor do parâmetro é definido no painel de configuração da ação por uma pessoa técnica. O valor será sempre o mesmo em jornadas. Ele não variará e o profissional de marketing não a verá ao usar a ação personalizada na jornada. Pode ser, por exemplo, uma ID que o sistema de terceiros espera. Nesse caso, o campo à direita da constante/variável de alternância é o valor transmitido.
* Variável significa que o valor do parâmetro varia. O profissional de marketing que usa essa ação personalizada em uma jornada poderá transmitir o valor desejado ou especificar onde recuperar o valor desse parâmetro (por exemplo, do evento, da Adobe Experience Platform etc.). Nesse caso, o campo à direita da constante/variável de alternância é o rótulo que o profissional de marketing verá na jornada para nomear esse parâmetro.

![](../assets/customactionpayloadmessage2.png)
