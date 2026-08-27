---
solution: Journey Optimizer
product: journey optimizer
title: Escolha como testar e validar sua jornada
description: Compare a Simulação de Jornada, o Modo de teste e o Jornada Dry run e escolha o método de validação correto para sua jornada antes de publicar.
feature: Journeys, Get Started, Test Profiles
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: testar, simular, simulação, modo de teste, simulação, jornada, validar, comparar, escolher, guia de decisão
version: Journey Orchestration
hide: true
source-git-commit: d10f3af7e2557c48be93694d4eb8f87d06332e42
workflow-type: tm+mt
source-wordcount: '2289'
ht-degree: 0%

---


# Escolha como testar e validar sua jornada {#choose-validation-method}

>[!BEGINSHADEBOX]

**Nesta página:** Compare a simulação da Jornada, o modo de Teste e o Dry run da Jornada e saiba qual delas se encaixa no estágio atual de criação de uma jornada — desde a iteração rápida durante o design até a verificação final de pré-lançamento em relação ao público-alvo em tempo real.

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] fornece três maneiras de validar uma jornada antes que ela entre em vigor. Elas não são intercambiáveis: cada uma usa um tipo diferente de dados, se encaixa em um estágio diferente de sua criação e carrega diferentes consequências reais. Entender a diferença antecipadamente ajuda a evitar dois erros comuns: gastar tempo criando perfis de teste quando uma simulação rápida faria ou presumir que uma etapa de validação é totalmente &quot;segura&quot; quando ainda pode entrar em contato com caixas de entrada reais ou fazer chamadas de saída reais.

Esta página foca na validação do fluxo de jornada e da lógica de ramificação. Para obter o quadro completo dos recursos de teste e aprovação, incluindo visualização de conteúdo, renderização de email e verificações de spam, experimentos A/B e fluxos de trabalho de aprovação, consulte [Testar, validar e aprovar](../../rp_landing_pages/test-landing-page.md).

## Novo na validação? Comece aqui {#quick-pick}

Se não tiver certeza de qual método se aplica a você, responda a esta pergunta:

* **Ainda estou projetando minha jornada e desejo testar uma ramificação rapidamente, sem criar perfis de teste.** → Use a **[Simulação de Jornada](simulate-journey-gs.md)**.
* **Desejo percorrer manualmente meu rascunho da jornada passo a passo, usando perfis reais (mas designados como teste).** → Use o **[Modo de teste](testing-the-journey.md)**.
* **Estou prestes a publicar e quero uma verificação final em relação ao meu público real de produção, sem entrar em contato com ninguém.** → Use **[Jornada simulação](journey-dry-run.md)**.

Ainda não tem certeza ou quer ter uma imagem completa? Continue lendo — cada método é explicado detalhadamente abaixo.

## Os três métodos de validação {#validation-methods}

>[!BEGINTABS]

>[!TAB Simulação de Jornada]

**Quando usar:** iteração rápida durante o design da jornada, especialmente antes do prazo ou ao testar novas ramificações de política de decisão.

[Simulação de Jornada](simulate-journey-gs.md) valida sua jornada com usuários temporários simulados, criados manualmente ou gerados automaticamente — não é necessário criar ou aguardar a propagação de perfis de teste reais do Adobe Experience Platform (AEP). O Agente de simulação de Jornada gera automaticamente os eventos de teste de que sua jornada precisa e os corresponde aos usuários simulados corretos, acionando a jornada em segundos.

Mecanismos principais:

* Os usuários simulados são temporários e descartáveis; eles não são perfis reais no AEP.
* Os critérios de saída, as políticas de consentimento, o limite de frequência/jornada, a opção de não participação/supressão e as horas de silêncio não são avaliados.
* As ações personalizadas e as chamadas de fonte de dados externa ainda fazem chamadas de saída reais — elas não são ridicularizadas.

