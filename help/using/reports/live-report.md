---
solution: Journey Optimizer
product: journey optimizer
title: Relatório em tempo real
description: Saiba como usar os dados do relatório em tempo real
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
TQID: https://experienceleague.adobe.com/RmJeQGDGLOM5LbdRS4HQbWE7sttyT4jGsuyXF-BdB-Q
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: b36ce7a039c976d80f49292e73be23c9b011b568
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 2%

---

# Introdução ao relatório em tempo real {#live-report}

>[!BEGINSHADEBOX]

**Nesta página:** comece a usar o relatório ao vivo do Adobe Journey Optimizer para visualizar o desempenho do jornada e da campanha em tempo real, personalizar widgets de painel e exportar seus relatórios.

>[!ENDSHADEBOX]

Use o **[!UICONTROL Relatório ao vivo]** para medir e visualizar em tempo real o impacto e o desempenho das suas jornadas e mensagens em um painel integrado. Os dados estão disponíveis no **[!UICONTROL Relatório em tempo real]** assim que a entrega é enviada ou a jornada é executada a partir da guia **[!UICONTROL Últimas 24 horas]**.

* Se quiser direcionar uma jornada no contexto de uma jornada, no menu **[!UICONTROL Jornadas]**, acesse o menu **[!UICONTROL Mais ações]** da jornada e clique no botão **[!UICONTROL Exibir relatório das últimas 24 horas]**.

  ![](assets/report_journey.png)

* Se quiser direcionar uma campanha, no menu **[!UICONTROL Campanhas]**, acesse sua campanha e clique no botão **[!UICONTROL Relatórios]** e depois em **[!UICONTROL Exibir relatório das últimas 24 horas]**.

  ![](assets/report_campaign.png)

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](#list-of-components-live).

>[!NOTE]
>
>São esperadas discrepâncias de curto prazo entre o relatório ao vivo e o relatório de todos os tempos. O relatório em tempo real usa feeds de dados quase em tempo real, enquanto o relatório de todos os tempos depende de dados agregados. Caso ocorram discrepâncias, aguarde no mínimo duas horas antes de reconciliar os dois relatórios, pois os dados normalmente se propagam para a exibição agregada dentro desse período.

## Personalizar painel {#modify-dashboard}

Cada painel de relatórios pode ser modificado redimensionando ou removendo widgets. Alterar os widgets afeta apenas o painel do usuário atual. Outros usuários verão seus próprios painéis ou os definidos por padrão.

1. No menu suspenso **[!UICONTROL Ações]**, escolha se deseja relatar uma ação específica de suas jornadas.

1. Escolha se deseja excluir eventos de teste de seus relatórios com a barra de alternância. Para obter mais informações sobre eventos de teste, consulte [esta página](../building-journeys/testing-the-journey.md).

   Observe que a opção **[!UICONTROL Excluir eventos de teste]** só está disponível para relatórios de Jornada.

   ![](assets/report_modify_6.png)

1. Para redimensionar ou remover widgets, clique em **[!UICONTROL Modificar]**.

   ![](assets/report_modify_7.png)

1. Ajuste o tamanho dos widgets arrastando o canto inferior direito.

   ![](assets/report_modify_8.png)

1. Clique em **[!UICONTROL Remover]** para remover qualquer widget desnecessário.

   ![](assets/report_modify_9.png)

1. Quando estiver satisfeito com a ordem de exibição e o tamanho dos seus widgets, clique em **[!UICONTROL Salvar]**.

1. Para personalizar a forma como seus dados são exibidos, você pode alternar entre diferentes opções de visualização, como gráficos, tabelas e gráficos de rosca.

   ![](assets/report_modify_11.png)

O painel foi salvo. Suas diferentes alterações serão reaplicadas para um uso posterior de seus relatórios ao vivo. Se necessário, use a opção **[!UICONTROL Redefinir]** para restaurar a ordem dos widgets e widgets padrão.

## Exportar seus relatórios {#export-reports}

É possível exportar facilmente seus diferentes relatórios para formatos PDF ou CSV, o que permite compartilhá-los ou imprimi-los.

>[!BEGINTABS]

>[!TAB Exportar seu relatório como um arquivo do PDF]

1. No seu relatório, clique em **[!UICONTROL Exportar]** e selecione **[!UICONTROL arquivo do PDF]**.

   ![](assets/export_6.png)

1. Na janela Imprimir, configure o documento conforme necessário. Observe que as opções podem variar dependendo do navegador.

1. Opte por imprimir ou salvar seu relatório como PDF.

1. Localize a pasta onde deseja salvar o arquivo, renomeie-a se necessário e clique em Salvar.

Seu relatório agora está disponível para visualização ou compartilhamento em um arquivo pdf.

>[!TAB Exportar seu relatório como um arquivo CSV]

1. Em seu relatório, clique em **[!UICONTROL Exportar]** e selecione **[!UICONTROL Arquivo CSV]** para gerar um arquivo CSV no nível de relatório geral.

   ![](assets/export_4.png)

1. Você também pode optar por exportar dados de um widget específico. Clique em **[!UICONTROL Baixar arquivo CSV]** ao lado do widget selecionado.

   ![](assets/export_5.png)

1. O arquivo é baixado automaticamente e pode ser localizado em seus arquivos locais.

   Se você gerou o arquivo no nível do relatório, ele contém informações detalhadas para cada widget, incluindo seu título e dados.

   Se você gerou o arquivo no nível do widget, ele fornece especificamente os dados para o widget selecionado.

>[!ENDTABS]
