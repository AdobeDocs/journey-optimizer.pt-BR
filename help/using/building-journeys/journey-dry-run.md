---
solution: Journey Optimizer
product: journey optimizer
title: Execução de prática de jornada
description: Saiba como publicar uma jornada no modo de simulação
feature: Journeys
role: User
level: Intermediate
badge: label="Disponibilidade limitada" type="Informative"
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: 62525caa9b065538c090b98d38c15dbd960dafe7
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 24%

---

# Execução de prática de jornada {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Modo de execução de prática"
>abstract="Esta jornada está em execução de prática. A Execução de prática da jornada é um modo de publicação especial no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais, sem entrar em contato com clientes reais ou atualizar informações de perfil.  Esse recurso ajuda os profissionais de jornada a ganharem confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Publicar uma jornada no modo de execução de prática"
>abstract="A Execução de prática da jornada é um modo de publicação especial no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais. Depois de projetar a jornada, execute um teste para confirmar sua funcionalidade e garantir que as etapas estejam corretas. Esse modo de publicação permite realizar um teste preliminar da jornada sem enviar comunicações para qualquer perfil."

A Execução de prática da jornada é um modo de publicação especial no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais, sem entrar em contato com clientes reais ou atualizar informações de perfil.  Esse recurso ajuda os profissionais de jornada a ganharem confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la.


>[!AVAILABILITY]
>
>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será implantado globalmente em uma versão futura.


## Principais benefícios {#journey-dry-run-benefits}

O Jornada Dry run aumenta a confiança do profissional e o sucesso da jornada, permitindo testes seguros e orientados por dados das jornadas do cliente usando dados de produção reais — sem o risco de entrar em contato com os clientes ou alterar as informações do perfil. Esse recurso permite que os profissionais de jornada validem o alcance do público-alvo e a lógica da ramificação antes de entrar em funcionamento, garantindo que as jornadas se alinhem às metas de negócios desejadas.

Com o Jornada Dry run, você obtém a capacidade de identificar problemas antecipadamente, otimizar estratégias de direcionamento e melhorar o design da jornada com base em dados reais, não em suposições. Integrado diretamente à tela do jornada, o Dry run oferece relatórios intuitivos e visibilidade dos principais indicadores de desempenho, permitindo que as equipes interajam com confiança e simplifiquem os fluxos de trabalho de aprovação. Isso aumenta a eficiência operacional, reduz o risco de lançamento e impulsiona melhores resultados de engajamento do cliente.

Em última análise, esse recurso melhora o tempo de implantação e reduz as falhas de jornada.

A jornada Dry run traz:

1. **Ambiente de teste seguro**: perfis no modo de simulação não são contatados, garantindo que não haja risco de envio de comunicações ou de impacto nos dados dinâmicos.
1. **Insights do público-alvo**: os profissionais de Jornada podem prever a acessibilidade do público-alvo em vários nós de jornada, incluindo recusas, exclusões e outras condições.
1. **Feedback em tempo real**: as métricas são exibidas diretamente na tela de jornada, de modo semelhante aos relatórios em tempo real, permitindo que os profissionais de jornada refinem seu design de jornada.

Durante a simulação, a jornada é executada com as seguintes especificidades:

* Os nós **Ação de canal**, incluindo emails, SMS ou notificações por push, não são executados
* **As ações personalizadas** estão desabilitadas durante a execução Seca e suas respostas estão definidas como nulas
* **Os nós de espera** são ignorados durante a execução Dry.
  <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
* **As fontes de dados**, incluindo as fontes de dados externas, são executadas por padrão

>[!CAUTION]
>
>* As permissões para iniciar o Dry Run estão restritas a usuários com a permissão de alto nível **[!DNL Publish journeys]**. As permissões para parar o Dry Run estão restritas a usuários com a permissão de alto nível **[!DNL Manage journeys]**. Saiba mais sobre como gerenciar os direitos de acesso de [!DNL Journey Optimizer] usuários em [esta seção](../administration/permissions-overview.md).
>
>* Antes de começar a usar o recurso Dry run, [leia as Medidas de Proteção e as Limitações](#journey-dry-run-limitations).


## Iniciar uma simulação {#journey-dry-run-start}

Você pode usar o recurso Dry run em qualquer jornada de rascunho sem erros.

Para ativar o Dry run, siga estas etapas:

1. Abra a jornada que deseja testar.
1. Selecione o botão **Execução seca**.

   ![Iniciar a simulação de jornada](assets/dry-run-button.png)

1. Confirme a publicação.

   Uma mensagem de status, **Ativando Dry run**, é exibida enquanto a transição está ocorrendo.

1. Uma vez ativada, a jornada entra no modo **Execução seca**.

## Monitorar uma simulação {#journey-dry-monitor}

Depois que a publicação no modo Seco for iniciada, você poderá visualizar a execução da jornada e como os perfis avançam por ramificações e nós de jornada.

As métricas são exibidas diretamente na tela de jornada. Saiba mais sobre métricas e relatórios ao vivo do jornada em [Relatório ao vivo na tela de jornada](report-journey.md).

![Monitorar a execução de simulação de jornada](assets/dry-run-metrics.png)


Você também pode acessar os **Últimos relatórios de 24 horas** e os **Relatórios de tempo integral** para o Dry run. Para acessar esses relatórios, clique no botão **Exibir relatório** no canto superior direito da tela de jornada.

![Acessar os relatórios para a execução de simulação de jornada](assets/dry-run-report.png)

>[!CAUTION]
>
> Os dados de relatório estão disponíveis somente quando a simulação está **ativa**.  Depois de interrompido, os dados de relatório não estarão mais acessíveis. Use o botão **Exportar** acima dos relatórios para baixá-los, se necessário.


## Parar uma simulação {#journey-dry-run-stop}

As jornadas de execução sem erros **devem** ser interrompidas manualmente.

Clique no botão **Fechar** para encerrar o teste e clique em **Voltar ao Rascunho** para confirmar.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## Medidas de proteção e limitações {#journey-dry-run-limitations}

* O modo simulação não está disponível para jornadas que contêm eventos de reação
* Os perfis no modo simulação são contados em perfis acionáveis
* Jornadas no modo simulação são contadas para a cota de jornada ativa
* As jornadas de simulação não afetam as regras de negócios
* Ao criar uma nova versão do jornada, se uma versão anterior do jornada for **Live**, a ativação do Dry run não será permitida na nova versão.
* O Jornada Dry run gera stepEvents. Estes stepEvents têm um sinalizador específico e um ID de simulação:
   * `_experience.journeyOrchestration.stepEvents.inDryRun` retorna `true` se a Execução Seca estiver ativada, caso contrário `false`
   * `_experience.journeyOrchestration.stepEvents.dryRunID` retorna a ID de uma instância de simulação

* Ao analisar métricas de relatório do jornada usando o serviço de consulta da Adobe Experience Platform, os eventos de etapa gerados por Dry Run devem ser excluídos. Para fazer isso, defina o sinalizador `inDryRun` como `false`.