>[!IMPORTANT]
>
>A simulação envia mensagens reais para os [endereços de execução](simulate-journey.md#test-users) (email, telefone, token de push) configurados nos usuários simulados — por exemplo, seu próprio endereço de email — usando o mesmo pipeline de entrega que a produção. Ele não entra em contato com clientes reais ou atualiza os dados do perfil ao vivo, mas as mensagens em si são reais.

**Perfeito para:** validar uma nova ramificação (por exemplo, dois novos caminhos de política de decisão) sem esperar pela propagação do perfil de teste do AEP.

➡️ [Introdução à simulação de jornada](simulate-journey-gs.md) | [Simular sua jornada](simulate-journey.md)

>[!TAB Modo de teste]

**Quando usar:** verificação manual passo a passo da lógica de ramificação e mensagem, com perfis reais (mas de teste designado) percorrendo a jornada de rascunho.

[O modo de teste](testing-the-journey.md) permite validar uma jornada de rascunho usando [perfis de teste do AEP](../audience/creating-test-profiles.md) persistentes. Você aciona eventos manualmente na interface para confirmar que a lógica de ramificação e a mecânica de entrega de mensagens funcionam conforme projetado, antes que qualquer público de produção toque na jornada.

Mecanismos principais:

* Somente perfis sinalizados como &quot;perfis de teste&quot; no Perfil do cliente em tempo real podem inserir uma jornada no modo de teste.
* O modo de teste está disponível somente para jornadas de rascunho que usam um [namespace](../audience/get-started-identity.md), já que ele deve verificar no AEP se uma pessoa é um perfil de teste.
* Um máximo de 100 perfis de teste pode inserir uma jornada durante uma única sessão de teste, e os eventos só podem ser acionados na interface, não de sistemas externos por meio da API.
* Desativar o modo de teste remove todos os perfis que entraram na jornada e limpa os relatórios.

>[!IMPORTANT]
>
>O modo de teste envia mensagens reais para as caixas de entrada reais dos perfis de teste, usando o mesmo pipeline de entrega que a produção. Ela não entra em contato com clientes reais, mas também não é uma simulação &quot;seca&quot; — verifique se os perfis de teste usam endereços controlados por você.

**Ponto problemático:** a criação e propagação de novos perfis de teste do AEP leva tempo, o que limita quando é necessário validar rapidamente uma nova ramificação. Se essa for a sua meta, [Simulação de Jornada](simulate-journey-gs.md) resolverá esse problema específico.

➡️ [Testar sua jornada](testing-the-journey.md)

>[!TAB Jornada execução seca]

**Quando usar:** uma verificação final, realista em produção, antes da publicação.

O [Jornada Dry run](journey-dry-run.md) é um modo de publicação de jornada especial que executa sua jornada em relação ao público-alvo de produção real e aos dados de segmentação, sem entrar em contato com clientes reais ou atualizar as informações do perfil. A jornada é ativada como uma jornada em tempo real — os perfis fluem por ramificações e nós exatamente como fariam na produção — mas os [nós de ação](about-journey-activities.md), como email, SMS e ações personalizadas, são ignorados.

Mecanismos principais:

* Usa seu público-alvo real de produção para que você veja o alcance e o direcionamento reais em escala (por exemplo, detectar um erro em que uma ramificação inteira recebe inesperadamente zero perfil).
* Em cada ativação, você pode optar por desativar as atividades de espera (para que as métricas voltem mais rápido) e desativar chamadas de fonte de dados externa (para que a jornada permaneça totalmente em silos).
* Este é atualmente um recurso de **Disponibilidade limitada**, sendo implantado globalmente ao longo do tempo.

**Perfeito para:** detectar problemas como nós de condição digitados incorretamente ou públicos que inesperadamente não alcançam uma ramificação, antes de ativar a jornada.

➡️ [Jornada Execução seca](journey-dry-run.md)

>[!ENDTABS]

## Qual método você deve usar? {#decision-guide}

A resposta geralmente se resume a uma pergunta: *a que distância da produção você precisa que esse teste esteja?*

Se você ainda estiver **iterando no design do jornada** — testando uma nova ramificação, trabalhando dentro de um prazo — use **Simulação de Jornada**. Ele não precisa de perfis reais e é executado em segundos. Lembre-se de que ele envia mensagens reais para os endereços de execução configurados nos usuários simulados.

Se você precisar **verificar manualmente etapa por etapa a lógica de mensagem e ramificação** e estiver disposto a criar ou reutilizar perfis de teste do AEP, use o **Modo de teste**. Lembre-se de que ele envia mensagens reais para as caixas de entrada reais desses perfis de teste.

Se você estiver prestes a **publicar** e quiser uma verificação final em relação ao seu público-alvo de produção real, sem entrar em contato com ninguém ou alterar os dados do perfil, use o **Jornada Dry run**.

>[!TIP]
>
>**Não tem certeza de onde começar?** A maioria das equipes usa a **Simulação de Jornada** durante a compilação e, em seguida, uma **Execução de Jornada** logo antes da publicação. Alcance o **Modo de teste** quando precisar percorrer manualmente a lógica de ramificação com perfis de teste reais em vez de simulados.

## Comparação rápida {#quick-comparison}

| Método | Dados usados | Envia mensagens reais? | Melhor para |
|---|---|---|---|
| [Simulação de Jornada](simulate-journey-gs.md) | Usuários temporários simulados, criados manualmente ou gerados automaticamente | Sim — para os endereços de execução configurados nos usuários simulados | Iteração rápida, especialmente para novas ramificações de políticas de decisão, sem esperar pela propagação real do perfil de teste |
| [Modo de teste](testing-the-journey.md) | Perfis de teste de AEP persistentes | Sim — para testar as caixas de entrada reais dos perfis, usando o pipeline de entrega de produção | Verificação manual passo a passo da lógica de ramificação/mensagem em uma jornada de rascunho |
| [Jornada execução seca](journey-dry-run.md) | Público-alvo/dados de produção real | Não (ações ignoradas) | Verificação final de pré-lançamento do alcance real do público, do direcionamento e da lógica da ramificação em escala real |

Nenhum desses métodos entra em contato com clientes reais. Os dados do perfil também são deixados intocados em todos os casos, exceto que o modo de Teste atualiza os perfis de teste usados para executá-lo (não perfis de clientes reais).

## Erros comuns a serem evitados {#common-mistakes}

* **Presumindo que a Simulação de Jornada é totalmente &quot;segura&quot;.** É a maneira mais rápida de testar, mas ainda envia mensagens reais para o endereço de execução configurado em cada usuário simulado — geralmente sua própria caixa de entrada. Não suponha que nada seja enviado.
* **Criar perfis de teste do AEP quando a Simulação de Jornada permitir.** Se você precisar validar uma nova ramificação ou caminho de política de decisão rapidamente, a simulação ignora totalmente a espera pela propagação do perfil de teste — salve o modo de Teste para quando você realmente precisar de perfis de teste reais.
* **Tratando o modo de Teste como &quot;seco&quot;.** Os perfis de modo de teste recebem mensagens reais por meio do pipeline de entrega de produção. Certifique-se de que os perfis de teste usem apenas endereços controlados por você.
* **Esperando o Jornada Dry run para capturar conteúdo ou problemas de entrega.** O modo de execução seca ignora completamente os nós de ação — valida o alcance do público-alvo e a lógica da ramificação, não o conteúdo da mensagem ou a mecânica de entrega. Use o modo Simulação ou Teste para isso.
* **Esquecendo o requisito de namespace para o modo de Teste.** O modo de teste só funciona em jornadas de rascunho que usam um namespace — sem um, o Journey Optimizer não pode verificar se um perfil está sinalizado como um perfil de teste.

## Próximas etapas {#next-steps}

* **[Introdução à simulação de jornada](simulate-journey-gs.md)** — Execute sua primeira simulação
* **[Testar sua jornada](testing-the-journey.md)** — Ativar modo de teste com perfis de teste do AEP
* **[Jornada simulação](journey-dry-run.md)** — Execute uma simulação realista de produção
* **[Publicar sua jornada](publish-journey.md)** — Pré-requisitos e o processo de publicação
* **[Introdução ao jornada](journey.md)** — visão geral de fundamentos e recursos
* **[Perguntas frequentes sobre o Journey Orchestration](journey-faq.md)** — perguntas comuns respondidas
* **[Testar, validar e aprovar](../../rp_landing_pages/test-landing-page.md)** — cenário completo de testes e aprovações, incluindo visualização de conteúdo, verificações de renderização/spam, experiências e fluxos de trabalho de aprovação

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página compara os três métodos de validação de jornada no Adobe Journey Optimizer — Simulação de Jornada, Modo de teste e Execução de Jornada seca — e fornece uma escolha rápida de uma pergunta, um guia de decisão, uma tabela de comparação rápida e uma lista de erros comuns para ajudar os usuários a escolher o correto para o estágio atual de criação de uma jornada.

**Intenções:**

* Escolha o método de validação correto para uma determinada etapa da criação de jornadas
* Comparar a simulação da Jornada, o modo de teste e a Jornada simulação lado a lado
* Entender quando usar a Simulação de Jornada para iteração rápida sem perfis de teste reais
* Entenda quando usar o modo de Teste para validação manual passo a passo com perfis de teste reais
* Entenda quando usar o Jornada Dry run para uma verificação de pré-lançamento final em relação aos dados de produção
* Entenda quais métodos de validação enviam mensagens reais ou entrem em contato com clientes reais
* Evite erros comuns ao selecionar ou usar um método de validação

**Glossário:**

* **Simulação de Jornada**: um método de validação que usa usuários temporários simulados, criados manualmente ou gerados automaticamente, para testar uma jornada sem precisar de perfis de teste reais do AEP. *(específico do produto)*
* **Modo de teste**: um método de validação que usa perfis de teste persistentes do AEP, sinalizados no Perfil do Cliente em Tempo Real, para percorrer manualmente a ramificação e a lógica de mensagem de uma jornada de rascunho. *(específico do produto)*
* **Execução seca da Jornada**: um modo de publicação que executa uma jornada em relação aos dados do público-alvo real de produção sem entrar em contato com os clientes ou atualizar os dados do perfil; os nós de ação são ignorados. *(específico do produto)*
* **Agente de Simulação**: o mecanismo que gera eventos de teste automaticamente e os corresponde aos usuários simulados durante a Simulação de Jornada. *(específico do produto)*

**Medidas de Proteção:**

* O modo de teste só está disponível para jornadas de rascunho que usam namespace e oferece suporte a no máximo 100 perfis de teste por sessão
* Os eventos do modo de teste só podem ser acionados na interface, não em sistemas externos por meio da API
* O modo de teste envia mensagens reais para testar as caixas de entrada reais dos perfis usando o pipeline de entrega de produção
* Desativar o modo de teste remove todos os perfis que entraram na jornada e limpa seus relatórios
* A Simulação de jornada não avalia os critérios de saída, as políticas de consentimento, o limite de frequência/jornada, a opção de não participação/supressão ou as horas de silêncio
* As ações personalizadas da Simulação de Jornada e as chamadas de fonte de dados externa são reais, não zombadas
* A Simulação de Jornada envia mensagens reais para os endereços de execução (email, telefone, token de push) configurados nos usuários simulados, usando o mesmo pipeline de entrega que a produção — ao contrário da Execução de Jornada seca, que nunca envia mensagens reais
* O Jornada Dry run é atualmente um recurso de Disponibilidade limitada, sendo implantado globalmente ao longo do tempo
* O Jornada Dry run ignora os nós de ação (email, SMS, ações personalizadas), mas ainda roteia perfis por ramificações e nós usando dados de produção reais

**Terminologia:**

* Nome canônico: Simulação de Jornada — variantes: simulate, modo de simulação
* Nome canônico: Modo de teste — variantes: teste de jornada, teste sua jornada
* Nome canônico: Jornada Dry run — variantes: dry run, modo dry run
* Não confunda: Simulação de Jornada (usuários temporários simulados, nenhum perfil de teste do AEP necessário, envia mensagens reais para os endereços de execução configurados dos usuários simulados) ≠ Modo de teste (perfis de teste persistentes do AEP, envia mensagens reais para as caixas de entrada reais desses perfis) ≠ Jornada Dry run (dados de público-alvo de produção real, nenhum contato, nenhuma atualização de perfil, nós de ação ignorados, nunca envia mensagens reais)

**Perguntas frequentes:**

* **P: Qual método de validação devo usar enquanto ainda estou projetando uma jornada?** — Use a simulação de Jornada; ela não precisa de perfis de teste reais e é executada em segundos, tornando-a ideal para iteração rápida.
* **P: A Simulação de Jornada envia mensagens reais?** — Sim. A simulação entrega mensagens reais aos endereços de execução (email, telefone, token de push) configurados nos usuários simulados — geralmente o próprio endereço do testador — usando o mesmo pipeline de entrega que a produção. Ele não entra em contato com clientes reais ou atualiza os dados do perfil ao vivo, mas as mensagens em si são reais.
* **P: O modo de Teste envia emails ou SMS reais?** — Sim. O modo de teste fornece mensagens reais para as caixas de entrada reais dos perfis de teste, usando o mesmo pipeline de entrega que a produção. Ela não entra em contato com clientes reais, mas as mensagens em si são reais.
* **P: O Jornada Dry run envia mensagens?** — Não. A execução seca ignora nós de ação, como email, SMS e ações personalizadas, para que os perfis fluam pela lógica da jornada sem que nenhuma mensagem seja enviada.
* **P: Preciso validar uma nova ramificação rapidamente antes do prazo. Qual método se encaixa?** — simulação de Jornada; gera usuários simulados descartáveis sob demanda em vez de exigir que você pré-crie e aguarde perfis de teste reais.
* **P: O Jornada Dry run está disponível para todos?** — no momento, esse é um recurso de disponibilidade limitada sendo implantado globalmente ao longo do tempo; verifique a disponibilidade para sua organização.
* **P: Posso acionar eventos do modo de teste de um sistema externo?** — Não; no modo de teste, os eventos só podem ser acionados da interface, não de sistemas externos por meio da API.

+++
