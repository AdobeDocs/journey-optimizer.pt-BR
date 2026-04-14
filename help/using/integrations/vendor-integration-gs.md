---
solution: Journey Optimizer
product: journey optimizer
title: Integração de fornecedores
description: Use as Integrações do Adobe Journey Optimizer com qualquer plataforma externa que exponha uma API válida, além de padrões de fornecedores testados pela engenharia para obter confiança ao projetar sua configuração.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: integração, fornecedor, terceiros
source-git-commit: 8a2c90b22dbe68de57bbdbe06123a957e54648a6
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# Introdução à integração de fornecedores {#vendor-integration}

>[!BEGINSHADEBOX]

Índice:

* [Trabalhar com integrações](external-sources.md)
* **[Introdução à integração de fornecedores](vendor-integration-gs.md)**
* [Fornecedores disponíveis](vendor-integration.md)
* [Perguntas frequentes](vendor-integration-faq.md)

>[!ENDSHADEBOX]

Você pode usar **Integrações** no Adobe Journey Optimizer para chamar **sistemas externos via HTTP** quando cada sistema expõe um **endpoint de API** que se adapta ao seu caso de uso e é compatível com a forma como as Integrações emite solicitações e consome respostas. Para obter o fluxo de trabalho completo, consulte [Trabalhar com integrações](external-sources.md).

A lista de soluções de terceiros descrita é ilustrativa, não exaustiva. Outras plataformas podem ser utilizadas se satisfizerem os requisitos do produto.

## Medidas de proteção operacionais {#operational-guardrails}

Aplique o seguinte ao configurar qualquer integração neste guia ou em um fornecedor semelhante:

* **Formato de resposta:** campos do mapa de integrações de **respostas JSON**. Criar chamadas para que a API retorne o JSON adequado para mapeamento no momento da criação.
* **Carga e campos:** solicite e mapeie apenas os atributos necessários. Respostas menores reduzem a latência e limitam a exposição de dados confidenciais.
* **Forma do ponto de extremidade:** prefira a recuperação estável de **recurso único** (por exemplo, uma entrada, produto ou membro) sobre pontos de extremidade de lista ou paginação amplos quando o produto esperar pesquisas direcionadas. Consulte [Limitações e exclusões](#limitations-exclusions) e [Trabalhar com integrações](external-sources.md).
* **Volume e confiabilidade:** Respeite os **limites de taxa** do fornecedor. Configure a política **timeout**, **repetir** e **cache** para seu canal (por exemplo, email em lote vs. envios transacionais) e valide sob carga.
* **Segurança:** armazene e gire tokens, chaves de API e credenciais OAuth de acordo com as políticas da sua organização. Não incorpore segredos no conteúdo da mensagem.

## Limitações e exclusões {#limitations-exclusions}

A lista de soluções de terceiros é **ilustrativa**, não exaustiva. As APIs do fornecedor, os hosts, os limites de taxa e as formas de resposta JSON podem mudar. Confirme os endpoints, a autenticação e o mapeamento de campo com a documentação atual do fornecedor e sua assinatura. Os padrões aqui pressupõem chamadas **orientadas para leitura** adequadas para personalização. Write-back, exportações em lote ou respostas não-JSON podem estar fora do escopo, a menos que seja observado.

## Navegação rápida {#quick-navigation}

Use esses links agrupados para ir rapidamente para o padrão do fornecedor relevante:

* **Conteúdo e CMS:** [Conteúdo](#contentful), [Sitecore](#sitecore), [Salsify](#salsify), [Contentstack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Fidelidade e recompensas:** [Voucherify](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Fidelidade do Salesforce](#salesforce-loyalty), [Capilar](#capillary)
* **Modelos e mensagens:** [Stensul](#stensul), [Marigold](#marigold), [Recomendações da Adobe Target](#adobe-target-recommendations)
* **Dados, clima e operações:** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Revisões, consentimento e redes sociais:** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)
