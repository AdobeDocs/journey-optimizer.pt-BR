---
solution: Journey Optimizer
product: journey optimizer
title: Criar um plano de aquecimento de IP
description: Saiba como criar um plano de aquecimento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, grupo, subdomínios, capacidade de entrega
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 5%

---

# Criar um plano de aquecimento de IP {#ip-warmup}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao aquecimento de IP](ip-warmup-gs.md)
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* **[Criar um plano de aquecimento de IP](ip-warmup-plan.md)**
* [Executar o plano de aquecimento de IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

## Acessar e gerenciar planos de aquecimento de IP {#manage-ip-warmup-plans}

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Planos de aquecimento de IP]** menu. Todos os planos de aquecimento de IP criados até o momento são exibidos.

   ![](assets/ip-warmup-filter-list.png)

1. Você pode filtrar pelo status. Os diferentes status são:

   * **Não iniciado**: não ocorreu nenhuma execução
   * **Em andamento**: assim que uma execução for iniciada <!--or is done?-->
   * **Em pausa**
   * **Concluído**: todas as execuções no plano foram concluídas

1. Para excluir um plano de aquecimento de IP, selecione o **[!UICONTROL Excluir]** ícone ao lado de um item de lista e confirme a exclusão.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >O plano de aquecimento de IP selecionado será excluído permanentemente.

## Criar um plano de aquecimento de IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Especificar seu plano de aquecimento de IP"
>abstract="Baixe o modelo CSV e preencha-o com os dados das fases de aquecimento de IP e o número alvo de perfis."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Selecionar uma superfície de marketing"
>abstract="Você deve selecionar a mesma superfície que a selecionada na campanha que deseja associar ao plano de aquecimento de IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=pt-BR" text="Configurar superfícies de canais"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=pt-BR" text="Criar campanhas de aquecimento de IP"

>[!CAUTION]
>
>Para criar, editar e excluir os planos de aquecimento de IP, você deve ter a **[!UICONTROL Consultor de avaliação de entrega]** permissão.
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

Quando uma ou mais campanhas ativas com o **[!UICONTROL Ativação do plano de aquecimento de IP]** estiver ativada, você poderá associá-los a um plano de aquecimento de IP.

>[!CAUTION]
>
>Trabalhe com seu consultor de entrega para garantir que seu modelo de plano de aquecimento de IP esteja configurado corretamente. <!--TBC-->

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Planos de aquecimento de IP]** e clique em **[!UICONTROL Criar plano de aquecimento de IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Preencha os detalhes do plano de aquecimento de IP: dê a ele um nome e uma descrição.

   ![](assets/ip-warmup-plan-details.png)

1. Selecione um [superfície](channel-surfaces.md). Somente as superfícies de marketing estão disponíveis para seleção. [Saiba mais sobre tipo de email](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >Você deve selecionar a mesma superfície que a selecionada na campanha que deseja associar ao plano de aquecimento de IP. [Saiba como criar uma campanha de aquecimento de IP](#create-ip-warmup-campaign)

1. Fazer upload do arquivo do Excel que contém seu plano de aquecimento de IP<!--which formats are allowed?-->. Você pode usar o template fornecido pela equipe de avaliação do delivery.<!--TBC?--> [Saiba mais](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Clique em **[!UICONTROL Criar]**. O número de fases definido no arquivo carregado é exibido automaticamente em todas as execuções de cada fase. [Saiba mais](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

### Recarregar um plano de aquecimento de IP {#re-upload-plan}

É possível fazer upload novamente de outro plano de aquecimento de IP usando o botão correspondente.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>Os detalhes do plano de aquecimento de IP serão alterados conforme o arquivo recém-carregado. As execuções completas e ativadas não são afetadas.

### Fazer upload do arquivo que contém o plano {#upload-plan}

Veja abaixo um exemplo de um arquivo contendo um plano de aquecimento de IP.

![](assets/ip-warmup-sample-file.png)

Cada fase corresponde a um período composto por várias execuções, às quais você atribuirá uma única campanha.

Para cada execução, você tem um determinado número de recipients e definirá uma data em que essa execução será executada.

Você pode ter quantas colunas quiser para os domínios que deseja entregar. Neste exemplo, você tem três colunas: Gmail, Adobe e Others, o que significa que

A ideia é ter mais execuções nas primeiras fases e aumentar progressivamente o número de endereços direcionados, reduzindo o número de execuções.
