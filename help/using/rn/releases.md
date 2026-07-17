---
solution: Journey Optimizer
product: journey optimizer
title: Ciclo de lançamento do Adobe Journey Optimizer
feature: Release Notes
description: Noções básicas sobre o ciclo de lançamento do Adobe Journey Optimizer
keywords: ciclo de versão, beta, disponibilidade limitada, disponibilidade geral, GA, LA, notas de versão
role: User
level: Beginner, Intermediate
exl-id: 344ae3cf-923c-4f0e-b3bc-0313993243c8
TQID: https://experienceleague.adobe.com/u8FJOgdav9VhwCk4CzrJoLrbFkVAa7BO83BCZ4SWsBc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: a7b2bfc5-be71-4740-b371-76fa6be8df02
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 1f2a71d3323b6a64b346a83aa58b23aed035eb29
workflow-type: tm+mt
source-wordcount: 993
ht-degree: 90%

---

# Ciclo de lançamento do Journey Optimizer {#releases}

O [!DNL Adobe Journey Optimizer] é atualizado regularmente para fornecer novos recursos, melhorias e correções. Esta página explica como o ciclo de lançamento funciona e o que cada fase do lançamento significa para que seja possível entender facilmente quando os recursos ficam disponíveis para a sua organização.

## Modelo de entrega contínua {#continuous-delivery-model}

O [!DNL Adobe Journey Optimizer] opera em um modelo de entrega contínua, permitindo uma abordagem escalável e em fases da implantação de recursos. Esse modelo permite que a Adobe ofereça inovações com mais rapidez e garanta estabilidade e desempenho contínuos durante a implantação.

>[!NOTE]
>
> Como o [!DNL Adobe Journey Optimizer] usa a entrega contínua, novos recursos podem aparecer progressivamente nas organizações ou regiões.

Como parte desse modelo:

* Novas funcionalidades e melhorias são implantadas na produção assim que estiverem prontas.

* As [**Notas de versão**](release-notes.md) são atualizadas entre os lançamentos mensais com uma seção de _Atualizações mais recentes_, que anuncia novos recursos e melhorias à medida que são implementadas, para a obtenção de informações em tempo real.

## Cronograma e frequência de lançamento {#release-timing}

O [!DNL Adobe Journey Optimizer] geralmente segue uma frequência de lançamento mensal com implantações que normalmente ocorrem durante a última semana de cada mês. As notas de versão mensais e a documentação relacionada são publicadas às terças-feiras da semana de lançamento. As notas de pré-lançamento são publicadas às sextas-feiras, antes da semana de lançamento.

>[!TIP]
>
> No final de cada trimestre, os lançamentos podem ser antecipados e implantados até duas semanas antes do final do mês para se alinharem aos cronogramas trimestrais ou aos lançamentos de produtos dependentes.

Enquanto a versão mensal introduz o conjunto principal de novos recursos e correções, a abordagem de entrega contínua permite que atualizações adicionais sejam implantadas entre os ciclos, quando prontas. Então, as notas de versão são atualizadas na seção _Atualizações mais recentes_ e a data de disponibilidade é mencionada. Todas as alterações disponibilizadas durante o mês são consolidadas nas notas de versão mensais na data de lançamento.


## Caminhos de lançamento {#release-paths}

Os recursos no [!DNL Journey Optimizer] seguem caminhos de versão diferentes, dependendo de sua complexidade, dependências e escopo. A plataforma usa vários rótulos de disponibilidade (Beta, Disponibilidade limitada, Disponibilidade geral), mas nem todos os recursos passam por todos eles.

Os caminhos de lançamento comuns incluem:

* **Direto para GA**: alguns novos recursos e melhorias vão direto para Disponibilidade geral (GA).
* **LA → GA**: alguns recursos estão disponíveis primeiro para um público-alvo limitado (Disponibilidade limitada) antes da implantação geral.
* **Beta → LA → GA**: recursos maiores ou experimentais avançam por todas as fases para teste e validação.
* **Beta → GA**: alguns recursos estáveis do Beta podem ser movidos diretamente para Disponibilidade geral, sem uma fase intermediária de Disponibilidade limitada.

>[!TIP]
>
> Se possuir interesse em obter acesso antecipado a recursos na Versão beta ou em Disponibilidade limitada, entre em contato com o representante da Adobe para discutir as opções de participação.


## Rótulos de disponibilidade {#availability-labels}

A tabela abaixo descreve cada rótulo de disponibilidade usado nos caminhos de versão, o que significa para acesso e suporte e o que esperar em cada estágio.

