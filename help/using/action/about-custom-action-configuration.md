---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Experienced
keywords: action, third-party, custom, jornada, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: bd7ed127c09e24dc1b29c4fcdecb8a2fd70c9009
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 13%

---

# Configurar uma ação personalizada {#configure-a-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Ações personalizadas"
>abstract="Se está usando um sistema de terceiros para enviar mensagens ou se quer que as jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. "

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que as jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com sua jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas aos profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da jornada, na categoria **[!UICONTROL Ação]**. Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).


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

## Limitações{#custom-actions-limitations}

As ações personalizadas vêm com algumas limitações listadas em [esta página](../start/guardrails.md).

Em parâmetros de ação personalizados, você pode passar uma coleção simples, bem como uma coleção de objetos. Saiba mais sobre as limitações de coleção em [esta página](../building-journeys/collections.md#limitations).

Observe também que os parâmetros de ações personalizadas têm um formato esperado (por exemplo: sequência, decimal etc.). Você deve ter cuidado para respeitar esses formatos esperados. Saiba mais neste [caso de uso](../building-journeys/collections.md).

As ações personalizadas só oferecem suporte ao formato JSON ao usar [solicitações](../action/about-custom-action-configuration.md#define-the-message-parameters) ou [cargas de resposta](../action/action-response.md).

>[!NOTE]
>
>Quando um ponto de extremidade tem um tempo de resposta superior a 0,75 segundos, suas chamadas de ação personalizadas são roteadas por um [serviço de ação personalizada](../configuration/external-systems.md#response-time) lento dedicado em vez do serviço padrão.


## Práticas recomendadas{#custom-action-enhancements-best-practices}

Ao escolher um ponto de acesso para destino usando uma ação personalizada, verifique se:

* Esse ponto de acesso pode suportar a taxa de transferência da jornada, usando configurações da [API de limitação](../configuration/throttling.md) ou da [API de limite](../configuration/capping.md) para limitá-la. Tenha cuidado, pois uma configuração de limitação não pode ficar abaixo de 200 TPS. Qualquer terminal direcionado precisará oferecer suporte a pelo menos 200 TPS. Saiba mais sobre taxas de processamento de jornada [nesta seção](../building-journeys/entry-management.md#journey-processing-rate).
* Esse ponto de acesso precisa ter um tempo de resposta o mais baixo possível. Dependendo da taxa de transferência esperada, ter um tempo de resposta alto pode afetar a taxa de transferência real.

Um limite máximo de 300.000 chamadas em um minuto é definido para todas as ações personalizadas. Além disso, o limite padrão é executado por host e por sandbox. Por exemplo, em uma sandbox, se você tiver dois endpoints com o mesmo host (por exemplo, `https://www.adobe.com/endpoint1` e `https://www.adobe.com/endpoint2`), o limite será aplicado a todos os endpoints no host adobe.com. &quot;endpoint1&quot; e &quot;endpoint2&quot; compartilharão a mesma configuração de limitação e fazer com que um endpoint atinja o limite terá impacto no outro endpoint.

>[!NOTE]
>
>O limite de 300.000 chamadas por minuto é aplicado como uma **janela deslizante** por sandbox e por ponto de extremidade para pontos de extremidade com tempos de resposta inferiores a 0,75 segundos. A janela deslizante pode começar a qualquer milissegundo, o que significa que erros de limite podem ocorrer mesmo se a taxa aparecer abaixo de 300 k/min quando alinhada aos minutos do relógio. Para endpoints com tempos de resposta maiores que 0,75 segundo, um limite separado de 150.000 chamadas por 30 segundos (também uma janela deslizante) é aplicado. Saiba mais sobre pontos de extremidade lentos em [esta página](../configuration/external-systems.md#response-time).

O limite padrão de 300.000 chamadas por minuto se aplica no nível de domínio (ou seja, example.com). Se você precisar de um limite mais alto, consulte o Suporte da Adobe com evidências de uso e confirme a taxa de transferência do seu endpoint. Para solicitar um aumento de limite, forneça detalhes sobre o volume de chamadas esperado e a capacidade do endpoint. A Adobe pode personalizar o limite se o teste de capacidade demonstrar que o endpoint pode lidar com uma taxa de transferência mais alta. Para práticas recomendadas, considere reestruturar jornadas ou implementar atividades de espera para escalonar chamadas de saída e evitar erros de limite.

Esse limite foi definido com base no uso do cliente para proteger endpoints externos direcionados por ações personalizadas. Se necessário, é possível substituir essa configuração aumentando o limite máximo por meio das APIs de limite e limitação. Consulte [esta página](../configuration/external-systems.md).

Você não deve direcionar endpoints públicos com ações personalizadas por vários motivos:

* Sem limitação ou limitação adequada, há o risco de enviar muitas chamadas para um endpoint público que pode não suportar esse volume.
* Os dados do perfil podem ser enviados por meio de ações personalizadas, portanto, o direcionamento a um endpoint público pode levar ao compartilhamento externo inadvertido de informações pessoais.
* Você não tem controle sobre os dados que estão sendo retornados por pontos de extremidade públicos. Se um endpoint alterar sua API ou começar a enviar informações incorretas, elas serão disponibilizadas nas comunicações enviadas, com possíveis impactos negativos.

## Consentimento e governança de dados {#privacy}

No Journey Optimizer, você pode aplicar políticas de consentimento e governança de dados às ações personalizadas para impedir que campos específicos sejam exportados para sistemas de terceiros ou excluir clientes que não consentiram em receber comunicações por email, push ou SMS. Para obter mais informações, consulte as seguintes páginas:

* [Governança de dados](../action/action-privacy.md).
* [Consentimento](../action/action-privacy.md).


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

1. Lidar com possíveis redirecionamentos (302 respostas). **As** ações personalizadas seguem automaticamente os redirecionamentos HTTP 302 com base em cada solicitação.

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

## Camada de segurança de transporte {#tls}

### Suporte ao protocolo TLS {#tls-protocol-support}

Por padrão, o Adobe Journey Optimizer é compatível com TLS 1.3 para ações personalizadas. Se um cliente também suportar TLS 1.3, a comunicação será conduzida por TLS 1.3. Caso contrário, o processo de negociação do TLS pode recorrer ao TLS 1.2.

### Suporte ao protocolo mTLS {#mtls-protocol-support}

Você pode usar o MTLS (Mutual Transport Layer Security) para garantir segurança aprimorada em conexões de saída para ações personalizadas de Adobe Journey Optimizer. O mTLS é um método de segurança completo para autenticação mútua que garante que ambas as partes que compartilham informações sejam quem afirmam ser antes que os dados sejam compartilhados. O mTLS inclui uma etapa adicional em comparação ao TLS, na qual o servidor também solicita o certificado do cliente e o verifica ao final.

A autenticação TLS mútuo (mTLS) é compatível com ações personalizadas. Não é necessária uma configuração adicional da ação personalizada ou jornada para ativar o mTLS; isso ocorre automaticamente ao detectar um ponto de acesso habilitado para mTLS. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption#mtls-protocol-support).

## Definir os parâmetros de carga {#define-the-message-parameters}

Você pode definir o parâmetro de carga útil conforme detalhado abaixo:

1. Na seção **[!UICONTROL Solicitação]**, cole um exemplo da carga JSON para enviar ao serviço externo. Este campo é opcional e só está disponível para os métodos de chamada POST e PUT.

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


* [Solução de problemas de ação personalizada](../action/troubleshoot-custom-action.md) - Saiba como solucionar problemas de uma ação personalizada


## Recursos adicionais

Navegue pelas seções abaixo para saber mais sobre como configurar, usar e solucionar problemas de ações personalizadas:

* [Introdução a ações personalizadas](../action/action.md) - Saiba o que é uma ação personalizada e como ela ajuda você a se conectar a sistemas de terceiros
* [Usar ações personalizadas](../building-journeys/using-custom-actions.md) - Saiba como usar ações personalizadas em suas jornadas
* [Solução de problemas de ação personalizada](../action/troubleshoot-custom-action.md) - Saiba como solucionar problemas de uma ação personalizada
* [Envio de coleções em parâmetros de ação personalizados](../building-journeys/collections.md) - Saiba como enviar uma coleção em parâmetros de ação personalizados que é preenchida dinamicamente no tempo de execução

