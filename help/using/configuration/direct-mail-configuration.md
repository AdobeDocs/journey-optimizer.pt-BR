---
title: Configuração de correspondência direta
description: Saiba como configurar o canal de correspondência direta no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bca233ab888e2ca33b866bc3def31653f2d55ea9
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Configuração de correspondência direta {#direct-mail-configuration}

[!DNL Journey Optimizer] permite personalizar e gerar os arquivos exigidos por provedores de correspondência direta para enviar emails para seus clientes.

When [criação de uma mensagem de mala direta](../messages/create-direct-mail.md), você define os dados do público-alvo, incluindo as informações de contato escolhidas (endereço postal por exemplo). Um arquivo contendo esses dados será gerado e exportado automaticamente para um servidor, onde seu provedor de correspondência direta poderá recuperá-lo e cuidar do envio real.

Antes de gerar esse arquivo, é necessário criar:

1. A [configuração de roteamento de arquivos](#file-routing-configuration) para especificar o servidor onde o arquivo será exportado.

1. A [superfície de correspondência direta](#direct-mail-surface) que referenciará a configuração de roteamento de arquivos.

>[!CAUTION]
>
>Se não tiver configurado nenhuma opção de roteamento de arquivos, você não poderá criar uma superfície de correspondência direta.

## Configurar roteamento de arquivos {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definir a configuração de roteamento de arquivos"
>abstract="Após criar uma mensagem de correspondência direta, o arquivo contendo os dados do público-alvo direcionado será gerado e exportado para um servidor. Você precisa especificar os detalhes do servidor para que seu provedor de correspondência direta possa acessar e usar esse arquivo para delivery de correspondência direta."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-direct-mail.html" text="Criar uma mensagem de correspondência direta"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definir a configuração de roteamento de arquivos"
>abstract="Você precisa definir onde o arquivo será exportado para que seu provedor de correspondência direta use."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuração do roteamento de arquivos"
>abstract="Selecione a configuração de roteamento de arquivos de sua escolha, que define onde o arquivo será exportado para que seu provedor de correspondência direta use."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Selecione o tipo de servidor para o arquivo"
>abstract="Escolha o tipo de servidor que deseja usar para exportar seus arquivos de correspondência direta. Atualmente, somente o Amazon S3 e SFTP são compatíveis com a Journey Optimizer."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Escolha a região do AWS"
>abstract="Selecione a região geográfica do servidor do AWS onde deseja exportar seus arquivos de correspondência direta. Como prática geral, é preferível escolher a região mais próxima da localização do provedor de correspondência direta."

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
>title="Definir as configurações de correspondência direta"
>abstract="Uma superfície de mala direta contém as configurações para a formatação do arquivo que contém os dados do público-alvo direcionado e será usada pelo provedor de email. Você também deve definir onde o arquivo será exportado selecionando a configuração de roteamento do arquivo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/direct-mail-configuration.html#file-routing-configuration" text="Configurar roteamento de arquivos"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definir o limite de divisão de arquivo"
>abstract="É necessário definir o número máximo de registros para cada arquivo contendo dados de público-alvo. Você pode selecionar qualquer número entre 1 e 200.000 registros. Depois que o limite especificado for atingido, outro arquivo será criado para os registros restantes."

Para enviar mala direta com o [!DNL Journey Optimizer], é necessário criar uma superfície de canal para definir as configurações de formatação do arquivo que será usado pelo provedor de email.

Uma superfície de correspondência direta também deve incluir a configuração de roteamento de arquivos que define o servidor onde seu arquivo de correspondência direta será exportado.

1. Crie uma superfície de canal. [Saiba mais](channel-surfaces.md)

1. Selecione o **[!UICONTROL Correspondência direta]** canal.

   ![](assets/surface-direct-mail-channel.png)

1. Defina as configurações de correspondência direta na seção dedicada da configuração da superfície do canal.

   ![](assets/surface-direct-mail-settings.png)

1. Selecione o formato de arquivo: **[!UICONTROL CSV]** ou **[!UICONTROL Delimitado por texto]**.

1. No **[!UICONTROL Inserção]** , é possível optar por remover automaticamente linhas duplicadas.

1. Defina o número máximo de registros (ou seja, linhas) para cada arquivo que contenha dados de perfil. Depois que o limite especificado for atingido, outro arquivo será criado para os registros restantes.

   ![](assets/surface-direct-mail-split.png)

   Por exemplo, se houver 100.000 registros no arquivo e o limite for definido como 60.000, os registros serão divididos em dois arquivos. O primeiro arquivo terá 60.000 linhas e o segundo arquivo conterá as 40.000 linhas restantes.

   >[!NOTE]
   >
   >É possível definir qualquer número entre 1 e 200.000 registros, o que significa que cada arquivo deve conter pelo menos 1 linha e não mais de 200.000 linhas.

1. Finalmente, selecione o **[!UICONTROL Configuração do roteamento de arquivos]** entre os que você criou. Isso define onde o arquivo será exportado para que seu provedor de correspondência direta use.

   >[!CAUTION]
   >
   >Se não tiver configurado nenhuma opção de roteamento de arquivos, você não poderá criar uma superfície de correspondência direta. [Saiba mais](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)

1. Envie a superfície da correspondência direta.

Agora você pode [criar uma mensagem de mala direta](../messages/create-direct-mail.md) dentro de uma campanha. Quando a campanha for iniciada, o arquivo contendo os dados do público-alvo direcionado será automaticamente exportado para o servidor que você definiu. O provedor de correspondência direta poderá recuperar esse arquivo e prosseguir com o delivery de correspondência direta.