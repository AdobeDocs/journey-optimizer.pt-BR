---
solution: Journey Optimizer
title: Configurar uma ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: bb582374f69e5c4113e22c7caed1a23d2c9ac231
workflow-type: tm+mt
source-wordcount: '1496'
ht-degree: 4%

---

# Configurar uma ação personalizada {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Ações personalizadas"
>abstract="Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. Por exemplo, você pode se conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Desenvolvedor de Adobe](https://developer.adobe.com/), Firebase, etc."

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. Por exemplo, você pode se conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Desenvolvedor de Adobe](https://developer.adobe.com){target=&quot;_blank&quot;}, Firebase, etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas para os profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da jornada, no **[!UICONTROL Action]** categoria . Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitações{#custom-actions-limitations}

As ações personalizadas vêm com algumas limitações listadas em [esta página](../start/limitations.md).

Em parâmetros de ação personalizados, é possível transmitir uma coleção simples, bem como uma coleção de objetos. Saiba mais sobre as limitações de coleção no [esta página](../building-journeys/collections.md#limitations).

Observe também que os parâmetros de ações personalizadas têm um formato esperado (por exemplo: string, decimal, etc.). Você deve ter cuidado para respeitar esses formatos esperados. Saiba mais nesta seção [caso de uso](../building-journeys/collections.md).

## Etapas de configuração {#configuration-steps}

Estas são as principais etapas necessárias para configurar uma ação personalizada:

1. Na seção do menu ADMINISTRATION (ADMINISTRAÇÃO), selecione **[!UICONTROL Configurations]**. No  **[!UICONTROL Actions]** seção , clique em **[!UICONTROL Manage]**. Clique em **[!UICONTROL Create Action]** para criar uma nova ação. O painel de configuração de ação é aberto no lado direito da tela.

   ![](assets/custom2.png)

1. Insira um nome para a ação.

   >[!NOTE]
   >
   >Não use espaços ou caracteres especiais. Não use mais de 30 caracteres.

1. Adicione uma descrição à ação. Esta etapa é opcional.
1. O número de jornadas que usam essa ação é exibido na variável **[!UICONTROL Used in]** campo. Você pode clicar no botão **[!UICONTROL View journeys]** para exibir a lista de jornadas usando essa ação.
1. Selecione o canal relacionado a esta ação personalizada: **Email**, **SMS** ou **Notificação por push**. Ele preencherá previamente o campo de ação de marketing necessário com a ação de marketing padrão para o canal selecionado. Se você selecionar **other**, nenhuma ação de marketing será definida.
1. Se quiser aplicar uma regra de consentimento a essa ação personalizada, selecione a opção **Ação de marketing necessária**. Consulte [esta seção](../action/about-custom-action-configuration.md#consent-management).
1. Defina as variáveis **[!UICONTROL URL Configuration]** parâmetros. Consulte [esta seção](../action/about-custom-action-configuration.md#url-configuration).
1. Configure o **[!UICONTROL Authentication]** seção. Essa configuração é igual à das fontes de dados.  Consulte [esta seção](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina as **[!UICONTROL Action parameters]**. Consulte [esta seção](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. 
1. Clique em **[!UICONTROL Save]**.

   A ação personalizada agora está configurada e pronta para ser usada em suas jornadas. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando uma ação personalizada é usada em uma jornada, a maioria dos parâmetros é somente leitura. Você só pode modificar o **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** e **[!UICONTROL Authentication]** seção.

## Configurar o URL {#url-configuration}

Ao configurar uma ação personalizada, você precisa definir o seguinte **[!UICONTROL URL Configuration]** parâmetros:

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

1. Selecione a chamada **[!UICONTROL Method]**: pode ser **[!UICONTROL POST]** ou **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > O **DELETE** não é suportado. Se precisar atualizar um recurso existente, selecione o **PUT** método .

1. No **[!UICONTROL Headers]** , defina os cabeçalhos HTTP da mensagem de solicitação a ser enviada ao serviço externo:
   1. Para adicionar um campo de cabeçalho, clique em **[!UICONTROL Add a header field]**.
   1. Insira a chave do campo de cabeçalho.
   1. Para definir um valor dinâmico para o par de valores chave, selecione **[!UICONTROL Variable]**. Caso contrário, selecione **[!UICONTROL Constant]**.

      Por exemplo, para um carimbo de data e hora, é possível definir um valor dinâmico.

   1. Se você selecionou **[!UICONTROL Constant]**, em seguida, insira o valor constante.

      Se você selecionou **[!UICONTROL Variable]**, você especificará essa variável ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

      ![](assets/journeyurlconfiguration2.png)

   1. Para excluir um campo de cabeçalho, aponte para o campo de cabeçalho e clique no botão **[!UICONTROL Delete]** ícone .
   O **[!UICONTROL Content-Type]** e **[!UICONTROL Charset]** os campos de cabeçalho são definidos por padrão. Não é possível modificar ou excluir esses campos.

   Após adicionar a ação personalizada a uma jornada, você ainda poderá adicionar campos de cabeçalho a ela se a jornada estiver em status de rascunho. Se não quiser que a jornada seja afetada por alterações de configuração, duplique a ação personalizada e adicione os campos de cabeçalho à nova ação personalizada.

   >[!NOTE]
   >
   >Os cabeçalhos são validados de acordo com as regras de análise de campo. Saiba mais em [esta documentação](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Definir os parâmetros de ação {#define-the-message-parameters}

![](assets/messageparameterssection.png)

No **[!UICONTROL Action parameters]** cole um exemplo da carga JSON para enviar ao serviço externo.

![](assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Os nomes de campo no payload não podem conter um &quot;.&quot; caractere. Eles não podem começar com um caractere &quot;$&quot;.

Você poderá definir o tipo de parâmetro (por exemplo: string, número inteiro, etc.).

Você também terá uma escolha entre especificar se um parâmetro é uma constante ou variável:

* Constante significa que o valor do parâmetro é definido no painel de configuração da ação por uma pessoa técnica. O valor será sempre o mesmo em jornadas. Ele não variará e o profissional de marketing não a verá ao usar a ação personalizada na jornada. Pode ser, por exemplo, uma ID que o sistema de terceiros espera. Nesse caso, o campo à direita da constante/variável de alternância é o valor transmitido.
* Variável significa que o valor do parâmetro varia. Os profissionais de marketing que usam essa ação personalizada em uma jornada poderão transmitir o valor desejado ou especificar onde recuperar o valor desse parâmetro (por exemplo, do evento, do Adobe Experience Platform etc.). Nesse caso, o campo à direita da variável/constante de alternância é o rótulo que os profissionais de marketing verão na jornada para nomear esse parâmetro.

![](assets/customactionpayloadmessage2.png)

## Gerenciamento de consentimento {#consent-management}

Os clientes agora podem definir políticas de consentimento, relacionadas à privacidade, para controlar dados de saída durante a execução da ação. Uma política de consentimento funciona como uma expressão em atributos de perfil, definindo regras para definir se uma ação pode ser executada para um determinado perfil ou não.

Consentimento em ação personalizada, passe a mensagem encore Conxent a tel type de communication ou usage de tel type de donnée champs dans profile qui vont sticker ce consent é aEP nuvelles de type policy políticas audij gouvernance policy. Exemplo de exemplo: direcionamento de email restrito. Associe label (C4/C5) a des marketing actions. Quand tu define o destino unitário, tipo de ação de marketing. Ex SFTP crée une dest qui, exportador dos données vers ce sftp, tu flague ce sftp avec une marketing action. Implemente a noção de ação de marketing rajoutée dans ação personalizada, ação de marketing por email/SMS/push. O nosso costume.

Rótulos: conjunto de dados quand tu def (où stocker tes données), gestão de dados onglet, pr chaque attribute tu peux definir le type de label associé a cet attribute. Código do país: C3/C4. Etiquetas ootb, tu peux en def d&#39;autres en fonction besoin.



— Comentários Jira—

descrever a &quot;ação de marketing adicional&quot; como uma forma de um profissional explicar a &quot;intenção&quot; de uma ação personalizada, por exemplo: minha ação personalizada é sobre comunicação de fluxo de trabalho, boletim informativo, comunicação de qualidade, etc.

Descreva o escopo do consentimento para essa primeira versão :

- As Ações e os atributos de marketing usados na personalização na ação personalizada são considerados
- Para jornadas acionadas por segmento (iniciadas com um segmento de leitura), os atributos usados como critérios nesse segmento são considerados
- Todas as atividades usadas em uma jornada, além de um Segmento de leitura ou uma Ação personalizada, não são consideradas
- A qualificação de segmento não é levada em conta, mesmo se for usada para iniciar uma jornada

Descreva que um perfil excluído por uma política de consentimento em uma ação personalizada ainda continuará a passar pela jornada (iso com lista de mensagens e supressão)

Lembrete para descrever a latência esperada: https://wiki.corp.adobe.com/display/DMSArchitecture/Consent+Latency
+ corrigir a latência de AJO de 1h a 6h

dois tipos de latência que devemos documentar:

- Latência do usuário, naquela ali Carolina Infante, não tenho certeza do que podemos dizer, olhando para isto:

Podemos confirmar se precisamos ou não da &quot;Projeção/Exportação de UPS&quot; para ocorrer, para atualizar o campo &quot;contentTo&quot; no nível do perfil (sabendo que isso é o que usamos no tempo de execução)? Como se esse fosse o caso, acho que deveríamos dizer que levaria até 48 horas, mas se não fosse, estaríamos apenas falando de &quot;latência de ingestão + latência de coleta&quot; (então alguns segundos a algumas horas do pior caso se houver picos ou interrupção na ingestão e/ou se levar muito tempo para o cliente coletar uma atualização do usuário).

- A latência da política de consentimento, eu diria &quot;até 6 horas&quot;, já que as jornadas ativas obterão políticas de consentimento a cada 6 horas. Carolina Infante, você sabe se somos afetados pela latência de filtro?
