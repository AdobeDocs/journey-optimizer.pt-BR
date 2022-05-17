---
title: Definir configurações de email
description: Saiba como definir configurações de email no nível predefinido de mensagens
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: a485c58366f0690fb2515139658224d59468a24f
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 1%

---

# Definir configurações de email {#email-settings}

Defina as configurações de email na seção dedicada da configuração predefinida de mensagem. Saiba como criar predefinições de mensagem em [esta seção](message-presets.md).

![](assets/preset-email.png)

## Tipo de email {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definir a categoria de email"
>abstract="Selecione o tipo de mensagem que será enviada ao usar esta predefinição: Marketing para mensagens promocionais, que exigem consentimento do usuário, ou Transacional para mensagens não comerciais, que também podem ser enviadas para perfis sem assinatura em contextos específicos."

No **TIPO DE EMAIL** selecione o tipo de mensagem que será enviada com a predefinição: **Marketing** ou **Transacional**.

* Choose **Marketing** para mensagens promocionais: essas mensagens exigem o consentimento do usuário.

* Choose **Transacional** para mensagens não comerciais, como confirmação de pedido, notificações de redefinição de senha ou informações de delivery, por exemplo.

>[!CAUTION]
>
>**Transacional** as mensagens podem ser enviadas aos perfis que cancelaram a assinatura das comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos.

