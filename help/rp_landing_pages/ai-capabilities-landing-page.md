---
solution: Journey Optimizer
product: Journey Optimizer
title: Recursos de IA no Adobe Journey Optimizer
description: Recursos de IA no Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 9d0460d303a3701ad7ff5b7f2487ac6ccdd6facd
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 3%

---

# Recursos de IA no Adobe Journey Optimizer{#section-overview}

A Adobe Journey Optimizer aproveita o poder da inteligência artificial e do aprendizado de máquina para transformar a maneira como você cria, otimiza e fornece experiências de cliente. Desde a geração de conteúdo personalizado em vários canais até a previsão do momento ideal para envolver os clientes, os recursos de IA simplificam seu fluxo de trabalho e maximizam o impacto. Esta seção explora como os recursos alimentados por IA funcionam juntos para ajudá-lo a tomar decisões mais inteligentes, automatizar tarefas complexas e criar experiências que realmente refletem no seu público-alvo. Independentemente de você estar aproveitando a IA gerativa para criação de conteúdo, usando modelos preditivos para tomada de decisão ou otimizando os tempos de envio para um melhor engajamento, você descobrirá ferramentas e estratégias práticas para explorar todo o potencial da IA na orquestração de jornadas do cliente.

## Recursos alimentados por IA

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/sparkles.svg)

Assistente de IA para geração de conteúdo

Aproveite a IA gerativa para criar e personalizar conteúdo em emails, SMS, notificações por push, páginas da Web e páginas de aterrissagem.

[Explorar o assistente de IA](ai-assistant-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=pt-BR)

Otimização de tempo de envio

Use a IA para prever o momento ideal para enviar mensagens e maximizar o envolvimento do cliente com base no comportamento histórico.

