---
solution: Journey Optimizer
product: journey optimizer
title: Exibir métricas de uso de SMS
description: Saiba como gerar relatórios de uso de SMS para reconciliar o volume de mensagens com a cobrança do fornecedor no Journey Optimizer.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: b519bcd5489c441e7f22cb47783d8b99a58c2442
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# Gerar relatório de uso de SMS {#sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_metrics"
>title="Métricas de uso de SMS"
>abstract="Gerar relatórios de uso de SMS para reconciliar o volume de mensagens com a cobrança do fornecedor. Os relatórios listam contagens terminadas por dispositivo móvel (MT) e originadas por dispositivo móvel (MO) para cada código curto ou número de telefone, agregadas por dia."

>[!BEGINSHADEBOX]

**Nesta página:** gere relatórios de uso de SMS no Adobe Journey Optimizer para reconciliar volumes MT (terminados por dispositivo móvel) e MO (originados por dispositivo móvel) com a cobrança do fornecedor, usando uma credencial da API MMS do Sinch e uma saída CSV para download.

>[!ENDSHADEBOX]

As métricas de uso de SMS estão disponíveis quando você compra SMS pelo Adobe Journey Optimizer. Os relatórios resumem o tráfego de envio e recebimento por código curto ou número de telefone, agregado por dia, nos últimos **90 dias**.

Para visualizar as métricas de uso, um administrador deve:

1. [Criar uma credencial da API do MMS Sinch](mobile-configuration-sinch.md#sinch-mms) usada apenas para recuperar dados de uso do Sinch.

   Os relatórios de uso exigem uma credencial de API com **[!UICONTROL fornecedor de SMS]** definida como **Sinch MMS**. Essa credencial conecta o Journey Optimizer ao Sinch para que os dados de uso possam ser recuperados. Ele é separado das credenciais do Sinch usadas para enviar mensagens SMS ou MMS, embora os valores de campo sejam provenientes do mesmo projeto do Sinch.

1. [Configurar e recuperar um relatório de uso de SMS](#configure-sms-usage-report).

Essas etapas exigem a permissão **[!UICONTROL Gerenciar configurações de SMS]**. [Saiba mais sobre permissões](../administration/high-low-permissions.md#administration-permissions).

## Configurar e exibir relatórios de uso de SMS {#configure-sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_report_name"
>title="Nome do relatório"
>abstract="Insira um rótulo que ajude a reconhecer esse relatório na lista posteriormente, por exemplo, revisão de cobrança de maio de 2026."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_credential"
>title="Credenciais de SMS"
>abstract="Selecione a credencial da API Sinch cujo tráfego de envio e recebimento deve aparecer neste relatório. Para adicionar ou atualizar credenciais, vá para **Administração** > **Canais** > **Credenciais da API** e escolha **Fornecedor de SMS** > **Sinch MMS**."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_start_date"
>title="Data inicial"
>abstract="Primeiro dia do intervalo de datas a ser incluído no relatório. Os dados de uso estão disponíveis somente para os últimos 90 dias."

Os relatórios de uso do SMS apresentam o volume de origem móvel (MO) e terminado por dispositivo móvel (MT) por código curto para oferecer suporte à reconciliação entre a atividade de mensagens e cobrança de fornecedores no Journey Optimizer.

1. No painel à esquerda, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de SMS]**.

1. Acesse o menu **[!UICONTROL Exibir métricas de uso de SMS]** e clique em **[!UICONTROL Configurar novo relatório]**.

   ![](assets/usage_report_1.png)

1. Configure o relatório:

   * **[!UICONTROL Nome do relatório]**: digite um rótulo que o ajude a reconhecer seu relatório.
   * **[!UICONTROL Credenciais de SMS]**: selecione a **Credencial de API do Sinch MMS** criada anteriormente para seus relatórios de uso de SMS.
   * **[!UICONTROL Data de início]** e **[!UICONTROL Data de término]**: defina o intervalo de datas do relatório. Os dados de uso estão disponíveis somente para os últimos 90 dias.

     ![](assets/usage_report_2.png)

1. Clique em **[!UICONTROL Configurar relatório]** para enviar a solicitação.

1. Na lista **[!UICONTROL Relatórios enviados]**, encontre o relatório configurado e clique em **[!UICONTROL Recuperar relatório]**.

   O status muda para **Pendente** enquanto o relatório é gerado.

1. Assim que o status do relatório for atualizado para **[!UICONTROL Pronto]**, clique em **[!UICONTROL Exibir]** para abrir o relatório. O relatório inclui:

   * **Resumo de uso**: total de mensagens com origem em dispositivo móvel (MO) e terminadas em dispositivo móvel (MT) para as datas selecionadas, detalhado por código curto.

   * **Volume de SMS diário**: volume de SMS por dia, detalhado por código curto.

     ![](assets/usage_report_3.png)

1. Para exportar o relatório, clique em **[!UICONTROL Baixar CSV]**. O Journey Optimizer baixa um arquivo CSV para o relatório que você está visualizando.
