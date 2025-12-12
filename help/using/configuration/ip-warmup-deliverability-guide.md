---
solution: Journey Optimizer
product: journey optimizer
title: Guia de entrega de IP warmup
description: Saiba mais sobre os fundamentos de capacidade de entrega e as práticas recomendadas para aquecimento de IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, capacidade de entrega, reputação, ISP, envolvimento
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 5%

---

# Guia de entrega de IP warmup {#ip-warmup-deliverability-guide}

Ao iniciar campanhas de email com novos endereços IP ou domínios no Adobe Journey Optimizer, entender os fundamentos da capacidade de entrega é fundamental para criar uma sólida reputação do remetente. Este guia aborda os principais conceitos, etapas de preparação e práticas recomendadas para ajudá-lo a fazer a transição da reputação zero para a inserção bem-sucedida da caixa de entrada.

➡️ Saiba mais sobre os fundamentos de capacidade de entrega, a criação de reputação e as práticas recomendadas para aumento gradual de IP no vídeo desta [publicação do blog do Adobe](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=pt){target="_blank"}.

>[!NOTE]
>
>Para obter instruções passo a passo sobre como implementar planos de aquecimento de IP no Adobe Journey Optimizer, consulte [Introdução aos planos de aquecimento de IP](ip-warmup-gs.md).

## Por que a reputação do IP e do domínio são importantes {#reputation-matters}

Os provedores de caixa de correio (Gmail, Yahoo, Microsoft, Apple Mail e outros) avaliam cada remetente com base em quatro pilares principais:

* **Reclamações**: os destinatários marcaram suas mensagens como spam?
* **Compromisso**: os destinatários abrem, clicam ou respondem aos seus emails?
* **Infraestrutura**: sua infraestrutura de envio é autenticada, estável e confiável?
* **Conteúdo**: o conteúdo da sua mensagem parece legítimo e valioso?

O aumento gradual de volume de IP aborda principalmente os três primeiros pilares, demonstrando aos provedores de caixa de correio que sua nova infraestrutura é legítima e desejada antes de chegar ao volume de envio completo.

## Lista de verificação antes do voo {#pre-flight-checklist}

Antes de começar a aquecer seus endereços IP, verifique se todos os elementos fundamentais estão em vigor. A tabela abaixo descreve as tarefas essenciais que devem ser concluídas antes de iniciar o plano de aquecimento de IP.

| Tarefa | Por que isso importa | Como realizar |
|------|----------------|-------------------|
| Reservar IP(s) fixo(s) e subdomínios delegados no AJO | Toda reputação futura se associa a esses elementos de infraestrutura. | Navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** > **[!UICONTROL Subdomínios]**. [Saiba mais](delegate-subdomain.md) |
| Configurar SPF e DKIM | Confirma que o servidor de envio é legítimo e autorizado. | Manipulado automaticamente pela Adobe após [delegação de subdomínio](delegate-subdomain.md) e [criação de configuração de canal](channel-surfaces.md). |
| Verifique se o registro do DMARC está configurado (p=none) | Habilita relatórios de autenticação de email e políticas de imposição futuras. | Verifique se o registro do DMARC está configurado para todos os subdomínios delegados. Ao delegar um novo subdomínio, você pode configurar o DMARC diretamente na interface. [Saiba mais](dmarc-record.md) |
| Configurar monitoramento da lista de propagação | Detecta problemas de posicionamento da caixa de entrada no início do processo de aquecimento. | Adicione seed addresses ao criar a configuração do canal. [Saiba mais](seed-lists.md) |
| Criar público-alvo de alto engajamento da Fase 1 | Aumenta as métricas de engajamento antecipado com os recipients mais ativos. | Crie um público-alvo com menos de 5.000 contatos que abriram ou clicaram nos últimos 30 dias. [Saiba mais](../audience/creating-a-segment-definition.md) |

>[!CAUTION]
>
>Problemas de autenticação (SPF, DKIM, DMARC) não podem ser resolvidos por meio do ramping de volume. Verifique se estão configurados corretamente antes de começar a enviar.

## Calendário de amostra de aquecimento de quatro semanas {#warmup-calendar}

Este calendário de exemplo fornece um aumento de volume progressivo com base na porcentagem do seu volume diário final (UDV). Ajuste esses números para se ajustarem às suas necessidades específicas de envio e trabalhe com seu consultor de capacidade de entrega para criar um plano personalizado.

| Days | % de UDV | Público-alvo | Recomendações de conteúdo |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5% | Seus destinatários mais envolvidos | Use o formato de texto simples e curto com uma call-to-action clara acima da dobra. |
| 4-7 | 1% | Usuários envolvidos e compradores recentes | Adicione uma imagem principal leve e limite os links a 3 ou menos. |
| 8-14 | 5% | Lista de assinantes ativos mais ampla | Apresente seu modelo de email padrão, mas evite conteúdo promocional pesado. |
| 15-21 | 25% | Assinantes ativos mais levemente inativos | Use o conteúdo de marketing normal enquanto monitora as taxas de reclamação de perto. |
| 22-28 | 50-100% | Lista completa (respeitando as listas de supressão) | Transição para a cadência de envio em estado estacionário. |

## Uso do recurso de planos de aquecimento de IP {#ajo-warmup-feature}

