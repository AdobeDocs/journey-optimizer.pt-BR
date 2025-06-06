---
solution: Journey Optimizer
product: journey optimizer
title: Jornada simulação
description: Saiba como publicar uma jornada no modo de simulação
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Disponibilidade limitada" type="Informative"
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: cd85b58350b4f8829aa1bc925c151be9b061b170
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 8%

---

# Jornada simulação {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Teste sua jornada"
>abstract="Depois de projetar a jornada, execute um teste para confirmar sua funcionalidade e garantir que as etapas estejam corretas. Esse modo de publicação permite realizar um teste preliminar da jornada sem enviar comunicações para qualquer perfil."

O Jornada Dry run é um modo de publicação de jornada especial no Adobe Journey Optimizer que permite que os profissionais de marketing testem uma jornada usando dados de produção reais sem entrar em contato com clientes reais ou atualizar informações de perfil.  Esse recurso ajuda os profissionais de marketing a ganhar confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la ao vivo.


>[!AVAILABILITY]
>
>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.


## Principais benefícios {#journey-dry-run-benefits}

O Jornada Dry run aumenta a confiança do profissional e o sucesso da jornada, permitindo testes seguros e orientados por dados das jornadas do cliente usando dados de produção reais — sem o risco de entrar em contato com os clientes ou alterar as informações do perfil. Esse recurso permite que os profissionais de marketing validem o alcance do público-alvo e a lógica da ramificação antes de entrar em funcionamento, garantindo que as jornadas se alinhem às metas comerciais desejadas.

Com o Jornada Dry run, você obtém a capacidade de identificar problemas antecipadamente, otimizar estratégias de direcionamento e melhorar o design da jornada com base em dados reais, não em suposições. Integrado diretamente à tela do jornada, o Dry run oferece relatórios intuitivos e visibilidade dos principais indicadores de desempenho, permitindo que as equipes interajam com confiança e simplifiquem os fluxos de trabalho de aprovação. Isso aumenta a eficiência operacional, reduz o risco de lançamento e impulsiona melhores resultados de engajamento do cliente.

Em última análise, esse recurso melhora o tempo de implantação, reduz as falhas de jornada e fortalece a posição da Adobe como a plataforma confiável para organizar jornadas personalizadas de alto impacto.

A jornada Dry run traz:

1. **Ambiente de teste seguro**: perfis no modo de simulação não são contatados, garantindo que não haja risco de envio de comunicações ou de impacto nos dados dinâmicos.
1. **Insights do público-alvo**: os profissionais de marketing podem prever a acessibilidade do público-alvo em vários nós de jornada, incluindo recusas, exclusões e outras condições.
1. **Feedback em tempo real**: as métricas são exibidas diretamente na tela de jornada, de modo semelhante aos relatórios em tempo real, permitindo que os profissionais de marketing refinem seu design de jornada.

## Iniciar uma simulação {#journey-dry-run-start}

Você pode usar o recurso Dry run em qualquer jornada de rascunho sem erros.

Para ativar o Dry run, siga estas etapas:

1. Abra a jornada que deseja testar.
1. Clique no botão **Execução seca**.

   ![Iniciar a simulação de jornada](assets/dry-run-button.png)

1. Confirmar a publicação

   Uma mensagem de status, **Ativando Dry run**, é exibida enquanto a transição está ocorrendo.

1. Uma vez ativada, a jornada entra no modo Dry run.

Durante a simulação, a jornada é executada com as seguintes especificidades:

* Os nós **Ação de canal** com notificações por email, SMS ou push não são executados.
* **As ações personalizadas** estão desabilitadas durante a execução Seca e suas respostas estão definidas como nulas.
* **Os nós de espera** são ignorados durante a execução Dry.
  <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
* **Fontes de dados externas** são executadas por padrão.

>[!NOTE]
>
> * Os perfis no modo de simulação são contados em perfis acionáveis.
> * As jornadas de simulação não afetam as regras de negócios. Por exemplo, um perfil em uma jornada Dry run não será excluído de outras jornadas devido a regras como `1 journey per day`.

## Monitorar uma simulação {#journey-dry-monitor}

Depois que a publicação no modo Seco for iniciada, você poderá visualizar a execução da jornada e como os perfis avançam por ramificações e nós de jornada.

As métricas são exibidas diretamente na tela de jornada.

![Monitorar a execução de simulação de jornada](assets/dry-run-metrics.png)

Para cada atividade, você pode verificar:

* **[!UICONTROL Informado]**: número total de indivíduos que entraram nesta atividade.
* **[!UICONTROL Saída (atender aos critérios de saída)]**: Número total de indivíduos que saíram da jornada dessa atividade devido a um critério de saída.
* **[!UICONTROL Saída (saída forçada)]**: Número total de indivíduos que saíram quando a jornada foi pausada. Essa métrica é sempre igual a zero para jornadas no modo de Execução em tempo real.
* **[!UICONTROL Erro]**: número total de indivíduos que tiveram um erro nessa atividade.


No nível da jornada, você pode verificar:

* O número total de **Perfis inseridos**
* O número total de **Perfis encerrados**
* O número total de **Perfis com erro**
* O número total de **Perfis descartados** na jornada

Você também pode acessar os **Últimos relatórios de 24 horas** e os **Relatórios de tempo integral** para o Dry run. Para acessar esses relatórios, clique no botão **Exibir relatório** no canto superior direito da tela de jornada.

![Acessar os relatórios para a execução de simulação de jornada](assets/dry-run-report.png)

>[!CAUTION]
>
> Os dados de relatório estão disponíveis somente quando a simulação está **ativa**.  Depois de interrompido, os dados de relatório não estarão mais acessíveis. Use o botão **Exportar** acima dos relatórios para baixá-los, se necessário.


## Parar uma simulação {#journey-dry-run-stop}

As jornadas de simulação devem ser interrompidas manualmente. Clique no botão **Fechar** para finalizar o teste e confirmar.

Após 14 dias, as jornadas de execução seca fazem a transição automática para o status Rascunho.
