---
solution: Journey Optimizer
product: journey optimizer
title: Definir configurações de email
description: Saiba como definir as configurações de email no nível dos canais
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: definições, email, configuração
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: d782c668b412cebeacd1289c79bbf86ec710786b
workflow-type: tm+mt
source-wordcount: '2484'
ht-degree: 98%

---

# Definir configurações de email {#email-settings}

Para começar a criar um email, é preciso configurar o canal de email e definir todos os parâmetros técnicos necessários para suas mensagens. [Saiba como criar configurações](../configuration/channel-surfaces.md)

>[!NOTE]
>
>Para preservar sua reputação e melhorar a capacidade de entrega, configure os subdomínios que serão usados para enviar emails antes de criar uma configuração de email. [Saiba mais](../configuration/about-subdomain-delegation.md)

Defina as configurações de email na seção dedicada da configuração de canal, conforme detalhado abaixo.

![](assets/surface-email-settings.png){width="50%" align="left"}

A configuração de email é selecionada para o envio de comunicações seguindo a lógica abaixo:

* Isso não se aplica a execuções de jornadas em lote que foram iniciadas antes de configurar a superfície de email. As alterações são aplicadas na próxima recorrência ou na nova execução.

* No caso de mensagens transacionais, a alteração é aplicada imediatamente na próxima comunicação (com um atraso de até cinco minutos).

>[!NOTE]
>
>As configurações de email atualizadas são aplicadas automaticamente nas jornadas ou campanhas em que são usadas.

## Tipo de email {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definir o tipo de email"
>abstract="Selecione o tipo de email que será enviado ao usar essa configuração: “Marketing” para emails promocionais que exigem consentimento do usuário ou “Transacional” para emails não comerciais que também podem ser enviados para perfis sem assinatura em contextos específicos."

Na seção **Tipo de email**, selecione o tipo de mensagem para a configuração: **[!UICONTROL Marketing]** ou **[!UICONTROL Transacional]**.

* Selecione **Marketing** para emails promocionais, como promoções semanais para uma loja de varejo. Essas mensagens exigem o consentimento do usuário.

* Selecione **Transacional** para emails não comerciais, como confirmações de pedidos, notificações de redefinição de senha ou informações de entrega, por exemplo. Esses emails podem ser enviados para perfis que **cancelaram a assinatura** de comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos.

Ao criar uma mensagem, é necessário escolher uma configuração de canal válida que corresponda à categoria selecionada para o email.

## Subdomínio {#subdomains}

Selecione o subdomínio que será usado para enviar os emails.

