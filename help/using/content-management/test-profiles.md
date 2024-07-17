---
title: Seleção de perfis de teste
description: Saiba como selecionar perfis de teste para visualizar e testar o conteúdo.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: feae2cb9d0bed35f12eb117cf2969c9290ebc06f
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 16%

---

# Seleção de perfis de teste {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Use perfis de teste para verificar o conteúdo"
>abstract="Use perfis de teste para visualizar e testar o conteúdo. Se você adicionou campos personalizados, é possível verificar como eles são exibidos usando dados de perfil de teste."

Antes de visualizar ou testar seu conteúdo, primeiro é necessário selecionar perfis de teste, que são recipients adicionais que não correspondem aos critérios de direcionamento definidos. [Saiba como criar perfis de teste](../audience/creating-test-profiles.md)

Para selecionar perfis de teste, siga estas etapas:

1. Na tela de edição de conteúdo da sua mensagem ou no Designer de Email, clique no botão **[!UICONTROL Simular conteúdo]**.

1. Clique no botão **[!UICONTROL Gerenciar perfis de teste]** e selecione o namespace a ser usado para identificar perfis de teste clicando no ícone de seleção **[!UICONTROL Namespace de identidade]**. [Saiba mais sobre os namespaces de identidade da Adobe Experience Platform](../audience/get-started-identity.md).

   No exemplo abaixo, usamos o namespace **Email**.

   ![](../email/assets/previewselect-namespace.png)

1. Use o campo de pesquisa para localizar o namespace, selecione-o e clique em **[!UICONTROL Selecionar]**

   ![](../email/assets/preview-email-namespace.png)

1. No campo **[!UICONTROL Valor de identidade]**, insira o valor (aqui o endereço de email) para identificar o perfil de teste e clique em **[!UICONTROL Adicionar perfil]**.

   <!--![](assets/preview-identity-value.png)-->

1. Se você adicionou personalização à mensagem, adicione outros perfis para testar diferentes variantes da mensagem, dependendo dos dados do perfil. Depois de adicionados, os perfis são listados nos campos selecionados.

   ![](../email/assets/preview-profile-list.png)

   Com base nos elementos de personalização da mensagem, essa lista exibe dados para cada perfil de teste nas colunas relacionadas.
