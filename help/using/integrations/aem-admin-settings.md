---
solution: Journey Optimizer
product: journey optimizer
title: Definir configurações do repositório do AEM
description: Saiba como os administradores configuram repositórios do AEM, domínios personalizados, publicações autenticadas e acesso somente a fragmentos de conteúdo do autor no Journey Optimizer.
feature: Integrations
topic: Administration
role: Admin
level: Experienced
hide: true
keywords: AEM, Fragmentos de conteúdo, administração, repositório, autenticação, autor, publicação
source-git-commit: 9da185872d2742799f1a2a2c85a840c84cb8b329
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Configurar o acesso ao repositório do Adobe Experience Manager {#aem-admin-settings}

O Adobe Journey Optimizer integra-se ao **[!DNL Adobe Experience Manager as a Cloud Service]** para que você possa usar **Fragmentos de conteúdo** em Jornadas e Campanhas. Por padrão, os **Fragmentos de conteúdo** são lidos do repositório de publicação do Adobe Experience Manager. Os administradores podem alternar para somente autor ou ajustar o acesso de publicação no menu **[!UICONTROL Integração do AEM]**.

➡️ Quando o repositório estiver configurado, continue com [Trabalhe com os Fragmentos de conteúdo do Experience Manager](../integrations/aem-fragments.md) para as tarefas de criação e seleção no Journey Optimizer.

## Configurar repositórios {#configure-ui}

>[!NOTE]
>
> **[!UICONTROL A Integração do AEM]** salva as configurações do repositório **por sandbox**. Cada sandbox mantém suas próprias integrações e elas não se aplicam a sandboxes.

O Journey Optimizer armazena uma integração por organização, sandbox e repositório do Adobe Experience Manager. Se você salvar uma nova integração para essa mesma combinação, ela substituirá as configurações anteriores, somente a configuração mais recente será mantida.

Para configurar o repositório:

1. Acesse **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Integração com o AEM]**.

1. Clique em **[!UICONTROL Criar integração]**.

   ![](assets/aem-admin-settings-1.png)

1. Se você usa **[!DNL Adobe Experience Manager Managed Services]**, insira um nome de host de repositório que termine com `adobecqms.net` no campo **[!UICONTROL ID de repositório AMS personalizada]**.

   ![](assets/aem-admin-settings-6.png)

1. Escolha qual repositório deve ser configurado e clique em **[!UICONTROL Avançar]**.

   Além disso, você pode clicar em **[!UICONTROL Exibir]** para acessar este repositório.

   >[!IMPORTANT]
   >
   >Salvar uma nova configuração para a mesma organização, sandbox e repositório **substitui** a configuração padrão, ou seja, **publicar** repositório.

   ![](assets/aem-admin-settings-2.png)

1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]**.

1. Escolha sua configuração:

   +++ Configuração somente do autor

   Selecione **[!UICONTROL Configuração somente de autor]** quando o Journey Optimizer precisar ler somente os Fragmentos de conteúdo do ambiente **de autor** do Adobe Experience Manager. A replicação de autor para publicar e atualizações de publicação em tempo real não é compatível.

   ![](assets/aem-admin-settings-3.png)

   +++

   +++ Configuração da instância de publicação

   1. Selecione **[!UICONTROL Configuração da instância de publicação]** para ativar as configurações da instância de publicação.

      ![](assets/aem-admin-settings-4.png)

   1. Habilite opcionalmente **[!UICONTROL Enviar token para a instância de publicação]** para que as credenciais de serviço sejam incluídas nas solicitações para a instância de publicação.

   1. Cole uma **[!UICONTROL Credencial de Serviço JSON]** válida para autenticação.

   1. Forneça opcionalmente um domínio personalizado se sua organização não conseguir acessar o host de publicação padrão do AEM (`publish-XX-XX.adobeaemcloud.com`) para buscar conteúdo.

      ![](assets/aem-admin-settings-5.png)

   +++

1. Depois de concluir a configuração da instância, escolha um Fragmento de conteúdo para confirmar se a integração funciona.

   ![](assets/aem-admin-settings-7.png)

1. Na janela **Supervisor de Conteúdo**, selecione o fragmento que deseja testar e clique em **[!UICONTROL Selecionar]**.

1. Clique em **[!UICONTROL Save]**.

1. Quando você salva com um Fragmento de conteúdo de teste selecionado, a validação é executada automaticamente. Se a validação falhar, uma lista de erros será exibida para que você possa corrigir a configuração.

   ![](assets/aem-admin-settings-8.png)

1. Para editar ou desabilitar essa integração de repositório, acesse a configuração criada anteriormente pelo menu **[!UICONTROL Integração do AEM]**.

Ao salvar essa configuração, o Journey Optimizer a armazena para esse repositório na sandbox atual. Você pode usar esse repositório e suas configurações ao navegar e selecionar conteúdo no seletor do **Supervisor de Conteúdo**.

