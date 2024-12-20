---
solution: Journey Optimizer
product: journey optimizer
title: Relatórios
description: Introdução aos relatórios
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: d2ff175a-8bca-4b62-931c-a909cfd9308d
source-git-commit: b3d1d02605ff5e759c665847efad2d78bef6a1cf
workflow-type: tm+mt
source-wordcount: '1083'
ht-degree: 1%

---

# Gerenciar seus relatórios {#channel-cja-manage}

## Analisar no Customer Journey Analytics {#analyze}

![](assets/cja-analyze.png)

Melhore sua experiência de análise de dados com sua licença do **[!DNL Customer Journey Analytics]** aproveitando o recurso **[!UICONTROL Analisar no CJA]**, disponível em todos os relatórios.

Essa poderosa opção redireciona você facilmente para o ambiente do **[!DNL Customer Journey Analytics]**, permitindo que você personalize seus relatórios extensivamente. Você pode enriquecer seus widgets com métricas de Customer Journey Analytics especializadas, elevando seus insights a um novo nível.

[Saiba mais sobre a interface Customer Journey Analytics.](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-getting-started)

## Definir o período do relatório {#report-period}

![](assets/cja-time-period.png)

Ao acessar um relatório, você pode aplicar um filtro de período de tempo, localizado no canto superior direito do relatório.

Por padrão, o período do filtro para uma campanha ou jornada é definido com suas datas de início e término. Se não houver uma data de término, o filtro assumirá como padrão a data atual.

Para modificar o filtro, é possível selecionar uma data de início e uma duração personalizadas ou escolher entre opções predefinidas, como semana passada ou dois meses atrás.

O relatório será atualizado automaticamente assim que o filtro for aplicado ou modificado.

## Exportar seus relatórios {#export-reports}

É possível exportar facilmente seus diferentes relatórios para formatos PDF ou CSV, o que permite compartilhá-los ou imprimi-los. As etapas para exportar relatórios estão detalhadas nas guias abaixo.

>[!BEGINTABS]

>[!TAB Exportar seu relatório como um arquivo CSV]

1. Em seu relatório, clique em **[!UICONTROL Compartilhar]** e selecione **[!UICONTROL Baixar CSV]** para gerar um arquivo CSV no nível de relatório geral.

   ![](assets/export_cja_csv.png)

1. O arquivo é baixado automaticamente e pode ser localizado em seus arquivos locais.

   Se você gerou o arquivo no nível do relatório, ele contém informações detalhadas para cada widget, incluindo seu título e dados.

>[!TAB Exportar seu relatório como um arquivo PDF]

1. No seu relatório, clique em **[!UICONTROL Compartilhar]** e selecione **[!UICONTROL Baixar PDF]**.

   ![](assets/export_cja_pdf.png)

1. Após o download ter sido solicitado, clique em **[!UICONTROL Download]**.

   ![](assets/export_cja_pdf_2.png)

1. O arquivo será aberto automaticamente no navegador.

Seu relatório agora está disponível para visualização, download ou compartilhamento em um arquivo pdf.

>[!ENDTABS]


## Agendar exportações {#schedule-export}

O **Agendar exportação** permite automatizar a entrega de até 10 relatórios em intervalos semanais, mensais ou anuais. Você também pode gerenciar facilmente os relatórios agendados, com opções para atualizar, editar, cancelar ou excluir qualquer uma das exportações agendadas.

1. Em seu relatório, clique em **[!UICONTROL Compartilhar]** e selecione **[!UICONTROL Exportação de agendamento]**.

   ![](assets/export-schedule-1.png)

1. Escolha seu **[!UICONTROL Tipo de arquivo]** entre CSV e PDF.

1. Se necessário, você pode adicionar uma **[!UICONTROL Descrição]** à sua exportação.

1. Insira o nome dos recipients que receberão esse delivery automatizado.

   ![](assets/export-schedule-2.png)

1. Escolha a **[!UICONTROL Frequência]**.

1. Com base na frequência selecionada, forneça os detalhes de agendamento relevantes, como:

   * Datas iniciais e finais

   * Intervalo (por exemplo, a cada poucas semanas)

   * Dia da semana específico

   * Semana do mês

   * Dia do mês

   * Mês do ano

1. Clique em **[!UICONTROL Enviar conforme agendado]**.

1. Para editar uma exportação agendada criada anteriormente, clique em **[!UICONTROL Compartilhar]** e selecione **[!UICONTROL Gerenciar agendamentos]**.

   ![](assets/export-schedule-3.png)

1. Na lista de exportações programadas, escolha a que deseja atualizar e faça as alterações necessárias.

1. Para excluir um relatório agendado, selecione um na lista de agendamentos gerenciados e clique em **[!UICONTROL Excluir]**.

   ![](assets/export-schedule-4.png)


## Criar uma métrica simples {#create-simple-metric}

Você pode criar métricas calculadas personalizadas diretamente dos seus relatórios. Você pode gerar insights mais personalizados e analisar melhor seus dados combinando duas métricas existentes de maneiras que se adaptam às suas necessidades específicas de relatórios.

1. Comece acessando o relatório no qual deseja adicionar uma nova métrica.

