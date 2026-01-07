---
solution: Journey Optimizer
product: Journey Optimizer
title: Visualizar e testar conteúdo
description: Validar a precisão da mensagem antes da inicialização. Pré-visualize o conteúdo personalizado com perfis de teste, envie provas para as partes interessadas, verifique a renderização de email entre clientes, avalie as pontuações de spam e teste várias variações de conteúdo com eficiência.
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: 6b83b015dfd74da9eb58bd06958d0963d81c6489
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 23%

---

# Visualizar e testar conteúdo{#section-overview}

>[!BEGINSHADEBOX]

**Finalidade:** ferramentas de validação de pré-lançamento para campanhas e jornadas\
**Usuários principais:** gerentes de campanha, profissionais de marketing por email, criadores de conteúdo\
**Resultado principal:** detectar erros antes da entrega ao cliente

>[!ENDSHADEBOX]

Garanta a entrega perfeita de mensagens, capturando os erros antes que eles cheguem aos clientes. A pré-visualização de conteúdo valida a precisão da personalização em diferentes perfis de clientes, enquanto as ferramentas de teste revelam problemas de renderização, riscos de spam e variações de conteúdo que podem afetar o engajamento. Acesse recursos abrangentes para enviar provas às partes interessadas, simular a personalização com dados de amostra, verificar a renderização de email entre clientes e avaliar as métricas de capacidade de delivery, tudo antes da ativação. Domine essas técnicas de validação para proteger a reputação da marca, maximizar a inserção da caixa de entrada e fornecer experiências excelentes para o cliente de maneira consistente.

## Visualizar e testar conteúdo

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Como visualizar e testar seu conteúdo

Saiba como usar perfis de teste e dados de entrada de amostra para visualizar e testar o conteúdo, enviar provas e garantir a precisão da personalização.

[Introdução à visualização e teste](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Como selecionar perfis de teste

Descubra como selecionar e gerenciar perfis de teste para visualizar e testar o conteúdo personalizado com eficiência.

[Saiba como selecionar perfis de teste](../using/content-management/test-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Visualizar o conteúdo usando perfis de teste

Guia passo a passo para visualizar conteúdo personalizado usando perfis de teste e simulando variações de conteúdo.

[Visualizar conteúdo com perfis de teste](../using/content-management/preview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Enviar provas usando dados de perfil de teste

Teste e valide suas mensagens de email enviando provas usando os dados do perfil de teste para garantir a precisão do conteúdo.

[Saiba como enviar provas](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg)

Como testar a renderização de email com o Litmus

Integre o Litmus para pré-visualizar a renderização de email em clientes de email populares e garantir a exibição adequada.

[Testar renderização de email com o Litmus](../using/content-management/rendering.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Como simular e testar variações de conteúdo

Simule variações de conteúdo usando amostras de dados de entrada para testar o conteúdo personalizado e garantir a precisão.

[Simular variações de conteúdo](../using/test-approve/simulate-sample-input.md)
:::

::::

## Guia de decisão rápida

**Contexto:** esta tabela mapeia metas de teste para ferramentas específicas no Adobe Journey Optimizer.

Escolha sua abordagem de teste com base em sua meta:

| **Se precisar...** | **Usar esta ferramenta** |
|----------------------|-------------------|
| Verificar se a personalização é exibida corretamente | [Perfis de teste](../using/content-management/test-profiles.md) |
| Teste rapidamente mais de 10 variações de conteúdo | [Dados de entrada de exemplo](../using/test-approve/simulate-sample-input.md) |
| Obter aprovação da parte interessada antes de enviar | [Enviar provas](../using/content-management/proofs.md) |
| Verificar exibição de email no Gmail, Outlook, Apple Mail | [Renderização de Litmus](../using/content-management/rendering.md) |
| Melhorar o posicionamento da caixa de entrada | [Relatório de spam](../using/content-management/spam-report.md) |
| Visualizar todas as variações de uma só vez | [Modo de visualização](../using/content-management/preview.md) |

## Teste da lista de verificação do fluxo de trabalho

**Contexto:** Sequência de teste de 5 etapas recomendada aplicável a todos os canais (email, SMS, push, Web, no aplicativo).

Siga esta sequência para uma validação abrangente:

1. **Visualização** - Use perfis de teste para verificar corretamente os renderizadores de personalização
2. **Variações de teste** - Carregue dados de amostra CSV/JSON para validar vários cenários
3. **Verificar a capacidade de entrega** (email) - Executar relatório de spam e testes de renderização
4. **Enviar provas** - Compartilhar com os participantes para revisão e aprovação
5. **Verificação final** - Verifique se todos os links, imagens e CTAs estão funcionando corretamente

**Dica profissional:** teste com pelo menos 3 perfis que representem segmentos de clientes diferentes (alto valor, novo, inativo) para capturar casos de borda.

## Cenários comuns

**Contexto:** exemplos reais que mostram como aplicar ferramentas de teste em casos de uso típicos.

**Cenário 1: testar emails personalizados para uma campanha com vários segmentos**
→ Use [dados de entrada de amostra](../using/test-approve/simulate-sample-input.md) para testar variações de 20 a 30 sem criar perfis de teste individuais. Faça upload de um CSV com diferentes atributos do cliente e visualize tudo de uma só vez.

**Cenário 2: validando renderização de email antes de um envio principal**
→ Execute [testes Litmus](../using/content-management/rendering.md) para verificar a exibição nos principais clientes de email e, em seguida, verifique o [relatório de spam](../using/content-management/spam-report.md) para garantir o posicionamento da caixa de entrada.

**Cenário 3: Obtendo aprovação da parte interessada**
→ [Envie provas](../using/content-management/proofs.md) para revisores internos com dados de perfil de teste para que eles vejam exatamente o que os clientes receberão.

## Principais pontos

- **Perfis de teste** são essenciais para a visualização de conteúdo personalizado; use dados de entrada de exemplo para testar mais de 10 variações com eficiência
- **As ferramentas específicas de email** incluem testes de renderização (Litmus), relatórios de spam e provas
- **Sequência recomendada:** Visualização → Variações de teste → Verificar capacidade de entrega → Enviar provas → Verificação final
- **Economia de tempo:** carregue CSV/JSON com atributos do cliente em vez de criar perfis de teste individuais

## Recursos adicionais

- **[Como usar o Relatório de spam por email](../using/content-management/spam-report.md)** - Avalie a pontuação de spam do conteúdo de email usando o recurso Relatório de spam para melhorar a capacidade de entrega.

**Tópicos relacionados:** [Testar e aprovar página de aterrissagem](test-landing-page.md) | [Fluxos de trabalho de aprovação](approve-landing-page.md) | [Criando perfis de teste](../using/audience/creating-test-profiles.md)
