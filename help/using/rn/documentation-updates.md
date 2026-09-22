---
solution: Journey Optimizer
product: journey optimizer
title: Atualizações de documentação
description: Saiba mais sobre as atualizações de documentação mais recentes do Adobe Journey Optimizer, incluindo novas páginas, reorganizações e esclarecimentos.
keywords: atualizações de documentação, notas de versão, otimizador de jornadas, changelog
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 723a2d044d7a1d184d83198d4b6e752997aff8f3
workflow-type: tm+mt
source-wordcount: '7183'
ht-degree: 82%
---

# Atualizações na documentação {#latest-updates}

Esta página lista todas as alterações mais recentes na documentação do [!DNL Journey Optimizer], além das atualizações relacionadas aos recursos e melhorias da versão mensal.

## Setembro de 2026 {#september-2026}

* As orientações para mirror pages de email foram expandidas: a documentação agora explica que os URLs de mirror page não podem ser recuperados por meio de uma API ou um conjunto de dados público, recomenda o arquivamento de Exportação de mensagens ou CCO para manter o conteúdo enviado e esclarece que os links de mirror page estão inativos em provas e simulações. [Leia mais](../email/message-tracking.md#mirror-page)

* Uma nova página de **Demonstração interativa** está disponível para desafios de fidelidade, vinculando a uma demonstração autoguiada e clicável que abrange o fluxo de criação de desafios do profissional de marketing (incluindo Traga seus próprios dados e os painéis de insights), a experiência do cliente final e o Gerenciamento de desafios de fidelidade no CX Coworker. [Leia mais](../loyalty-challenges/loyalty-challenges-demo.md)

* A página **Personalizar sua tela de fundo de email** foi expandida e aprimorada. Agora, ela documenta a lista suspensa **Posicionamento da imagem** para imagens de plano de fundo e adiciona novas práticas recomendadas para cores e imagens de plano de fundo, incluindo uma recomendação para testar imagens de plano de fundo em clientes de email reais, em vez de depender exclusivamente da visualização do Designer de email. [Leia mais](../email/backgrounds.md)

* O conteúdo **Design do zero com a página Email Designer** foi reorganizado e esclarecido: ele distingue a estrutura da **[!UICONTROL n:n coluna]** das estruturas de predefinição fixa, documenta que a contagem de colunas de uma estrutura pode ser aumentada sem perder conteúdo existente, explica o comportamento de empilhamento de colunas em dispositivos móveis e adiciona uma nova etapa no uso de **[!UICONTROL Módulos]** para a criação de emails de início rápido. [Leia mais](../email/content-from-scratch.md)

* A página **Criar sua jornada** agora inclui uma seção de tutorial completa sobre a nova experiência da tela, que aborda como adicionar atividades, usar os ícones da barra de ferramentas, selecionar várias atividades para ações em massa, copiar e colar atividades e ingressar ou desanexar ramificações. [Leia mais](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

* Novas orientações foram adicionadas para verificar a entrega de ação personalizada: a página **Exemplos de consulta de conjunto de dados** agora explica como escolher entre os conjuntos de dados de Evento de feedback de mensagem, Rastreamento de email e Evento de etapa de Jornada, dependendo do tipo de ação, e documenta como resolver um erro &quot;Tabela não provisionada para conjunto de dados&quot;. As páginas **Visão geral dos eventos de etapa da Jornada** e **Solução de problemas de execução da jornada em tempo real** foram atualizadas de acordo, esclarecendo que uma chamada de ação personalizada bem-sucedida apenas confirma que o Journey Optimizer executou a ação, não que o sistema externo tenha entregue uma mensagem. [Leia mais](../data/datasets-query-examples.md#choose-the-correct-dataset)

* Foram adicionadas informações sobre o CX Coworker à página **Trabalhar com IA**, que aborda o que é o CX Coworker, como ele se relaciona com o Assistente de IA e referências à documentação oficial do Colaborador. Páginas de habilidades dedicadas também foram adicionadas a cada guia de recursos — [Habilidades do CX Coworker para jornada](../building-journeys/journeys-coworker-skills.md), [Habilidades do CX Coworker para fidelidade](../loyalty-challenges/loyalty-coworker-skills.md) e [ferramentas de gerenciamento de conteúdo do CX Coworker](../content-management/content-management-coworker-skills.md). [Leia mais](../start/ai-features.md#cx-coworker)

* Uma nova habilidade **Analisar anomalias de Jornada** foi documentada em **Analisar Jornada** na página do CX Coworker. Ele detecta picos, quedas ou linhas achatadas inesperados nas contagens de entrada, saída ou envio de uma jornada em relação às linhas de base históricas e executa diagnósticos somente leitura para mostrar uma causa raiz provável. [Leia mais](../building-journeys/journeys-coworker-skills.md#journey-analyze)

* As páginas **Medidas de proteção e limitações** e **propriedades de Jornada** foram atualizadas para documentar o limite de carga de jornada padrão como **2 MB (2.000.000 bytes)**, esclarecer que o valor reflete a definição de jornada serializada em vez de apenas a contagem de atividades e explicar os limites de aviso de 90% e de bloqueio de 100%. [Leia mais](../start/guardrails.md#journey-payload-size) e [saiba mais](../building-journeys/journey-properties.md#journey-payload-size)

* A página **Medidas de proteção e limitações** foi corrigida para refletir o fato de que fragmentos visuais com mais de 100 KB ou fragmentos de expressão com mais de 200 KB não podem mais causar problemas de truncamento na entrega de email: agora uma única medida de proteção de tamanho de fragmento de 700 KB é aplicada. [Leia mais](../start/guardrails.md#fragments-guardrails)

* A página **Criar uma atividade ao vivo** foi corrigida: o campo `executionMetadata` está disponível somente para campanhas **Transacionais acionadas por API**, não para campanhas de Marketing acionadas por API, conforme declarado anteriormente. [Leia mais](../mobile-live/create-mobile-live.md#metadata)

* A documentação do **Conjunto de Dados de Eventos de Feedback de Mensagens do AJO** foi expandida para esclarecer que abrange o feedback de entrega de mensagens em todos os canais (Email, SMS/RCS/MMS, Mala direta), não apenas email e push, e agora inclui uma seção **Classificar execuções de teste e não teste** explicando como interpretar o campo `isTestExecution`, incluindo `NULL` ou valores ausentes. [Leia mais](../data/datasets-query-examples.md#classify-test-executions)

* Um novo recurso **Gerenciamento de conteúdo** foi documentado para o CX Coworker, alimentado por 15 ferramentas de MCP de leitura/gravação que permitem descobrir, criar, atualizar, clonar e publicar modelos de conteúdo, fragmentos, páginas de aterrissagem e conteúdo de mensagem em linha do jornada/campaign usando prompts de linguagem natural. [Leia mais](../content-management/content-management-coworker-skills.md#content-management)

* A documentação **Adicionar conteúdo à página de aterrissagem** agora descreve uma opção **Tornar campo de formulário obrigatório** para caixas de seleção de consentimento: quando habilitada, o formulário não pode ser enviado, a menos que a caixa de seleção esteja marcada e a seleção seja imposta no lado do cliente e no lado do servidor. [Leia mais](../landing-pages/lp-content.md#use-form-component)

* A página **Introdução à Simulação de Jornada** foi atualizada para documentar que os nós de Decisão de Conteúdo e o método de regra de Direcionamento da atividade **Otimizar** agora são compatíveis com a Simulação (listada anteriormente como bloqueio), com uma nova tabela **Comportamento de decisão** que detalha como a qualificação da oferta, as regras de elegibilidade, os públicos-alvo e os métodos de classificação são avaliados durante a execução da simulação. [Leia mais](../building-journeys/simulate-journey-gs.md#limitations)

* A página **Converter imagens para modelos de conteúdo de email** foi corrigida para remover um requisito de permissões impreciso: a permissão **Gerenciar modelos de conteúdo** não é necessária para acessar e criar modelos com a imagem no conversor do HTML — somente a permissão **Gerar conteúdo** é necessária. [Leia mais](../content-management/image-to-html.md#access-image-to-html)

* A página **Sistemas externos (ações personalizadas)** foi corrigida: o disjuntor para pontos de extremidade de ação personalizada lenta agora é ativado quando mais de 20% das chamadas em uma janela de 120 segundos excedem **5 segundos** (documentado anteriormente como 10 segundos). [Leia mais](../configuration/external-systems.md#response-time)

* A página **Definir a configuração do canal** agora inclui uma observação esclarecendo que o esquema usado para a dimensão secundária deve ter uma chave primária e que não há suporte para chaves primárias compostas. [Leia mais](../orchestrated/channel-config.md)

* Os **conjuntos de dados e dados de fidelidade** e **Introdução às fontes** foram atualizados para incluir o LAVA como um conector de fidelidade e recompensa compatível, junto com o Talon.One, Capillary e Kobie. [Leia mais](../loyalty-challenges/loyalty-data-and-datasets.md)

## Agosto de 2026 {#august-2026}

* A página **Adicionar fragmentos visuais aos seus emails** agora esclarece que um fragmento com conteúdo dinâmico e um estado padrão vazio aparece em branco no Email Designer — simule com um perfil correspondente para visualizar o conteúdo. [Leia mais](../email/use-visual-fragments.md#fragment-dynamic-content)

* A página **Rastrear suas mensagens** foi atualizada para esclarecer que caracteres de URL não suportados (por exemplo, apóstrofos) devem ser codificados por porcentagem, e que deixá-los não codificados pode quebrar os links rastreados e os parâmetros de rastreamento de URL. [Leia mais](../email/message-tracking.md#insert-links)

* A página **Enviar usando ondas** foi atualizada para documentar que a última onda em uma jornada de público-alvo de leitura deve ser agendada dentro de **6 dias e 18 horas** do início da jornada. Exceder essa janela aciona um erro de validação e impede que a jornada entre no modo de teste ou entre em funcionamento. [Leia mais](../delivery/send-using-waves.md#limitations-guardrails)

* Uma nova seção **Suprimir eventos de comentários** foi adicionada à página **Coleta de dados de gerenciamento de decisão**, documentando como usar o sinalizador `dryRun` para suprimir eventos de decisão durante o teste e impedir que os comentários sejam capturados para contadores de relatório e limite de frequência. [Leia mais](../offers/data-collection/data-collection.md#suppress-feedback)

* Uma nova página **Escolher um método de validação** está disponível. Ele compara Simulação de Jornada, Modo de teste e Execução de Jornada seca — os dados que cada um usa, se envia mensagens reais, erros comuns a serem evitados e um guia de decisão para escolher o método correto em cada estágio da criação de uma jornada. [Leia mais](../building-journeys/choose-validation-method.md)

* A página **Medidas de proteção e limitações** foi atualizada para esclarecer a atividade de Qualificação de público-alvo e Medidas de proteção de eventos: a redação agora se refere consistentemente às **atividades** de Qualificação de público-alvo (em vez de nós), incluindo quando usadas como critérios de saída, e ambas as medidas de proteção agora abrangem explicitamente as **jornadas em tempo real, encerradas, pausadas, modo de teste e execução de teste**. [Leia mais](../start/guardrails.md#audience-qualif-g)

* Uma observação foi adicionada à seção **Testar otimização de tamanho do HTML** para esclarecer que os tamanhos de prova refletem o tamanho do modelo do HTML (Handlebars no valor mínimo), não o tamanho final do email entregue, que pode ser maior depois que expressões dinâmicas são resolvidas no momento da entrega. [Leia mais](../email/create-email.md#optimize-html-proof)

* Uma nova seção **Limitações do navegador móvel** foi adicionada à página **Introdução ao design de email**, documentando por que os emails podem ser renderizados de forma diferente no Gmail ou no Outlook quando acessados por um navegador móvel, juntamente com uma dica de solução alternativa. [Leia mais](../email/get-started-email-design.md#mobile-web-limitations)

* Uma nova seção **Considerações sobre a renderização do Outlook** foi adicionada à página **Introdução ao design de email**, listando peculiaridades comuns do Outlook que devem ser consideradas durante o design: números pares para preenchimento e larguras, larguras de tabela baseadas em pixels, atributos de largura da imagem do HTML, texto ALT, bordas em células de tabela e cantos arredondados. [Leia mais](../email/get-started-email-design.md#outlook-tips)

* A página **Medidas de proteção de vida útil (TTL) dos conjuntos de dados** foi atualizada com uma tabela **Conjuntos de dados afetados** significativamente expandida, agora cobrindo todos os conjuntos de dados gerados pelo sistema do Journey Optimizer (incluindo vários não listados anteriormente, como o Serviço de Consentimento do AJO, o Perfil de Mensagens Interativas, o Perfil de Push e os conjuntos de dados de Exportação de Mensagens) juntamente com uma nova coluna **Disponibilidade** indicando se cada conjunto de dados está incluído por padrão ou se requer um complemento ou licença específica. A página **Medidas de proteção e limitações** também foi atualizada para refletir a data de imposição confirmada para esta medida de proteção: a alteração será aplicada em **sandboxes de clientes existentes** a partir de **1º de outubro de 2026**. [Leia mais](../data/datasets-ttl.md#datasets)

* Uma nova seção **Usar modo de configurações de imagem** foi adicionada à documentação de conteúdo generativo. Ela explica os modos **Balanceado**, **DAM** e **Criativo** disponíveis em **[!UICONTROL Configurações de imagem]**, que controlam se as imagens de fontes de conteúdo geradas por IA da sua biblioteca de Gerenciamento de Ativos Digitais são geradas com IA ou mescladas com ambas. [Leia mais](../content-management/generative-uc.md#image-mode)

* A descrição de **Destinos** em **Navegação à esquerda > Seções principais** foi atualizada para observar que organizações com [!DNL Real-Time CDP] ou [!DNL Adobe Journey Optimizer] também podem ativar públicos para destinos de personalização qualificados, como [!DNL Adobe Target], do catálogo de destinos do Experience Platform. [Leia mais](../start/user-interface.md#main-sections)

* Os vídeos explicativos foram adicionados à documentação Desafios de fidelidade para criar desafios, configurar provedores de recompensa e monitorar o desempenho dos desafios. [Assista aos vídeos de desafio](../loyalty-challenges/create-challenges.md#video), [assista ao vídeo do provedor de premiação](../loyalty-challenges/reward-definition-guide.md#video) e [assista ao vídeo de relatórios](../loyalty-challenges/loyalty-reporting.md#video).

## Julho de 2026 {#july-2026}

* Uma nova seção **Configurações de entrega** foi adicionada à navegação da documentação. Ela agrupa recursos relacionados à entrega que se aplicam a jornadas, campanhas e campanhas orquestradas: **Enviar usando ondas**, **Otimização de hora de envio** e **Otimização de canal** foram movidos para lá da seção Jornadas.

* As páginas separadas da documentação **Enviar usando ondas** para jornadas e campanhas de ação foram mescladas em uma única página, agora também englobando campanhas orquestradas. [Leia mais](../delivery/send-using-waves.md)

* Uma dica apontando para o artigo da comunidade da Experience League sobre **como desanexar e reingressar em nós** na nova tela de jornada foi adicionada à página **Criar sua jornada**. [Leia mais](../building-journeys/using-the-journey-designer.md)

* A seção do componente **Grade** foi adicionada à página **Componentes de conteúdo do Designer de email**. Ela permite organizar o conteúdo em uma grade estruturada de linhas e colunas, onde cada célula pode conter outros componentes de conteúdo. [Leia mais](../email/content-components.md#grid)

* A documentação da **API de Migração de Decisão** foi atualizada com um esclarecimento de que a sandbox de destino **pode ser igual à sandbox de origem**. O processo de migração trata desse cenário e garante a integridade dos dados, independentemente de os objetos serem migrados na mesma sandbox ou para uma diferente. [Leia mais](../experience-decisioning/decisioning-migration-api.md#target-sandbox-preparation)

* A documentação da **API de migração de decisão** foi aprimorada com orientação abrangente sobre como migrar objetos da Gestão de decisões para o Decisioning. As novas seções incluem: referência de mapeamento de entidade com 10 convenções de nomenclatura, cobertura dentro e fora do escopo, comparações detalhadas de modelos de solicitação/resposta, três padrões de implementação (lado do cliente, lado do servidor, híbrido) com tratamento de cookies, requisitos de rastreamento de eventos com 5 exemplos JSON de evento, pré-requisitos de migração entre sandboxes, um processo de migração completo de 5 etapas e perguntas frequentes sobre migração. [Leia mais](../experience-decisioning/decisioning-migration-api.md)

* Uma nova página **Habilidades de profissionais de CX** está disponível. Ela fornece documentação abrangente de todas as Habilidades de jornada disponíveis no Journey Optimizer, incluindo Criação de jornada, Criação de conteúdo de canal, Gerenciamento de desafio de fidelidade e Análise de jornada, com casos de uso, prompts de amostra e práticas recomendadas para cada habilidade. [Leia mais](../start/ai-features.md#cx-coworker)

* A documentação da função **Para precisão** foi atualizada para esclarecer que `toPrecision` se comporta como JavaScript `toFixed()`: ela retorna uma string com um número fixo de casas decimais, incluindo preenchimento com zeros quando necessário. [Leia mais](../personalization/functions/math.md#to-precision)

* A página **Encerrar uma jornada** foi atualizada para esclarecer o tempo de parada automático para jornadas de Leitura de público-alvo não recorrentes: um buffer de segurança de aproximadamente **96 horas (~4 dias)** após a execução agendada (janela ociosa de 24 horas + permissão para Período de silêncio de 72 horas), durante a qual a jornada pode permanecer no status **Ativa** antes da transição para **Interrompida** logo após o término do buffer. A página agora também esclarece que as jornadas baseadas em ondas (multiondas) e as jornadas que usam a Otimização de tempo de envio são excluídas dessa interrupção automática e, em vez disso, seguem o tempo limite padrão de jornada de 91 dias. [Leia mais](../building-journeys/end-journey.md#auto-stop-non-recurring)

* A página **Criar campanhas de aquecimento de IP** foi atualizada para esclarecer que as regras de direcionamento podem ser aplicadas a campanhas de aquecimento de IP e para documentar o comportamento de avaliação: a associação de público-alvo é corrigida na ativação de execução (segmentação diária em lote), enquanto os atributos de perfil são lidos no tempo de execução dos dados em lote assimilados mais recentemente. [Leia mais](../configuration/ip-warmup-campaign.md)

* Um aviso foi adicionado à página **Editar registros PTR** para informar aos clientes que, ao adicionar um novo registro DNS de encaminhamento à sua plataforma, o registro DNS de encaminhamento para o subdomínio antigo não deve ser removido até que a movimentação seja concluída, pois isso fará com que a edição falhe. [Leia mais](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

* As páginas **Enviar usando ondas** foram atualizadas para esclarecer o comportamento de reavaliação do público-alvo nas ondas: a associação do público-alvo é corrigida no momento da ativação (instantâneo), mas os atributos do perfil e o consentimento são avaliados no momento em que cada onda é processada. Isso significa que as opções de não participação que ocorrem entre ondas são respeitadas. Leia mais na [seção de perguntas frequentes](../delivery/send-using-waves.md#faq).

* A página **Governança de dados** foi atualizada para esclarecer que a imposição de política DULE se aplica somente a **campos de atributo de perfil**. Campos baseados em eventos (atributos de contexto, como campos de evento de jornada) não são compatíveis: os rótulos aplicados a esses campos na interface não restringem o uso de dados. [Leia mais](../action/action-privacy.md)

* A documentação da **Otimização de tempo de envio** foi atualizada para refletir o novo limite de **[!UICONTROL Envio na(s) próxima(s)]** de **2-100 horas** (antes entre 1-168), e para documentar as regiões de Hub da AEP com suporte para esse recurso. [Leia mais](../building-journeys/send-time-optimization.md#use-send-time-optimization)


* As páginas do **Modelo de otimização personalizado** foram atualizadas para refletir as melhorias mais recentes no modelo, abordando como o modelo de conjunto funciona, requisitos do conjunto de dados, casos de uso, premissas principais e comportamento de inicialização imediata. Leia mais nas seções [Escolha de experiências](../experience-decisioning/ranking/personalized-optimization-model.md) e [Definição de ofertas](../offers/ranking/personalized-optimization-model.md).

* Uma observação foi adicionada à página **Fórmulas de classificação de arbitragem de Jornada** para especificar que as fórmulas de classificação só estão disponíveis para organizações que compraram a oferta complementar de **Decisão**. [Leia mais](../conflict-prioritization/journey-ranking-formulas.md)

* Uma nova página de **Fragmentos dinâmicos** está disponível. Ela documenta como usar a resolução de fragmento dinâmico no [!DNL Journey Optimizer] para selecionar qual fragmento publicado é inserido em uma mensagem no tempo de execução, com base em atributos de perfil, pesquisas de conjunto de dados ou dados de contexto transmitidos no momento do envio. [Leia mais](../content-management/dynamic-fragments.md)

## Junho de 2026 {#june-2026}

* A página **Verificar e enviar mensagem de correspondência direta** foi atualizada para esclarecer o momento da exportação e o comportamento de processamento em lote da correspondência direta, incluindo o agendamento fixo de exportação às 4h UTC, o motivo pelo qual múltiplos arquivos podem ser gerados em um único dia, quando a ação **[!UICONTROL Atualizar perfil]** é executada nas jornadas e recomendações para cenários de um arquivo por dia. [Leia mais](../direct-mail/test-send-direct-mail.md#dm-export-timing)

* Uma nova página **Tipos de jornada: escolha a certa** já está disponível. Ela compara todos os pontos de entrada de jornada — Público-alvo de leitura, Qualificação de público-alvo, Evento unitário e Evento de negócios — com guias de decisão e uma matriz de compatibilidade de recursos para ajudar você a selecionar o tipo certo para seu caso de uso. [Leia mais](../building-journeys/journey-types-selection.md)

* Uma nova página **Jornadas vs. campanhas** está disponível. Ela compara Jornadas, Campanhas de ação e Campanhas acionadas por API em estilos de execução, modelos de dados e casos de uso, incluindo ativação de canal de entrada para personalização de borda de baixa latência, entrega de entrada em várias superfícies e orientação sobre quando usar campanhas orquestradas (composição de público-alvo ad-hoc, dados federados). [Leia mais](../start/journeys-vs-campaigns.md)

* A página **Modo de alta taxa de transferência** foi atualizada para refletir a disponibilidade regional expandida: o recurso agora está disponível em todas as regiões, exceto na Suíça para organizações licenciadas com o complemento de mensagens transacionais de alta taxa de transferência. [Leia mais](../campaigns/api-triggered-high-throughput.md)

* Uma nova seção **Uso de licença e perfis ativáveis** foi adicionada à página **Introdução aos perfis** como fonte única da verdade para esse conceito, com referências direcionadas adicionadas nas seções de Públicos-alvo, Campanhas e Decisão. [Leia mais](../audience/get-started-profiles.md#engageable-profiles)

* A documentação de atividade **Divisão** foi atualizada para documentar o campo **[!UICONTROL Código de segmento]**, disponível em cada configuração de subconjunto, que permite atribuir um identificador exclusivo a cada segmento de público-alvo para fins de rastreamento e relatórios. [Leia mais](../orchestrated/activities/split.md)

* A página **Configurar uma dimensão de direcionamento** foi atualizada para documentar os dois tipos de dimensão de direcionamento disponíveis em campanhas orquestradas: a **dimensão de direcionamento de perfil** integrada (nenhuma configuração é necessária) e a **dimensão de direcionamento personalizada** com base em esquemas relacionais. [Leia mais](../orchestrated/target-dimension.md)

* A documentação **Aproveitar temas em um fragmento** foi esclarecida para documentar explicitamente o limite de compatibilidade de 5 temas (incluindo a restrição de tema padrão da Adobe) e explicar que a inserção de fragmento está bloqueada quando o tema de email não é um dos temas associados ao fragmento. [Leia mais](../email/apply-email-themes.md#leverage-themes-fragment)

* As páginas **Introdução aos conjuntos de dados** e **Introdução aos esquemas** foram atualizadas com orientações sobre como ativar conjuntos de dados e esquemas para o Perfil do cliente em tempo real, incluindo considerações principais, a distinção entre desabilitar um conjunto de dados e seu esquema subjacente, e links para o planejamento da Adobe Experience Platform e a documentação de práticas recomendadas. [Saiba mais sobre conjuntos de dados](../data/get-started-datasets.md) e [Saiba mais sobre esquemas](../data/get-started-schemas.md)

* Um novo hub de integração **Introdução ao Adobe Journey Optimizer** está disponível. Novos usuários podem escolher o caminho de acordo com sua função, explorar os conceitos básicos ou ir direto para as tarefas do dia a dia, caso já tenham concluído a integração, sem precisar saber por onde começar. [Leia mais](../../rp_landing_pages/get-started-landing-page.md)

* Uma nova página **Iniciar da meta** permite começar com o que você deseja realizar, em vez de um nome de recurso. Ela mapeia metas comerciais do recurso recomendado do [!DNL Journey Optimizer] em configurações, jornadas, campanhas, personalização, decisões e relatórios. [Leia mais](../start/ajo-use-case-guide.md)

* O guia de função **Introdução para desenvolvedores** foi atualizado com introduções mais claras para cada seção e aprimorou as guias **Colaborar entre funções**, que fazem referência a jornadas e vinculam a páginas de implementação principais. [Leia mais](../start/path/developer.md)

* Uma nova subseção **Atribuição de caminho no reingresso na jornada** foi adicionada à documentação **Experimentação de caminhos**. Ela esclarece que a atribuição de caminho é persistente para um perfil em várias entradas na mesma versão da jornada, mas somente nessa versão da jornada. As atribuições são redefinidas quando uma nova versão da jornada é publicada e cada atividade de experimentação de caminho em uma jornada aplica uma atribuição aleatória independente. [Leia mais](../building-journeys/path-experimentation.md#path-assignment)
* As referências à **Adobe Experience Cloud** foram alinhadas com a marca **[!DNL Adobe CX Enterprise]** na documentação do [!DNL Journey Optimizer].

* A documentação da **`nowWithDelta()`função de data** foi atualizada para esclarecer o comportamento no fim do mês: quando o mês de destino tem menos dias do que o dia atual do mês, o resultado é ajustado para o último dia válido desse mês. [Leia mais](../building-journeys/functions/date-functions.md#nowWithDelta)

* A página **Introdução à capacidade de entrega** foi atualizada com uma nova subseção **Provedores sem FBL por destinatário**. Ela lista os principais provedores de email que não retornam reclamações de spam por destinatário — Gmail/Google Workspace, Apple iCloud e Corporate Microsoft 365/Exchange Online — e explica por que a ausência de uma entrada de lista de supressão é esperada para destinatários que usam esses serviços. [Leia mais](../reports/deliverability.md#providers-no-fbl)

* **A Escolha de experiências agora está disponível no canal de correspondência direta.** Uma nova página **Decisão em lote na correspondência direta** descreve como usar o mecanismo de tomada de decisões para personalizar arquivos de extração de correspondência direta ou exportar perfis e seus resultados de tomada de decisão para uso em sistemas downstream. A **correspondência direta** foi adicionada como um canal com suporte na documentação de Tomada de decisões (Introdução, Criar uma política de decisão, Uso de políticas de decisão em mensagens, Introdução a políticas de decisão), incluindo a capacidade de retornar vários itens de decisão por perfil através do campo **[!UICONTROL Número de itens]**. [Leia mais](../experience-decisioning/batch-decisioning-direct-mail.md)

* A documentação dos **Fragmentos de jornada** não é mais sinalizada como Disponibilidade limitada. A página agora inclui uma observação que desfaz a ambiguidade entre Fragmentos de jornada, **[!UICONTROL Fragmentos]** de conteúdo e **Fragmentos de conteúdo do AEM** (com link cruzado de todas as três páginas), e documenta o suporte para **Ferramentas de sandbox**, **Logs de auditoria** e **marcações**. Os Fragmentos de jornada também foram adicionados à página **Introdução a jornadas**. [Leia mais](../building-journeys/journey-fragments.md)

* As documentações de **Fontes de dados externas** e **Ação personalizada** foram atualizadas para autenticação personalizada. O campo `tokenInResponse` agora permite especificar se `access_token` ou `id_token` é usado como credencial de autenticação quando um ponto de acesso retorna ambos. Para a autenticação personalizada baseada em certificado, os campos `subType` e `aud` agora são obrigatórios, o ponto de acesso do token `method` deve ser `POST` e as referências à “Azure Entra ID” foram corrigidas para “Microsoft Entra ID”. [Leia mais](../datasource/external-data-sources.md#certificate-credential)

* A página **Introdução à Tomada de decisões** foi atualizada com um gráfico de processo que resume o fluxo de trabalho de Tomada de decisões de ponta a ponta, desde o gerenciamento de itens de decisão e a configuração de estratégias de seleção até a incorporação de políticas de decisão em uma jornada ou campanha. [Leia mais](../experience-decisioning/gs-experience-decisioning.md#process)

* A documentação dos **Cabeçalhos do remetente** agora esclarece que o **[!UICONTROL Nome do remetente]** e o **[!UICONTROL Email do remetente]** devem ser ambos preenchidos ou ambos deixados em branco, caso contrário, as jornadas e campanhas não poderão ser publicadas. [Leia mais](../email/header-parameters.md#sender-header)

## Maio de 2026 {#may-2026}

* As limitações e práticas recomendadas ao usar conteúdo dinâmico em fragmentos visuais foram mescladas em uma única seção **Gerenciar conteúdo condicional em fragmentos** para melhorar a legibilidade. [Leia mais](../email/use-visual-fragments.md#fragment-dynamic-content)

* Duas novas permissões de alto nível foram adicionadas: **Gerenciar registro de chaves**, que permite que os usuários exibam, criem, girem e revoguem chaves no registro de chaves, e **Exibir registro de chaves**, que permite que os usuários exibam a listagem de registro de chaves e os detalhes das chaves. [Leia mais](../administration/high-low-permissions.md#administration-permissions)

* A documentação **Usar políticas de decisão em mensagens** agora descreve como visualizar a estrutura completa de uma política de decisão a partir do resumo da campanha e copiar um resumo técnico JSON para a área de transferência com o objetivo de solucionar problemas. [Leia mais](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

* A página herdada do **Gestão de decisões**, [Modelos de otimização automática](../offers/ranking/auto-optimization-model.md), foi reescrita para se alinhar à documentação atualizada do Serviço de decisão, incluindo visão geral do aprendizado por reforço, requisitos e limitações, balanceamento entre otimização e aprendizado e detalhes sobre a amostragem de Thompson. [Leia mais](../offers/ranking/auto-optimization-model.md)

* A página **Notas de versão** foi reestruturada com um layout baseado em tópicos. As alterações agora são agrupadas por área de produto, e não por tipo de alteração, com uma nova seção **Melhorias de usabilidade** dedicada. As entradas &quot;Em breve&quot; aparecem como acordeões expansíveis em cada tópico. [Leia mais](release-notes.md)

* A página **Limitações e medidas de proteção de campanhas orquestradas** agora documenta o limite de **atividades de canal** por campanha orquestrada. [Leia mais](../orchestrated/guardrails.md#activities-limitations)

* A documentação **Copiar objetos do Journey Optimizer entre sandboxes** agora inclui uma observação importante para as **campanhas orquestradas**: após a importação, duplique a campanha na sandbox de destino e use a duplicata para execução, a fim de garantir que os relatórios capturem corretamente os dados de feedback e de rastreamento. [Leia mais](../configuration/copy-objects-to-sandbox.md#copy-to-sandbox)

* A página **Terminologia principal** foi reformulada: seis novos termos adicionados, uma nova seção **Termos de conflito e priorização** introduzida e um novo guia de desambiguação **Quando os termos parecem semelhantes** adicionado para quatro pares de termos comumente confundidos. Os termos específicos da Adobe Experience Platform foram removidos e substituídos por uma nota com um link para o glossário da Adobe Experience Platform. [Leia mais](../start/terminology.md)

* A documentação de **deep links** foi expandida com uma nova seção **Criação de deep links** detalhando as duas opções disponíveis para email (interface do Designer de email e código do Editor de personalização) e a sintaxe da função de URL para SMS. A página **Criar uma mensagem SMS** agora inclui uma etapa de deep link no fluxo de criação de conteúdo. [Leia mais](../email/deeplinks.md)

* A referência auxiliar **URL** foi atualizada com uma seção dedicada na documentação de personalização. [Leia mais](../personalization/functions/helpers.md#url)

* Uma limitação foi adicionada à documentação auxiliar **Metadados de execução**: a função não tem suporte nos canais de entrada (Web, experiência baseada em código, Mensagem no aplicativo, Cartões de conteúdo). [Leia mais](../personalization/functions/helpers.md#execution-metadata)

* Uma nova página de **Receitas de personalização** foi adicionada, oferecendo padrões de personalização prontos para uso para os casos de uso mais comuns no [!DNL Journey Optimizer]. Ela abrange receitas de data e hora (formatação de data atual, contagem regressiva para expirar, cálculos de dias anteriores, exibição apenas do tempo e detecção de fim de semana vs. dia da semana), receitas de strings (usando `replaceAll` com atribuição variável) e receitas de substituição condicional (substituições de campo vazio usando `isEmpty`). [Leia mais](../personalization/personalization-recipes.md)

* A documentação da **Sintaxe de personalização** foi atualizada com uma introdução expandida esclarecendo a diferença entre as sintaxes de Handlebars (`{{...}}`) e de PQL (`{%= ... %}`), incluindo uma tabela de uso, orientação sobre como evitar aspas duplas literais e uma nova seção **regras de sintaxe do PQL para chaves de atributos especiais** que abrange palavras-chave reservadas, chaves de atributos hifenizadas e IDs de eventos numéricos. A observação sobre o escape com um sinal grave (backtick) também foi corrigida: nomes de campos hifenizados podem ser referenciados diretamente em blocos `{{...}}`; somente a sintaxe com sinal grave falha nesse contexto. [Leia mais](../personalization/personalization-syntax.md)

* A documentação de **Funções de data e hora** foi aprimorada com novos exemplos reais: um padrão de contagem regressiva para `dateDiff`, uma condição de fim de semana vs. dia da semana para `dayOfWeek` (com uma observação sobre o uso da atividade de Condição de jornada para casos de uso de roteamento) e um padrão de exibição somente de tempo combinando `extractHours` e `extractMinutes` com um protetor de zero à esquerda. [Leia mais](../personalization/functions/dates.md)

* A documentação de **Funções de string** foi atualizada com um novo exemplo para `replaceAll` que mostra como atribuir o resultado a uma variável `{% let %}` para reutilização em várias expressões no mesmo modelo. [Leia mais](../personalization/functions/string.md#replace-all)

* A documentação das **Funções de matriz** foi atualizada com uma nova seção **Iterar sobre uma matriz** documentando o auxiliar de bloco Handlebars `{{#each}}`, incluindo uma observação esclarecendo que somente o editor de personalização oferece suporte a `{{#each}}` e que ele não pode ser usado em atividades de condição de jornada. [Leia mais](../personalization/functions/arrays-list.md#each-loop)

* A página **Introdução aos conjuntos de dados** foi atualizada com um novo item **Entrada** na seção de conjuntos de dados do sistema, documentando o _Conjunto de dados de eventos de atividade de entrada do AJO_. Adição de uma observação para esclarecer que um perfil deve ter pelo menos uma mensagem enviada de [!DNL Journey Optimizer] antes que as mensagens de entrada sejam capturadas neste conjunto de dados. [Leia mais](../data/get-started-datasets.md#system-datasets)

* A documentação **Exportar conteúdo da mensagem** foi expandida com **Perguntas frequentes sobre exportação de mensagens** (conteúdo personalizado, imagens e mídia, links rastreados, PII, retenção, casos de uso etc.) e exemplos de **JSON de amostra exportado** para SMS e email. [Leia mais](../configuration/message-export.md)

* Uma nova página de **Esquema de exportação de mensagens do AJO** documenta cada campo no Conjunto de dados de exportação de mensagens do AJO, com tipos de dados e hierarquia para o email e o conteúdo de SMS exportados. [Leia mais](../configuration/message-export-schema.md)

* Foi adicionada uma nova página **Personalizar URLs em emails**, consolidando orientações sobre personalização dinâmica de URL, personalização completa/base de URL, personalização do parâmetro de rastreamento de URL e medidas de proteção de chave. [Leia mais](../email/url-personalization.md)

* Foi adicionada uma nova seção **Consultas de regras de negócio** à página de exemplos de consulta, fornecendo uma consulta de Data Lake para verificar todos os descartes de perfil devido a exclusões de limite de frequência de jornada em uma jornada específica após uma data específica. A consulta inclui o campo `eventCodeReason` para identificar se os perfis foram excluídos por ter sido atingido um limite (`CAP_REACHED`) ou devido a uma prioridade mais baixa (`LOWER_PRIORITY`). [Leia mais](../reports/query-examples.md#business-rules-queries)

* A documentação **Propriedades da jornada** foi atualizada para documentar o novo indicador **Tamanho atual do conteúdo da jornada** no painel de propriedades da jornada. Este campo somente leitura mostra o tamanho atual do conteúdo útil da jornada em comparação ao limite configurado (por exemplo, 1,5 MB de 2 MB), ajudando a monitorar a complexidade da jornada antes da publicação e a evitar erros de publicação relacionados ao tamanho. [Leia mais](../building-journeys/journey-properties.md#journey-payload-size)

## Abril de 2026 {#april-2026}

* A documentação da atividade **Mudar dimensão** foi atualizada para esclarecer que, embora a atividade use uma associação externa e mantenha todos os registros na etapa de alteração de dimensão, os registros sem um perfil correspondente na nova dimensão de direcionamento são excluídos silenciosamente no momento da entrega da mensagem. [Leia mais](../orchestrated/activities/change-dimension.md)

* As medidas de proteção na documentação **Adicionar um campo CC a emails** foram aprimoradas. Agora, eles especificam que o endereço CC não é verificado em relação ao consentimento ou à supressão, e que as aberturas e click-throughs de emails enviados para o endereço CC são consideradas no total de aberturas e cliques da análise de envio. [Leia mais](../configuration/cc-email-field.md)

* A documentação das **Atividades de canal** foi atualizada com uma nova seção **Mensagens de marketing vs. transacionais** que explica as diferenças de comportamento entre as duas categorias de canal: requisitos de aceitação, aplicativo de regra de negócios, tipo de configuração de canal e casos de uso recomendados. [Leia mais](../orchestrated/activities/channels.md#marketing-vs-transactional)

* A documentação da **Atividade de bifurcação** foi aprimorada com uma nova seção **Exemplos** que ilustra como usar a atividade de bifurcação para dividir um público-alvo em duas ramificações de email paralelas — uma de Marketing e outra Transacional — em uma única execução de campanha. [Leia mais](../orchestrated/activities/fork.md#fork-examples)

* A documentação **Criar atividade de público-alvo** foi aprimorada com um novo exemplo que mostra como filtrar perfis por um atributo de plano de assinatura usando o construtor de regras. [Leia mais](../orchestrated/activities/build-audience.md#build-audience-examples)

* A página **Introdução às Campanhas orquestradas** documenta o padrão de nível de entrada **Criar público-alvo → Bifurcação → Canal A + Canal B** em **O que há dentro de uma Campanha orquestrada?**, com referências cruzadas à atividade de Bifurcação e páginas de mensagens de Marketing vs. Transacionais. [Leia mais](../orchestrated/gs-orchestrated-campaigns.md#gs-ms-campaign-inside)

* A página **Editar conteúdo de email com o editor avançado de HTML** foi movida da seção Gerenciamento de conteúdo para a seção **Email** da documentação. A página agora documenta que o editor avançado de HTML está disponível no Designer de email para mensagens de email, bem como para modelos de conteúdo de email. [Leia mais](../email/email-expert-mode.md)

* A documentação **Iniciar e monitorar campanhas orquestradas** foi atualizada com uma nova seção que detalha a sequência de execução interna do tempo de publicação, juntamente com uma tabela de status do ciclo de vida da campanha, uma lista de verificação de pré-publicação e um aviso de confirmação de envio para campanhas não recorrentes. [Leia mais](../orchestrated/start-monitor-campaigns.md#publication-sequence)

* A documentação da atividade **Salvar público-alvo** foi atualizada com uma observação esclarecendo que as atividades Salvar público-alvo sempre são executadas antes das atividades de mensagem no momento da publicação. [Leia mais](../orchestrated/activities/save-audience.md)

* Três novas perguntas e respostas foram adicionadas às **Perguntas frequentes sobre campanhas orquestradas**: o que acontece internamente no momento da publicação, uma lista de verificação de 7 motivos pelos quais as mensagens podem não ser enviadas após a publicação e como a pesquisa de instantâneo de perfil difere da resolução de perfil em tempo real. [Leia mais](../orchestrated/orchestrated-campaigns-faq.md)

* Uma nova seção **[Eventos descartados devido a uma instância de jornada bloqueada](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)** foi adicionada à documentação de solução de problemas da jornada, explicando o motivo do descarte do `maxInstanceStackEventsReached`, quando ele ocorre e como atenuá-lo. As medidas de proteção e as páginas de lista de campos de evento de etapa também foram atualizadas adequadamente.

* A documentação **Aproveitar fragmentos nas políticas de decisão** agora inclui notas de medidas de proteção para o canal **Email**: **[!UICONTROL Simular conteúdo]** não exibe fragmentos de expressão do item de decisão, enquanto que **[!UICONTROL Enviar prova]** e as campanhas ativadas exibem. A página também declara que **[!UICONTROL fragmentos visuais]** não podem ser atribuídos a um item de decisão — somente **fragmentos de expressão** são aceitos neste contexto. [Leia mais](../experience-decisioning/fragments-decision-policies.md)

## Março de 2026 {#march-2026}

* A documentação de **visualização de experiências baseadas em código com a Escolha de experiências** agora esclarece que **[!UICONTROL Simular conteúdo]** é somente para visualização de conteúdo. Os dados de contexto de solicitações do Edge em tempo real não são simulados na pré-visualização de criação. [Leia mais](../code-based/test-code-based.md#preview-code-based)

* A documentação **Usar dados da Adobe Experience Platform** foi atualizada: as medidas de proteção não indicam mais que as pesquisas de conjunto de dados não podem ser encadeadas, refletindo o comportamento atual do produto. [Leia mais](../data/lookup-aep-data.md)

* A documentação da atividade **Atualizar perfil** foi atualizada para documentar o suporte à atualização de até cinco atributos de perfil em uma única ação. [Leia mais](../building-journeys/update-profiles.md)

* A documentação da atividade **Ler público-alvo** e das **Propriedades da jornada** foi atualizada para esclarecer o ciclo de vida de jornada de 91 dias para jornadas recorrentes sempre ativas. A seção de programação agora confirma explicitamente que as jornadas recorrentes sem data final permanecem ativas após 91 dias, e as perguntas frequentes sobre tempo limite global foram expandidas para distinguir o TTL de 91 dias do perfil da janela de relatório de 91 dias. [Leia mais](../building-journeys/read-audience.md#schedule)

* A documentação da atividade **Pesquisa de conjunto de dados** foi atualizada para esclarecer que a chave de pesquisa deve ser configurada no modo avançado para que a sintaxe `@datasetLookup{}` funcione em atividades de condição downstream. Uma seção de solução de problemas foi adicionada com orientação sobre como resolver o erro “Pesquisa de conjunto de dados não encontrada”. [Leia mais](../building-journeys/dataset-lookup.md#troubleshooting)

* A documentação de **Funções de data e hora** foi atualizada com um novo exemplo que mostra como formatar um carimbo de data e hora a partir de um atributo de evento de contexto, incluindo o requisito `toDateTime()`, a sintaxe de backtick para IDs de evento numéricas e uma chamada de erro comum para o erro “entrada incompatível” do PQL. [Leia mais](../personalization/functions/dates.md#format-date)

* As documentações **Medidas de proteção e limitações de campanhas orquestradas** e **Introdução aos conectores de origem** foi atualizada para esclarecer que, para a captura de dados de alteração baseada em arquivo, o campo `_change_request_type` é obrigatório e seus valores devem estar em letras minúsculas `u` (substituição) ou `d` (exclusão), e não em letras maiúsculas. [Leia mais](../orchestrated/guardrails.md)

* A documentação **Adicionar links e rastrear mensagens** foi atualizada com orientações sobre como os identificadores de rastreamento (urlID) são gerados: uma urlID exclusiva só é atribuída quando o URL e o rótulo são exclusivos. Para rastrear o mesmo URL em vários emails (ou várias vezes em um email), os usuários devem usar um rótulo exclusivo para cada URL semelhante; caso contrário, o [!DNL Journey Optimizer] não pode determinar qual link foi clicado. [Leia mais](../email/message-tracking.md#track-across-multiple-emails)

* A documentação **Criar perfis de teste** foi atualizada com uma observação importante sobre os requisitos do descritor de identidade: quando um conjunto de dados é excluído e recriado, o esquema deve manter o descritor de identidade correto no campo de identidade principal. Sem ela, os perfis ingeridos não são sinalizados como `testProfile = true` mesmo que a ingestão seja concluída com êxito. Uma lista de verificação de solução de problemas foi adicionada. [Leia mais](../audience/creating-test-profiles.md)

* A documentação da atividade **Ler público-alvo** foi atualizada para esclarecer que uma atividade **Evento de negócios** é uma exceção à regra de que Ler público-alvo deve ser a primeira atividade em uma jornada. Uma observação também foi adicionada referenciando a atividade **Otimizar** como uma alternativa avançada para controlar o direcionamento de público-alvo. [Leia mais](../building-journeys/read-audience.md)

* **Enviar usando ondas** em jornadas agora está disponível. O sinalizador de Disponibilidade limitada foi removido da documentação. [Leia mais](../delivery/send-using-waves.md)

* A documentação da atividade **Saltar** foi aprimorada com uma nova seção de estratégia de design — **Subjornadas de tamanho reduzido** — explicando como dividir fluxos completos complexos em subjornadas menores e focadas conectadas por meio da atividade Saltar. [Leia mais](../building-journeys/jump.md#jump-strategy)

* A documentação de **Tags** foi atualizada com orientações sobre o uso de categorias de tag como uma alternativa às convenções de nomenclatura complexas. Uma nova seção explica como configurar categorias de tags para um gerenciamento de jornada escalável. [Leia mais](../building-journeys/tags.md)

* A documentação **Sobre fontes de dados** agora inclui uma nova seção que ajuda os profissionais a escolher entre três estratégias de acesso a dados: acessar dados externos por meio de ações personalizadas, usar um conjunto de dados não habilitado para perfil ou usar um conjunto de dados habilitado para perfil. Cada opção é descrita com variações e casos de uso recomendados. [Leia mais](../datasource/about-data-sources.md#data-access-strategy)

* A documentação de **Design de notificação por push** foi atualizada com uma observação esclarecendo o comportamento de links universais no iOS: se o URL de notificação for registrado como um link universal, o aplicativo associado será aberto independentemente da ação de URL da Web escolhida. Foram adicionadas orientações sobre como forçar a abertura de um navegador. [Leia mais](../push/design-push.md)

* Uma nova página **Monitorar modelos de IA** está disponível na documentação da Decisão. Ela explica como rastrear a integridade, o status do treinamento e o desempenho de modelos de otimização personalizados diretamente no [!DNL Journey Optimizer]. [Leia mais](../experience-decisioning/ranking/ai-model-observability.md)

* O **Editor avançado de HTML** (modo especialista) para modelos de email agora está em Disponibilidade limitada. A página de documentação agora está acessível publicamente. Esse recurso permite visualizar e editar a fonte de HTML bruta de modelos de conteúdo de email diretamente no Designer de email. [Leia mais](../email/email-expert-mode.md)

* A documentação de **Rastreamento de URL** e **Solução de problemas de jornada** foi atualizada para documentar o comportamento de `context.system.source.actionId` em jornadas fechadas. Jornadas fechadas ou não republicadas podem produzir espaços reservados `{}` vazios nos URLs de rastreamento. Foram adicionadas orientações sobre como resolver o problema republicando a jornada ou removendo o parâmetro afetado. [Leia mais](../email/url-tracking.md)

* A documentação da **Fonte de dados da Adobe Experience Platform** foi atualizada com uma observação de que somente esquemas baseados em perfil individual XDM são aceitos na configuração da fonte de dados. [Leia mais](../datasource/adobe-experience-platform-data-source.md)

* A documentação de **Medidas de proteção de tempo de vida (TTL) de conjuntos de dados** foi aprimorada com uma nova entrada de Perguntas frequentes para identificar claramente quais conjuntos de dados estão sujeitos ao TTL. O TTL aplica-se exclusivamente a conjuntos de dados de séries temporais — conjuntos de dados de tipo de registro, como conjuntos de dados de entidades, conjuntos de dados de classificação e repositórios de objetos de decisão, não estão sujeitos ao TTL e não serão afetados pela implantação da medida de proteção. [Leia mais](../data/datasets-ttl.md)

* A documentação de **Propriedades de jornada** e **Pausar uma jornada** foi atualizada para documentar os novos campos de pausa e retomada disponíveis nos detalhes técnicos da jornada. O botão **Copiar detalhes técnicos** agora inclui `lastPausedAt`, `lastPausedBy`, `lastPausedById`, `lastResumedAt`, `lastResumedBy` e `lastResumedById`, além do bloco `pausedJourneySettings` existente. Uma nova seção também foi adicionada à página **Pausar uma jornada** explicando como exibir os carimbos de data e hora de pausa e retomada diretamente das propriedades da jornada. [Leia mais](../building-journeys/journey-properties.md)

## Fevereiro de 2026 {#february-2026}

* Uma nova página está disponível para a Gestão de decisões. Ela lista todos os operadores, auxiliares e funções compatíveis ao personalizar o conteúdo da oferta (representações) com o editor de personalização. Use esta lista para evitar erros de tempo de execução. Somente as funções documentadas são compatíveis ao personalizar conteúdo na Definição de ofertas. [Leia mais](../offers/offer-library/personalization-editor-supported-functions.md)

* A documentação **Criar políticas de decisão** e **Usar políticas de decisão em mensagens** foi atualizada para Email: uma observação agora explica que quando a mesma oferta pode ser selecionada por mais de uma política de decisão no corpo do email, o mecanismo desduplica as ofertas (cada posicionamento recebe uma oferta diferente). Para exibir a mesma oferta em vários posicionamentos (por exemplo, cabeçalho e rodapé), use **Reutilizar saída de decisão**. [Leia mais](../experience-decisioning/create-decision-policy.md)

* A página Itens de decisão foi atualizada com informações sobre Canal de push e Limite de evento personalizado. [Leia mais](../experience-decisioning/items.md#capping)

* A **Pesquisa de evento de experiência em jornadas** foi atualizada com a linha do tempo de descontinuação: a partir de 1º de abril de 2026, as organizações que não tiverem usado atributos de evento de experiência em expressões de jornada nos últimos 90 dias não terão mais acesso a esse recurso. As Perguntas frequentes agora se concentram na linha do tempo de descontinuação e em quem é afetado, e a página Esquema de evento de experiência foi alinhada com um link direto para abordagens alternativas. [Leia mais](../building-journeys/exp-event-lookup.md)

* A documentação da **Decisão** foi atualizada para a **pesquisa de conjunto de dados** com dados da Adobe Experience Platform: a medida de proteção de canais compatíveis agora declara que a pesquisa de conjunto de dados funciona para todos os canais em que a Decisão está disponível (experiência baseada em código, email, push, SMS e atividade de Decisão de conteúdo em jornadas). A disponibilidade limitada e as notas beta públicas foram removidas das páginas de regras de decisão, fórmulas de classificação e itens de decisão. [Leia mais](../experience-decisioning/aep-data-exd.md)

* A página Integração de sistemas externos foi atualizada com links para fontes de dados personalizadas e ações personalizadas, e esclarece que o proxy de saída fornece um IP estático para chamadas de saída de **Ações personalizadas** para seus sistemas externos. [Leia mais](../configuration/external-systems.md)

* A documentação de Execução de teste de jornada foi esclarecida: os atributos de evento de etapa `inDryRun` e `dryRunID` agora documentam o retorno de `true`/ID de instância quando estão no modo de Execução de teste e `null` para jornadas de teste ou ativas. As orientações para excluir eventos de etapa de Execução de teste em consultas de relatório foram atualizadas adequadamente. [Leia mais](../building-journeys/journey-dry-run.md)

* **Push da Web** agora está disponível a todos. A documentação de notificação por push foi reestruturada e atualizada adequadamente (começar, projetar, enviar, criar). [Leia mais](../push/get-started-push.md)

* A página de configuração de push da Web agora está disponível na documentação. [Leia mais](../push/push-configuration-web.md)

* A documentação sobre o uso de fragmentos na Decisão foi atualizada: notas foram adicionadas nas seções Fragmentos e Decisão, e a página Fragmentos em políticas de decisão foi atualizada. [Leia mais](../experience-decisioning/fragments-decision-policies.md)

* A documentação do webhook de SMS foi atualizada: o conteúdo do webhook do Twilio foi removido. [Leia mais](../mobile/mobile-webhook.md)

* A documentação **Converter imagens em modelos de conteúdo** foi aprimorada com medidas de proteção e recomendações expandidas, casos de uso comuns e orientações mais claras para converter designs de imagem em modelos de conteúdo editáveis de HTML. Também menciona o fato de que agora você pode usar um tema como entrada para a conversão. [Leia mais](../content-management/image-to-html.md)

* A documentação da API de migração da Decisão foi atualizada. [Leia mais](../experience-decisioning/decisioning-migration-api.md)

* A atividade **Decisão de conteúdo** agora está disponível. A página de atividade Decisão de conteúdo foi atualizada com uma seção sobre Dados de decisão disponíveis nos eventos de etapa. [Leia mais](../building-journeys/content-decision.md)

* Links para a documentação da API de desafio de fidelidade foram adicionados à seção Desafios de fidelidade (começar, criar desafios, criar tarefas, acessar desafios de fidelidade). [Leia mais](../loyalty-challenges/get-started.md)

* As informações de canais compatíveis na documentação do assistente de criação de campanha foram corrigidas. As páginas de perguntas frequentes sobre Introdução aos canais e Campanhas orquestradas foram atualizadas adequadamente. [Leia mais](../campaigns/get-started-with-campaigns.md)

* A documentação de permissões foi corrigida com relação às permissões **Gerenciar** e **Aprovar**. jornadas. [Leia mais](../administration/ootb-permissions.md)

* A documentação de integrações do AEM (Adobe Experience Manager) foi atualizada com nomes revisados (conteúdo dinâmico do AEM e fragmentos do AEM). [Leia mais](../integrations/aem-fragments.md)

* Um novo motivo de exclusão foi adicionado à lista de exclusões: **UnsubscribeLinkNotValid** (código de erro 050081). Esta exclusão é gerada quando o comprimento do assunto do mailTo do List-Unsubscribe é maior que o limite de 998 caracteres definido pela RFC. [Leia mais](../reports/exclusion-list.md)

* A documentação da função auxiliar formatDate foi aprimorada com uma observação de que a função requer um tipo de campo de data-hora (não uma string) e com vários exemplos: formatação de um campo de data-hora, conversão de uma string em data primeiro, data completa com nome de dia, data dinâmica a partir da hora do sistema e formato de dia da semana, incluindo resultado em minúsculas. [Leia mais](../personalization/functions/dates.md#format-date)

* A documentação de email em formato de texto foi aprimorada com orientações abrangentes sobre casos de uso, incluindo critérios de decisão para quando usar texto simples personalizado em vez de sincronização automática, exemplos práticos com cenários do mundo real e uma seção de perguntas frequentes com dúvidas comuns. [Leia mais](../email/text-version-email.md#when-to-use)

* A documentação dos temas do Designer de email foi atualizada com informações sobre as limitações de suporte a fontes da web e a importância de fontes alternativas. [Leia mais](../email/apply-email-themes.md#themes-guardrails)

* Uma limitação foi adicionada à documentação de ajuda Metadados de execução para esclarecer que os metadados não são capturados de perfis excluídos da ação. [Leia mais](../personalization/functions/helpers.md#execution-metadata)

* A documentação de amostras de implementação baseada em código foi atualizada para incluir o campo de tokens na propositionAction para rastreamento e atribuição precisos na Decisão. [Leia mais](../code-based/code-based-implementation-samples.md#client-side-how)

* Uma observação foi adicionada à documentação de rastreamento de URL e cancelamento de assinatura de lista para esclarecer que a ordem dos parâmetros de rastreamento de URL anexados aos URLs é aleatória e não pode ser controlada. [Leia mais](../email/url-tracking.md)

## Janeiro de 2026 {#january-2026}

* A documentação do painel de uso da licença foi esclarecida com orientações atualizadas sobre os **Perfis engajáveis**, incluindo detalhes de definição e orientações para solução de problemas. [Leia mais](../audience/license-usage.md#what-is-engageable-profile)

* Uma observação foi adicionada à documentação de temas do Designer de email para esclarecer as limitações de suporte a fontes da Web. [Leia mais](../email/apply-email-themes.md#themes-guardrails)

* Uma nova seção de proteção foi adicionada ao documento validação do tamanho do conteúdo da jornada, incluindo limites de aviso e erro e orientação sobre como otimizar as jornadas. [Leia mais](../start/guardrails.md#journey-payload-size)

* A documentação de medidas de proteção do Decisioning foi atualizada para incluir limitações de tamanho de itens de decisão (1 KB para itens que incluem atributos com no máximo 30 atributos). [Leia mais](../experience-decisioning/decisioning-guardrails.md)

* Uma observação foi adicionada à documentação de criação de políticas de decisão para informar aos usuários que, uma vez criada uma política de decisão, qualquer alteração poderá levar até 15 minutos para se propagar em todas as regiões de dados e até 30 minutos para o Canadá. [Leia mais](../experience-decisioning/create-decision-policy.md#review)

* Uma observação foi adicionada à documentação de fragmentos para avisar que quando o rótulo do botão e o URL se tornam editáveis em um fragmento, o conjunto de dados de rastreamento registra o valor do URL em vez do valor do rótulo. [Leia mais](../content-management/customizable-fragments.md#visual)

* Uma nova página está disponível descrevendo os benefícios da migração da Gestão de decisões para o Decisioning, incluindo informações sobre as próximas APIs de ferramentas de migração. [Leia mais](../experience-decisioning/migrate-to-decisioning.md)

* Adição de uma medida de proteção para esclarecer que os conjuntos de dados de pesquisa estão disponíveis para ativação baseada na borda de entrada somente na região em que a sandbox do conjunto de dados reside. [Leia mais](../data/lookup-aep-data.md#guidelines)

* Uma nova seção foi adicionada à documentação de configuração de canais de Campanhas orquestradas explicando como usar atributos contextuais (como ID da campanha, nome e detalhes de ação) em parâmetros de rastreamento de URL para fins de análise e relatórios. [Leia mais](../orchestrated/channel-config.md#url-tracking)

* A documentação de otimização de conteúdo foi reestruturada para oferecer mais clareza. A página de otimização principal foi dividida em quatro subpáginas focadas: uma página de introdução, uma página dedicada ao direcionamento, uma para experimentação e outra para combinação de ambas as abordagens. [Leia mais](../content-management/gs-message-optimization.md)

* As notas de Disponibilidade limitada foram removidas dos três alertas de jornada (Jornada publicada, Jornada concluída e Limite de ação personalizada acionado), pois esses recursos agora estão disponíveis. [Leia mais](../reports/alerts.md)

* A página de destino Testar, validar e aprovar foi aprimorada com novas seções, incluindo: visão geral dos recursos de teste, perguntas frequentes comuns, árvore de decisão com links de navegação e terminologia aprimorada com links da documentação. [Leia mais](../../rp_landing_pages/test-landing-page.md)

* Uma nova seção foi adicionada à documentação da sintaxe de personalização para esclarecer como usar palavras-chave reservadas em expressões de personalização. Determinadas palavras-chave no PQL, como `next`, `last` e `this`, devem ser delimitadas com sinal grave quando usadas como nomes de campo no esquema XDM. [Leia mais](../personalization/personalization-syntax.md#reserved-keywords)

* As páginas [Introdução às campanhas](../campaigns/get-started-with-campaigns.md) e [Gerenciar campanhas](../campaigns/manage-campaigns.md) foram reestruturadas com uma arquitetura de informações aprimorada, incluindo um fluxo de trabalho abrangente com guias específicos de tipo, comparações aprimoradas de tipos de campanha e uma tabela de status consolidada.

* A página de destino Jornadas foi reprojetada para facilitar a integração com um novo fluxo de trabalho de 6 etapas, comparações melhoradas de tipos de jornada e a navegação aprimorada em toda a documentação. [Leia mais](../building-journeys/journey.md)

* Uma seção detalhada foi adicionada para ajudar os usuários a gerar chaves privadas OpenSSH codificadas em Base64 para autenticação SFTP ao configurar o roteamento de arquivos para Correspondência direta, evitando erros de conexão. [Leia mais](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* Uma observação foi adicionada à documentação de delegação de subdomínio para orientar os usuários a permitir a propagação de DNS por 24 a 48 horas antes da tentativa de delegação à Adobe. [Leia mais](../configuration/delegate-subdomain.md#set-up-subdomain)
