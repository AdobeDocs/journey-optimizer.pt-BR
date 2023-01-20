---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Actions
topic: Administration
role: Admin
level: Experienced
keywords: ação, terceiros, personalizado, jornadas, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 6%

---

# Configurar uma ação personalizada {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Ações personalizadas"
>abstract="Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. Por exemplo, você pode se conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase, etc."

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. Por exemplo, você pode se conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas aos profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da jornada, no **[!UICONTROL Ação]** categoria . Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitações{#custom-actions-limitations}

As ações personalizadas vêm com algumas limitações listadas em [esta página](../start/guardrails.md).

Em parâmetros de ação personalizados, é possível transmitir uma coleção simples, bem como uma coleção de objetos. Saiba mais sobre as limitações de coleção no [esta página](../building-journeys/collections.md#limitations).

Observe também que os parâmetros de ações personalizadas têm um formato esperado (por exemplo: string, decimal, etc.). Você deve ter cuidado para respeitar esses formatos esperados. Saiba mais nesta seção [caso de uso](../building-journeys/collections.md).

## Consentimento e governança de dados {#privacy}

No Journey Optimizer, você pode aplicar políticas de controle e consentimento de dados às ações personalizadas para impedir que campos específicos sejam exportados para sistemas de terceiros ou excluir clientes que não consentiram em receber email, mensagens de push ou comunicações por SMS. Para obter mais informações, consulte as seguintes páginas:

* [Governança de dados](../action/action.md).
* [Consentimento](../action/action.md).


## Etapas de configuração {#configuration-steps}

Estas são as principais etapas necessárias para configurar uma ação personalizada:

1. Na seção do menu ADMINISTRATION (ADMINISTRAÇÃO), selecione **[!UICONTROL Configurações]**. No  **[!UICONTROL Ações]** seção , clique em **[!UICONTROL Gerenciar]**. Clique em **[!UICONTROL Criar ação]** para criar uma nova ação. O painel de configuração de ação é aberto no lado direito da tela.

   ![](assets/custom2.png)

1. Insira um nome para a ação.

   >[!NOTE]
   >
   >Não use espaços ou caracteres especiais. Não use mais de 30 caracteres.

1. Adicione uma descrição à ação. Esta etapa é opcional.
1. O número de jornadas que usam essa ação é exibido na variável **[!UICONTROL Usado em]** campo. Você pode clicar no botão **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas usando essa ação.
1. Defina as variáveis **[!UICONTROL Configuração de URL]** parâmetros. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure o **[!UICONTROL Autenticação]** seção. Essa configuração é igual à das fontes de dados.  Consulte [esta seção](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina as **[!UICONTROL Parâmetros de ação]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Clique em **[!UICONTROL Salvar]**.

   A ação personalizada agora está configurada e pronta para ser usada em suas jornadas. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando uma ação personalizada é usada em uma jornada, a maioria dos parâmetros é somente leitura. Você só pode modificar o **[!UICONTROL Nome]**, **[!UICONTROL Descrição]**, **[!UICONTROL URL]** e **[!UICONTROL Autenticação]** seção.

## Configurar o URL {#url-configuration}

Ao configurar uma ação personalizada, você precisa definir o seguinte **[!UICONTROL Configuração de URL]** parâmetros:

![](assets/journeyurlconfiguration.png)

1. No **[!UICONTROL URL]** , especifique o URL do serviço externo:

   * Se o URL for estático, insira o URL neste campo.

   * Se o URL incluir um caminho dinâmico, insira apenas a parte estática do URL, ou seja, o esquema, o host, a porta e, opcionalmente, uma parte estática do caminho.

      Exemplo: `https://xxx.yyy.com/somethingstatic/`

      Você especificará o caminho dinâmico do URL ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >Por motivos de segurança, recomendamos que você use o esquema HTTPS para o URL. Não permitimos o uso de endereços Adobe que não são públicos e o uso de endereços IP.
   >
   >Somente as portas padrão são permitidas ao definir uma ação personalizada: 80 para http e 443 para https.

1. Selecione a chamada **[!UICONTROL Método]**: pode ser **[!UICONTROL POST]** ou **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > O **DELETE** não é suportado. Se precisar atualizar um recurso existente, selecione o **PUT** método .

1. No **[!UICONTROL Cabeçalhos]** , defina os cabeçalhos HTTP da mensagem de solicitação a ser enviada ao serviço externo:
   1. Para adicionar um campo de cabeçalho, clique em **[!UICONTROL Adicionar um campo de cabeçalho]**.
   1. Insira a chave do campo de cabeçalho.
   1. Para definir um valor dinâmico para o par de valores chave, selecione **[!UICONTROL Variável]**. Caso contrário, selecione **[!UICONTROL Constante]**.

      Por exemplo, para um carimbo de data e hora, é possível definir um valor dinâmico.

   1. Se você selecionou **[!UICONTROL Constante]**, em seguida, insira o valor constante.

      Se você selecionou **[!UICONTROL Variável]**, você especificará essa variável ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

      ![](assets/journeyurlconfiguration2.png)

   1. Para excluir um campo de cabeçalho, aponte para o campo de cabeçalho e clique no botão **[!UICONTROL Excluir]** ícone .
   O **[!UICONTROL Tipo de conteúdo]** e **[!UICONTROL Charset]** os campos de cabeçalho são definidos por padrão. Não é possível modificar ou excluir esses campos.

   Após adicionar a ação personalizada a uma jornada, você ainda poderá adicionar campos de cabeçalho a ela se a jornada estiver em status de rascunho. Se não quiser que a jornada seja afetada por alterações de configuração, duplique a ação personalizada e adicione os campos de cabeçalho à nova ação personalizada.

   >[!NOTE]
   >
   >Os cabeçalhos são validados de acordo com as regras de análise de campo. Saiba mais em [esta documentação](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Definir os parâmetros de ação {#define-the-message-parameters}

![](assets/messageparameterssection.png)

No **[!UICONTROL Parâmetros de ação]** cole um exemplo da carga JSON para enviar ao serviço externo.

![](assets/customactionpayloadmessage.png)

>[!NOTE]
>
>O exemplo de carga útil não pode conter valores nulos. Os nomes de campo no payload não podem conter um &quot;.&quot; caractere. Eles não podem começar com um caractere &quot;$&quot;.

Você poderá definir o tipo de parâmetro (por exemplo: string, número inteiro, etc.).

Você também terá uma escolha entre especificar se um parâmetro é uma constante ou variável:

* Constante significa que o valor do parâmetro é definido no painel de configuração da ação por uma pessoa técnica. O valor será sempre o mesmo em jornadas. Ele não variará e o profissional de marketing não a verá ao usar a ação personalizada na jornada. Pode ser, por exemplo, uma ID que o sistema de terceiros espera. Nesse caso, o campo à direita da constante/variável de alternância é o valor transmitido.
* Variável significa que o valor do parâmetro varia. Os profissionais de marketing que usam essa ação personalizada em uma jornada poderão transmitir o valor desejado ou especificar onde recuperar o valor desse parâmetro (por exemplo, do evento, do Adobe Experience Platform etc.). Nesse caso, o campo à direita da variável/constante de alternância é o rótulo que os profissionais de marketing verão na jornada para nomear esse parâmetro.

![](assets/customactionpayloadmessage2.png)
