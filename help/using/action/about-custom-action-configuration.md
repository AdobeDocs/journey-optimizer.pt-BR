---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, third-party, custom, jornada, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 067c990f7f82594418d59c3b1587a62a04799c09
workflow-type: tm+mt
source-wordcount: '1561'
ht-degree: 13%

---

# Configurar uma ação personalizada {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Ações personalizadas"
>abstract="Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase etc."

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas aos profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da jornada, no **[!UICONTROL Ação]** categoria. Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitações{#custom-actions-limitations}

As ações personalizadas vêm com algumas limitações listadas na [esta página](../start/guardrails.md).

Em parâmetros de ação personalizados, você pode passar uma coleção simples, bem como uma coleção de objetos. Saiba mais sobre as limitações de coleção no [esta página](../building-journeys/collections.md#limitations).

Observe também que os parâmetros de ações personalizadas têm um formato esperado (por exemplo: sequência, decimal etc.). Você deve ter cuidado para respeitar esses formatos esperados. Saiba mais nesta página [caso de uso](../building-journeys/collections.md).

As ações personalizadas oferecem suporte ao formato JSON somente ao usar [solicitação](../action/about-custom-action-configuration.md#define-the-message-parameters) ou [cargas de resposta](../action/action-response.md).

## Práticas recomendadas{#custom-action-enhancements-best-practices}

Ao escolher um ponto de acesso para destino usando uma ação personalizada, verifique se:

* Esse ponto de acesso pode suportar a taxa de transferência da jornada, usando configurações da [API de limitação](../configuration/throttling.md) ou da [API de limite](../configuration/capping.md) para limitá-la. Tenha cuidado, pois uma configuração de limitação não pode ficar abaixo de 200 TPS. Qualquer ponto de acesso como destino precisará oferecer suporte a pelo menos 200 TPS.
* Esse ponto de acesso precisa ter um tempo de resposta o mais baixo possível. Dependendo da taxa de transferência esperada, ter um tempo de resposta alto pode afetar a taxa de transferência real.

Um limite máximo de 300.000 chamadas em um minuto é definido para todas as ações personalizadas. Além disso, o limite padrão é executado por host e por sandbox. Por exemplo, em uma sandbox, se você tiver dois pontos de acesso com o mesmo host (por exemplo: `https://www.adobe.com/endpoint1` e `https://www.adobe.com/endpoint2`), o limite será aplicado a todos os pontos de acesso no host adobe.com. &quot;endpoint1&quot; e &quot;endpoint2&quot; compartilharão a mesma configuração de limitação e fazer com que um endpoint atinja o limite terá impacto no outro endpoint.

Esse limite foi definido com base no uso pelos clientes, para proteger pontos de acesso externos direcionados por ações personalizadas. É necessário considerar isso em jornadas baseadas em público-alvo, definindo uma taxa de leitura apropriada (5.000 perfis por segundo ao utilizar ações personalizadas). Se necessário, é possível substituir essa configuração aumentando o limite máximo por meio das APIs de limite e limitação. Consulte [esta página](../configuration/external-systems.md).

Você não deve direcionar endpoints públicos com ações personalizadas por vários motivos:

* Sem limitação ou limitação adequada, há o risco de enviar muitas chamadas para um endpoint público que pode não suportar esse volume.
* Os dados do perfil podem ser enviados por meio de ações personalizadas, portanto, o direcionamento a um endpoint público pode levar ao compartilhamento externo inadvertido de informações pessoais.
* Você não tem controle sobre os dados que estão sendo retornados por pontos de extremidade públicos. Se um endpoint alterar sua API ou começar a enviar informações incorretas, elas serão disponibilizadas nas comunicações enviadas, com possíveis impactos negativos.

## Consentimento e governança de dados {#privacy}

No Journey Optimizer, você pode aplicar políticas de consentimento e governança de dados às ações personalizadas para impedir que campos específicos sejam exportados para sistemas de terceiros ou excluir clientes que não consentiram em receber comunicações por email, push ou SMS. Para obter mais informações, consulte as seguintes páginas:

* [Governança de dados](../action/action-privacy.md).
* [Consentimento](../action/action-privacy.md).


## Etapas de configuração {#configuration-steps}

Estas são as principais etapas necessárias para configurar uma ação personalizada:

1. Na seção de menu ADMINISTRAÇÃO, selecione **[!UICONTROL Configurações]**. No  **[!UICONTROL Ações]** clique em **[!UICONTROL Gerenciar]**. Clique em **[!UICONTROL Criar ação]** para criar uma nova ação. O painel de configuração de ação é aberto no lado direito da tela.

   ![](assets/custom2.png)

1. Digite um nome para a ação.

   >[!NOTE]
   >
   >Somente caracteres alfanuméricos e sublinhados são permitidos. O comprimento máximo é de 30 caracteres.

1. Adicione uma descrição à ação. Esta etapa é opcional.
1. O número de jornadas que usam esta ação é exibido no **[!UICONTROL Usado em]** campo. Você pode clicar no link **[!UICONTROL Exibir jornadas]** botão para exibir a lista de jornadas usando esta ação.
1. Definir o diferente **[!UICONTROL Configuração de URL]** parâmetros. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure o **[!UICONTROL Autenticação]** seção. Essa configuração é a mesma das fontes de dados.  Consulte [nesta seção](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina o **[!UICONTROL Parâmetros de ação]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Clique em **[!UICONTROL Salvar]**.

   A ação personalizada agora está configurada e pronta para ser usada em suas jornadas. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando uma ação personalizada é usada em uma jornada, a maioria dos parâmetros é somente leitura. Você só pode modificar a variável **[!UICONTROL Nome]**, **[!UICONTROL Descrição]**, **[!UICONTROL URL]** e os **[!UICONTROL Autenticação]** seção.

## Configuração do endpoint {#url-configuration}

Ao configurar uma ação personalizada, você precisa definir o seguinte **[!UICONTROL Configuração do endpoint]** parâmetros:

![](assets/action-response1bis.png){width="70%" align="left"}

1. No **[!UICONTROL URL]** especifique o URL do serviço externo:

   * Se o URL for estático, insira o URL neste campo.

   * Se o URL incluir um caminho dinâmico, insira apenas a parte estática do URL, ou seja, o esquema, o host, a porta e, opcionalmente, uma parte estática do caminho.

     Exemplo: `https://xxx.yyy.com/somethingstatic/`

     Você especificará o caminho dinâmico do URL ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Por motivos de segurança, recomendamos que você use o esquema HTTPS para o URL. Não permitimos o uso de endereços Adobe que não sejam públicos e o uso de endereços IP.
   >
   >Somente as portas padrão são permitidas ao definir uma ação personalizada: 80 para http e 443 para https.

1. Selecionar a chamada **[!UICONTROL Método]**: pode ser **[!UICONTROL POST]**, **[!UICONTROL GET]** ou **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > A variável **DELETE** não há suporte para o método. Se precisar atualizar um recurso existente, selecione o **PUT** método.

1. Defina os cabeçalhos e parâmetros de consulta:

   * No **[!UICONTROL Cabeçalhos]** clique em **[!UICONTROL Adicionar um campo de cabeçalho]** para definir os cabeçalhos HTTP da mensagem de solicitação a ser enviada ao serviço externo. A variável **[!UICONTROL Tipo de conteúdo]** e **[!UICONTROL Conjunto de caracteres]** os campos de cabeçalho são definidos por padrão. Não é possível excluir esses campos. Somente o **[!UICONTROL Tipo de conteúdo]** cabeçalho pode ser modificado. Seu valor deve respeitar o formato JSON. Este é o valor padrão:

   ![](assets/content-type-header.png)

   * No **[!UICONTROL Parâmetros de consulta]** clique em **[!UICONTROL Adicionar um campo de parâmetro de Query]** para definir os parâmetros que deseja adicionar ao URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Insira o rótulo ou o nome do campo.

1. Selecione o tipo: **[!UICONTROL Constante]** ou **[!UICONTROL Variável]**. Se você selecionou **[!UICONTROL Constante]**, em seguida, insira o valor constante na variável **[!UICONTROL Valor]** campo. Se você selecionou **[!UICONTROL Variável]**, em seguida, você especificará essa variável ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Depois de ter adicionado a ação personalizada a uma jornada, ainda será possível adicionar campos de parâmetros de cabeçalho ou consulta a ela se a jornada estiver em status de rascunho. Se não quiser que a jornada seja afetada pelas alterações de configuração, duplique a ação personalizada e adicione os campos à nova ação personalizada.
   >
   >Os cabeçalhos são validados de acordo com as regras de análise de campo. Saiba mais em [esta documentação](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Suporte ao protocolo mTLS {#mtls-protocol-support}

Agora você pode usar o MTLS (Mutual Transport Layer Security) para garantir segurança aprimorada em conexões de saída para ações personalizadas de Adobe Journey Optimizer. O mTLS é um método de segurança completo para autenticação mútua que garante que ambas as partes que compartilham informações sejam quem afirmam ser antes que os dados sejam compartilhados. O mTLS inclui uma etapa adicional em comparação ao TLS, na qual o servidor também solicita o certificado do cliente e o verifica ao final.

A autenticação TLS mútuo (mTLS) é compatível com ações personalizadas. Não há necessidade de configuração adicional na ação personalizada ou na jornada para ativar o mTLS; isso ocorre automaticamente quando um terminal habilitado para mTLS é detectado. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption#mtls-protocol-support).

## Definir os parâmetros de carga {#define-the-message-parameters}

1. No **[!UICONTROL Solicitação]** cole um exemplo da carga JSON para enviar ao serviço externo. Esse campo é opcional e só está disponível para métodos de chamada POST e PUT.

1. No **[!UICONTROL Resposta]** cole um exemplo da carga útil retornada pela chamada. Este campo é opcional e está disponível para todos os métodos de chamada. Para obter informações detalhadas sobre como aproveitar as respostas de chamada da API em ações personalizadas, consulte [esta página](../action/action-response.md).

>[!NOTE]
>
>O recurso de resposta está disponível atualmente na versão beta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>O exemplo de carga útil não pode conter valores nulos. Os nomes de campos na carga não podem conter &quot;.&quot; caractere. Eles não podem começar com um caractere &quot;$&quot;.

Você poderá definir o tipo de parâmetro (por exemplo: sequência, número inteiro etc.).

Você também terá uma escolha entre especificar se um parâmetro é uma constante ou uma variável:

* **Constante** significa que o valor do parâmetro é definido no painel de configuração de ação por uma pessoa técnica. O valor será sempre o mesmo nas jornadas. Ela não variará e o profissional de marketing não a verá ao usar a ação personalizada na jornada. Pode ser, por exemplo, uma ID que o sistema de terceiros espera. Nesse caso, o campo à direita da constante/variável de alternância é o valor transmitido.
* **Variável** significa que o valor do parâmetro varia. Os profissionais de marketing que usam essa ação personalizada em uma jornada poderão passar o valor desejado ou especificar onde recuperar o valor desse parâmetro (por exemplo, do evento, do Adobe Experience Platform etc.). Nesse caso, o campo à direita da constante/variável de alternância é o rótulo que os comerciantes verão na jornada para nomear esse parâmetro.

![](assets/customactionpayloadmessage2.png)
