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
source-git-commit: d645b6528fa7a1ae5169f129613f9085672e2ebb
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 19%
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

Os seguintes recursos e melhorias estão chegando aos canais nesta versão.

<table>
<thead>
<tr>
<th><strong>Canal de saída personalizado (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Os </strong> canais de saída personalizados permitem que os administradores levem qualquer canal de mensagens baseado em HTTP de saída — como WeChat, Kakao Talk, Messenger ou um provedor proprietário — diretamente para a Journey Optimizer por meio de um Channel Builder sem código. Depois de configurados, os canais personalizados ficam disponíveis em campanhas, jornadas e campanhas orquestradas, com o mesmo conjunto completo de recursos dos canais nativos: personalização com o editor de expressão, experimentação de conteúdo, pré-visualização e prova, relatórios prontos para uso e aplicação de consentimento e governança.</p>
<p>Com esta versão, os canais de saída personalizados também ganham vários novos recursos:</p>
<ul>
<li>Use o Journey Optimizer Decisioning na carga útil do canal personalizado por meio do Editor do Personalization, da mesma forma que nas experiências baseadas em código.</li>
<li>Aplique regras de negócios a canais personalizados, da mesma forma que já é possível em canais nativos.</li>
<li>Selecione canais personalizados na lista de canais para campanhas acionadas por API, o que não era possível anteriormente.</li>
<li>Defina um webhook de relatórios para um canal personalizado e anexe-o a uma configuração de canal, para que você possa enriquecer seus relatórios do Journey Optimizer com eventos de interação.</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Canal de email {#sep-26-email-channel}

Os seguintes recursos e melhorias estão chegando ao canal de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Substituir configurações do canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ao criar suas jornadas e campanhas, agora é possível substituir os parâmetros de email derivados da configuração de canal selecionada diretamente no nível de jornada ou ação de campanha.</p>
<p>Isso permite personalizar os campos de cabeçalho de email (<strong>Do nome</strong>, <strong>Do prefixo de email</strong>, <strong>Responder ao nome</strong> e <strong>Responder ao email</strong>), o endereço de execução e os valores de cancelamento de inscrição na lista, usando atributos de perfil ou dados contextuais para obter um controle mais preciso. Especificamente, isso permite que os detalhes do remetente reflitam o supervisor, o local ou a ramificação relevante para cada recipient, em vez de rotear todos os envios por meio de um único endereço corporativo.</p>
</td>
</tr>
</tbody>
</table>

* **Substituição da lista de supressão no nível de ação de email** - o Journey Optimizer agora permite substituir o comportamento da lista de supressão diretamente no nível de ação de email em jornadas e campanhas. Isso proporciona às equipes mais flexibilidade para comunicações operacionais ou críticas para conformidade que exigem uma configuração de envio dedicada, preservando os controles de lista de supressão global existentes para todos os outros envios. Esse aprimoramento ajuda as organizações a lidar com cenários de exceção com precisão sem alterar seu modelo de governança de supressão mais amplo.

* **Validação da sintaxe de URL na criação de email** - o Journey Optimizer agora valida URLs anteriormente no fluxo de criação de email e fornece orientações mais claras quando sintaxe mal formada é detectada. Isso ajuda os autores a identificar problemas antes da finalização, reduzir erros de publicação e melhorar a confiança do delivery.

### Designer de email {#sep-26-email-designer}

Os seguintes recursos e melhorias estão chegando ao Designer de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte ao modo escuro para variantes de tema de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os temas de email agora oferecem suporte ao modo escuro, para que cada variante de cor possa ser renderizada com uma aparência personalizada para os recipients que visualizam seu email em um cliente habilitado para o modo escuro.</p>
<p>Quando habilitada, uma paleta escura padrão é gerada automaticamente para cada variante, e você pode personalizá-la ainda mais com uma paleta diferente ou com suas próprias cores personalizadas, independentemente do design do modo claro. Portanto, as alterações feitas em um modo não afetam o outro.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Importar modelos do Dynamic Media diretamente de arquivos do PSD no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O componente Dynamic Media do Designer de email agora permite importar um arquivo do Photoshop (PSD) diretamente como um novo modelo, além de navegar pelos modelos existentes do Dynamic Media. Arraste e solte um arquivo do PSD no componente e o Adobe Journey Optimizer o converte automaticamente em um modelo do Dynamic Media armazenado no Dynamic Media — não é necessária nenhuma conversão manual ou viagem de ida e volta pelo Adobe Experience Manager. Após a importação, o modelo é editado com o editor dinâmico de mídia integrado, a mesma experiência usada para o conteúdo Adobe Express no Designer de email.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novo componente de tabela no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Designer de email agora inclui um <strong>componente de Tabela</strong> interno, permitindo que você estruture o conteúdo em linhas e colunas diretamente no seu email. Arraste e solte o componente na tela, personalize o número de linhas e colunas e estilize cada célula independentemente para criar layouts claros e organizados sem depender de HTML personalizados.</p>
</td>
</tr>
</tbody>
</table>

* **Fontes substitutas para fontes personalizadas em temas de email** - Agora é possível definir uma fonte substituta para qualquer fonte personalizada (da Web) aplicada por temas de email. Se o cliente de email de um assinante não oferecer suporte à fonte personalizada, o Adobe Journey Optimizer exibirá automaticamente a fonte de fallback especificada, em vez de deixar a opção para o padrão do cliente de email. Isso mantém a tipografia de email mais próxima das diretrizes da sua marca e reduz as inconsistências de renderização de fonte nos clientes de email.
