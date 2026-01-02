---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a jornadas
description: Introdução a jornadas
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: jornada, descobrir, introdução
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 87351e845c7a6267cc78c26c838e69e77325f2b8
workflow-type: tm+mt
source-wordcount: '1420'
ht-degree: 3%

---


# Introdução a jornadas{#jo-general-principle}

O Adobe Journey Optimizer permite criar jornadas personalizadas e em várias etapas para o cliente, que se adaptam em tempo real ao comportamento e às necessidades do seu público-alvo. Usando uma tela intuitiva de arrastar e soltar, você pode orquestrar mensagens e ações em vários canais, aproveitando dados contextuais e o direcionamento de público-alvo para obter o máximo impacto.

Este guia fornece um roteiro claro para ajudá-lo a entender os fundamentos de jornada, escolher o tipo de jornada certo para o seu caso de uso e criar com confiança jornadas que proporcionem experiências significativas e oportunas ao cliente.

## O que são jornadas?

jornada **As** são experiências automatizadas e em várias etapas do cliente que organizam interações personalizadas entre canais em resposta ao comportamento do cliente, eventos comerciais ou campanhas programadas.

Use [!DNL Journey Optimizer] para:

* Crie casos de uso de **orquestração em tempo real** usando dados contextuais armazenados em eventos ou fontes de dados
* Crie **cenários avançados com várias etapas** que respondam dinamicamente ao comportamento do cliente e aos eventos comerciais
* Forneça **1:1 experiências personalizadas** em escala por email, push, SMS, no aplicativo, Web e muito mais

![Interface do designer do Jornada com paleta, tela e painel de propriedades](assets/journey38.png)

➡️ **Pronto para começar a criar?** [Crie sua primeira jornada](journey-gs.md) em 5 minutos.

## Escolha seu tipo de jornada {#journey-types}

**Antes de começar a criar**, é importante entender que tipo de jornada se adapta ao seu caso de uso. A Adobe Journey Optimizer oferece suporte a quatro tipos de jornadas, cada uma projetada para diferentes mecanismos de entrada e cenários de negócios:

>[!BEGINTABS]

>[!TAB jornadas unitárias]

**Quando usar:** experiências acionadas por eventos em tempo real

As **jornadas unitárias** são acionadas individualmente quando ocorre uma ação específica (compra, entrada no aplicativo, envio de formulário). Os perfis são inseridos um de cada vez em tempo real, tornando-os ideais para respostas imediatas e orientadas por comportamento.

**Perfeito para:**

* Confirmações de pedidos após a compra
* Emails de boas-vindas quando alguém assinar
* Abandono do carrinho acionado pela navegação
* Notificações de redefinição de senha

➡️ [Saiba mais sobre eventos](../event/about-events.md) | [Caso de uso de mensagem para assinantes](message-to-subscribers-uc.md)

>[!TAB Ler jornadas de Público-Alvo]

**Quando usar:** campanhas agendadas para segmentos de público-alvo

**Ler jornadas de Público-Alvo** comece com um público-alvo da Adobe Experience Platform e envie mensagens em lote para todos os perfis simultaneamente. Esse tipo de jornada é ideal para comunicações programadas em larga escala.

**Perfeito para:**

* Boletins informativos mensais
* Campanhas promocionais para segmentar segmentos
* Anúncios de produto
* Campanhas de marketing sazonais

➡️ [Saiba mais sobre a Leitura de Público](read-audience.md) | [Introdução aos públicos-alvo](../audience/about-audiences.md)

>[!TAB jornadas de qualificação de público-alvo]

**Quando usar:** respostas em tempo real para alterações de associação de público-alvo

**As jornadas de qualificação de público-alvo** são acionadas quando os perfis se qualificam para (ou saem de) um público-alvo específico. Os perfis entram individualmente, pois atendem aos critérios em tempo real, permitindo envolvimento imediato quando o comportamento do cliente muda.

**Perfeito para:**

* Notificações de atualização de nível do VIP
* Reengajamento quando os clientes se tornam inativos
* Mensagens de celebração da primeira compra
* Direcionamento geográfico quando os clientes se movem

➡️ [Saiba mais sobre a qualificação de público-alvo](audience-qualification-events.md) | [Criando públicos-alvo](../audience/creating-a-segment-definition.md)

>[!TAB jornadas de eventos comerciais]

**Quando usar:** Condições comerciais que afetam vários clientes

As **jornadas de eventos comerciais** são acionadas por eventos comerciais (atualizações de ações, alertas meteorológicos, alterações de preço) que afetam vários perfis simultaneamente. Elas respondem a condições empresariais mais amplas, em vez de ações individuais.

**Perfeito para:**

