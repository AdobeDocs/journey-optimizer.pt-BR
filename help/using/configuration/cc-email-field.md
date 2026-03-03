---
solution: Journey Optimizer
product: journey optimizer
title: CC (Carbon Copy) na configuração do canal de email
description: Configure os recipients do CC visíveis no canal de email do Journey Optimizer. Saiba como definir o campo CC, como ele difere do campo CC e limitações.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
hide: true
hidefromtoc: true
keywords: CC, cópia carbono, email, configuração de canal, cabeçalhos de email, Cco
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 5b804de873124b8ff53d55c943b3c95649dd9a7c
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 1%

---

# Adicionar um campo CC aos emails {#cc-email-field}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_cc"
>title="Definir um endereço de email CC"
>abstract="Você pode adicionar um campo CC visível (cópia carbono) aos emails enviados com essa configuração de canal. Insira um endereço de email fixo ou use a personalização (atributo de perfil ou variável de contexto). Esteja ciente de que o uso do CC é contabilizado em relação ao volume de mensagens qualificado."

>[!AVAILABILITY]
>
>Este recurso está disponível para todos os clientes com Disponibilidade Limitada. Entre em contato com o representante da Adobe para obter acesso.

Você pode adicionar um campo CC visível (cópia carbono) aos emails enviados por [!DNL Journey Optimizer] por meio de suas jornadas e campanhas. Este recurso opcional é configurado no nível [configuração de canal](channel-surfaces.md), junto com os parâmetros de cabeçalho de email e a opção de email CCO.

>[!CAUTION]
>
>O uso do recurso CC é contabilizado em relação ao número de mensagens para as quais você está licenciado. Habilite-o somente onde precisar de recipients visíveis do CC. Verifique se há volumes licenciados em seu contrato.

Assim como [Cco](archiving-support.md#bcc-email), o campo Cc deve enviar uma cópia do email para um endereço adicional. No entanto, ele difere do Cco das seguintes maneiras:

* O endereço de email CC está visível para o recipient principal, portanto, ele permite que o recipient principal veja quem é copiado e saiba com quem contatar para acompanhamento.
* Ao contrário do CCO, o campo de email CCO é compatível com a personalização, que permite usar uma configuração de canal para vários cenários e enviar a cópia para a pessoa certa por recipient (por exemplo, o gerente de relacionamento). Para campanhas acionadas por API, é possível fazer o CC do endereço relevante para um evento ou transação específica.

>[!NOTE]
>
>Se você precisar manter cópias nas quais o endereço não deve estar visível para o destinatário para fins de arquivamento ou conformidade, use [Cco](archiving-support.md#bcc-email) em vez de CC.

## Habilitar email CC {#enable-cc}

Para habilitar a opção de **[!UICONTROL email CC]**, configure o campo CC na [configuração do canal de email](../email/email-settings.md).

![](assets/email-config-cc.png)

Você pode especificar qualquer endereço externo no formato correto, exceto um endereço de email definido em um subdomínio delegado à Adobe. Por exemplo, se você delegou o subdomínio *marketing.luma.com* à Adobe, qualquer endereço como *abc@marketing.luma.com* será proibido.

>[!CAUTION]
>
>Você só pode definir um endereço de email. Verifique se o endereço CC tem capacidade de recepção suficiente para armazenar todos os emails enviados usando a configuração de canal atual.
>
>Mais recomendações estão listadas em [esta seção](#cc-recommendations-limitations).

O campo **[!UICONTROL Email CC]** aceita três tipos de valores:

* Um **valor codificado**, que pode ser um endereço de email fixo.

* Um **atributo de perfil**, como o endereço de email do gerente de relacionamento, disponível no perfil.

* Um **atributo contextual** - este valor só pode **ser usado em campanhas acionadas por API**. Ele é recuperado da carga da API que deve incluir a variável de contexto `context.channel.email.ccvalues` com o valor de endereço CC.

  >[!WARNING]
  >
  >Quando CC é definida usando uma **variável de contexto**, ela só tem suporte em **campanhas acionadas por API**. Se você usar essa configuração de canal em uma campanha de jornada ou ação, o email será enviado somente para o recipient principal; nenhuma cópia será enviada para o endereço CC.

Qualquer [anexo](../email/pdf-attachments.md) incluído na mensagem é enviado ao destinatário primário e ao endereço CC.

Se o valor CC for inválido ou estiver ausente no momento do envio (por exemplo, uma variável de contexto vazia), a cópia CC será ignorada; o recipient principal ainda receberá o email.

Se houver vários valores para o campo CC (por exemplo, ao usar um atributo ou expressão de perfil que resolve para vários endereços), somente o primeiro valor será usado para enviar o email.

## Editar email CC nas configurações de canal existentes {#cc-edit}

Se você [editar uma configuração de email](channel-surfaces.md#edit-channel-surface) e adicionar ou alterar o campo CC, só poderá usar:

* Um endereço de email CC **codificado** ou
* Uma **variável de contexto** (para uso acionado por API).

>[!CAUTION]
>
>Ao editar uma configuração de canal de email existente, você não pode adicionar novos [atributos de perfil](../personalization/personalization-build-expressions.md#sources) ao campo de **[!UICONTROL email CC]**. Você deve criar uma [nova configuração de canal](channel-surfaces.md#create-channel-surface).

## Recomendações e limitações {#cc-recommendations-limitations}

* **Direitos:** o uso de CC é contado em relação ao volume de mensagens qualificado. Use CC somente onde precisar de destinatários CC visíveis. Verifique se há volumes licenciados em seu contrato.

* **Privacidade e conformidade:** para garantir sua conformidade com a privacidade, os emails CC devem ser processados por um sistema capaz de armazenar informações de identificação pessoal (PII) seguras, quando aplicável. Como as mensagens podem conter dados confidenciais ou privados, como PII, verifique se o endereço CC está correto e proteja o acesso às mensagens.

* **Gerenciamento da caixa de entrada:** sua caixa de entrada usada para CC deve ser gerenciada corretamente para espaço e entrega. Se a caixa de entrada retornar devoluções, alguns emails podem não ser recebidos.

* **Tempo de entrega:** as mensagens podem ser entregues ao endereço de email CC antes dos destinatários de destino. As mensagens CC também podem ser enviadas mesmo que as mensagens originais tenham [devolvido](../reports/suppression-list.md#delivery-failures).

* **Relatórios:** aberturas, cliques e outros engajamentos de destinatários CC estão incluídos nas métricas de relatório de email. Assim, qualquer abertura ou clique de destinatários CC causará erros de cálculo em [relatórios](../reports/report-gs-cja.md).

* **Spam:** não marque mensagens como spam na caixa de entrada CC, pois isso afetará todos os outros emails enviados para este endereço.

* **Capacidade de entrega:** use a CC de acordo com suas práticas de envio e expectativas de destinatários. O uso excessivo de CC pode afetar a capacidade de entrega; siga as [práticas recomendadas de capacidade de entrega](../reports/deliverability.md) e os termos do contrato.

>[!CAUTION]
>
>Não clique no link de cancelamento de inscrição nos emails enviados para o endereço CC, pois você cancelará imediatamente a inscrição do destinatário de email **Para**.