1. Na tabela do relatório, selecione as métricas desejadas, mantendo pressionadas as teclas `Shift` ou `CTRL/CMD` enquanto clica nelas. Em seguida, clique com o botão direito e selecione **[!UICONTROL Criar métrica a partir da seleção]**.

   Se você selecionar mais de duas métricas, somente as duas primeiras serão usadas no construtor de métricas.

   ![](assets/cja-create-metric_2.png)

1. No Criador de métrica calculada, nomeie sua nova métrica digitando o campo **[!UICONTROL Título]**. Você também pode adicionar uma **[!UICONTROL Descrição]**.

   >[!NOTE]
   >
   >Se você tiver o Customer Journey Analytics, poderá personalizar ainda mais suas métricas com opções adicionais. [Saiba mais](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-build-metrics#areas-of-the-calculated-metrics-builder)

1. Escolha as **[!UICONTROL Casas decimais]** apropriadas e selecione um **[!UICONTROL Formato]** (Decimal, Hora, Porcentagem ou Moeda) com base em como você deseja que sua métrica seja exibida.

1. Selecione o operador, como adição, subtração, multiplicação ou divisão, que determinará como a métrica é calculada.

   ![](assets/cja-create-metric.png)

1. Você pode reordenar os componentes, se necessário.

1. Quando estiver satisfeito com suas configurações, clique em **[!UICONTROL Aplicar]** para finalizar sua nova métrica.

1. Sua nova métrica aparecerá ao lado das métricas originais em seu relatório.

   ![](assets/cja-create-metric_3.png)

A métrica recém-criada será incluída ao exportar o relatório como um PDF ou CSV. No entanto, ela será removida do relatório assim que você fechá-lo.

## Explorar dados com a Análise Exploratória {#exploratory}

Use a ferramenta de Análise Exploratória para criar facilmente tabelas e visualizações a partir dos **[!UICONTROL Dimension]** e **[!UICONTROL Métricas]** selecionados. Essa ferramenta simplifica a exploração de dados, permitindo personalizar e analisar informações automaticamente com facilidade. Saiba mais em [esta documentação](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/quickinsight).

1. Comece acessando o relatório no qual deseja usar a Análise Exploratória.

1. Selecione o menu Análise exploratória no menu do painel esquerdo.

   ![](assets/exploratory_analysis_1.png)

1. Crie uma consulta escolhendo um **[!UICONTROL Dimension]** e uma **[!UICONTROL Métrica]** usando os menus suspensos. Você também pode selecionar um **[!UICONTROL Segmento]**, se necessário.

   ![](assets/exploratory_analysis_2.png)

1. Defina o intervalo de datas da análise para especificar o período em que deseja se concentrar. Por padrão, o intervalo de datas será definido como aquele usado no painel de relatórios.

1. Use as opções **[!UICONTROL Adicionar detalhamento]** ou **[!UICONTROL Adicionar métrica]** para incluir dimensões adicionais, permitindo um detalhamento de dados mais detalhado.

   Observe que você só pode adicionar até três **[!UICONTROL Dimension]**, **[!UICONTROL Métricas]** e **[!UICONTROL Segmentos]**.

Agora você pode analisar seus dados usando suas ferramentas personalizadas de tabela e visualização.

<!--## Create a down-funnel metric {#down-funnel}

1. Create a new journey or open an existing one. [Learn more on journey creation](../building-journeys/journey-gs.md)

1. On the canvas editor, select the option to "add a metric".

c. In the metric selector, choose whichever conversion metric seems appropriate and publish your journey

d. Open the report for the journey that you added the metric to and ensure that the metric has been added to the table alongside all the other pre-configured metrics.
-->

## Criar um público-alvo a partir dos dados de relatórios {#create-audience}

>[!IMPORTANT]
>
>Cada organização está limitada à publicação de 25 públicos-alvo. Além disso, os usuários podem publicar no máximo 5 públicos-alvo por hora e 20 por dia.
> Públicos-alvo únicos têm uma duração de 48 horas. Portanto, se 25 públicos-alvo forem publicados dentro desse período, públicos-alvo adicionais só poderão ser publicados após o período de 48 horas.

Agora é possível selecionar dados específicos na tabela e criar um público-alvo diretamente nessas seleções, simplificando e simplificando o processo de criação de público-alvo.

1. Comece navegando até a tabela de relatório que contém os dados que você deseja transformar em um público-alvo.

1. Clique com o botão direito na célula desejada e selecione **[!UICONTROL Criar público-alvo]**.

   Como alternativa, você pode iniciar a criação de públicos-alvo no widget **[!UICONTROL tela de Jornada]** selecionando um nó e clicando com o botão direito do mouse nele.

1. Na janela **[!UICONTROL Criar público-alvo]**, digite um **[!UICONTROL Nome]** e defina um **[!UICONTROL Intervalo de datas único]** para o público-alvo que você pretende publicar.

   >[!NOTE]
   >
   >Se você tiver o Customer Journey Analytics, poderá personalizar ainda mais suas métricas com opções adicionais. [Saiba mais](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/audiences/publish)

   ![](assets/audience_1.png)

1. Clique no botão **[!UICONTROL Criar]** para finalizar a criação do público-alvo. Observe que esse processo pode levar algum tempo para ser concluído.

Agora você pode continuar a usar o público recém-criado com uma Jornada ou Campanha.

