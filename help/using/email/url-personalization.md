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
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# Personalizar URLs em emails {#url-personalization}

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

## Práticas recomendadas e medidas de proteção {#best-practices}

Para manter os links válidos, clicáveis e rastreáveis, siga as práticas recomendadas e as medidas de proteção abaixo.

### Chaves para URLs dinâmicos {#use-braces}

Ao inserir uma URL que contenha personalização, use três chaves (`{{{ ... }}}`) para a parte dinâmica da URL. Isso impede que o escape altere caracteres especiais (por exemplo, `/` e `+`) e ajuda a evitar URLs corrompidas, redirecionamentos incorretos ou problemas de rastreamento.

Exemplo:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>Usar saída bruta (`{{{ ... }}}`) significa que o valor é inserido como está. Use-a somente com valores em que você confia e que devem ser seguros para URL (por exemplo, valores gerados ou validados upstream).

### Rastreamento correto de URL {#enable-url-tracking}

* Ao usar a personalização para gerar a URL, verifique se o valor resolvido começa com `http`/`https` para cada destinatário. Caso contrário, o rastreamento pode não ser aplicado e o link pode não se comportar conforme esperado.

* Não use lógica dinâmica, como instruções `let`, `each` ou `if` diretamente no campo URL do editor de personalização. Elas estão desativadas por motivos de segurança.

* Se o cenário envolver uma lógica complexa para gerar URLs personalizados, evite colocar essa lógica diretamente no campo URL do editor de personalização. Em vez disso:
   * Adicione a lógica e as instruções necessárias no conteúdo do HTML acima ou próximo ao campo URL.
   * Gere e armazene atributos personalizados separadamente e, em seguida, faça referência a eles no conteúdo do seu email.

### Codificação e comprimento do URL {#encoding}

* As regras de sintaxe de URI ([padrão RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) se aplicam a todas as URLs no seu conteúdo de email. No entanto, URLs personalizados têm mais probabilidade de apresentar problemas de codificação, pois valores específicos do recipient podem introduzir caracteres reservados (por exemplo, em parâmetros de consulta). Portanto, verifique se seus valores dinâmicos são codificados por URL (especialmente espaços, `&`, `#`, `%` e `+`) e evite usar `+` para valores de consulta.

* URLs muito longos podem ser truncados ou rejeitados por navegadores, clientes de email ou sistemas downstream. Por exemplo, os URLs de mirror page podem crescer significativamente quando a personalização em tempo de execução é intensa. Mantenha cargas personalizadas pequenas e evite incorporar objetos grandes em URLs.

### Etapas de validação recomendadas {#validation}

Antes de ativar uma jornada ou campanha, siga as recomendações abaixo:

* Envie uma [prova](../content-management/proofs.md) e clique em links para confirmar se a URL resolvida começa com `http`/`https` e mantém a estrutura esperada.
* Se os parâmetros de rastreamento forem anexados, confirme se o URL final os inclui (por meio do rastreamento de URL no nível de configuração ou parâmetros de rastreamento por link).

