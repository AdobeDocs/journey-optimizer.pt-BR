---
solution: Journey Optimizer
product: journey optimizer
title: Configurar subdomínios da Web
description: Saiba como configurar subdomínios da Web com o Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
keywords: web, subdomínios, configuração
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

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
>title="Definir um subdomínio padrão"
>abstract="Você pode criar vários subdomínios da Web, mas somente o subdomínio padrão será usado. Você pode alterar o subdomínio da Web padrão, mas somente um pode ser usado de cada vez."

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

1. Para definir esse subdomínio como padrão, selecione a opção correspondente.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Somente a variável **default** será usado. Você pode alterar o subdomínio da Web padrão, mas somente um pode ser usado de cada vez.

1. Clique em **[!UICONTROL Enviar]**. O subdomínio obtém a variável **[!UICONTROL Sucesso]** status. Ele está pronto para ser usado em suas experiências da Web.

1. O **[!UICONTROL Padrão]** o selo é exibido ao lado do subdomínio que está sendo usado como padrão no momento. Para alterar o subdomínio padrão, selecione **[!UICONTROL Definir como padrão]** do **[!UICONTROL Mais ações]** ao lado do subdomínio desejado.

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.-->

1. Você só pode excluir um **[!UICONTROL Falha]** subdomínio para limpar a lista. Para fazer isso, selecione **[!UICONTROL Excluir]** do **[!UICONTROL Mais ações]** ao lado do subdomínio desejado.

<!--You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->