O Adobe Journey Optimizer inclui um recurso simplificado de [planos de aquecimento de IP](ip-warmup-gs.md) que elimina a necessidade de limitação manual de volume por meio de configurações complexas de jornada. Essa funcionalidade garante uma abordagem padronizada para criar a reputação do remetente.

### Como funciona

1. **Criar campanhas de aquecimento de IP**: crie uma ou mais campanhas com a opção **[!UICONTROL Ativação do plano de aquecimento de IP]** habilitada. [Saiba mais](ip-warmup-campaign.md)

1. **Configurar seu plano**: acesse **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** > **[!UICONTROL Planos de aquecimento de IP]** e carregue seu modelo de aquecimento em fases preparado com seu consultor de entrega. [Saiba mais](ip-warmup-plan.md)

1. **Executar fases**: selecione uma campanha para cada fase e ative as execuções correspondentes. O sistema exclui automaticamente os perfis de execuções anteriores para evitar contato excessivo. [Saiba mais](ip-warmup-execution.md)

1. **Monitorar e ajustar**: use o painel de relatórios consolidado para monitorar o progresso, monitorar status de execução e modificar seu plano se surgirem problemas. [Saiba mais](ip-warmup-execution.md#monitor-plan)

## Monitoramento em tempo real e métricas principais {#monitoring}

O Adobe Journey Optimizer fornece recursos de relatórios integrados para rastrear o desempenho de aquecimento de IP:

* **Relatórios ao vivo**: acesse a medição e a visualização em tempo real de suas campanhas na guia **[!UICONTROL Últimas 24 horas]**. [Saiba mais](../reports/campaign-live-report.md#email-live)

* **Todos os relatórios de tempo**: para obter insights mais profundos, use o Customer Journey Analytics para analisar dados do Adobe Experience Platform e criar visualizações personalizadas. [Saiba mais](../reports/report-gs-cja.md)

### Métricas do Target

Monitore esses indicadores-chave de desempenho durante o aquecimento:

| Métrica | Limite do público alvo | Ação corretiva |
|--------|-----------------|-------------------|
| Taxa de reclamação | ≤ 0,1 % | Se excedido, segmento de auditoria e suprimir reclamadores crônicos. |
| Taxa de rejeição permanente | ≤ 2 % | Se excedido, revise a qualidade da lista e as práticas de higiene. |
| Taxa de abertura | ≥ 10% | Se for muito baixo, verifique se você está direcionando públicos envolvidos. |

## Manual de solução de problemas {#troubleshooting}

Use esta matriz de decisão para resolver problemas comuns durante o aquecimento:

| Sintoma | Causa provável | Ação recomendada |
|---------|--------------|-------------------|
| Falhas temporárias do Yahoo (erros 421) | Volume aumentado muito rapidamente | Pausar o envio por 24 horas e reiniciar no nível anterior. |
| Taxa de abertura abaixo de 2% em contas iniciais | IP ➡ incluir na lista de bloqueios | Verifique as [Ferramentas de Postmaster do Google](https://postmaster.google.com/) e o [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/); abra um tíquete de capacidade de entrega, se necessário. |
| Taxa de reclamação excede 0,3% | Público mal direcionado ou obsoleto | Auditoria de definições de segmentos e exclusão de reclamadores crônicos da sua [lista de supressão](manage-suppression-list.md). |

>[!IMPORTANT]
>
>É melhor desacelerar seu aquecimento do que tentar reparar uma reputação de remetente danificada posteriormente. Sempre priorize a manutenção de métricas íntegras em vez de ramping de volume agressivo.

## Práticas recomendadas pós-aquecimento {#post-warmup}

Depois de concluir o plano de aquecimento, as métricas se estabilizaram:

* **Manter a consistência**: mantenha o volume diário aumentado abaixo de 30% semana a semana para preservar a reputação estabelecida.

* **Monitorar continuamente**: agende verificações trimestrais de integridade da reputação para identificar e solucionar problemas de forma proativa.

* **Respeitar sinais de engajamento**: continue a priorizar destinatários engajados e implementar campanhas de reengajamento para assinantes inativos.

* **Mantenha a autenticação atualizada**: verifique regularmente se seus registros SPF, DKIM e DMARC permanecem configurados corretamente.

## Principais pontos {#key-takeaways}

* **O aquecimento de IP é essencial**: ignorar o processo de aquecimento custa mais tempo e reputação do que o esforço necessário para executá-lo corretamente.

* **Decisões orientadas por dados**: controle diariamente as taxas de reclamação, rejeição e engajamento e ajuste sua estratégia antes que os ISPs o penalizem.

* **Autenticação primeiro, volume segundo**: resolva todos os problemas de SPF, DKIM e DMARC antes de começar a aumentar o volume.

* **Questões de consistência**: os provedores de caixa de correio favorecem padrões de envio previsíveis; evitem picos de volume repentinos ou agendas de envio irregulares.

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=pt).-->

## Tópicos relacionados {#related-topics}

* [Introdução aos planos de aquecimento de IP](ip-warmup-gs.md)
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* [Criar um plano de aquecimento de IP](ip-warmup-plan.md)
* [Executar o plano de aquecimento de IP](ip-warmup-execution.md)
* [Definir configurações de canal](channel-surfaces.md)
* [Delegar subdomínios](delegate-subdomain.md)
* [Gerenciar lista de supressão](manage-suppression-list.md)
* [Guia de Práticas Recomendadas de Entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=pt-BR)

