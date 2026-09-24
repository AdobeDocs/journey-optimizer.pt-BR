---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 16ed1a917bdc0a32bba166dc7a71c2c1d2fdea95
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 37%
---

# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer fornece de forma contínua novos recursos, melhorias para os recursos já existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

## Notas de pré-lançamento de 26 de setembro {#sep-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas podem ser lançadas posteriormente — consulte a “Data de disponibilidade” listada de cada entrada para obter detalhes.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 22 a 23 de setembro de 2026


<!--
### Onboarding {#sep-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A <strong>dedicated workspace</strong> lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

-->

### Jornadas {#sep-26-journeys}

Os recursos e melhorias a seguir estão chegando às jornadas nesta versão.

* **Eventos de etapa reduzidos para atividades de espera e de evento** - Os eventos de etapa não são mais gerados para atividades de **espera** e **evento** quando o perfil não foi realmente processado nessa atividade. <!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

### Canais {#sep-26-channels}

As seguintes melhorias estão chegando aos canais nesta versão.

* **Correspondência direta - Dividir arquivos grandes automaticamente** - Os arquivos de Correspondência Direta agora podem ser divididos em várias partes automaticamente quando excedem aproximadamente 20 GB ou manualmente escolhendo um tamanho de arquivo de destino na configuração de roteamento de arquivos.

* **Correspondência direta - Aumento do limite de público-alvo** - O limite de público-alvo do canal de correspondência direta aumentou de 3 milhões para 100 milhões de perfis, permitindo que você direcione públicos-alvo muito maiores sem encontrar erros de criação de arquivos.

### Campanhas orquestradas {#sep-26-oc}

Os recursos e melhorias a seguir estão chegando às campanhas orquestradas nesta versão.


* **Novas APIs de monitoramento de Campanhas Orquestradas** - Novas **especificações de API** estão disponíveis para campanhas orquestradas, permitindo que você crie, gerencie e acione campanhas orquestradas de forma programática, permitindo uma integração mais profunda com sistemas externos e pipelines de automação.


### Melhorias de usabilidade {#sep-26-usability}

* **Melhorias de usabilidade na experiência de Simulação de conteúdo** - A nova experiência de Simulação de conteúdo agora permite nomear e organizar suas variantes para facilitar a comparação, copiar ou excluir detalhes da variante diretamente de cada cartão, exibir caminhos completos de atributos e configuração de canal por cartão sob demanda e carregar seus próprios perfis CSV, JSON ou JSONL com um botão de carregamento mais destacado.

* **Calendário unificado para Campanhas, Jornadas e campanhas orquestradas** - A exibição de calendário para jornadas e campanhas agora sai de inventários separados em um menu unificado acessível no painel esquerdo que mostra ambos em uma exibição combinada.