>[!NOTE]
>
>Para ter maior controle sobre as configurações de email, é possível definir subdomínios dinâmicos. [Saiba mais](../email/surface-personalization.md#dynamic-subdomains)

Para preservar a reputação do domínio, acelerar o processo de aquecimento de IP e aprimorar a capacidade de entrega, delegue os subdomínios de envio à Adobe. [Saiba mais](../configuration/about-subdomain-delegation.md)

## Detalhes do pool de IP {#ip-pools}

Selecione o pool de IP para associar à configuração. [Saiba mais](../configuration/ip-pools.md)

![](assets/surface-subdomain-ip-pool.png){width="50%" align="left"}

Não é possível continuar a criar a configuração enquanto o pool de IP selecionado estiver em [edição](../configuration/ip-pools.md#edit-ip-pool) (status **[!UICONTROL Processando]**) e não tiver sido associado ao subdomínio selecionado. Caso contrário, a versão mais antiga da associação de pool/subdomínio de IP ainda será usada. Se esse for o caso, salve a configuração como rascunho e tente novamente depois que o pool de IP atingir o status **[!UICONTROL Sucesso]**.

>[!NOTE]
>
>Para ambientes de não produção, a Adobe não cria subdomínios de teste prontos para uso nem concede acesso a um pool de IP de envio compartilhado. Nesses casos, é necessário [delegar seus próprios subdomínios](../configuration/delegate-subdomain.md) e usar os IPs do pool atribuído à sua organização.

Após selecionar um pool de IP, as informações de PTR ficam visíveis ao passar o mouse sobre os endereços IP exibidos abaixo da lista suspensa do pool de IP. [Saiba mais sobre registros PTR](../configuration/ptr-records.md)

>[!NOTE]
>
>Se não houver um registro PTR configurado, entre em contato com o(a) representante da Adobe.

## Cancelar inscrição em lista {#list-unsubscribe}

Ao selecionar um subdomínio na lista, a opção **[!UICONTROL Habilitar List-Unsubscribe]** é exibida. Ela é ativada por padrão.

Ele permite incluir um URL de cancelamento de inscrição de um clique no cabeçalho do email. [Saiba mais](list-unsubscribe.md)

## Parâmetros de cabeçalho {#email-header}

Na seção **[!UICONTROL Parâmetros de cabeçalho]**, digite os nomes e endereços de email do remetente associados aos tipos de emails enviados usando essa configuração.

>[!NOTE]
>
>Para ter maior controle sobre as configurações de email, é possível personalizar os parâmetros do cabeçalho. [Saiba mais](../email/surface-personalization.md#personalize-header)

* **[!UICONTROL Nome do remetente]**: o nome do remetente, como o nome da sua marca.
* **[!UICONTROL Prefixo do email do remetente]**: o endereço de email que você deseja usar para suas comunicações.
* **[!UICONTROL Responder a (nome)]**: o nome que será usado quando o destinatário clicar no botão **Responder** do software do cliente de email.
* **[!UICONTROL Email de resposta]**: o endereço de email que será usado quando o destinatário clicar no botão **Responder** do software do cliente de email. [Saiba mais](#reply-to-email)
* **[!UICONTROL Prefixo do email de erro]**: todos os erros gerados pelos ISPs após alguns dias de entrega de emails (rejeições assíncronas) são recebidos neste endereço. As notificações de ausência e as respostas de desafio também são recebidas neste endereço.

  Se quiser receber notificações de ausência e respostas de desafio em um endereço de email específico que não esteja delegado à Adobe, será necessário configurar um [processo de encaminhamento](#forward-email). Nesse caso, verifique se você tem uma solução manual ou automatizada para processar os emails que chegam a essa caixa de entrada.

>[!NOTE]
>
>Os endereços de **[!UICONTROL Prefixo do email do remetente]** e **[!UICONTROL Prefixo do email de erro]** usam o [subdomínio delegado](../configuration/about-subdomain-delegation.md) selecionado no momento para enviar o email. Por exemplo, se o subdomínio delegado for *marketing.luma.com*:
>* Insira *contato* como o **[!UICONTROL Prefixo do email do remetente]**: o email do remetente é *contact@marketing.luma.com*.
>* Insira *erro* como o **[!UICONTROL Prefixo do email de erro]**: o endereço de erro é *error@marketing.luma.com*.


![](assets/preset-header.png){width="80%"}

>[!NOTE]
>
>Os endereços devem começar com uma letra (A-Z) e só podem conter caracteres alfanuméricos. Também é possível usar os caracteres de sublinhado `_`, ponto `.` e hífen `-`.

### Email de resposta {#reply-to-email}

É possível especificar qualquer endereço como **[!UICONTROL Email de resposta]**, desde que este seja um endereço de email válido, esteja no formato correto e não contenha erros de digitação.

A caixa de entrada de respostas receberá todos os emails de resposta, exceto notificações de ausência e respostas de desafio, que serão recebidos no endereço de **Email de erro**.

Para garantir o gerenciamento de respostas adequado, siga as recomendações abaixo:

* Verifique se a caixa de entrada dedicada tem capacidade suficiente para receber todos os emails de resposta enviados usando a configuração de email. Se a caixa de entrada retornar rejeições, algumas respostas de clientes podem não ser recebidas.

* O processamento de respostas deve respeitar os requisitos de privacidade e conformidade, pois estas podem conter informações de identificação pessoal (PII).

* Não marque mensagens como spam na caixa de entrada de resposta, pois isso afetará todas as outras respostas enviadas para esse endereço.

Além disso, ao definir o endereço de **[!UICONTROL Email de resposta]**, certifique-se de usar um subdomínio que tenha uma configuração de registro MX válida, caso contrário, o processamento da configuração de email falhará.

Se você receber um erro ao enviar a configuração de email, isto significa que o registro MX não está configurado para o subdomínio do endereço inserido. Entre em contato com o(a) admin para configurar o registro MX correspondente ou use outro endereço com uma configuração de registro MX válida.

>[!NOTE]
>
>Se o subdomínio do endereço inserido for um domínio [totalmente delegado](../configuration/delegate-subdomain.md#full-subdomain-delegation) à Adobe, entre em contato com o departamento executivo de conta da Adobe.

### Email de encaminhamento {#forward-email}

Para encaminhar a um endereço de email específico todos os emails recebidos pelo [!DNL Journey Optimizer] referentes ao subdomínio delegado, entre em contato com o Atendimento ao cliente da Adobe.

>[!NOTE]
>
>Se o subdomínio usado para o endereço de **[!UICONTROL Email de resposta]** não for delegado à Adobe, o encaminhamento não funcionará para esse endereço.

É necessário fornecer:

* O endereço de email de encaminhamento de sua escolha. Observe que o domínio do endereço de email de encaminhamento não pode corresponder a nenhum subdomínio delegado à Adobe.
* O nome da sandbox.
* O nome da configuração ou o subdomínio para o qual o endereço de email de encaminhamento será usado.
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>Só é permitido um endereço de email de encaminhamento por subdomínio. Consequentemente, se várias configurações usarem o mesmo subdomínio, o mesmo endereço de email de encaminhamento deverá ser usado em todas elas.

O endereço de email de encaminhamento é definido pela Adobe. Isso pode levar de 3 a 4 dias.

Após a conclusão desse processo, todas as mensagens recebidas nos endereços de **[!UICONTROL Email de resposta]** e **Email de erro**, bem como todos os emails enviados para o endereço de **Email do remetente** serão encaminhados para o endereço de email específico fornecido.

>[!NOTE]
>
>Se o encaminhamento não estiver habilitado, os emails enviados diretamente para o endereço de **Email do remetente** serão descartados por padrão.

## Email de cópia (CCO) {#bcc-email}

É possível enviar uma cópia idêntica (ou cópia oculta) de emails enviados pelo [!DNL Journey Optimizer] a uma caixa de entrada em cópia (CCO), onde serão armazenados para fins de conformidade ou arquivamento.

Para fazer isso, habilite o recurso opcional **[!UICONTROL Email de cópia (CCO)]** no nível de configuração do canal. [Saiba mais](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

Além disso, ao definir o endereço de **[!UICONTROL Email de cópia (CCO)]**, certifique-se de usar um subdomínio que tenha uma configuração de registro MX válida, caso contrário, o processamento da configuração de email falhará.

Se você receber um erro ao enviar a configuração de email, isto significa que o registro MX não está configurado para o subdomínio do endereço inserido. Entre em contato com o(a) admin para configurar o registro MX correspondente ou use outro endereço com uma configuração de registro MX válida.

## Envio para endereços de email suprimidos {#send-to-suppressed-email-addresses}

>[!CONTEXTUALHELP]
>id="ajo_surface_suppressed_addresses"
>title="Substituir precedência da lista de supressão"
>abstract="Você pode decidir enviar mensagens transacionais a perfis mesmo que seus endereços de email estejam na lista de supressão do Adobe Journey Optimizer devido a uma reclamação de spam. Essa opção está desabilitada por padrão."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html?lang=pt-BR" text="Gerenciar a lista de supressão"

>[!IMPORTANT]
>
>Esta opção só estará disponível se você tiver selecionado o tipo de email **[!UICONTROL Transacional]**. [Saiba mais](#email-type)

No [!DNL Journey Optimizer], todos os endereços de email marcados como rejeições permanentes, rejeições temporárias e spam são automaticamente coletados na [lista de supressão](../configuration/manage-suppression-list.md) e excluídos da lista de envio de uma jornada ou campanha.

No entanto, é possível continuar enviando mensagens do tipo **transacional** aos perfis, mesmo que seus endereços de email estejam na lista de supressão devido a reclamações de spam do usuário.

Na verdade, as mensagens transacionais geralmente contêm informações úteis e esperadas, como uma confirmação de pedido ou uma notificação de redefinição de senha. Portanto, mesmo que tenham relatado uma de suas mensagens de marketing como spam, na maioria das vezes, é desejável que seus clientes recebam esse tipo de email não comercial.

Para incluir endereços de email suprimidos devido a reclamações de spam no público-alvo da mensagem transacional, selecione a opção correspondente na seção **[!UICONTROL Enviar para endereços de email suprimidos]**.

![](assets/preset-suppressed-email-addresses.png)

>[!NOTE]
>
>Essa opção está desabilitada por padrão.

Como prática recomendada de capacidade de entrega, essa opção é desabilitada por padrão para garantir que clientes que optaram por rejeitar mensagens não sejam contatados. No entanto, é possível alterar essa opção padrão, o que permite enviar mensagens transacionais a clientes.

Após habilitar essa opção, mesmo se um(a) cliente marcar o email de marketing como spam, ele(a) poderá receber as mensagens transacionais usando a configuração atual. Certifique-se sempre de gerenciar as preferências de recusa de acordo com as práticas recomendadas de capacidade de entrega.

## Lista de sementes {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="Adicionar uma lista de seeds"
>abstract="Selecione uma lista de seeds de sua escolha para adicionar automaticamente endereços internos específicos aos seus públicos-alvo. Esses seed addresses serão incluídos na hora da execução da tarefa e receberão uma cópia exata da mensagem para fins de garantia."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html?lang=pt-BR#use-seed-list" text="O que são listas de seeds?"

Uma lista de seeds no [!DNL Journey Optimizer] permite incluir seed addresses de emails específicos automaticamente em suas entregas. [Saiba mais](../configuration/seed-lists.md)

>[!CAUTION]
>
>Atualmente, esse recurso se aplica somente ao canal de email.

Selecione a lista relevante na seção **[!UICONTROL Lista de seeds]**. Saiba como criar uma lista de seeds [nesta seção](../configuration/seed-lists.md#create-seed-list).

![](../configuration/assets/seed-list-surface.png){width="80%"}

>[!NOTE]
>
>Só é possível selecionar uma lista de seeds por vez.

Ao usar a configuração atual em uma campanha ou jornada, os endereços de email na lista de seeds selecionada são incluídos no tempo de execução da entrega, o que significa que receberão uma cópia da entrega para fins de garantia.

Saiba como usar listas de seeds em uma campanha ou jornada [nesta seção](../configuration/seed-lists.md#use-seed-list).

## Parâmetros de nova tentativa do email {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Ajustar o período de nova tentativa"
>abstract="As tentativas são executadas por 3,5 dias (84 horas) quando uma entrega de email falha devido a um erro de rejeição temporária. Você pode ajustar esse período de tentativas padrão para atender melhor às suas necessidades."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html?lang=pt-BR" text="Sobre tentativas"

É possível configurar os **parâmetros de nova tentativa do email**.

![](assets/preset-retry-parameters.png)

Por padrão, o [período de nova tentativa](../configuration/retries.md#retry-duration) está definido como 84 horas, mas é possível ajustar essa configuração para melhor atender às suas necessidades.

Você deve inserir um valor inteiro (em horas ou minutos) dentro do seguinte intervalo:

* Para emails de marketing, o período mínimo para novas tentativas é de 6 horas.
* Para emails transacionais, o período mínimo para novas tentativas é de 10 minutos.
* Para ambos os tipos de email, o período máximo de novas tentativas é de 84 horas (ou 5040 minutos).

Saiba mais sobre novas tentativas [nesta seção](../configuration/retries.md).

## Rastreamento de URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Definir parâmetros de rastreamento de URL"
>abstract="Use essa seção para anexar automaticamente parâmetros de rastreamento aos URLs presentes no seu conteúdo de email. Esse recurso é opcional."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Visualizar parâmetros de rastreamento do URL"
>abstract="Analise como os parâmetros de rastreamento serão anexados aos URLs presentes no seu conteúdo de email."

Use os **[!UICONTROL parâmetros de rastreamento de URL]** para medir a eficácia de suas ações de marketing em todos os canais. Esse recurso é opcional.

Os parâmetros definidos nesta seção serão anexados ao final dos URLs incluídos no conteúdo da mensagem de email. É possível capturar esses parâmetros em ferramentas de análise da web, como o Adobe Analytics ou Google Analytics, a fim de criar vários relatórios de desempenho.

É possível adicionar até 10 parâmetros de rastreamento usando o botão **[!UICONTROL Adicionar novo parâmetro]**.

![](assets/preset-url-tracking.png){width="80%"}

Para configurar um parâmetro de rastreamento de URL, insira os valores desejados diretamente nos campos **[!UICONTROL Nome]** e **[!UICONTROL Valor]**.

É possível editar cada campo de **[!UICONTROL Valor]** usando o [editor de personalização](../personalization/personalization-build-expressions.md). Clique no ícone de edição para abrir o editor. Em seguida, selecione os atributos contextuais disponíveis e/ou edite diretamente o texto.

![](assets/preset-url-tracking-editor.png)

Os seguintes valores predefinidos estão disponíveis por meio do editor de personalização:

* **ID da ação de origem**: ID da ação de email adicionada à jornada ou campanha.

* **Nome da ação de origem**: nome da ação de email adicionada à jornada ou campanha.

* **ID de origem**: ID da jornada ou campanha com a qual o email foi enviado.

* **Nome de origem**: nome da jornada ou campanha com a qual o email foi enviado.

* **ID da versão de origem**: ID da versão da jornada ou campanha com a qual o email foi enviado.

* **ID da oferta**: ID da oferta usada no email.

>[!NOTE]
>
>É possível digitar valores de texto e também usar atributos contextuais do editor de personalização. Cada campo **[!UICONTROL Valor]** pode conter um número de caracteres até o limite de 5 KB.

<!--You can drag and drop the parameters to reorder them.-->

Veja abaixo alguns exemplos de URLs compatíveis com o Adobe Analytics e o Google Analytics.

* URL compatível com o Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatível com o Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

É possível visualizar o URL de rastreamento resultante em tempo real. Cada vez que você adiciona, edita ou remove um parâmetro, a visualização é atualizada automaticamente.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>Também é possível adicionar parâmetros de rastreamento personalizados e dinâmicos aos links presentes no conteúdo do email, mas isso não é possível no nível de configuração. Você deve fazer isso ao criar sua mensagem usando o designer de email. [Saiba mais](message-tracking.md#url-tracking)

## Endereço de execução {#execution-address}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="Substituir o endereço de execução padrão a ser usado"
>abstract="Quando vários endereços de email estão disponíveis no banco de dados (pessoal, profissional etc.), você pode escolher qual deles priorizar para envio. O endereço principal é definido no nível da sandbox, mas aqui você pode substituir a configuração padrão para essa configuração de email específica."

Ao direcionar um perfil, pode haver vários endereços de email disponíveis no banco de dados (endereço de email profissional, endereço de email pessoal etc.).

Nesse caso, o [!DNL Journey Optimizer] usa o endereço especificado nos **[!UICONTROL Campos de execução]** no nível da sandbox para determinar qual endereço de email do serviço de perfil usar com prioridade. [Saiba mais](../configuration/primary-email-addresses.md)

>[!NOTE]
>
>Para verificar os campos que são usados por padrão no momento, acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Campos de execuções]**.

No entanto, é possível alterar esse campo de execução padrão no nível de configuração do canal de email. É possível aplicar essa configuração a campanhas ou jornadas específicas.

Para fazer isso, edite o campo **[!UICONTROL Endereço de entrega]** e selecione um item na lista de campos XDM do tipo email disponíveis.

![](assets/email-config-delivery-address.png)

O campo de execução é atualizado e usado como o endereço principal. Isso substitui a configuração geral no nível da sandbox.
