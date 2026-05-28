---
solution: Journey Optimizer
product: journey optimizer
title: Integração de fornecedores
description: Use as Integrações do Adobe Journey Optimizer com qualquer plataforma externa que exponha uma API válida, além de padrões de fornecedores testados pela engenharia para obter confiança ao projetar sua configuração.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integração, fornecedor, terceiros
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 375
ht-degree: 0%

---


# Integração de fornecedores {#vendor-integration}

Você pode usar **Integrações** no Adobe Journey Optimizer para chamar **sistemas externos via HTTP** quando cada sistema expõe um **endpoint de API** que se adapta ao seu caso de uso e é compatível com a forma como as Integrações emite solicitações e consome respostas. Para obter o fluxo de trabalho completo, consulte [Trabalhar com integrações](integrations.md).

A lista de soluções de terceiros descrita é ilustrativa, não exaustiva. Outras plataformas podem ser utilizadas se satisfizerem os requisitos do produto.

## Medidas de proteção operacionais {#operational-guardrails}

Aplique o seguinte ao configurar qualquer integração neste guia ou em um fornecedor semelhante:

* **Formato de resposta:** campos do mapa de integrações de **respostas JSON** ou **HTML**. Criar chamadas para que a API retorne JSON ou HTML adequados para mapeamento no momento da criação.
* **Carga e campos:** solicite e mapeie apenas os atributos necessários. Respostas menores reduzem a latência e limitam a exposição de dados confidenciais.
* **Forma do ponto de extremidade:** prefira a recuperação estável de **recurso único** (por exemplo, uma entrada, produto ou membro) sobre pontos de extremidade de lista ou paginação amplos quando o produto esperar pesquisas direcionadas. Consulte [Limitações e exclusões](#limitations-exclusions) e [Trabalhar com integrações](integrations.md).
* **Volume e confiabilidade:** Respeite os **limites de taxa** do fornecedor. Configure a política **timeout**, **repetir** e **cache** para seu canal (por exemplo, email em lote vs. envios transacionais) e valide sob carga.
* **Segurança:** armazene e gire tokens, chaves de API e credenciais OAuth de acordo com as políticas da sua organização. Não incorpore segredos no conteúdo da mensagem.


## Limitações e exclusões {#limitations-exclusions}

A lista de soluções de terceiros é **ilustrativa**, não exaustiva. As APIs do fornecedor, os hosts, os limites de taxa e as formas de resposta JSON ou HTML podem mudar. Confirme os endpoints, a autenticação e o mapeamento de campo com a documentação atual do fornecedor e sua assinatura. Os padrões aqui pressupõem chamadas **orientadas para leitura** adequadas para personalização. As integrações suportam o mapeamento somente de respostas **JSON** e **HTML**. **Write-back**, **exportações em lote** e respostas em qualquer outro formato não têm suporte.

## Navegação rápida {#quick-navigation}

Use esses links agrupados para ir rapidamente para o padrão do fornecedor relevante:

* **Sistema de gerenciamento de conteúdo:** [Conteúdo](vendor-integration.md#contentful), [Sitecore](vendor-integration.md#sitecore), [Salsify](vendor-integration.md#salsify), [Contentstack](vendor-integration.md#contentstack), [Akeneo](vendor-integration.md#akeneo), [Magnolia](vendor-integration.md#magnolia)
* **Fidelidade e recompensas:** [Voucherify](vendor-integration.md#voucherify), [Talon.One](vendor-integration.md#talon-one), [Antavo](vendor-integration.md#antavo), [Fidelidade do Salesforce](vendor-integration.md#salesforce-loyalty), [Capilar](vendor-integration.md#capillary)
* **Modelos, personalização e recomendações:** [Stensul](vendor-integration.md#stensul), [Marigold](vendor-integration.md#marigold), [Recomendações do Adobe Target](vendor-integration.md#adobe-target-recommendations)
* **Dados, clima e operações:** [AccuWeather](vendor-integration.md#accuweather), [ShipStation](vendor-integration.md#shipstation), [RevenueCat](vendor-integration.md#revenuecat), [Databricks](vendor-integration.md#databricks)
* **Revisões, consentimento e redes sociais:** [Bynder](vendor-integration.md#bynder), [Trustpilot](vendor-integration.md#trustpilot), [Bazaarvoice](vendor-integration.md#bazaarvoice), [OneTrust](vendor-integration.md#onetrust), [Meta](vendor-integration.md#meta), [Aprimo](vendor-integration.md#aprimo), [Epsilon (Epsilon3)](vendor-integration.md#epsilon)
