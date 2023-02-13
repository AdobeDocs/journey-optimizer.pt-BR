---
solution: Journey Optimizer
product: journey optimizer
title: Visualizar mensagens e enviar provas
description: Saiba como visualizar e testar seu email
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: visualização, conteúdo, email, prova, teste, perfil
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 5%

---

# Visualizar e testar o email {#preview-and-proof}

Após definir o conteúdo do email, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu [conteúdo personalizado](../personalization/personalize.md), é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

Para detectar possíveis erros no conteúdo do email ou nas configurações de personalização, envie provas para testar perfis. Uma prova deve ser enviada sempre que uma alteração for feita, para validar o conteúdo mais recente.

>[!CAUTION]
>
>Você precisa ter perfis de teste disponíveis para pré-visualizar suas mensagens e enviar provas.
>
>Saiba como criar perfis de teste [nesta página](../segment/creating-test-profiles.md).

Para testar seu conteúdo de email, é necessário:

* [Selecionar perfis de teste](#select-test-profiles)
* [Verificar a pré-visualização da mensagem](#preview-your-messages)

Você poderá [enviar provas](#send-proofs) aos seus perfis de teste.

Além disso, use a conta do **Litmus** no [!DNL Journey Optimizer] para pré-visualizar instantaneamente a **renderização de email** em clientes de email populares. Em seguida, você pode melhorar seu conteúdo de email e garantir que ele e funcione corretamente em cada caixa de entrada. Saiba como desbloquear visualizações de email do Litmus em [esta seção](#email-rendering).

>[!CAUTION]
>
>Ao visualizar uma mensagem ou enviar provas, somente os dados de personalização de perfil são exibidos. A personalização com base em dados de contexto, como informações de evento, só pode ser testada no contexto de uma jornada. Saiba como testar a personalização no [este caso de uso](../personalization/personalization-use-case.md).

➡️ [Saiba como visualizar e provar seu email neste vídeo](#video-preview)

## Selecionar perfis de teste {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Visualizar e testar suas mensagens"
>abstract="Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/preview.html?lang=en#email-rendering" text="Renderização de email"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/preview.html?lang=en#preview-email" text="Visualização"

Use [Testar perfis](../segment/creating-test-profiles.md) para direcionar recipients adicionais que não correspondem aos critérios de direcionamento definidos.

Para selecionar perfis de teste, siga as etapas abaixo:

1. No [Editar conteúdo](create-email.md#define-email-content) ou no Designer de email, clique no botão **[!UICONTROL Simular conteúdo]** para acessar a seleção de perfil de teste.

   ![](assets/email-preview-button.png)

1. Selecionar **[!UICONTROL Gerenciar perfis de teste]**.

   ![](assets/email-preview_manage-test-profiles.png)

1. Selecione o namespace a ser usado para identificar perfis de teste clicando no botão **[!UICONTROL Namespace de identidade]** ícone de seleção.

   ![](assets/previewselect-namespace.png)

   Saiba mais sobre os namespaces de identidade da Adobe Experience Platform [nesta seção](../segment/get-started-identity.md).

   No exemplo abaixo, usaremos a variável **Email** namespace.

1. Use o campo de pesquisa para localizar o namespace, selecione-o e clique em **[!UICONTROL Selecionar]**

   ![](assets/preview-email-namespace.png)

1. No **[!UICONTROL Valor de identidade]** , insira o valor (aqui, o endereço de email) para identificar o perfil de teste e clique em **[!UICONTROL Adicionar perfil]**.

   <!--![](assets/preview-identity-value.png)-->

1. Se você tiver adicionado personalização à sua mensagem, adicione outros perfis para poder testar diferentes variantes da mensagem, dependendo dos dados do perfil. Depois de adicionados, os perfis são listados nos campos selecionados.

   ![](assets/preview-profile-list.png)

   Com base nos elementos de personalização da mensagem, essa lista exibe os dados para cada perfil de teste nas colunas relacionadas.

### Visualização de email {#preview-email}

Uma vez [perfis de teste](#select-test-profiles) forem selecionadas, você poderá visualizar seu conteúdo de email. Siga as etapas abaixo:

1. No [Editar conteúdo](create-email.md#define-email-content) ou no Designer de email, clique no botão **[!UICONTROL Simular conteúdo]** botão.

1. Selecione um perfil de teste. Você pode verificar os valores disponíveis nas colunas. Use as setas para a direita/esquerda para navegar pelos dados.

   ![](assets/preview-select-profile.png)

   >[!NOTE]
   >
   >Para adicionar mais perfis de teste, selecione **[!UICONTROL Gerenciar perfis de teste]**. [Saiba mais](#select-test-profiles)

1. Clique no botão **[!UICONTROL Selecionar dados]** ícone acima da lista para adicionar ou remover colunas.

   ![](assets/preview-select-data.png)

   Você pode ver campos de personalização específicos da mensagem atual no final da lista. Neste exemplo, a cidade do perfil, o nome e o sobrenome. Selecione esses campos e verifique se esses valores estão preenchidos nos perfis de teste.

1. Na visualização da mensagem, os elementos personalizados são substituídos pelos dados de perfil de teste selecionados.

   Por exemplo, para essa mensagem, o conteúdo do email e o assunto do email são personalizados:

   ![](assets/preview-test-profile.png)

1. Selecione outros perfis de teste para visualizar a renderização de email para cada variante da mensagem.

## Enviar provas {#send-proofs}

Uma prova é uma mensagem específica que permite testar uma mensagem antes de enviá-la para o público principal. Os recipients da prova são responsáveis pela aprovação da mensagem: renderização, conteúdo, configurações de personalização, configuração.

Uma vez [perfis de teste](#select-test-profiles) forem selecionadas, você poderá enviar provas.

1. No **[!UICONTROL Simulate]** clique no botão **[!UICONTROL Enviar prova]** botão.

   ![](assets/send-proof-button.png)

1. No **[!UICONTROL Enviar prova]** , digite o email do destinatário e clique em **[!UICONTROL Adicionar]** para enviar a prova para você mesmo ou para membros de sua organização.

   Observe que você pode adicionar até dez recipients para o delivery de prova.

   ![](assets/send-proof-add.png)

1. Em seguida, selecione a **Testar perfis** que será usada para personalizar o conteúdo da mensagem.

   Cada recipient da prova receberá quantas mensagens for o número de perfis de teste selecionados. Por exemplo, se você adicionou cinco emails de recipient e selecionou dez perfis de teste, você enviará cinquenta mensagens de prova e cada recipient receberá dez deles.

1. Você pode adicionar um prefixo à linha de assunto da prova, se necessário. Somente caracteres alfanuméricos e caracteres especiais, como . - _ ( ) [ ] são permitidos como prefixo na linha de assunto.

1. Clique em **[!UICONTROL Enviar prova]**.

   ![](assets/send-proof-select.png)

1. De volta ao  **[!UICONTROL Simulate]** clique no botão  **[!UICONTROL Exibir provas]** para verificar o status.

   ![](assets/send-proof-view.png)

É recomendável enviar provas após cada modificação ao conteúdo da mensagem.

>[!NOTE]
>
>Na prova enviada, o link para a mirror page não está ativo. Ela só é ativada nas mensagens finais.

## Usar renderização de email {#email-rendering}

Você pode aproveitar seu **Litmus** conta em [!DNL Journey Optimizer] para visualizar instantaneamente sua **renderização de email** em clientes de email populares.

Para acessar os recursos de renderização de email, é necessário:

* Ter uma conta Litmus
* [Selecionar perfis de teste](#select-test-profiles)

Em seguida, siga as etapas abaixo:

1. No [Editar conteúdo](create-email.md#define-email-content) ou no Designer de email, clique no botão **[!UICONTROL Simular conteúdo]** botão.

1. Selecione o **[!UICONTROL Renderizar email]** botão.

   ![](assets/email-rendering-button.png)

1. Clique em **Conecte sua conta Litmus** na seção superior direita.

   ![](assets/email-rendering-litmus.png)

1. Insira suas credenciais e faça logon.

   ![](assets/email-rendering-credentials.png)

1. Clique no botão **Executar teste** para gerar visualizações de email.

1. Verifique seu conteúdo de email em clientes populares de desktop, dispositivos móveis e baseados na Web.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>Ao conectar seu **Litmus** conta com [!DNL Journey Optimizer], você concorda que as mensagens de teste são enviadas ao Litmus: depois de enviados, esses emails não são mais gerenciados pelo Adobe. Como consequência, a política de email de retenção de dados Litmus se aplica a esses emails, incluindo dados de personalização que podem ser incluídos nessas mensagens de teste.

## Vídeo tutorial {#video-preview}

Saiba como testar a renderização de email nas caixas de entrada, como visualizar seus emails personalizados em relação a perfis de teste e enviar provas.

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
