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
TQID: https://experienceleague.adobe.com/DvcQ6AcWhNIZXnTtmPozvSTp1Ait-oo-8wlo8hQ6xlI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2: id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371id: d6e5c7fd-c1d6-4137-98cd-138ccde6752fid: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 2e74574c9364113c55c9ce5dd048b2a58b60e29b
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 11%

---

# Medidas de proteção de tempo de vida (TTL) dos conjuntos de dados {#ttl-guardrail}

>[!BEGINSHADEBOX]

**Nesta página:** Entenda os limites de retenção de tempo de vida útil em conjuntos de dados gerados pelo sistema da Journey Optimizer para que você possa planejar por quanto tempo os dados de rastreamento, feedback e jornada permanecerão disponíveis e reterão os dados críticos antes que expirem.

>[!ENDSHADEBOX]

A partir de fevereiro de 2025, uma medida de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema do Journey Optimizer para **novas sandboxes e organizações** da seguinte maneira:

* 90 dias para dados na loja de perfis,
* 13 meses para dados no data lake.

Esta alteração será aplicada em **sandboxes de clientes existentes** a partir de **1º de outubro de 2026**.

## Conjuntos de dados afetados {#datasets}

A tabela abaixo lista todos os conjuntos de dados afetados e seu respectivo Tempo de vida no data lake e no [Repositório de perfis](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}.

| Conjunto de dados | TTL do Data Lake | TTL de armazenamento de perfil |
|------|-----|-----|
| Conjunto de dados do evento de feedback de mensagem do AJO | 13 meses | 90 dias |
| Conjunto de dados de evento de experiência de rastreamento de email do AJO | 13 meses | 90 dias |
| Conjunto de dados de evento de experiência de rastreamento de push do AJO | 13 meses | 90 dias |
| Conjunto de dados do AJO Surfaces | 13 meses | n/d |
| Conjunto de dados do evento de atividade de entrada do AJO | 13 meses | 90 dias |
| Conjunto de dados do evento de feedback secundário do destinatário do AJO | 13 meses | n/d |
| Conjunto de dados do evento da entidade | 13 meses | n/d |
| Jornada eventos de etapa | 13 meses | n/d |
| ODE DecisionEvents - decisão de produção | 13 meses | n/d |

## Perguntas frequentes {#faq}

Você encontrará abaixo Perguntas frequentes sobre conjuntos de dados Tempo de vida (TTL).

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer a pergunta ou conecte-se à [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}.

+++Quais tipos de conjuntos de dados estão sujeitos ao TTL?

O TTL se aplica somente a conjuntos de dados de séries temporais. Conjuntos de dados do tipo registro (como conjuntos de dados de entidade, conjuntos de dados de classificação e repositórios de objetos de decisão) não estão sujeitos ao TTL e, portanto, não aparecem na tabela Conjuntos de dados afetados acima.

+++

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
>Os dados armazenados no perfil estão sujeitos ao direito Total de volume de dados. Portanto, qualquer aumento no armazenamento de dados no perfil como resultado de uma extensão TTL contaria em relação ao direito ao Volume de dados total. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html){target=&quot;_blank}

+++

+++Os clientes podem aumentar o TTL para os dados do conjunto de dados do sistema [!DNL Journey Optimizer] no data lake? 

As extensões TTLs não são compatíveis no momento. Os clientes podem exportar dados por meio do Destinos para reter os dados por mais tempo. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html){target=&quot;_blank}. Além disso, os clientes com um direito ao **[!DNL Data Distiller]** podem criar conjuntos de dados derivados para armazenar os dados no data lake sem um TTL. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=&quot;_blank}

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

+++Como o novo TTL afeta casos de uso que exigem retenção de dados mais longa (por exemplo, excluir perfis que receberam um email nos últimos 120 dias ou limitar emails em um ano)?

A nova política de TTL limitará o período de retrospectiva para dados do conjunto de dados gerados pelo sistema no armazenamento de perfil para 90 dias e no data lake para 13 meses. Os casos de uso que exigirem acesso aos dados além desses períodos serão afetados. Por exemplo, a segmentação de público ou o limite de frequência com base em eventos com mais de 90 dias na loja de perfis não será mais possível usando conjuntos de dados do sistema.

+++

+++Quais alternativas estão disponíveis para reter dados por mais tempo do que o TTL?

Os clientes que exigem retenção mais longa têm duas opções:

* **Exportar para armazenamento externo**: exporte dados relevantes dos conjuntos de dados do AJO antes da expiração do TTL. O Adobe Journey Optimizer oferece suporte à exportação de conjuntos de dados para vários destinos de armazenamento em nuvem (Amazon S3, Azure Blob, Google Cloud Storage etc.). [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html){target=&quot;_blank}
* **Conjuntos de dados derivados do Data Distiller**: os clientes com um direito ao Data Distiller podem configurar consultas automatizadas para copiar dados críticos em um conjunto de dados derivado no data lake, que pode ser armazenado sem um TTL. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=&quot;_blank}

+++

+++O que os clientes devem fazer para se preparar para a alteração do TTL?

* Analise seus casos de uso e identifique qualquer um que exija retenção de dados além dos novos TTLs.
* Configure consultas automatizadas para copiar dados críticos em conjuntos de dados derivados antes que os dados sejam excluídos.
* Entre em contato com seu representante da Adobe para discutir sobre necessidades adicionais ou possíveis extensões TTL (planejadas para versões futuras).

+++

+++Como os clientes são notificados antes que o TTL seja aplicado nas sandboxes existentes?

A Adobe notifica os clientes afetados antes de aplicar o TTL nas sandboxes existentes. Para essa implantação, a Adobe enviou uma notificação no produto e publicou essa alteração nas notas de versão do produto, informando aos clientes com cerca de dois meses de antecedência para que a garantia entre em vigor em 1º de outubro de 2026.

+++

+++Posso excluir conjuntos de dados gerados pelo sistema da Journey Optimizer?

Os conjuntos de dados gerados pelo sistema da Journey Optimizer são protegidos e não podem ser excluídos por meio da interface do usuário padrão do Adobe Experience Platform. Esses conjuntos de dados são essenciais para a funcionalidade do Journey Optimizer e são gerenciados pelo sistema.

Se você precisar remover permanentemente um conjunto de dados de sistema da Journey Optimizer (por exemplo, para ambientes de controle de qualidade, limpeza de sandbox ou requisitos específicos de higiene de dados), entre em contato com o departamento de engenharia da Adobe ou com o Atendimento ao cliente da Adobe. Esses conjuntos de dados exigem procedimentos de back-end especializados para garantir uma remoção completa e segura.

>[!NOTE]
>
>Para limpeza de dados de rotina nesses conjuntos de dados do sistema, use as operações do **[!UICONTROL Ciclo de Vida dos Dados]** disponíveis por meio da Privacy Service para excluir registros ou identidades específicos. [Saiba mais](../privacy/data-hygiene.md)


+++
