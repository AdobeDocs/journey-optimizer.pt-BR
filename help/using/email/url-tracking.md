---
solution: Journey Optimizer
product: journey optimizer
title: Configurar rastreamento de URL
description: Saiba como configurar o rastreamento de URL no nível de configuração de canal de email
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: definições, email, configuração
exl-id: 5a12280c-b937-4cd9-a1ef-563bab48e42e
source-git-commit: ffcf4711d733dad725cbb95fd30438535c922bda
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 75%

---

# Rastreamento de URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Definir parâmetros de rastreamento de URL"
>abstract="Use essa seção para anexar automaticamente parâmetros de rastreamento aos URLs presentes no seu conteúdo de email. Esse recurso é opcional."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Visualizar parâmetros de rastreamento do URL"
>abstract="Analise como os parâmetros de rastreamento serão anexados aos URLs presentes no seu conteúdo de email."

Ao configurar uma nova [configuração de canal de email](email-settings.md), você pode definir **[!UICONTROL parâmetros de rastreamento de URL]** para medir a eficácia de seus esforços de marketing em todos os canais. A ativação desse recurso é opcional.

Os parâmetros definidos na seção correspondente serão anexados ao final dos URLs incluídos no conteúdo da mensagem de email. É possível capturar esses parâmetros em ferramentas de análise da web, como o Adobe Analytics ou Google Analytics, a fim de criar vários relatórios de desempenho.

É possível adicionar até 10 parâmetros de rastreamento usando o botão **[!UICONTROL Adicionar novo parâmetro]**.

![](assets/preset-url-tracking.png){width="80%"}

Para configurar um parâmetro de rastreamento de URL, insira os valores desejados diretamente nos campos **[!UICONTROL Nome]** e **[!UICONTROL Valor]**.

É possível editar cada campo de **[!UICONTROL Valor]** usando o [editor de personalização](../personalization/personalization-build-expressions.md). Clique no ícone de edição para abrir o editor. Em seguida, selecione os atributos contextuais disponíveis e/ou edite diretamente o texto.

![](assets/preset-url-tracking-editor.png)

Os seguintes valores predefinidos estão disponíveis por meio do editor de personalização:

* **ID do perfil de mensagem**: atributo orientado por mensagem que identifica exclusivamente cada mensagem enviada para cada perfil direcionado em uma entrega.

* **ID da oferta**: ID da oferta usada no email.

* **ID da ação de origem**: ID da ação de email adicionada à jornada ou campanha.

* **Nome da ação de origem**: nome da ação de email adicionada à jornada ou campanha.

* **ID de origem**: ID da jornada ou campanha com a qual o email foi enviado.

* **Nome de origem**: nome da jornada ou campanha com a qual o email foi enviado.

* **ID da versão de origem**: ID da versão da jornada ou campanha com a qual o email foi enviado.

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
>Você também pode adicionar parâmetros de rastreamento personalizados dinâmicos aos links presentes no seu conteúdo de email. [Saiba mais](surface-personalization.md#personalize-url-tracking)
