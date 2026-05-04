---
solution: Journey Optimizer
product: journey optimizer
title: Habilitar integrações externas
description: Integre integrações externas ao processo de criação de canal para enriquecer o conteúdo com informações personalizadas e dinâmicas
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: integração
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

---


# Uso de integrações externas para personalização {#integrations-personalization}

Antes de usar integrações externas em seu conteúdo, confirme se um administrador **configurou e ativou** cada integração (ponto de extremidade, autenticação, políticas, carga de resposta e ativação) conforme descrito em [Trabalhar com integrações](integrations.md).

Você pode adicionar até **3** integrações por **[!UICONTROL Fragmento]** e até **5** na mensagem. As integrações provenientes apenas de fragmentos não contam no **5**.

## Aplicar personalização da integração ao seu conteúdo {#apply-integration-personalization}

Como profissional de marketing, você pode usar integrações configuradas para personalizar seu conteúdo. Siga estas etapas:

1. Acesse o conteúdo da campanha e clique em **[!UICONTROL Adicionar personalização]** a partir do Texto ou dos **[!UICONTROL Componentes]** do HTML.

   [Saiba mais sobre componentes](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Navegue até a seção **[!UICONTROL Integrações]** e clique em **[!UICONTROL Abrir integrações]** para exibir todas as integrações ativas.

   Observe que os **Fragmentos de Journey Optimizer** estão disponíveis com Integrações, mas oferecem suporte somente a canais de saída. Depois que um fragmento é publicado, a adição e o salvamento de novas integrações são desativados para evitar impacto nas jornadas e campanhas existentes.

   ![](assets/external-integration-content-2.png)

1. Selecione uma integração e clique em **[!UICONTROL Salvar]**.

   ![](assets/external-integration-content-3.png)

1. Habilite o modo **[!UICONTROL Pills]** para desbloquear o menu de integração avançado.

   ![](assets/external-integration-content-4.png)

1. Ao criar a personalização da integração, o Auxiliar de integrações inclui um campo **`required`** que define como as falhas ou os dados ausentes interagem com o conteúdo padrão:

   * **`required=true`** (padrão): a renderização para essa mensagem. O envio é excluído com **`ExternalDataLookupExclusion`**, e essa exclusão é registrada no **conjunto de dados de comentários da mensagem**.
   * **`required=false`**: A variável de resultado está definida como **`null`** e a renderização continua. Use texto padrão, fallbacks ou lógica condicional no modelo para que os perfis não recebam conteúdo vazio quando a integração não retornar dados.

     ![](assets/external-integration-content-8.png)

1. Para concluir a configuração de integração, defina os atributos de integração, que foram especificados anteriormente durante a [configuração](integrations.md#configure).

   Você pode designar valores a esses atributos usando valores estáticos, que permanecem constantes, ou atributos de perfil, que extraem dinamicamente informações dos perfis do usuário.

   ![](assets/external-integration-content-5.png)

1. Depois que os atributos de integração forem definidos, você poderá usar os campos de integração no seu conteúdo para mensagens personalizadas clicando no ícone ![adicionar](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >Os tokens no modelo devem usar somente campos expostos pelo administrador na configuração de integração. Por exemplo, `{{weatherResponse.temperature}}` é válido quando `temperature` é exposto; `{{weatherResponse.humidity}}` é rejeitado no editor se `humidity` não foi exposto.

1. Clique em **[!UICONTROL Salvar]**.

A personalização da sua integração agora é aplicada com sucesso ao seu conteúdo, garantindo que cada recipient receba uma experiência personalizada e relevante com base nos atributos configurados.

![](assets/external-integration-content-7.png)

<!--

## Map one API call to another {#map-integration-chain}

You can **chain** integrations so that values returned by one active integration drive the inputs (path, headers, or query parameters) of another. That lets you build a real-time data flow in a single message without custom code.

Before you start, make sure that:

* An administrator has configured and activated every integration you need. See [Configure your Integration](integrations.md).
* Variable path placeholders, headers, and query parameters are set up in the integration configuration with marketer-facing labels.
* The administrator exposed the response fields you need in each integration's **[!UICONTROL Response payload]** so they appear when authoring.

In the below example, a reservation system integration returns a flight booking reference from the profile context. A separate flight-information integration expects that reference as a **path variable**. In the personalization editor, you map the second integration's variable to a field from the first integration's response, instead of a static value or profile attribute alone.

1. Open your message or fragment and place the cursor where you want personalized content (for example, a **[!UICONTROL Text]** field).

1. Open the personalization editor and go to **[!UICONTROL Integrations]** → **[!UICONTROL Open integrations]**.

1. Select the integration whose output will supply the downstream input (in the example, the reservation or profile API that returns the flight identifier).

1. Define that integration's inputs as usual—static values, profile attributes, or other allowed mappings—then save so its response is available for chaining.

    >[!NOTE]
    >
    > Fields must appear in the administrator-defined response payload for each integration. You cannot reference response properties that were not exposed in configuration.

1. Select the **second** integration (for example, the API that needs the flight number or booking reference on the URL path).

1. For each input that must come from the first call—often a **path variable** or **variable** header/query parameter—choose the mapping source that references the **first integration's response** (for example, the flight booking reference field from the reservation payload). Do not use a static test value if you need live, profile-specific data.

1. Insert the response tokens you need in the content (for example, destination name from the flight API, loyalty balance from a loyalty integration) using the ![add](assets/do-not-localize/Smock_Add_18_N.svg) control.

1. Save the personalization.

When you **simulate** or send, Journey Optimizer resolves integrations in order: the first call runs with the profile context you configured; its output is used to build the second request. Different integrations may run at simulation time and at send time according to your setup and channel behavior.

-->

## Vídeo tutorial {#video}

Este vídeo mostra como as **Integrações** conectam o Adobe Journey Optimizer a APIs externas para que você possa receber dados e conteúdo em **canais de saída**, email, SMS e push, para personalizações mais relevantes.

>[!VIDEO](https://video.tv.adobe.com/v/3484118/?learn=on)
