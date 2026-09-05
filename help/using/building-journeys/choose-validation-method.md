---
solution: Journey Optimizer
product: journey optimizer
title: Escolha um método de validação
description: Compare a Simulação de Jornada, o modo Teste de Jornada e o Jornada Dry run e escolha o método de validação correto para sua jornada antes de publicar.
feature: Journeys, Get Started, Test Profiles
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: testar, simular, simulação, modo de teste, simulação, jornada, validar, comparar, escolher, guia de decisão
version: Journey Orchestration
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 0%

---


# Escolha um método de validação {#choose-validation-method}

>[!BEGINSHADEBOX]

**Nesta página:** Comparar Simulação de Jornada, Modo de Teste de Jornada e Execução de Jornada Seca. Saiba qual se encaixa no estágio atual de criação de uma jornada, desde a iteração rápida durante o design até a verificação final de pré-lançamento em relação ao público-alvo em tempo real.

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] fornece três maneiras de validar uma jornada antes que ela entre em vigor. Elas não são intercambiáveis: cada uma usa um tipo diferente de dados, se encaixa em um estágio diferente de sua criação e carrega diferentes consequências reais. Entender a diferença antecipadamente ajuda a evitar dois erros comuns. A primeira é gastar tempo criando perfis de teste quando uma simulação rápida serviria. A segunda é supor que uma etapa de validação seja totalmente &quot;segura&quot; quando ainda puder entrar em contato com caixas de entrada reais ou fazer chamadas de saída reais.

Esta página foca na validação do fluxo de jornada e da lógica de ramificação. Para obter o quadro completo dos recursos de teste e aprovação, incluindo visualização de conteúdo, renderização de email e verificações de spam, experimentos A/B e fluxos de trabalho de aprovação, consulte [Testar, validar e aprovar](../../rp_landing_pages/test-landing-page.md).

## Novo na validação? Comece aqui {#quick-pick}

Se não tiver certeza de qual método se aplica a você, responda a esta pergunta:

* **Ainda estou projetando minha jornada e desejo validar rapidamente a lógica de uma ramificação, sem criar perfis de teste.** → Use a **[Simulação de Jornada](simulate-journey-gs.md)**.
* **Quero validar manualmente passo a passo a lógica da jornada de rascunho, usando perfis reais (mas de teste designado).** → Use o **[modo de teste do Jornada](testing-the-journey.md)**.
* **Estou prestes a publicar e quero uma verificação final dos volumes esperados em relação ao meu público real de produção, sem entrar em contato com ninguém.** → Use **[Jornada simulação](journey-dry-run.md)**.

Ainda não tem certeza ou quer ter uma imagem completa? Continue lendo — cada método é explicado detalhadamente abaixo.

## Os três métodos de validação {#validation-methods}

>[!BEGINTABS]

>[!TAB Simulação de Jornada]

**Quando usar:** iteração rápida durante o design da jornada, especialmente antes do prazo ou ao testar novas ramificações ou caminhos. Também funciona bem como um método de validação contínua sempre que não for prático criar um perfil de teste adequado para o caso de uso.

A [Simulação de Jornada](simulate-journey-gs.md) valida sua jornada com usuários temporários simulados — não é necessário criar ou aguardar a propagação de perfis de teste reais do Adobe Experience Platform (AEP). Você pode criar usuários simulados manualmente ou permitir que a IA gere automaticamente os eventos de teste de que sua jornada precisa e os faça corresponder aos usuários simulados corretos, acionando a jornada em segundos.

Mecanismos principais:

