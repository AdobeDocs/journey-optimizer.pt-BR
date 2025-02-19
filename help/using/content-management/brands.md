---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar marca
description: Saiba como criar e gerenciar as diretrizes da sua marca
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: b1ccacd30acb886e06a3305f0c7046d85f558357
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 22%

---

# Criar e gerenciar marcas {#brands}

>[!AVAILABILITY]
>
>Esse recurso foi lançado como um beta privado. Ele estará progressivamente disponível para todos os clientes em versões futuras.

As diretrizes da marca são um conjunto detalhado de regras e padrões que estabelecem a identidade visual e verbal de uma marca. Eles atuam como uma referência para manter uma representação de marca consistente em todas as plataformas de marketing e comunicação.

No [!DNL Journey Optimizer], agora há a opção de inserir e organizar manualmente os detalhes da sua marca ou carregar documentos de diretrizes da marca para extração automática de informações.

## Marcas de acesso {#generative-access}

Para acessar o menu **[!UICONTROL Marcas]** em [!DNL Adobe Journey Optimizer], os usuários precisam receber as permissões do **[!UICONTROL Kit de marcas gerenciadas]** ou **[!UICONTROL Habilitar assistente de IA]**. [Saiba mais](../administration/permissions.md)

+++  Saiba como atribuir permissões relacionadas à marca

1. No produto **Permissões**, abra a guia **Funções** e selecione a **função** desejada.

1. Clique em **Editar** para modificar as permissões.

1. Adicione o recurso **Assistente de IA** e selecione **Kit de marca gerenciado** ou **[!UICONTROL Habilitar assistente de IA]** no menu suspenso.

   Observe que a permissão **[!UICONTROL Habilitar assistente de Ia]** fornece acesso somente leitura ao menu Marcas.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Clique em **Salvar** para aplicar as alterações.

   As permissões de todos os usuários já atribuídos a essa função serão atualizadas automaticamente.

1. Para atribuir essa função a novos usuários, navegue até a guia **Usuários** no painel **Funções** e clique em **Adicionar usuário**.

1. Insira o nome do usuário, seu endereço de email ou escolha na lista e clique em **Salvar**.

1. Se o usuário não tiver sido criado anteriormente, consulte [esta documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Criar sua marca {#create-brand-kit}

Para criar e gerenciar as diretrizes de marca, você pode inserir os detalhes por conta própria ou fazer upload do documento de diretrizes de marca para que as informações sejam extraídas automaticamente:

1. No menu **[!UICONTROL Marcas]**, clique em **[!UICONTROL Criar marca]**.

   ![](assets/brands-1.png)

1. Digite um **[!UICONTROL Nome]** para sua marca<!--and a **[!UICONTROL Description]** to your brand guideline-->.

   ![](assets/brands-2-temp.png)

<!--

[Upload feature currently behind feature flag so hidden from doc - should be available again by EOM (Feb)]

1. Drag and drop or select your file to upload your brand guidelines and extract automatically relevant brand information. Click **[!UICONTROL Create brand]**.

    The information extraction process now begins. Note that it may take several minutes to complete.

    ![](assets/brands-2.png)

1. Your Content and visual creation standards are now automatically populated. Browse through the different tabs to adapt the information as needed.

-->

1. Na guia **[!UICONTROL Estilo de Escrita]**, clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar uma diretriz ou exclusão. Você também pode adicionar exemplos.

   ![](assets/brands-3.png)

1. Na guia **[!UICONTROL Visual content]**, clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar outra diretriz ou exclusão.

1. Para adicionar um exemplo de imagem, clique em **[!UICONTROL Selecionar imagem]**. Você também pode adicionar uma imagem mostrando o uso incorreto como exemplo de exclusão.

   ![](assets/brands-4.png)

1. Após a configuração, clique em **[!UICONTROL Salvar]** e depois em **[!UICONTROL Publicar]** para disponibilizar as diretrizes de marcas no assistente de IA.

1. Para fazer modificações na sua marca publicada, clique em **[!UICONTROL Editar marca]**. Observe que essa ação cria uma cópia temporária no modo de edição, substituindo a versão ativa após a publicação.

   ![](assets/brands-8.png)

1. No painel **[!UICONTROL Marcas]**, abra o menu avançado clicando no ícone ![](assets/do-not-localize/Smock_More_18_N.svg) para:

   * Exibir marca
   * Editar
   * Duplicar
   * Publicar
   * Cancelar publicação
   * Excluir

   ![](assets/brands-6.png)

As Diretrizes da marca agora podem ser acessadas no menu suspenso Marcas no menu do assistente de IA, permitindo gerar conteúdo e ativos alinhados às suas especificações. [Saiba mais sobre o assistente de IA](gs-generative.md)

![](assets/brands-7.png)
