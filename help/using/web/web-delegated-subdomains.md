---
solution: Journey Optimizer
product: journey optimizer
title: Configurar subdomínios da Web
description: Saiba como configurar subdomínios da Web com o Journey Optimizer
role: Admin
level: Intermediate
keywords: web, subdomínios, configuração
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: b05c7e88c223af44cd2f7d10ea76c39359662cbd
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 2%

---

# Configurar subdomínios da Web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Delegar um subdomínio da Web"
>abstract="Você configurará seu subdomínio para uso do canal da Web. Escolha entre os subdomínios que já foram delegados ao Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Delegar um subdomínio da Web"
>abstract="Se você adicionar conteúdo proveniente do Adobe Experience Manager Assets Essentials às suas experiências da Web, deverá configurar o subdomínio que será usado para publicar esse conteúdo. Selecione entre os subdomínios já delegados ao Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Definir um subdomínio da Web"
>abstract="Selecione um subdomínio da lista de subdomínios delegados ao Adobe. É possível definir esse subdomínio da Web como padrão, mas apenas um subdomínio padrão pode ser usado de cada vez."

Ao criar experiências da Web, se você adicionar conteúdo proveniente do [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) , você deve configurar o subdomínio que será usado para publicar esse conteúdo.

Para fazer isso, você deve escolher na lista de subdomínios já delegados ao Adobe. Saiba mais sobre como delegar subdomínios ao Adobe [esta seção](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>A configuração de subdomínio da Web é comum a todos os ambientes. Portanto:
>
>* Para acessar e editar subdomínios da Web, é necessário ter a variável **[!UICONTROL Gerenciar subdomínios da Web]** permissão na sandbox de produção.
>
> * Qualquer modificação em um subdomínio da Web também afetará as sandboxes de produção.


Você pode criar vários subdomínios da Web, mas somente a variável **default** será usado. Você pode alterar o subdomínio da Web padrão, mas somente um pode ser usado de cada vez.

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Configuração da Web]** > **[!UICONTROL Subdomínios da Web]**.

   ![](assets/web-access-subdomains.png)

1. Clique em **[!UICONTROL Configurar subdomínio]**.

1. Selecione um subdomínio delegado na lista.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >Não é possível selecionar um subdomínio que já esteja sendo usado como subdomínio da Web.

1. O prefixo que será exibido no URL da Web é adicionado automaticamente.

1. Para definir esse subdomínio como padrão, selecione a opção correspondente.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Somente a variável **default** será usado.

1. Clique em **[!UICONTROL Enviar]**. O subdomínio obtém a variável **[!UICONTROL Sucesso]** status. Ele está pronto para ser usado em suas experiências da Web.

1. O **[!UICONTROL Padrão]** o selo é exibido ao lado do subdomínio que está sendo usado como padrão no momento. Para alterar o subdomínio padrão, selecione **[!UICONTROL Definir como padrão]** do **[!UICONTROL Mais ações]** ao lado do subdomínio desejado.

   >[!NOTE]
   >
   >Você pode alterar o subdomínio da Web padrão, mas somente um pode ser usado de cada vez.

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You can only delete a **[!UICONTROL Failed]** subdomain to clean up the list. To do so, select **[!UICONTROL Delete]** from the **[!UICONTROL More actions]** button next to the desired subdomain.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