When [criação de uma mensagem](../messages/get-started-content.md#create-new-message), você deve escolher uma predefinição de mensagem válida que corresponda à categoria selecionada para a mensagem.

## Subdomínio e pool IP {#subdomains-and-ip-pools}

No **DETALHES DO SUBDOMÍNIO E DO POOL IP** na seção , você deve:

1. Selecione o subdomínio a ser usado para enviar os emails. [Saiba mais](about-subdomain-delegation.md)

1. Selecione o pool de IP a ser associado à predefinição. [Saiba mais](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

Não é possível continuar com a criação predefinida enquanto o pool de IP selecionado estiver em [edição](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** e nunca foi associado ao subdomínio selecionado. Caso contrário, a versão mais antiga da associação do pool de IP/subdomínio ainda será usada. Se esse for o caso, salve a predefinição como rascunho e tente novamente depois que o pool de IP tiver a variável **[!UICONTROL Success]** status.

>[!NOTE]
>
>Para ambientes não relacionados à produção, o Adobe não cria subdomínios de teste prontos para uso nem concede acesso a um pool IP de envio compartilhado. Você precisa [delegar seus próprios subdomínios](delegate-subdomain.md) e usar os IPs do pool atribuído à sua organização.

## List-Unsubscribe {#list-unsubscribe}

Em [selecionar um subdomínio](#subdomains-and-ip-pools) na lista, a variável **[!UICONTROL Enable List-Unsubscribe]** será exibida.

![](assets/preset-list-unsubscribe.png)

Essa opção está ativada por padrão.

Se você deixá-lo ativado, um link de cancelamento de subscrição será incluído automaticamente no cabeçalho do email, como:

![](assets/preset-list-unsubscribe-header.png)

Se você desativar esta opção, nenhum link de cancelamento de subscrição será exibido no cabeçalho do email.

O link de cancelamento de subscrição consiste em dois elementos:

* Um **cancelar inscrição do endereço de email**, para a qual todas as solicitações de cancelamento de subscrição são enviadas.

   Em [!DNL Journey Optimizer], o endereço de email de cancelamento de inscrição é o padrão **[!UICONTROL Mailto (unsubscribe)]** endereço exibido na predefinição de mensagem, com base no [subdomínio selecionado](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* O **cancelar inscrição do URL**, que é o URL da landing page onde o usuário será redirecionado depois de cancelado a assinatura.

   Se você adicionar um [link para opção de não participação com um clique](../messages/consent.md#one-click-opt-out) para uma mensagem criada usando essa predefinição, o URL de cancelamento de subscrição será o URL definido para o link de recusa de um clique.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Se você não adicionar um link para opção de não participação com um clique no conteúdo da mensagem, nenhuma landing page será exibida para o usuário.

Saiba mais sobre como adicionar um link de cancelamento de subscrição de cabeçalho às suas mensagens em [esta seção](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parâmetros de cabeçalho{#email-header}

No **[!UICONTROL HEADER PARAMETERS]** , insira os nomes do remetente e os endereços de email associados ao tipo de mensagens enviadas usando essa predefinição.

>[!CAUTION]
>
>Os endereços de email devem usar o [subdomínio delegado](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**: O nome do remetente, como o nome da sua marca.

* **[!UICONTROL Sender email]**: O endereço de email que deseja usar para suas comunicações. Por exemplo, se o subdomínio delegado for *marketing.luma.com*, você pode usar *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**: O nome que será usado quando o recipient clicar no **Responder** no software cliente de email.

* **[!UICONTROL Reply to (email)]**: O endereço de email que será usado quando o recipient clicar no link **Responder** no software cliente de email. Você deve usar um endereço definido no subdomínio delegado (por exemplo, *reply@marketing.luma.com*), caso contrário, os emails serão descartados.

* **[!UICONTROL Error email]**: Todos os erros gerados pelos ISPs após alguns dias de envio de email (rejeições assíncronas) são recebidos neste endereço.

![](assets/preset-header.png)

>[!NOTE]
>
>Os endereços devem começar com uma letra (A-Z) e só podem conter caracteres alfanuméricos. Você também pode usar o sublinhado `_`, ponto`.` e hífen `-` caracteres.

## Parâmetros de nova tentativa de email {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Ajustar o período de tempo de nova tentativa"
>abstract="As tentativas são executadas por 3,5 dias (84 horas) quando uma mensagem de email falha devido a um erro temporário de devolução temporária. Você pode ajustar esse período de tentativas padrão para atender melhor às suas necessidades."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="Sobre tentativas"

Você pode configurar o **Parâmetros de nova tentativa de email**.

![](assets/preset-retry-parameters.png)

Por padrão, a variável [período de tempo de nova tentativa](retries.md#retry-duration) está definida para 84 horas, mas você pode ajustar essa configuração para melhor atender às suas necessidades.

Você deve inserir um valor inteiro (em horas ou minutos) dentro do seguinte intervalo:

* Para emails de marketing, o período mínimo de nova tentativa é de 6 horas.
* Para emails transacionais, o período mínimo de nova tentativa é de 10 minutos.
* Para ambos os tipos de email, o período máximo de tentativas é de 84 horas (ou 5040 minutos).

Saiba mais sobre tentativas em [esta seção](retries.md).

## Rastreamento de URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Parâmetros de rastreamento de URL"
>abstract="Use esta seção para anexar parâmetros de rastreamento automaticamente aos URLs da campanha presentes no seu conteúdo de email."

Você pode usar **[!UICONTROL URL Tracking Parameters]** para medir a eficácia de seus esforços de marketing em todos os canais. Este recurso é opcional.

Os parâmetros definidos nesta seção serão anexados ao final dos URLs incluídos no conteúdo da mensagem de email. Em seguida, você pode capturar esses parâmetros em ferramentas de análise da Web, como Adobe Analytics ou Google Analytics, e criar vários relatórios de desempenho.

![](assets/preset-url-tracking.png)

Três parâmetros de rastreamento de URL são preenchidos automaticamente como um exemplo ao criar uma predefinição de mensagem. Você pode editá-los e adicionar até 10 parâmetros de rastreamento usando o **[!UICONTROL Add new parameter]** botão.

Para configurar um parâmetro de rastreamento de URL, você pode inserir diretamente os valores desejados no **[!UICONTROL Name]** e **[!UICONTROL Value]** ou escolha em uma lista de valores predefinidos navegando até os seguintes objetos:

* Atributos de jornada: **ID de origem**, **Nome da origem**, **ID da versão de origem**
* Atributos da mensagem: **ID da ação**, **Nome da ação**
* Atributos do offer decisioning: **ID da oferta**, **Nome da oferta**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Não selecione uma pasta: navegue até a pasta necessária e selecione um atributo de perfil para usar como valor de parâmetro de rastreamento.

Abaixo estão exemplos de URLs compatíveis com Adobe Analytics e Google Analytics.

* URL compatível com Adobe Analytics: www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_imagem_{{context.system.source.name}}

* URL compatível com Google Analytics: www.YourLandingURL.com?utm_medium=email&amp;utm_source=AJO&amp;utm_campaign={{context.system.source.id}}&amp;utm_content=image

>[!NOTE]
>
>É possível combinar a digitação de valores de texto e a seleção de valores predefinidos. Cada **[!UICONTROL Value]** pode conter até 255 caracteres no total.