* Alertas de baixo inventário para clientes interessados
* Anúncios de venda do Flash
* Promoções baseadas no clima
* Notificações de queda de preço
* Alertas de produtos devolvidos ao estoque

➡️ [Saiba mais sobre eventos comerciais](../event/about-creating-business.md) | [Gerenciamento de entradas](entry-management.md)

>[!ENDTABS]

>[!NOTE]
>
>Não tem certeza de qual tipo escolher? Comece com **jornadas unitárias** para experiências baseadas em eventos ou **Leia jornadas de público-alvo** para campanhas agendadas, que abrangem os casos de uso mais comuns.

## Criar com o designer do jornada {#journey-designer}

O **[Designer do jornada](using-the-journey-designer.md)** é sua tela visual para criar experiências do cliente. Com uma interface intuitiva de arrastar e soltar, você pode orquestrar cada etapa da jornada sem escrever código.

![Interface do designer do Jornada com paleta, tela e painel de propriedades](assets/journey38.png)

### O que você pode fazer no designer:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Definir pontos de entrada**

Escolha como os clientes entram: por meio de um evento, segmento de público ou qualificação de público.

[Saiba mais sobre gerenciamento de entradas](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Envio de mensagens**

Use ações de canal integradas para email, push, SMS/MMS, no aplicativo, Web e muito mais, tudo projetado no Journey Optimizer.

[Enviar mensagens no jornada](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Adicionar lógica e condições**

Ramifique sua jornada com base em atributos de perfil, associação de público ou eventos em tempo real.

[Condições de uso](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Aproveitar dados**

Use dados contextuais de eventos, Adobe Experience Platform ou serviços de API de terceiros.

[Trabalhar com fontes de dados](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Conectar sistemas externos**

Crie ações personalizadas para integrar sistemas de terceiros para enviar mensagens ou acionar workflows.

[Configurar ações personalizadas](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Adicionar atividades de orquestração**

Use tempos de espera, saltos, atualizações de perfil e gerenciamento de público-alvo para criar fluxos sofisticados.

[Explorar todas as atividades](about-journey-activities.md)
:::

::::

➡️ **Aprendizado prático:** [Assista ao vídeo do designer do jornada](#video) ou [explore casos de uso completos](jo-use-cases.md)

## Seu fluxo de trabalho de criação de jornadas {#workflow}

A criação de jornadas bem-sucedidas segue um processo claro e repetível. Este é o seu fluxo de trabalho passo a passo:

**1. Plano** → **2. Design** → **3. Teste** → **4. Publicar** → **5. Monitor** → **6. Otimizar**

### &#x200B;1. **Planeje sua jornada** {#plan}

Antes de abrir o designer, esclareça seus objetivos:

* **Qual é a meta?** (por exemplo, integrar novos clientes, reengajar usuários inativos)
* **Quem é o público-alvo?** (segmento específico, indivíduos orientados por eventos)
* **Que tipo de jornada se encaixa?** (Consulte [tipos de jornada](#journey-types) acima)
* **Quais canais você usará?** (email, push, SMS etc.)

### &#x200B;2. **Design na tela** {#design}

Use o designer de jornadas para criar o fluxo:

1. **Definir condições de entrada** - Defina como os perfis entram (evento, público-alvo, qualificação)
2. **Adicionar lógica de orquestração** - Incluir tempos de espera, condições e pontos de decisão
3. **Configurar mensagens** - Projete suas comunicações ou use modelos existentes
4. **Configurar ações** - Configurar ações integradas ou personalizadas para execução
5. **Definir critérios de saída** - Especifique quando e como os perfis concluem a jornada

[Saiba como usar o designer de jornadas →](using-the-journey-designer.md)

### &#x200B;3. **Testar antes de entrar em funcionamento** {#test}

Sempre teste sua jornada para detectar problemas antes que os clientes os enfrentem:

* Usar **modo de teste** para simular a jornada com perfis de teste
* Use **dry run** para visualizar a execução da jornada sem afetar os dados reais ou enviar mensagens
* Verifique se todas as condições, mensagens e ações funcionam conforme esperado
* Verificar tempo, fluxos de dados e personalização

[Testar sua jornada →](testing-the-journey.md) | [Saiba mais sobre simulação →](journey-dry-run.md)

### &#x200B;4. **Publicar sua jornada** {#publish}

Quando o teste for concluído, publique para ativar sua jornada:

* Revisar configurações e propriedades finais
* Publicar para ativar para clientes reais
* Observação: o Live jornada pode ser interrompido, mas não editado (você deve criar uma nova versão)

[Publicar sua jornada →](publish-journey.md)

### &#x200B;5. **Monitorar desempenho** {#monitor}

Rastreie o desempenho de sua jornada no mundo real:

* Exibir relatórios e análises do jornada
* Monitorar as taxas de entrada, conclusão e erro
* Configurar alertas para problemas críticos

[Monitorar e relatar →](report-journey.md) | [Configurar alertas →](../reports/alerts.md)

### &#x200B;6. **Otimizar e iterar** {#optimize}

Use insights para melhorar:

* Analisar métricas de envolvimento e taxas de conversão
* Testar otimização de tempo de envio
* Criar novas versões do jornada com melhorias
* Usar recomendações alimentadas por IA

[Otimizar suas jornadas →](optimize.md) | [Otimização de hora de envio →](send-time-optimization.md)

➡️ **Pronto para começar?** [Criar sua primeira jornada agora →](journey-gs.md)

## Casos de uso reais {#use-cases}

Aprenda com exemplos práticos que demonstram como aplicar conceitos de jornada para resolver desafios de marketing comuns:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Bem-vindo(a) aos novos assinantes**

Quando um cliente assinar seu serviço, acione uma jornada de boas-vindas que o incentive a concluir as etapas de integração.

[Exibir caso de uso →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Otimização de hora de envio**

Use a IA para enviar emails quando cada cliente tiver maior probabilidade de se envolver, maximizando as taxas de abertura e de clique.

[Exibir caso de uso →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Aumentar entregas**

Aumente gradualmente o volume de mensagens para aquecer a reputação de envio e evitar problemas de capacidade de delivery.

[Exibir caso de uso →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Direcionar por dia da semana**

Envie conteúdo diferente com base no dia da semana em que os clientes digitam sua jornada para melhor relevância.

[Exibir caso de uso →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Campanhas multicanais**

Orquestrar experiências perfeitas em canais de email, push, SMS e Web em uma única jornada.

[Exibir caso de uso →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Todos os casos de uso**

Explore a biblioteca completa de casos de uso do jornada com implementações passo a passo.

[Procurar tudo →](jo-use-cases.md) | [Biblioteca de casos de uso →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Explorar recursos do jornada {#capabilities}

À medida que se sentir mais confortável com a criação de jornadas, explore esses recursos avançados para criar experiências sofisticadas para o cliente:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Expressões avançadas**

Crie condições dinâmicas e personalização usando o editor de expressão para manipulação de dados e lógica complexa.

[Saiba mais sobre expressões](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**Gerenciamento de fuso horário**

Lidar com públicos globais com ajustes automáticos de fuso horário e tempos de envio ideais.

[Gerenciar fusos horários](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Modo de teste e simulação**

Valide jornadas com perfis de teste antes de entrar em funcionamento e visualize a execução sem afetar os dados reais.

[Usar simulação](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Copiar para sandbox**

Duplique jornadas em sandboxes para simplificar os fluxos de trabalho de teste e implantação.

[Copiar jornadas](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Marcas e organização**

Use tags para categorizar e filtrar jornadas para melhorar o gerenciamento em escala.

[Organizar com tags](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Controle de taxa de transferência**

Limite a taxa de transferência de mensagens para gerenciar a reputação de envio e evitar a sobrecarga dos sistemas.

[Controlar taxa de transferência](limit-throughput.md)
:::

::::

[Ver todos os recursos do jornada →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Aprender assistindo {#video}

Obtenha uma introdução visual aos componentes do jornada e aprenda as noções básicas para criar jornadas na tela:

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **Quer mais vídeos?** [Explorar tutoriais em vídeo do jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Precisa de ajuda? {#help}

### Links rápidos para tarefas comuns

* **[Crie sua primeira jornada](journey-gs.md)** - Guia passo a passo para iniciantes
* **[Perguntas frequentes sobre o Jornada](journey-faq.md)** - Perguntas frequentes respondidas
* **[Solução de problemas](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnosticar e corrigir problemas
* **[Referência de códigos de erro](error-codes-reference.md)** - Compreender as mensagens de erro
* **[Medidas de proteção e limitações](../start/guardrails.md)** - Limites técnicos e práticas recomendadas

### Receber notificação sobre problemas

Configure os **[alertas de jornada](../reports/alerts.md)** para receber notificações em tempo real quando o jornada encontrar erros ou padrões incomuns.

### Recursos adicionais

* **[hub de gerenciamento de Jornadas](/help/rp_landing_pages/manage-journey-landing-page.md)** - Ferramentas de filtragem, otimização e gerenciamento de perfis
* **[Referência de atividades de Jornada](/help/rp_landing_pages/about-journey-building-landing-page.md)** - Guia completo para todos os tipos de atividades
* **[Solução de problemas de execução](troubleshooting-execution.md)** - Depurar problemas de execução de jornada
* **[Solução de problemas de atividades de entrada](troubleshooting-inbound.md)** - Corrigir problemas de entrada e qualificação

**Pronto para criar sua primeira jornada?** [Começar agora →](journey-gs.md)
