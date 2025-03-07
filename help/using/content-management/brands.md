---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar marca
description: Saiba como criar e gerenciar as diretrizes da sua marca
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: b1b7abbe-8600-4a8d-b0b5-0dbd49abc275
source-git-commit: 12dc96bb08f03865c82382baac276f46bc42baeb
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 15%

---

# Criar e gerenciar suas marcas {#brands}

>[!CONTEXTUALHELP]
>id="ajo_brand_overview"
>title="Introdução às marcas"
>abstract="Crie e personalize suas próprias marcas para definir sua identidade visual e verbal exclusiva, facilitando a geração de conteúdo que corresponda ao estilo e à voz da sua marca."

>[!CONTEXTUALHELP]
>id="ajo_brand_ai_menu"
>title="Selecione sua marca"
>abstract="Escolha sua marca para garantir que todo o conteúdo gerado por IA seja personalizado para se alinhar às especificações e diretrizes da sua marca."

>[!CONTEXTUALHELP]
>id="ajo_brand_score_overview"
>title="Seleção da marca"
>abstract="Selecione sua marca para garantir que o conteúdo seja criado em alinhamento com as diretrizes, os padrões e a identidade específicos, mantendo a consistência e a integridade da marca."

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="Pontuação de alinhamento da marca"
>abstract="A pontuação de alinhamento da sua marca mede o desempenho do seu conteúdo em seguir as diretrizes da marca, garantindo a consistência nas cores, fontes, logotipo, imagem e estilo de escrita."


>[!AVAILABILITY]
>
>Esse recurso foi lançado como um beta privado. Ele estará progressivamente disponível para todos os clientes em versões futuras.

As diretrizes da marca são um conjunto detalhado de regras e padrões que estabelecem a identidade visual e verbal de uma marca. Eles atuam como uma referência para manter uma representação de marca consistente em todas as plataformas de marketing e comunicação.

No [!DNL Journey Optimizer], agora há a opção de inserir e organizar manualmente os detalhes da sua marca ou carregar documentos de diretrizes da marca para extração automática de informações.

## Acessar marcas {#generative-access}

Para acessar o menu **[!UICONTROL Marcas]** em [!DNL Adobe Journey Optimizer], os usuários precisam receber as permissões do **[!UICONTROL Kit de marcas gerenciadas]** ou **[!UICONTROL Habilitar assistente de IA]**. [Saiba mais](../administration/permissions.md)

+++  Saiba como atribuir permissões relacionadas à marca

1. No produto **Permissões**, abra a guia **Funções** e selecione a **função** desejada.

1. Clique em **Editar** para modificar as permissões.

1. Adicione o recurso **Assistente de IA** e selecione **Kit de marca gerenciado** ou **[!UICONTROL Habilitar assistente de IA]** no menu suspenso.

   Observe que a permissão **[!UICONTROL Habilitar assistente de Ia]** fornece acesso somente leitura ao menu **[!UICONTROL Marcas]**.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Clique em **Salvar** para aplicar as alterações.

   As permissões de todos os usuários já atribuídos a essa função serão atualizadas automaticamente.

1. Para atribuir essa função a novos usuários, navegue até a guia **Usuários** no painel **Funções** e clique em **Adicionar usuário**.

1. Insira o nome do usuário, seu endereço de email ou escolha na lista e clique em **Salvar**.

1. Se o usuário não tiver sido criado anteriormente, consulte [esta documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Criar sua marca {#create-brand-kit}

>[!CONTEXTUALHELP]
>id="ajo_brands_create"
>title="Criar sua marca"
>abstract="Insira o nome da sua marca e faça upload do arquivo de diretrizes da marca. A ferramenta extrairá automaticamente os principais detalhes, facilitando a manutenção da identidade da sua marca."

Para criar e gerenciar as diretrizes de marca, você pode inserir os detalhes por conta própria ou fazer upload do documento de diretrizes de marca para que as informações sejam extraídas automaticamente:

1. No menu **[!UICONTROL Marcas]**, clique em **[!UICONTROL Criar marca]**.

   ![](assets/brands-1.png)

1. Digite um **[!UICONTROL Nome]** para sua marca.

1. Arraste e solte ou selecione seu arquivo para fazer upload das diretrizes da marca e extrair automaticamente informações relevantes sobre a marca. Clique em **[!UICONTROL Criar marca]**.

   O processo de extração de informações agora começa. Observe que pode levar vários minutos para ser concluído.

   ![](assets/brands-2.png)

1. Seus padrões de criação de conteúdo e visual agora são preenchidos automaticamente. Navegue pelas diferentes guias para adaptar as informações conforme necessário.

1. Na guia **[!UICONTROL Estilo de Escrita]**, clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar uma diretriz ou exclusão, incluindo exemplos.

   ![](assets/brands-3.png)

1. Na guia **[!UICONTROL Visual content]**, clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar outra diretriz ou exclusão.

1. Para adicionar uma imagem mostrando o uso correto, selecione **[!UICONTROL Exemplo]** e clique em **[!UICONTROL Selecionar imagem]**. Você também pode adicionar uma imagem mostrando o uso incorreto como exemplo de exclusão.

   ![](assets/brands-4.png)

1. Após a configuração, clique em **[!UICONTROL Salvar]** e em **[!UICONTROL Publicar]** para disponibilizar a diretriz da marca no assistente de IA.

1. Para fazer modificações na sua marca publicada, clique em **[!UICONTROL Editar marca]**.

   >[!NOTE]
   >
   >Isso cria uma cópia temporária no modo de edição, substituindo a versão online depois de publicada.

   ![](assets/brands-8.png)

1. No painel **[!UICONTROL Marcas]**, abra o menu avançado clicando no ícone ![](assets/do-not-localize/Smock_More_18_N.svg) para:

   * Exibir marca
   * Editar
   * Duplicar
   * Publicação
   * Cancelar publicação
   * Excluir

   ![](assets/brands-6.png)

As diretrizes da sua marca agora podem ser acessadas no menu suspenso **[!UICONTROL Marca]** do menu do assistente de IA, permitindo que ele gere conteúdo e ativos alinhados às suas especificações. [Saiba mais sobre o assistente de IA](gs-generative.md)

![](assets/brands-7.png)
