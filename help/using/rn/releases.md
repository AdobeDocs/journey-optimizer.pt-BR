---
solution: Journey Optimizer
product: journey optimizer
title: Ciclo de versão do Adobe Journey Optimizer
feature: Release Notes
description: Noções básicas sobre o ciclo de versão do Adobe Journey Optimizer
source-git-commit: cef105e55f3353c616e18be84faa0ee774aeac06
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 1%

---

# Ciclo de versão do Journey Optimizer {#releases}

O [!DNL Adobe Journey Optimizer] é atualizado regularmente para fornecer novos recursos, melhorias e correções. Esta página explica como o ciclo de lançamento funciona e o que cada fase de lançamento significa, para que você possa entender facilmente quando os recursos ficam disponíveis para sua organização.

## Modelo de entrega contínua {#continuous-delivery-model}

O [!DNL Adobe Journey Optimizer] opera em um modelo de entrega contínua, permitindo uma abordagem escalável e em fases para a implantação de recursos. Esse modelo permite que a Adobe ofereça inovações com mais rapidez e garanta estabilidade e desempenho contínuos durante a implantação.

>[!NOTE]
>
> Como o [!DNL Adobe Journey Optimizer] usa entrega contínua, novos recursos podem aparecer progressivamente entre organizações ou regiões.

Como parte desse modelo:

* Novas funcionalidades e melhorias são implantadas na produção assim que estiverem prontas.

* As [**Notas de versão**](release-notes.md) são atualizadas entre os lançamentos mensais com uma seção de _Atualizações mais recentes_, que anuncia novos recursos e melhorias à medida que são implementadas, para que você se mantenha informado em tempo real.

## Tempo e cadência da versão {#release-timing}

O [!DNL Adobe Journey Optimizer] geralmente segue uma cadência de lançamento mensal, com implantações que geralmente ocorrem durante a última semana de cada mês. As notas de versão mensais e a documentação relacionada são publicadas às terças-feiras da semana de lançamento. As notas de pré-lançamento são publicadas às sextas-feiras antes da semana de lançamento.

>[!TIP]
>
> No final de cada trimestre, as versões podem ser antecipadas e distribuídas até duas semanas antes do final do mês para se alinharem às programações trimestrais ou às versões dependentes do produto.

Embora a versão mensal introduza o conjunto principal de novos recursos e correções, a abordagem de entrega contínua permite que atualizações adicionais sejam implantadas entre os ciclos, quando prontas. As notas de versão são atualizadas adequadamente na seção _Atualizações mais recentes_, e a data de disponibilidade é mencionada. Todas as alterações lançadas durante o mês são consolidadas nas notas de versão mensais na data de lançamento.


## Caminhos de liberação {#release-paths}

Os recursos no Journey Optimizer seguem caminhos de versão diferentes, dependendo de sua complexidade, dependências e escopo. A plataforma usa vários rótulos de disponibilidade (Beta, Disponibilidade limitada, Disponibilidade geral), mas nem todos os recursos passam por todos eles.

Os caminhos de versão comuns incluem:

* **Direto para disponibilidade geral** — alguns novos recursos e melhorias vão direto para Disponibilidade Geral (GA).
* **LA → GA** — Alguns recursos estão disponíveis primeiro para um público-alvo limitado (disponibilidade limitada) antes da implantação geral.
* **Beta → LA → GA** — Recursos maiores ou experimentais avançam por todas as fases para teste e validação.
* **Beta → GA** — Alguns recursos estáveis do Beta podem ser movidos diretamente para GA, sem uma fase intermediária de LA.

>[!TIP]
>
> Se você estiver interessado em obter acesso antecipado a recursos no Beta ou em Disponibilidade limitada, entre em contato com o representante da Adobe para discutir as opções de participação.


## Rótulos de disponibilidade {#availability-labels}

