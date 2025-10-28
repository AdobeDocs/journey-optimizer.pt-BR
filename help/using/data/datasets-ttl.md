---
solution: Journey Optimizer
product: journey optimizer
title: Sobre conjuntos de dados Proteções de tempo de vida (TTL)
description: Medidas de proteção de tempo de vida dos conjuntos de dados em  [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: plataforma, data lake, criar, lake, conjuntos de dados, perfil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: c4f6b7754255ce3bf0229702b10955abf9843548
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 17%

---

# Medidas de proteção de tempo de vida (TTL) dos conjuntos de dados {#ttl-guardrail}

A partir de fevereiro de 2025, uma medida de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema do Journey Optimizer para **novas sandboxes e organizações** da seguinte maneira:

* 90 dias para dados na loja de perfis,
* 13 meses para dados no data lake.

Esta alteração está sendo implantada em **sandboxes de cliente existentes** em uma fase subsequente.

## Conjuntos de dados afetados {#datasets}

A tabela abaixo lista todos os conjuntos de dados afetados e seu respectivo tempo de vida no data lake e no armazenamento de perfis.

| Conjunto de dados | TTL do Data Lake | TTL de armazenamento de perfil |
|------|-----|-----|
| Conjunto de dados do evento de feedback de mensagem do AJO | 13 meses | 90 dias |
| Conjunto de dados de evento de experiência de rastreamento de email do AJO | 13 meses | 90 dias |
| Conjunto de dados de evento de experiência de rastreamento de push do AJO | 13 meses | 90 dias |
| Conjunto de dados da entidade AJO | 13 meses | 90 dias |
| Conjunto de dados do AJO Surfaces | 13 meses | n/d |
| Conjunto de dados do evento de atividade de entrada do AJO | 13 meses | 90 dias |
| Conjunto de dados de classificação do AJO | 13 meses | n/d |
| Conjunto de dados do evento de feedback Cco do email do AJO | 13 meses | n/d |
| Conjunto de dados do evento acpEntity | 13 meses | n/d |
| Jornadas | 13 meses | n/d |
| Jornada eventos de etapa | 13 meses | n/d |
| Repositório de objetos de decisão - Ofertas personalizadas | 13 meses | n/d |
| Repositório de objetos de decisão - Ofertas substitutas | 13 meses | n/d |
| Repositório de objetos de decisão - Posicionamentos | 13 meses | n/d |
| Repositório de objetos de decisão - Atividades | 13 meses | n/d |
| Repositório de objetos do Experience Decisioning - Itens de oferta personalizados | 13 meses | n/d |
| ODE DecisionEvents - decisão de produção | 13 meses | n/d |

## Perguntas frequentes {#faq}

Você encontrará abaixo Perguntas frequentes sobre conjuntos de dados Tempo de vida (TTL).

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer sua pergunta ou conecte-se com a [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

+++Essa alteração se aplicará somente às sandboxes de produção ou também se aplicará às sandboxes de desenvolvimento?

Essa alteração será aplicada a todos os tipos de sandbox.

+++

+++Para o TTL de 90 dias no armazenamento de perfis, os próprios perfis são afetados?

Os dados do conjunto de dados gerados pelo sistema no perfil são descartados após 90 dias, não os próprios perfis.

+++

+++Se os dados de um conjunto de dados gerado pelo sistema forem enviados para o [!DNL Customer Journey Analytics] (CJA), os dados no CJA também serão afetados pelo TTL?

Os dados em [!DNL Customer Journey Analytics] são mantidos em sincronia com o Experience Platform. Portanto, uma remoção de dados devido a um TTL em dados do conjunto de dados gerados pelo sistema também afetará os dados em [!DNL Customer Journey Analytics].

+++

+++ Os clientes podem aumentar o TTL para dados do conjunto de dados do sistema [!DNL Journey Optimizer] no armazenamento de perfil? 

As extensões TTLs não são compatíveis no momento. No entanto, está previsto o trabalho de otimização do processo TTL para permitir essas solicitações de extensão a partir do último semestre de 2025.

>[!NOTE]
>
>Os dados armazenados no perfil estão sujeitos ao direito Total de volume de dados. Portanto, qualquer aumento no armazenamento de dados no perfil como resultado de uma extensão TTL contaria em relação ao direito ao Volume de dados total. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html){target=_blank}

+++

+++Os clientes podem aumentar o TTL para os dados do conjunto de dados do sistema [!DNL Journey Optimizer] no data lake? 

As extensões TTLs não são compatíveis no momento. Os clientes podem exportar dados por meio do Destinos para reter os dados por mais tempo. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html){target=_blank}. Além disso, os clientes com um direito ao **[!DNL Data Distiller]** podem criar conjuntos de dados derivados para armazenar os dados no data lake sem um TTL. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++Os recursos a seguir serão afetados pelos TTLs? 

* **Repositório de pesquisa**: Não
* **limite de Jornada**: Não
* **Limite de oferta**: Não
* **Enviar Otimização de Tempo (STO)**: Não
* **Limite de frequência de mensagem** (ou seja, Regras de negócio): Não
* **Relatórios**: Não

  >[!NOTE]
  >
  >Um TTL já está implementado na conexão [!DNL Customer Journey Analytics] (CJA), o que reduz para 13 meses o período máximo efetivo de retrospectiva dos dados do conjunto de dados afetados.

* **Fonte de dados do Experience Platform**: não aplicável - a recuperação de eventos de experiência não tem suporte por meio de fontes de dados.
* **Atributos computados**: Sim - o cálculo de preenchimento retroativo inicial será limitado aos últimos 90 dias de dados; o atributo computado será atualizado com base em eventos incrementais para atualizações subsequentes. Assim que as atualizações subsequentes atingirem o período de retrospectiva (máximo de 6 meses), o TTL essencialmente não afetará mais o atributo calculado. Saiba mais.
* **Segmentação e redirecionamento**: sim - a segmentação depende dos dados no repositório de perfis; portanto, a retrospectiva é limitada a 90 dias nos dados do conjunto de dados afetados.
* **Rastreamento**: sim - reduz o período máximo efetivo de pesquisa dos dados do conjunto de dados afetados para 90 dias. Os dados dos conjuntos de dados afetados permanecem por 13 meses no data lake.

+++

+++Qual carimbo de data e hora é usado para aplicar o TTL (por exemplo, para casos de uso de preenchimento retroativo)? 

O carimbo de data e hora do evento é usado (ou seja, não a data de assimilação).

+++
