---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar marca
description: Saiba como criar e gerenciar as diretrizes da sua marca
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 4919c8c749f9216be526bab2437a815da0136df5
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 19%

---

# Criar e gerenciar marcas {#brands}

>[!AVAILABILITY]
>
>Esse recurso foi lançado como um beta privado. Ele estará progressivamente disponível para todos os clientes em versões futuras.
>

As diretrizes da marca são um conjunto detalhado de regras e padrões que estabelecem a identidade visual e verbal de uma marca. Eles atuam como uma referência para manter uma representação de marca consistente em todas as plataformas de marketing e comunicação.

No Journey Optimizer, agora há a opção de inserir e organizar manualmente os detalhes da sua marca ou carregar documentos de diretrizes da marca para extração automática de informações.

## Marcas de acesso {#generative-access}

Para acessar o menu Marca no Adobe Journey Optimizer, os usuários precisam receber as permissões **Kit de marcas gerenciado** ou **[!UICONTROL Habilitar assistente de IA]**. [Saiba mais](../administration/permissions.md)

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

1. No menu **[!UICONTROL Marcas]**, clique em **[!UICONTROL Adicionar marca]**.

   ![](assets/brands-1.png)

1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** para a diretriz de marca.

1. Arraste e solte ou selecione seu arquivo para fazer upload das diretrizes da marca e extrair automaticamente informações relevantes sobre a marca. Clique em **[!UICONTROL Adicionar marca]**.

   O processo de extração de informações agora começa. Observe que pode levar vários minutos para ser concluído.

   ![](assets/brands-2.png)

1. Seus padrões de criação de conteúdo e visual agora são preenchidos automaticamente. Navegue pelas diferentes guias para adaptar as informações conforme necessário.

1. Nos **[!UICONTROL Padrões de criação de conteúdo]**, clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar outra diretriz, exemplo ou exclusão.

   ![](assets/brands-3.png)

1. Nos **[!UICONTROL Padrões de criação visual]**, clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar outra diretriz, exemplo ou exclusão.

1. Para adicionar um exemplo de imagem, clique em **[!UICONTROL Selecionar imagem]**. Você também pode adicionar qualquer insight incorreto identificado.

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