| **Rótulo** | **Propósito** | **Disponibilidade** | **Observações sobre a Chave** |
|------------|-------------|------------------|----------------|
| **Beta** | Teste antecipado e coleta de feedback. | Restrito a clientes ou organizações selecionados que participam do programa Beta da Adobe. | - Não destinado a utilização na produção.<br>- A funcionalidade ou o design podem mudar antes do GA.<br>- O feedback ajuda a refinar a implementação final. |
| **Disponibilidade Limitada (DL)** | Implantação controlada para validação e monitoramento. | Ativado somente para clientes ou ambientes selecionados (por exemplo, sandboxes de desenvolvimento). | - Pronto para produção e com suporte total.<br>- Usado para validar o desempenho e a escalabilidade antes do lançamento geral.<br>- O acesso requer aprovação do Adobe. |
| **Disponibilidade Geral** | Versão ampla da funcionalidade totalmente compatível. | Ativado por padrão para todas as organizações elegíveis. | - Pronto para produção e com suporte total.<br> - Licenciamento ou direitos podem se aplicar.<br> - Pode ser implantado progressivamente entre regiões. |


## Implantação e disponibilidade {#rollout}

Mesmo após um anúncio no GA, a implantação pode ocorrer gradualmente entre organizações ou regiões. Se um novo recurso não aparecer imediatamente em seu ambiente, ele normalmente estará disponível em alguns dias após o lançamento.

Essa implantação gradual ajuda a Adobe a monitorar a estabilidade, o desempenho e a experiência do usuário antes de concluir a implantação.


## Manter-se informado {#staying-informed}

Para se manter atualizado:

* Revise as [**notas de versão mais recentes**](release-notes.md) para obter recursos novos e atualizados.
* Verifique a seção **_Atualizações mais recentes_** entre as versões mensais para implantações em tempo real.
* Monitore as **Notas de Pré-lançamento** (quando disponíveis) para obter uma visualização dos recursos futuros.
* Entre em contato com o representante da Adobe para obter informações sobre acesso ou direitos de Disponibilidade limitada da Beta.

Você pode assinar **alertas por email e no produto** para lançamentos de produtos da Journey Optimizer. Para inscrever-se:

1. Acesse as **Preferências da Adobe Experience Cloud**
1. Em **Notificações**, localize o **Journey Optimizer**
1. Habilitar **Novas versões** notificações no aplicativo e por email

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}

## Perguntas frequentes {#faq}

Você encontrará abaixo Perguntas frequentes sobre o ciclo de lançamento do Adobe Journey Optimizer.

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer sua pergunta ou conecte-se com a [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}.

+++ Quando as versões do Adobe Journey Optimizer estão programadas?

O [!DNL Adobe Journey Optimizer] normalmente lança atualizações durante a última semana de cada mês. No final de cada trimestre, a versão pode ser adiada em até duas semanas para se alinhar a atualizações entre soluções ou plataformas.

+++

+++ Por que não vejo um novo recurso imediatamente após seu anúncio?

Alguns recursos do GA são lançados progressivamente para garantir a estabilidade e o desempenho da plataforma. Se você não vir um recurso imediatamente, ele aparecerá quando a implantação for concluída para sua região ou organização.

+++

+++ Qual é a diferença entre o Beta, a disponibilidade limitada e o GA?

* **Beta**: fase de teste antecipado, acesso limitado, com base em comentários.
* **Disponibilidade Limitada (DL)**: Implantação controlada para validação final.
* **Disponibilidade Geral (GA)**: versão completa para todos os clientes autorizados.

+++

+++ Todos os recursos passam pelo Beta e pela Disponibilidade Limitada?

Não. Alguns recursos são lançados diretamente para GA ou somente para LA, dependendo de sua natureza e disponibilidade.O caminho de lançamento é personalizado para cada recurso para equilibrar agilidade, qualidade e estabilidade.

+++

+++ Como posso participar de programas do Beta ou de disponibilidade limitada?

O acesso é feito por convite ou solicitação por meio de um representante da Adobe. A participação ajuda a moldar o design de recursos e garante que seus casos de uso sejam considerados na versão final.

+++

+++ Com que frequência as notas de versão são atualizadas?

As notas de versão são atualizadas continuamente. Além dos lançamentos mensais, a seção _Atualizações mais recentes_ é atualizada sempre que novos recursos ou melhorias são encaminhados para produção.

+++
