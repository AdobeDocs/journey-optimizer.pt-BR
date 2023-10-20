---
title: Selecionar perfis de teste
description: Saiba como selecionar perfis de teste para visualizar e testar o conteúdo.
feature: Preview, Proofs
role: User
level: Beginner
source-git-commit: 6da7f4c8caa5a0a6cfda1e90d0c6cd4787c6afca
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---

# Selecionar perfis de teste {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Usar perfis de teste para verificar seu conteúdo"
>abstract="Use perfis de teste para visualizar e testar seu conteúdo. Se você adicionou campos personalizados, é possível verificar como eles são exibidos usando dados de perfil de teste."

Antes de visualizar ou testar seu conteúdo, primeiro é necessário selecionar perfis de teste, que são recipients adicionais que não correspondem aos critérios de direcionamento definidos. [Saiba como criar perfis de teste](../audience/creating-test-profiles.md)

Para selecionar perfis de teste, siga estas etapas:

1. Na tela de edição de conteúdo da sua mensagem ou no Designer de email, clique no **[!UICONTROL Simular conteúdo]** botão.

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** e, em seguida, selecione o namespace a ser usado para identificar perfis de teste clicando no link **[!UICONTROL Namespace de identidade]** ícone de seleção. [Saiba mais sobre os namespaces de identidade da Adobe Experience Platform](../audience/get-started-identity.md).

   No exemplo abaixo, usamos o **E-mail** namespace.

   ![](../email/assets/previewselect-namespace.png)

1. Use o campo de pesquisa para localizar o namespace, selecione-o e clique em **[!UICONTROL Selecionar]**

   ![](../email/assets/preview-email-namespace.png)

1. No **[!UICONTROL Valor de identidade]** insira o valor (aqui o endereço de email) para identificar o perfil de teste e clique em **[!UICONTROL Adicionar perfil]**.

   <!--![](assets/preview-identity-value.png)-->

1. Se você adicionou personalização à mensagem, adicione outros perfis para testar diferentes variantes da mensagem, dependendo dos dados do perfil. Depois de adicionados, os perfis são listados nos campos selecionados.

   ![](../email/assets/preview-profile-list.png)

   Com base nos elementos de personalização da mensagem, essa lista exibe dados para cada perfil de teste nas colunas relacionadas.