| **Rótulo** | **Propósito** | **Disponibilidade** | **Observações principais** |
|------------|-------------|------------------|----------------|
| **Beta** | Teste antecipado e coleta de feedback. | Restrito a clientes ou organizações selecionados que participam do programa Beta da Adobe. | - Não destinado ao uso em produção.<br>- A funcionalidade ou o design podem mudar antes da disponibilidade geral.<br>- O feedback ajuda a refinar a implementação final. |
| **Disponibilidade limitada (LA)** | Implantação controlada para validação e monitoramento. | Habilitado somente para clientes ou ambientes selecionados (por exemplo: sandboxes de desenvolvimento). | - Pronto para produção e com suporte total.<br>- Usado para validar o desempenho e a escalabilidade antes da versão geral.<br>- O acesso exige aprovação da Adobe. |
| **Disponibilidade geral (GA)** | Lançamento amplo de funcionalidade totalmente compatível. | Habilitado por padrão para todas as organizações elegíveis. | - Pronto para produção e com suporte total.<br> - Podem ser aplicáveis licenças ou autorizações.<br> - Pode ser implantado progressivamente nas regiões. |


## Implantação e disponibilidade {#rollout}

Mesmo após um anúncio de GA, a implantação pode ocorrer gradualmente nas organizações ou regiões. Se um novo recurso não aparecer imediatamente no ambiente, ele normalmente estará disponível em alguns dias após o lançamento.

Essa implantação gradual ajuda a Adobe a monitorar a estabilidade, o desempenho e a experiência do usuário antes de concluir a implantação.


## Manter-se informado(a) {#staying-informed}

Para se manter atualizado(a):

* Revise as [**notas de versão mais recentes**](release-notes.md) para obter recursos novos e atualizados.
* Verifique a seção **_Atualizações mais recentes_** entre os lançamentos mensais para implantações em tempo real.
* Monitore as **Notas de pré-lançamento** (quando disponíveis) para uma visualização dos recursos futuros.
* Entre em contato com o representante da Adobe para obter informações sobre o acesso ou os direitos da Versão beta ou da Disponibilidade limitada.

Você pode assinar **alertas por email e no produto** para as versões de produto do [!DNL Journey Optimizer]. Para inscrever-se:

1. Acesse as **Preferências da Adobe Experience Cloud**
1. Em **Notificações**, localize **Journey Optimizer**
1. Habilitar notificações por email e no aplicativo de **Novas versões**

![Painel de preferências de notificação da Adobe Experience Cloud para Journey Optimizer, com notificações no aplicativo e por email habilitadas para as categorias Alertas, Aprovações e Novas Versões](assets/do-not-localize/pulse-notif.png){width="70%"}

## Perguntas frequentes {#faq}

Você encontrará abaixo Perguntas frequentes sobre o ciclo de lançamento do [!DNL Adobe Journey Optimizer].

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer a pergunta ou conecte-se à [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}.

+++ Quando as versões do [!DNL Adobe Journey Optimizer] estão agendadas?

O [!DNL Adobe Journey Optimizer] normalmente lança atualizações durante a última semana de cada mês. No final de cada trimestre, o lançamento pode ser antecipado em até duas semanas para se alinhar a atualizações entre soluções ou em toda a plataforma.

+++

+++ Por que não vejo um novo recurso imediatamente após seu anúncio?

Alguns recursos de Disponibilidade geral são implantados progressivamente para garantir a estabilidade e o desempenho da plataforma. Caso não veja um recurso imediatamente, ele aparecerá quando a implantação for concluída na sua região ou organização.

+++

+++ Qual é a diferença entre Beta, Disponibilidade limitada e Disponibilidade geral?

* **Beta**: fase de testes antecipados, acesso limitado, baseada em comentários.
* **Disponibilidade limitada (LA)**: implantação controlada para validação final.
* **Disponibilidade geral (GA)**: versão completa para todos os clientes autorizados.

+++

+++ Todos os recursos passam pelo Beta e pela Disponibilidade limitada?

Não. Alguns recursos são lançados diretamente em disponibilidade geral ou somente em disponibilidade limitada, dependendo da sua natureza e do seu preparo. O caminho de lançamento é personalizado para cada recurso, a fim de equilibrar agilidade, qualidade e estabilidade.

+++

+++ Como posso participar de programas do Beta ou da Disponibilidade limitada?

O acesso é por convite ou solicitação por meio de um representante da Adobe. A participação ajuda a dar forma ao design de recursos e garante que seus casos de uso sejam considerados na versão final.

+++

+++ Com que frequência as notas de versão são atualizadas?

As notas de versão são atualizadas continuamente. Além dos lançamentos mensais, a seção _Atualizações mais recentes_ é atualizada sempre que novos recursos ou melhorias são encaminhados para a produção.

+++