* Os usuários simulados não são perfis reais no AEP; você também pode salvá-los no [inventário](simulate-journey.md#test-users) para serem reutilizados em simulações futuras, em vez de criá-los do zero a cada vez.
* Os critérios de saída, as políticas de consentimento, o limite de frequência/jornada, a opção de não participação/supressão e as horas de silêncio não são avaliados.
* As ações personalizadas e as chamadas de fonte de dados externa ainda fazem chamadas de saída reais — elas não são ridicularizadas.

>[!IMPORTANT]
>
>A simulação envia mensagens reais para os [endereços de execução](simulate-journey.md#test-users) (email, telefone, token de push) configurados nos usuários simulados — por exemplo, seu próprio endereço de email. Ele usa o mesmo pipeline de entrega que a produção. Ele não entra em contato com clientes reais ou atualiza os dados do perfil ao vivo, mas as mensagens em si são reais.

**Perfeito para:** validar uma nova ramificação (por exemplo, dois novos caminhos de política de decisão) sem esperar pela propagação do perfil de teste do AEP.

➡️ [Introdução à simulação de jornada](simulate-journey-gs.md) | [Simular sua jornada](simulate-journey.md)

>[!TAB Modo de teste de Jornada]

**Quando usar:** verificação manual passo a passo da lógica de ramificação e mensagem, com perfis reais (mas de teste designado) percorrendo a jornada de rascunho.

O [modo de Teste de Jornada](testing-the-journey.md) permite validar uma jornada de rascunho usando [perfis de teste persistentes do AEP](../audience/creating-test-profiles.md). Para confirmar se a lógica de ramificação e a mecânica de entrega de mensagens funcionam como projetados antes que qualquer público de produção toque na jornada, acione eventos manualmente na interface.

Mecanismos principais:

* Somente perfis sinalizados como &quot;perfis de teste&quot; no Perfil do cliente em tempo real podem inserir uma jornada no modo de teste de Jornada.
* O modo Jornada teste está disponível somente para jornadas de rascunho que usam um [namespace](../audience/get-started-identity.md), já que ele deve verificar no AEP se uma pessoa é um perfil de teste.
* Um máximo de 100 perfis de teste pode inserir uma jornada durante uma única sessão de teste, e os eventos só podem ser acionados na interface, não de sistemas externos por meio da API.
* Desativar o modo de Teste de Jornada remove todos os perfis que entraram na jornada e apaga os relatórios.

>[!IMPORTANT]
>
>O modo Jornada teste envia mensagens reais para as caixas de entrada reais dos perfis de teste, usando o mesmo pipeline de entrega que a produção. Ela não entra em contato com clientes reais, mas também não é uma simulação &quot;seca&quot; — verifique se os perfis de teste usam endereços controlados por você.

**Ponto problemático:** Criar e propagar novos perfis de teste do AEP leva tempo. [A Simulação de Jornada](simulate-journey-gs.md) oferece uma alternativa rápida que não requer nenhum perfil de teste. Isso é útil não apenas enquanto você espera que os perfis se propaguem, mas não é prático criar um perfil de teste adequado para seu caso de uso a qualquer momento.

➡️ [Testar sua jornada](testing-the-journey.md)

>[!TAB Jornada execução seca]

**Quando usar:** uma verificação final, realista em produção, antes da publicação.

O [Jornada Dry run](journey-dry-run.md) é um modo de publicação de jornada especial que executa sua jornada em relação ao público-alvo de produção real e aos dados de segmentação, sem entrar em contato com clientes reais ou atualizar as informações do perfil. A jornada é ativada como uma jornada em tempo real, e os perfis fluem por ramificações e nós exatamente como fariam na produção. No entanto, os [nós de ação](about-journey-activities.md), como email, SMS e ações personalizadas, são ignorados.

Mecanismos principais:

* Usa seu público-alvo real de produção para que você veja o alcance e o direcionamento reais em escala (por exemplo, detectar um erro em que uma ramificação inteira recebe inesperadamente zero perfil).
* Em cada ativação, para obter as métricas de volta mais rápido, você pode desativar as atividades de espera e, para manter a jornada totalmente em silos, você pode desativar chamadas de fonte de dados externas.
* Este é atualmente um recurso de **Disponibilidade limitada**, sendo implantado globalmente ao longo do tempo.

**Perfeito para:** detectar problemas como nós de condição digitados incorretamente ou públicos que inesperadamente não alcançam uma ramificação, antes de ativar a jornada.

➡️ [Jornada Execução seca](journey-dry-run.md)

>[!ENDTABS]

## Qual método você deve usar? {#decision-guide}

Comece com uma pergunta simples: você já tem perfis de teste que se encaixam no seu caso de uso? Em caso afirmativo, o **modo de Teste de Jornada** permite validar passo a passo com eles. Caso contrário — ou se não for prático criá-los para esse caso de uso específico — A **Simulação de Jornada** é validada em segundos.

Além dessa escolha, a resposta geralmente se resume a mais uma pergunta: *a que distância da produção você precisa que esse teste esteja?*

Se você ainda estiver **iterando no design do jornada** — testando uma nova ramificação, trabalhando dentro de um prazo — use **Simulação de Jornada**. Ele não precisa de perfis reais e é executado em segundos. Também permanece uma opção válida posteriormente em sua criação, sempre que não for prático criar perfis de teste adequados para seu caso de uso. Lembre-se de que ele envia mensagens reais para os endereços de execução configurados nos usuários simulados.

Se você precisar **verificar manualmente etapa por etapa a lógica de ramificação e mensagem** e estiver disposto a criar ou reutilizar perfis de teste do AEP, use o **Modo de teste de Jornada**. Lembre-se de que ele envia mensagens reais para as caixas de entrada reais desses perfis de teste.

Se você estiver prestes a **publicar** e quiser uma verificação final dos volumes esperados em relação ao seu público-alvo real de produção, use o **Jornada Dry run**. Ele nunca contata ninguém ou altera os dados do perfil.

>[!TIP]
>
>**Não tem certeza de onde começar?** A maioria das equipes usa a **Simulação de Jornada** durante a compilação e, em seguida, uma **Execução de Jornada** logo antes da publicação. Alcance o **modo de Teste de Jornada** quando precisar passar manualmente pela lógica de ramificação com perfis de teste reais em vez de perfis simulados.

## Comparação rápida {#quick-comparison}

| Método | Dados usados | Envia mensagens reais? | Melhor para |
|---|---|---|---|
| [Simulação de Jornada](simulate-journey-gs.md) | Usuários temporários simulados, criados manualmente ou gerados automaticamente | Sim — para os endereços de execução configurados nos usuários simulados | Iteração rápida em novas ramificações ou caminhos, sem esperar pela propagação real do perfil de teste |
| [Modo de teste de Jornada](testing-the-journey.md) | Perfis de teste de AEP persistentes | Sim — para testar as caixas de entrada reais dos perfis, usando o pipeline de entrega de produção | Verificação manual passo a passo da lógica de ramificação/mensagem em uma jornada de rascunho |
| [Jornada execução seca](journey-dry-run.md) | Público-alvo/dados de produção real | Não (ações ignoradas) | Verificação final de pré-lançamento do alcance real do público, do direcionamento e da lógica da ramificação em escala real |

Nenhum desses métodos entra em contato com clientes reais. Os dados do perfil também são deixados intocados em todos os casos, exceto que o modo Jornada teste atualiza os perfis de teste usados para executá-lo (não perfis de clientes reais).

## Erros comuns a serem evitados {#common-mistakes}

* **Presumindo que a Simulação de Jornada é totalmente &quot;segura&quot;.** É a maneira mais rápida de testar, mas ainda envia mensagens reais para o endereço de execução configurado em cada usuário simulado — geralmente sua própria caixa de entrada. Não suponha que nada seja enviado.
* **Criar perfis de teste do AEP quando a Simulação de Jornada permitir.** Se você precisar validar rapidamente uma nova ramificação ou um novo caminho de política de decisão, a simulação ignora totalmente a espera pela propagação do perfil de teste — salve o modo Jornada teste para quando você realmente precisar de perfis de teste reais.
* **Tratando o modo de Teste de Jornada como &quot;seco&quot;.** Os perfis do modo de Teste de Jornada recebem mensagens reais por meio do pipeline de entrega de produção. Certifique-se de que os perfis de teste usem apenas endereços controlados por você.
* **Esperando o Jornada Dry run para capturar conteúdo ou problemas de entrega.** O modo de execução seca ignora completamente os nós de ação — valida o alcance do público-alvo e a lógica da ramificação, não o conteúdo da mensagem ou a mecânica de entrega. Use o modo Simulação ou Teste de Jornada para isso.
* **Esquecendo o requisito de namespace para o modo de Teste de Jornada.** O modo Jornada teste só funciona em jornadas de rascunho que usam um namespace, porque o Journey Optimizer precisa de um namespace para verificar se um perfil está sinalizado como um perfil de teste.

## Próximas etapas {#next-steps}

* **[Introdução à simulação de jornada](simulate-journey-gs.md)** — Execute sua primeira simulação
* **[Testar sua jornada](testing-the-journey.md)** — Ativar o modo de Teste de Jornada com perfis de teste do AEP
* **[Jornada simulação](journey-dry-run.md)** — Execute uma simulação realista de produção
* **[Publicar sua jornada](publish-journey.md)** — Pré-requisitos e o processo de publicação
* **[Introdução ao jornada](journey.md)** — visão geral de fundamentos e recursos
* **[Perguntas frequentes sobre o Journey Orchestration](journey-faq.md)** — perguntas comuns respondidas
* **[Testar, validar e aprovar](../../rp_landing_pages/test-landing-page.md)** — cenário completo de testes e aprovações, incluindo visualização de conteúdo, verificações de renderização/spam, experiências e fluxos de trabalho de aprovação

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-choose-validation-method.md}}
