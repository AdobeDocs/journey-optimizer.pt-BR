---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao Journey Optimizer para o Administrador do sistema
description: Como administrador do sistema, saiba mais sobre como trabalhar com o Journey Optimizer
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: ht
source-wordcount: '707'
ht-degree: 100%

---

# Introdução para administradores do sistema {#get-started-sys-admins}

Antes de começar a usar [!DNL Adobe Journey Optimizer], várias etapas são necessárias para preparar seu ambiente.  Você deve executar essas etapas para que as variáveis [Engenheiro de dados](data-engineer.md) e [Profissional de jornada](marketer.md) possam começar a trabalhar com [!DNL Adobe Journey Optimizer].


Como um **Administrador do sistema**, é necessário **compreender perfis de produtos e atribuir permissões** para administração de sandbox e configuração de canal. Você também precisa configurar sandboxes e gerenciá-las para os perfis de produto disponíveis. É possível atribuir membros da equipe a perfis de produtos.

Esses recursos podem ser gerenciados por **[!UICONTROL Administradores do produto]** com acesso ao Admin Console. [Saiba mais sobre o Adobe Admin Console](https://helpx.adobe.com/br/enterprise/admin-guide.html){target="_blank"}.

Saiba mais sobre o gerenciamento de acesso nas seguintes páginas:

1. **Criar sandboxes** para particionar suas instâncias em ambientes virtuais separados e isolados. Os **Sandboxes** são criados em [!DNL Journey Optimizer]. Saiba mais na seção [Sandboxes](../../administration/sandboxes.md).

   >[!NOTE]
   >Como um **Administrador do sistema**, se você não conseguir ver o menu **[!UICONTROL Sandboxes]** no [!DNL Journey Optimizer], atualize suas permissões no [Admin Console](https://adminconsole.adobe.com/){target="_blank"}. Saiba como atualizar o perfil de produto [nesta página](../../administration/permissions.md#edit-product-profile).
   >

1. **Entender os perfis de produto**. Os perfis de produto são um conjunto de direitos unitários que permitem aos usuários acessarem determinadas funcionalidades ou objetos na interface. Saiba mais na seção [Perfis de produto prontos para uso](../../administration/ootb-product-profiles.md).

1. **Defina permissões** para perfis de produtos, incluindo **Sandboxes**, e conceda acesso aos membros da sua equipe, atribuindo-os a perfis de produtos diferentes. Essa etapa é executada no [Admin Console](https://adminconsole.adobe.com/){target="_blank"}. As permissões são direitos unitários que permitem definir as autorizações atribuídas ao **[!UICONTROL Perfil do produto]**. Cada permissão é coletada em recursos, por exemplo, Jornada ou Ofertas, que representam as diferentes funcionalidades ou objetos em [!DNL Journey Optimizer]. Saiba mais na seção [Níveis de permissão](../../administration/high-low-permissions.md).

Além disso, você deve adicionar usuários que precisam de acesso ao Assets Essentials para os perfis do produto **Usuários do cliente do Assets Essentials** e/ou **Usuários do Assets Essentials**. [Leia mais na documentação do Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=pt-BR){target="_blank"}.

>[!NOTE]
>Para produtos do Journey Optimizer obtidos antes de 6 de janeiro de 2022, é necessário implantar o [!DNL Adobe Experience Manager Assets Essentials] para sua organização. Saiba mais na seção [Implantar o Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=pt-BR){target="_blank"}.

Ao acessar [!DNL Journey Optimizer] pela primeira vez, você é provisionado com uma sandbox de produção e aloca um determinado número de IPs dependendo do seu contrato.

Para criar suas jornadas e enviar mensagens, acesse o menu **ADMINISTRAÇÃO**. Navegue pelo menu **[!UICONTROL Canais]** para definir suas configurações de canal e mensagens (ou seja, predefinições de mensagem).

>[!NOTE]
>Como um **Administrador do sistema**, se você não conseguir ver o menu **[!UICONTROL Canais]** no [!DNL Journey Optimizer], atualize suas permissões no [Admin Console](https://adminconsole.adobe.com/){target="_blank"}. Saiba como atualizar o perfil de produto [nesta página](../../administration/permissions.md#edit-product-profile).
>

Siga as etapas listadas abaixo:

1. **Configurar mensagens e canais**: definir configurações, adaptar e personalizar configurações de email, SMS e mensagens por push

   * Definir **configurações de notificações por push** em ambos [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch]. [Saiba mais](../../push/push-gs.md)

   * Crie **configurações de canal** (ou seja, predefinições de mensagens) para configurar todos os parâmetros técnicos necessários de notificações por email, SMS e push. [Saiba mais](../../configuration/channel-surfaces.md)

   * Configure o **Canal SMS** para configurar todos os parâmetros técnicos necessários para o SMS. [Saiba mais](../../sms/sms-configuration.md)

   * Gerencie o número de dias durante os quais são executadas **tentativas** antes do envio de endereços de email para a lista de supressão. [Saiba mais](../../configuration/manage-suppression-list.md)

1. **Delegar subdomínios**: para qualquer novo subdomínio ser usado no Journey Optimizer, a primeira etapa será delegá-lo. [Saiba mais](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Criar pools de IP**: melhore a capacidade de entrega de email e a reputação, agrupando os endereços IP provisionados com sua instância. [Saiba mais](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Gerenciar a supressão e as listas de permissões**: melhore sua capacidade de entrega com supressão e listas de permissões

   * A [lista de supressão](../../reports/suppression-list.md) consiste em endereços de email que você deseja excluir de suas entregas, pois o envio para esses contatos pode prejudicar sua reputação de envio e as taxas de entrega. Você pode monitorar todos os endereços de email que são excluídos automaticamente do envio em uma jornada, como endereços inválidos, endereços que rejeitam de forma consistente e podem afetar negativamente sua reputação de email, e destinatários que emitem uma reclamação de spam de algum tipo contra uma de suas mensagens de email. Saiba como gerenciar a [lista de supressão](../../configuration/manage-suppression-list.md) e as [tentativas](../../configuration/retries.md).

   ![](../assets/suppression-list-filtering-example.png)

   * A [lista de permissões](../../configuration/allow-list.md) permite especificar endereços de email ou domínios individuais que serão os únicos destinatários ou domínios autorizados a receber os emails enviados de uma sandbox específica. Isso pode impedir que você envie emails acidentalmente para endereços de clientes reais quando estiver em um ambiente de teste. Saiba como [habilitar a lista de permissões](../../configuration/allow-list.md).

   Saiba mais sobre a gestão de capacidade de entrega [!DNL Adobe Journey Optimizer] [nesta página](../../reports/deliverability.md).
