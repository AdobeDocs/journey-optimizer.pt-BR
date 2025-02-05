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
source-git-commit: aec3d79ad07ec6904e55afd6fc61ba9b4f403fc8
workflow-type: tm+mt
source-wordcount: '1670'
ht-degree: 20%

---

# Configurar uma ação personalizada {#configure-a-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Ações personalizadas"
>abstract="Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que as jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com sua jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase etc."

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que as jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com sua jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas aos profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da jornada, na categoria **[!UICONTROL Ação]**. Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitações{#custom-actions-limitations}

As ações personalizadas vêm com algumas limitações listadas em [esta página](../start/guardrails.md).

Em parâmetros de ação personalizados, você pode passar uma coleção simples, bem como uma coleção de objetos. Saiba mais sobre limitações de coleção em [esta página](../building-journeys/collections.md#limitations).

Observe também que os parâmetros de ações personalizadas têm um formato esperado (por exemplo: sequência, decimal etc.). Você deve ter cuidado para respeitar esses formatos esperados. Saiba mais neste [caso de uso](../building-journeys/collections.md).

As ações personalizadas só oferecem suporte ao formato JSON ao usar [solicitações](../action/about-custom-action-configuration.md#define-the-message-parameters) ou [cargas de resposta](../action/action-response.md).

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

1. Na seção de menu ADMINISTRAÇÃO, selecione **[!UICONTROL Configurações]**. Na seção **[!UICONTROL Ações]**, clique em **[!UICONTROL Gerenciar]**. Clique em **[!UICONTROL Criar ação]** para criar uma nova ação. O painel de configuração de ação é aberto no lado direito da tela.

   ![](assets/custom2.png)

1. Digite um nome para a ação.

   >[!NOTE]
   >
   >Somente caracteres alfanuméricos e sublinhados são permitidos. O comprimento máximo é de 30 caracteres.

1. Adicione uma descrição à ação. Esta etapa é opcional.
1. O número de jornadas que usam esta ação é exibido no campo **[!UICONTROL Usado em]**. Você pode clicar no botão **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas usando esta ação.
1. Defina os diferentes parâmetros de **[!UICONTROL Configuração de URL]**. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure a seção **[!UICONTROL Autenticação]**. Essa configuração é a mesma das fontes de dados.  Consulte [esta seção](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina os **[!UICONTROL Parâmetros de ação]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Clique em **[!UICONTROL Salvar]**.

   A ação personalizada agora está configurada e pronta para ser usada em suas jornadas. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando uma ação personalizada é usada em uma jornada, a maioria dos parâmetros é somente leitura. Você só pode modificar os campos **[!UICONTROL Nome]**, **[!UICONTROL Descrição]**, **[!UICONTROL URL]** e a seção **[!UICONTROL Autenticação]**.

## Configuração do endpoint {#url-configuration}

Ao configurar uma ação personalizada, você precisa definir os seguintes parâmetros de **[!UICONTROL Configuração do Ponto de Extremidade]**:

![](assets/action-response1bis.png){width="70%" align="left"}

1. No campo **[!UICONTROL URL]**, especifique a URL do serviço externo:

   * Se o URL for estático, insira o URL neste campo.

   * Se o URL incluir um caminho dinâmico, insira apenas a parte estática do URL, ou seja, o esquema, o host, a porta e, opcionalmente, uma parte estática do caminho.

     Exemplo: `https://xxx.yyy.com/somethingstatic/`

     Você especificará o caminho dinâmico do URL ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Por motivos de segurança, recomendamos que você use o esquema HTTPS para o URL. Não permitimos o uso de endereços Adobe que não sejam públicos e o uso de endereços IP.
   >
   >Somente as portas padrão são permitidas ao definir uma ação personalizada: 80 para http e 443 para https.

1. Selecione a chamada **[!UICONTROL Método]**: pode ser **[!UICONTROL POST]**, **[!UICONTROL GET]** ou **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > Não há suporte para o método **DELETE**. Se precisar atualizar um recurso existente, selecione o método **PUT**.

1. Defina os cabeçalhos e parâmetros de consulta:

   * Na seção **[!UICONTROL Cabeçalhos]**, clique em **[!UICONTROL Adicionar um campo de cabeçalho]** para definir os cabeçalhos HTTP da mensagem de solicitação a ser enviada ao serviço externo. Os campos de cabeçalho **[!UICONTROL Content-Type]** e **[!UICONTROL Charset]** são definidos por padrão. Não é possível excluir esses campos. Somente o cabeçalho **[!UICONTROL Content-Type]** pode ser modificado. Seu valor deve respeitar o formato JSON. Este é o valor padrão:

   ![](assets/content-type-header.png)

   * Na seção **[!UICONTROL Parâmetros de consulta]**, clique em **[!UICONTROL Adicionar um campo de parâmetro de consulta]** para definir os parâmetros que deseja adicionar à URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Insira o rótulo ou o nome do campo.

1. Selecione o tipo: **[!UICONTROL Constante]** ou **[!UICONTROL Variável]**. Se você selecionou **[!UICONTROL Constante]**, insira o valor constante no campo **[!UICONTROL Valor]**. Se você selecionou **[!UICONTROL Variável]**, especificará essa variável ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Depois de ter adicionado a ação personalizada a uma jornada, ainda será possível adicionar campos de parâmetros de cabeçalho ou consulta a ela se a jornada estiver em status de rascunho. Se não quiser que a jornada seja afetada pelas alterações de configuração, duplique a ação personalizada e adicione os campos à nova ação personalizada.
   >
   >Os cabeçalhos são validados de acordo com as regras de análise de campo. Saiba mais em [esta documentação](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Suporte ao protocolo mTLS {#mtls-protocol-support}

Você pode usar o MTLS (Mutual Transport Layer Security) para garantir segurança aprimorada em conexões de saída para ações personalizadas de Adobe Journey Optimizer. O mTLS é um método de segurança completo para autenticação mútua que garante que ambas as partes que compartilham informações sejam quem afirmam ser antes que os dados sejam compartilhados. O mTLS inclui uma etapa adicional em comparação ao TLS, na qual o servidor também solicita o certificado do cliente e o verifica ao final.

A autenticação TLS mútuo (mTLS) é compatível com ações personalizadas. Não é necessária uma configuração adicional da ação personalizada ou jornada para ativar o mTLS; isso ocorre automaticamente ao detectar um ponto de acesso habilitado para mTLS. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption#mtls-protocol-support).

## Definir os parâmetros de carga {#define-the-message-parameters}

Você pode definir o parâmetro de carga útil conforme detalhado abaixo:

1. Na seção **[!UICONTROL Solicitação]**, cole um exemplo da carga JSON para enviar ao serviço externo. Esse campo é opcional e só está disponível para métodos de chamada POST e PUT.

   Habilite a opção **[!UICONTROL Permitir valores NULL]** para manter valores Null na chamada externa. Observe que o envio de matrizes de int, string etc. com valores Null em não é totalmente compatível. Por exemplo, a seguinte matriz de inteiros `[1, null, 2, 3]` é enviada como `[1, 2, 3]` mesmo que esta opção esteja marcada. Além disso, se tal matriz for nula, ela será enviada como uma matriz vazia.

   ![](assets/null-values.png){width="70%" align="left"}

1. Na seção **[!UICONTROL Resposta]**, cole um exemplo da carga retornada pela chamada. Este campo é opcional e está disponível para todos os métodos de chamada. Para obter informações detalhadas sobre como aproveitar as respostas de chamada da API em ações personalizadas, consulte [esta página](../action/action-response.md).

>[!NOTE]
>
>Os nomes de campos na carga não podem conter um caractere de ponto `.`, nem começar com um caractere `$`.
>

![](assets/customactionpayloadmessage2.png)

Na configuração do campo, você deve:

* Selecione o tipo de parâmetro, por exemplo: string, inteiro etc.

* Defina uma constante ou um parâmetro de variável:

   * **Constante** significa que o valor do parâmetro é definido no painel de configuração da ação por um usuário técnico. O valor será sempre o mesmo nas jornadas. Ela não varia e o profissional de marketing não consegue visualizá-la ao usar a ação personalizada na jornada. Pode ser, por exemplo, uma ID que o sistema de terceiros espera. Nesse caso, o valor constante é definido no campo à direita da constante/variável de alternância.

   * **Variável** significa que o valor do parâmetro pode variar. Os profissionais de marketing que usam essa ação personalizada em uma jornada podem passar o valor desejado ou especificar onde recuperar o valor desse parâmetro (por exemplo, do evento, do Adobe Experience Platform etc.). Nesse caso, o campo à direita da constante/variável de alternância é o rótulo que os comerciantes verão na jornada para nomear esse parâmetro.

  Para parâmetros opcionais, habilite a opção **[!UICONTROL Is optional]** no final da linha. Ao marcar essa opção, você marca o parâmetro como não obrigatório e permite que os profissionais de jornada optem por preenchê-lo ou não ao criar essa ação personalizada em uma jornada.

>[!NOTE]
>
>Se você configurar parâmetros opcionais enquanto permite valores Nulos, os parâmetros não preenchidos por um profissional do jornada serão enviados como Nulos.
>