[Saiba mais sobre a otimização de tempo de envio](../using/building-journeys/send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Modelos de IA para a decisão

Crie modelos de otimização automática e personalizada para classificar e fornecer as melhores ofertas aos seus clientes.

[Descubra modelos de IA](ai-models-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/help.svg)

Conhecimento de produto do AI Assistant

Obtenha respostas instantâneas e insights operacionais sobre o Adobe Journey Optimizer usando IA conversacional.

[Trabalhar com o Assistente de IA](../using/start/ai-assistant.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/experiment.svg)

Experimentação de conteúdo com IA

Gere várias variações de conteúdo e execute experimentos para identificar o conteúdo com melhor desempenho para o seu público-alvo.

[Saiba mais sobre experimentação de IA](../using/content-management/generative-experimentation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/user-group.svg?lang=pt-BR)

Integração da IA do cliente

Integre-se aos Serviços inteligentes da Adobe para prever o comportamento do cliente e usar pontuações de churn e conversão em suas jornadas.

[Explorar os serviços inteligentes](../using/building-journeys/ai-services-overview.md)
:::

::::


## Recursos adicionais

- **[Pontuação de alinhamento da marca](../using/content-management/brands-score.md)** - Avalie como o conteúdo gerado por IA se alinha às diretrizes da sua marca usando a pontuação habilitada por IA.
- **[Acelerador de experimentos](../using/content-management/experiment-accelerator-gs.md)** - Acelere seu processo de experimentação de conteúdo com insights e recomendações orientados por IA.
- **[APIs alimentadas por IA](../using/configuration/ajo-apis.md)** - Acesse os recursos de IA e aprendizado de máquina do Journey Optimizer programaticamente por meio das APIs.

## Perguntas frequentes

+++**Que permissões são necessárias para usar os recursos de IA?**

Para usar o Assistente de IA para geração de conteúdo, os usuários devem receber a permissão **Gerar conteúdo**. Essa permissão é atribuída por meio do recurso Assistente de IA no produto Permissões. Para usar o AI Assistant para obter conhecimento do produto e insights operacionais, os usuários devem concordar com as Diretrizes de usuário da IA gerativa da Adobe Experience Cloud.

[Saiba mais sobre permissões](../using/administration/ootb-permissions.md)

+++

+++**Quais canais oferecem suporte à geração de conteúdo do Assistente de IA?**

O Assistente de IA para geração de conteúdo está disponível para os canais **Email**, **Push**, **SMS** e **Web**. No momento, não está disponível para os canais Correspondência direta, Cartões de conteúdo, LINE ou WhatsApp.

+++

+++**Quais são as práticas recomendadas para usar o Assistente de IA?**

- **Usar prompts bem definidos** - A qualidade do conteúdo gerado é fortemente afetada pelo seu objetivo e prompt de marketing. Seja específico e claro.
- **Carregar ativos da marca** - Forneça ativos da marca no formato PDF, JPEG, PNG ou ZIP (máx. 50 MB) para obter conteúdo preciso sobre a marca.
- **Usar modelos personalizados** - Aproveite os modelos de email específicos da marca com até 8 a 10 imagens para obter os melhores resultados.
- **Fornecer feedback** - Relate saídas problemáticas usando miniatura, miniatura ou ícones de sinalizador para ajudar a refinar os modelos.
- **Aproveite apenas um ativo de marca por geração** - Embora você possa carregar vários ativos, use apenas um para cada geração específica.

[Saiba mais sobre as medidas de proteção do Assistente de IA](../using/content-management/gs-generative.md#generative-guardrails)

+++

+++**Quais são as práticas recomendadas para a Otimização de Tempo de Envio?**

- **Aguarde 30 dias** - Use ações de email e push por pelo menos 30 dias antes de habilitar a Otimização de Tempo de Envio para garantir uma coleta de dados suficiente.
- **Escolha os tempos de espera ideais** - Defina o tempo máximo de espera entre 6 e 24 horas para obter melhores resultados. Durações mais curtas limitam o potencial de otimização; durações mais longas podem resultar em mensagens desatualizadas.
- **Otimizar para a métrica correta** - Para emails, otimizar para Cliques ao direcionar ações ou Abrir para conteúdo informativo. As mensagens de push são sempre otimizadas para Aberturas.
- **Evite mensagens com detecção de hora** - Não use a Otimização de Hora de Envio para mensagens operacionais urgentes, como confirmações de pedidos, redefinições de senha ou notificações de viagem. Mais adequado para comunicações de marketing, como promoções e boletins informativos.
- **Agendar envios por push pela manhã** - Para evitar notificações noturnas, agendar envios por push em lote pela manhã com durações mais curtas (por exemplo, envio às 9h com tempo de espera de 8 horas).

[Saiba mais sobre a Otimização de tempo de envio](../using/building-journeys/send-time-optimization.md)

+++

+++**Quais são as limitações da Otimização de Tempo de Envio?**

- **Canais** - disponível somente para canais de email e notificação por push no Jornada. Não disponível em Campanhas ou por meio de ações personalizadas.
- **Disponibilidade** - Deve ser habilitada pelo Atendimento ao cliente da Adobe ou pelo representante da Adobe.
- **Período de treinamento** - Requer pelo menos 30 dias de dados históricos de email ou push antes de usar.
- **Treinamento do modelo** - Os modelos são treinados inicialmente semanalmente, usando as últimas 16 semanas de dados, e depois retreinados mensalmente.
- **Exploração vs. Otimização** - 5% das mensagens recebem tempos de envio de exploração aleatórios; 95% recebem tempos de envio otimizados.

+++

+++**Quais são as limitações dos modelos de IA no Decisioning?**

- **Máximo de modelos de IA** - Até 5 modelos de classificação de IA por organização.
- **Requisitos do conjunto de dados** - Pelo menos 2 ofertas devem ter mais de 100 eventos de exibição e mais de 5 eventos de clique nos últimos 14 dias para modelos de otimização automática.
- **Eventos de feedback** - Devem ser enviados como eventos de experiência; não coletados automaticamente nos canais da Journey Optimizer.
- **Limitações de API** - Os modelos de otimização automática não funcionam com a API de decisão em lote (somente Gerenciamento de decisão).

[Saiba mais sobre os modelos de IA](../using/experience-decisioning/ranking/ai-models.md)

+++

+++**Que medidas de proteção se aplicam à decisão baseada em IA?**

| Componente | Limite |
|-----------|-------|
| Modelos de classificação de IA | 5 por organização |
| Solicitações de decisão (com base em código com a segmentação do Edge) | 1.500 por segundo |
| Solicitações de decisão (com base em código sem segmentação do Edge) | 5.000 por segundo |
| Coleções de itens | 10.000 no total |
| Itens de oferta por coleção | 500 |
| Estratégias de seleção por política de decisão | 10 |
| Itens de oferta retornados por política de decisão | 30 |
| Regras de elegibilidade + fórmulas de classificação | 10.000 combinados |
| Atributos de perfil por regra | 25 |
| Atributos de dados de contexto por regra | 30 |

[Saiba mais sobre Medidas de proteção de decisão](../using/experience-decisioning/decisioning-guardrails.md)

+++

+++**Preciso concordar com algum termo para usar os recursos de IA?**

Sim, você deve concordar com as [Diretrizes de usuário da IA gerativa da Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) antes de usar o Assistente de IA na Journey Optimizer. Entre em contato com seu representante da Adobe para obter mais informações. Além disso, a Adobe aplica o Content Credentials a ativos gerados pela Firefly como parte de seu compromisso com a transparência no uso da IA gerativa.

+++

+++**O conteúdo gerado por IA é sempre preciso?**

Não. O conteúdo de IA gerativa pode nem sempre ser preciso. Sempre revise as saídas geradas por IA para verificar a precisão e verifique se são apropriadas para o seu caso de uso. Compartilhe feedback usando as ferramentas de classificação fornecidas para ajudar os engenheiros a refinar os modelos.

+++

