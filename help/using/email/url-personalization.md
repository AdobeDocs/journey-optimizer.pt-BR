---
solution: Journey Optimizer
product: journey optimizer
title: Personalizar URLs em emails
description: Saiba mais sobre as práticas recomendadas e limitações para gerar URLs dinamicamente, além de manter o rastreamento confiável
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: url, link, personalização, rastreamento, codificar, chaves
feature_v2: []
subfeature_v2:
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 1%

---

# Personalizar URLs em emails {#url-personalization}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como personalizar URLs de email com atributos de perfil, incluindo URLs completas ou básicas e parâmetros de rastreamento por link, mantendo os links válidos e rastreáveis.

>[!ENDSHADEBOX]

As URLs personalizadas ajudam você a fornecer experiências contextuais por meio de suas mensagens de email do [!DNL Journey Optimizer], como a geração de links específicos para destinatários ou a anexação de parâmetros dinâmicos.

Eles levam os recipients para páginas específicas de um site ou para um microsite personalizado, dependendo dos atributos do perfil.

## Personalizar um URL {#personalize-url}

Para personalizar um URL, siga as etapas abaixo.

1. No Designer Email, selecione um elemento no conteúdo e [insira um link](message-tracking.md#insert-links) usando a barra de ferramentas contextual.

   >[!IMPORTANT]
   >
   >O Personalization só está disponível para **[!UICONTROL Link externo]**, **[!UICONTROL Link de unsubscription]** e **[!DNL Opt-Out]**. Selecione um tipo de link apropriado.

1. Selecione o ícone de personalização.

   ![](assets/message-tracking-insert-link-perso.png)

1. Use o editor de personalização para adicionar os atributos de perfil com os quais deseja personalizar o URL.

1. Salve as alterações.

Estes são alguns exemplos de URLs personalizados:

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>Ao editar um URL personalizado no editor de personalização, as funções auxiliares e a associação de públicos-alvo são desativadas por motivos de segurança.
>
>Não há suporte para espaços nos tokens de personalização usados em urls.

Para obter renderização e rastreamento confiáveis, siga as [práticas recomendadas e medidas de proteção](#best-practices) abaixo.

## Personalizar um URL completo/básico {#personalize-complete-base-url}

A Journey Optimizer também oferece suporte à personalização da URL **inteira** ou do **domínio base** de uma URL, por exemplo:

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>Para habilitar a personalização completa ou básica do URL, entre em contato com a Adobe e forneça sua lista de domínios aceitos. Isso é necessário para ajudar a impedir redirecionamentos inseguros.

## Personalizar parâmetros de rastreamento do URL {#personalize-url-tracking-parameters}

O [rastreamento de URL](url-tracking.md) é gerenciado no nível de configuração de canal e se aplica a todas as URLs incluídas no conteúdo da mensagem. Você também pode personalizar parâmetros de rastreamento de URL para um link individual no Designer de email. Isso permite anexar um parâmetro específico do recipient a um único link (por exemplo, para transmitir um identificador para suas ferramentas do Web Analytics).

Para fazer isso, [insira um link](message-tracking.md#insert-links), selecione o ícone de personalização, adicione o parâmetro de rastreamento de URL e selecione o atributo de perfil de sua escolha no [editor de personalização](../personalization/personalization-build-expressions.md).

![](assets/message-tracking-perso-parameter.png)

Repita as etapas acima para cada link ao qual deseja adicionar esse parâmetro de rastreamento.

Agora, quando o email é enviado, esse parâmetro é anexado automaticamente ao final do URL. Em seguida, você pode capturar esse parâmetro nas ferramentas do Web Analytics ou nos relatórios de desempenho.

>[!NOTE]
>
>Para verificar a URL final, você pode [enviar uma prova](../content-management/proofs.md) e clicar no link no conteúdo do email depois de receber a prova. O URL deve exibir o parâmetro de rastreamento. Por exemplo: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

<!--
## Best practices and guardrails {#best-practices}

To keep links valid, clickable, and trackable, follow the best practices and guardrails below.

### Braces for dynamic URLs {#use-braces}

When inserting a URL that contains personalization, use three curly braces (`{{{ ... }}}`) for the dynamic portion of the URL. This prevents escaping from altering special characters (for example `/` and `+`) and helps avoid broken URLs, incorrect redirects, or tracking issues.

Here is an example:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>Using raw output (`{{{ ... }}}`) means the value is inserted as-is. Only use it with values you trust and that are intended to be URL-safe (for example, values you generate or validate upstream).

### Correct URL tracking {#enable-url-tracking}

* When using personalization to generate the URL, ensure the resolved value starts with `http`/`https` for every recipient. Otherwise, tracking may not be applied and the link may not behave as expected.

* Do not use dynamic logic such as `let`, `each`, or `if` statements directly in the personalization editor's URL field. These are disabled for security reasons.

* If your scenario involves complex logic to generate personalized URLs, avoid placing that logic directly in the personalization editor's URL field. Instead:
    * Add the necessary logic and statements in the HTML content above or near the URL field.
    * Generate and store personalized attributes separately, then reference them in your email content.

### URL encoding and length {#encoding}

* URI syntax rules ([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) apply to all URLs in your email content. However, personalized URLs are more likely to surface encoding issues because recipient-specific values can introduce reserved characters (for example in query parameters). Therefore, ensure your dynamic values are URL-encoded (especially spaces, `&`, `#`, `%`, and `+`) and avoid using `+` for query values.

* Very long URLs can be truncated or rejected by browsers, mail clients, or downstream systems. For example, mirror page URLs can grow significantly when runtime personalization is heavy. Keep personalized payloads small and avoid embedding large objects into URLs.

### Recommended validation steps {#validation}

Before activating a journey or campaign, follow the recommendations below:

* Send a [proof](../content-management/proofs.md) and click links to confirm the resolved URL starts with `http`/`https` and keeps the expected structure.
* If tracking parameters are appended, confirm the final URL includes them (either via configuration-level URL tracking or per-link tracking parameters).
-->
