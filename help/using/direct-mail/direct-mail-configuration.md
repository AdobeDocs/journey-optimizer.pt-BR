---
title: Configuração de correspondência direta
description: Saiba como configurar o canal de correspondência direta no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
hide: true
hidefromtoc: true
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
badge: label="Beta" type="Informative"
source-git-commit: 55f1c6a681aece6446a3330184466ff61e4db580
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 32%

---

# Configuração de correspondência direta {#direct-mail-configuration}

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* [Criar uma correspondência direta](create-direct-mail.md)
* **[Configurar correspondência direta](direct-mail-configuration.md)**

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] permite personalizar e gerar os arquivos exigidos por provedores de correspondência direta para enviar emails para seus clientes.

When [criação de uma mensagem de mala direta](../direct-mail/create-direct-mail.md), você define os dados do público-alvo, incluindo as informações de contato escolhidas (endereço postal por exemplo). Um arquivo contendo esses dados será gerado e exportado automaticamente para um servidor, onde seu provedor de correspondência direta poderá recuperá-lo e cuidar do envio real.

Antes de gerar esse arquivo, é necessário criar:

1. A [configuração de roteamento de arquivos](#file-routing-configuration) para especificar o servidor onde o arquivo será exportado.

1. A [superfície de correspondência direta](#direct-mail-surface) que referenciará a configuração de roteamento de arquivos.

>[!CAUTION]
>
>Se não tiver configurado nenhuma opção de roteamento de arquivos, você não poderá criar uma superfície de correspondência direta.

## Configurar o roteamento de arquivos {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definir a configuração de roteamento de arquivos"
>abstract="Após criar uma mensagem de correspondência direta, o arquivo contendo os dados do público-alvo direcionado será gerado e exportado para um servidor. Você precisa especificar os detalhes do servidor para que seu provedor de correspondência direta possa acessar e usar esse arquivo para a entrega da correspondência direta."

<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/create-direct-mail.html" text="Create a direct mail message"-->

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definir a configuração de roteamento de arquivos"
>abstract="Você precisa definir para onde o arquivo será exportado para que seu provedor de correspondência direta o use."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuração do roteamento de arquivos"
>abstract="Selecione a configuração de roteamento de arquivos de sua escolha, que define para onde o arquivo será exportado para que seu provedor de correspondência direta o use."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Selecionar o tipo de servidor para o arquivo"
>abstract="Escolha o tipo de servidor que deseja usar para exportar os arquivos de correspondência direta. Atualmente, somente o Amazon S3 e SFTP são compatíveis com o Journey Optimizer."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Escolha a região do AWS"
>abstract="Selecione a região geográfica do servidor do AWS para onde deseja exportar os arquivos de correspondência direta. Como prática geral, é preferível escolher a região mais próxima da localização do provedor de correspondência direta."

Para enviar uma mensagem de mala direta, [!DNL Journey Optimizer] gera e exporta o arquivo contendo os dados do público-alvo direcionado para um servidor.

Você precisa especificar os detalhes do servidor para que seu provedor de correspondência direta possa acessar e usar esse arquivo para delivery de correspondência.

Para configurar o roteamento de arquivos, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configuração do roteamento de arquivos]** > **[!UICONTROL Roteamento de arquivo]** , em seguida, clique em **[!UICONTROL Criar configuração de roteamento]**.

   ![](assets/file-routing-config-button.png)

1. Defina um nome para sua configuração.

1. Selecione o **[!UICONTROL Tipo de servidor]** que você deseja usar para exportar os arquivos de correspondência direta.

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Atualmente, somente o Amazon S3 e SFTP são compatíveis com o [!DNL Journey Optimizer].

1. Preencha os detalhes e as credenciais do servidor, como endereço do servidor, chave de acesso etc.

   ![](assets/file-routing-config-sftp-details.png)

1. Se você selecionou **[!UICONTROL Amazon S3]**, escolha o **[!UICONTROL Região do AWS]** onde a infraestrutura do servidor estará localizada.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >As regiões do AWS são áreas geográficas que a AWS usa para hospedar suas infraestruturas de nuvem. Como prática geral, é preferível escolher a região mais próxima da localização do provedor de correspondência direta.

1. Selecione **[!UICONTROL Enviar]**. A configuração de roteamento de arquivos é criada com a variável **[!UICONTROL Ativo]** status. Agora está pronto para ser usado em um [superfície de correspondência direta](#direct-mail-surface).

   >[!NOTE]
   >
   >Você também pode selecionar **[!UICONTROL Salvar como rascunho]** para criar a configuração de roteamento de arquivos, mas você não poderá selecioná-la em uma superfície até que seja **[!UICONTROL Ativo]**.

## Criar uma superfície de correspondência direta {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Definir as configurações da correspondência direta"
>abstract="A superfície de correspondência direta contém as configurações para a formatação do arquivo que contém os dados do público direcionado e será usada pelo provedor de email. Você também pode definir para onde o arquivo será exportado selecionando a configuração de roteamento do arquivo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/direct-mail-configuration.html?lang=br#file-routing-configuration" text="Configurar o roteamento de arquivos"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definir o limite de divisão de arquivo"
>abstract="É necessário definir o número máximo de registros para cada arquivo contendo dados de público. Você pode selecionar qualquer número entre 1 e 200.000 registros.. Depois que o limite especificado for atingido, outro arquivo será criado para os registros restantes."

Para enviar mala direta com o [!DNL Journey Optimizer], é necessário criar uma superfície de canal para definir as configurações de formatação do arquivo que será usado pelo provedor de email.

Uma superfície de correspondência direta também deve incluir a configuração de roteamento de arquivos que define o servidor onde seu arquivo de correspondência direta será exportado.

1. Crie uma superfície de canal. [Saiba mais](../configuration/channel-surfaces.md)

1. Selecione o **[!UICONTROL Correspondência direta]** canal.

   ![](assets/surface-direct-mail-channel.png)

1. Defina as configurações de correspondência direta na seção dedicada da configuração da superfície do canal.

   ![](assets/surface-direct-mail-settings.png)

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Selecione o formato de arquivo: **[!UICONTROL CSV]** ou **[!UICONTROL Delimitado por texto]**.

1. Selecione o **[!UICONTROL Configuração do roteamento de arquivos]** entre os que você criou. Isso define onde o arquivo será exportado para que seu provedor de correspondência direta use.

   >[!CAUTION]
   >
   >Se não tiver configurado nenhuma opção de roteamento de arquivos, você não poderá criar uma superfície de correspondência direta. [Saiba mais](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Envie a superfície da correspondência direta.

Agora você pode [criar uma mensagem de mala direta](../direct-mail/create-direct-mail.md) dentro de uma campanha. Quando a campanha for iniciada, o arquivo contendo os dados do público-alvo direcionado será automaticamente exportado para o servidor que você definiu. O provedor de correspondência direta poderá recuperar esse arquivo e prosseguir com o delivery de correspondência direta.

>[!NOTE]
>
>As linhas duplicadas serão removidas automaticamente.
>
>Se o número máximo de registros (ou seja, linhas) para cada arquivo contendo dados de perfil for muito alto, outro arquivo será criado automaticamente para os registros restantes.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->