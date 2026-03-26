---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às páginas de destino
description: Saiba mais sobre páginas de destino no Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: destino, página de destino, início, introdução
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# Introdução às páginas de destino {#get-started-lp}

Uma página de destino é uma página da Web independente para a qual o usuário é direcionado depois de clicar em um email, site, anúncio ou qualquer outro local digital.

O [!DNL Journey Optimizer] permite criar e projetar páginas de aterrissagem para direcionar seus usuários para formulários online, onde eles podem aceitar ou recusar receber suas comunicações ou um serviço específico, como um boletim informativo.

➡️ [Saiba como configurar assinaturas e criar páginas de destino neste vídeo](#video)

## Quando usar landing pages {#when-to-use}

Use landing pages quando quiser:

* Permitir que os clientes **aceitem ou recusem** comunicações de marketing ou um serviço ou boletim informativo específico a partir de um link em um email ou campanha, incluindo listas de assinaturas para serviços direcionados. [Leia mais](lp-use-cases.md#subscription-to-a-service)
* **Coletar consentimento** antes de enviar comunicações e enviar um **email de confirmação** por aceitação ou recusa. [Leia mais](lp-use-cases.md#send-confirmation-email)
* **Capturar ou atualizar dados de perfil** usando formulários em **[!UICONTROL páginas de aterrissagem de Captura de Dados]** — para criação progressiva de perfis, preferências, registros e cenários semelhantes. [Leia mais](#data-capture-lp)
* Redirecionar usuários para um **formulário Web dedicado** sem criar uma página externa fora do [!DNL Journey Optimizer]
* Criar **páginas de aterrissagem responsivas** usando os recursos de design de conteúdo do [!DNL Journey Optimizer]

### Captura de dados com landing pages {#data-capture-lp}

As páginas de aterrissagem da **[!UICONTROL Captura de Dados]** permitem que você insira formulários publicados para que os visitantes possam enviar atributos gravados no seu conjunto de dados [!DNL Adobe Experience Platform] por meio da conexão de streaming configurada na predefinição do formulário. [Saiba como criar e incorporar formulários em uma página de aterrissagem](lp-forms.md)

>[!NOTE]
>
>A captura de dados por meio de formulários de página de aterrissagem tem suporte para **perfis conhecidos** (perfis existentes identificados em [!DNL Adobe Experience Platform]). A página de aterrissagem deve ser aberta a partir de um **link personalizado** (por exemplo, de uma campanha de email) para que a identidade do perfil possa ser resolvida quando a página for carregada.

Veja a seguir exemplos de casos de uso:

1. **Enriquecimento progressivo de perfil** — Colete atributos adicionais de clientes conhecidos, como número de telefone, data de nascimento ou local, por meio de uma página de aterrissagem personalizada para enriquecer o perfil [!DNL Experience Platform] existente para segmentação e personalização.

2. **Atualização da central de preferências** — Permita que assinantes conhecidos gerenciem suas preferências de comunicação (canal, interesses de tópico) por meio de uma página de aterrissagem, com alterações normalmente refletidas em seu perfil [!DNL Experience Platform] em cerca de 15 minutos.

3. **Registro de evento ou webinário** — capture dados específicos de eventos de perfis conhecidos em uma página de registro, atualize o perfil com atributos de registro e acione uma jornada de confirmação.

4. **Fidelidade ou inscrição no programa** — permita que os clientes existentes se inscrevam em programas de fidelidade ou níveis de associação enviando detalhes adicionais por meio de uma página de aterrissagem, enriquecendo o perfil para direcionamento downstream.

5. **Entrada de concurso ou competição** — permita que clientes conhecidos entrem em concursos ou sorteios por meio de um formulário de página de aterrissagem; capture os detalhes específicos da entrada (respostas, preferências ou declarações) e grave-os no perfil para oferecer suporte à qualificação, à seleção de vencedores e às jornadas de acompanhamento.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="Lead" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>Criar páginas de destino</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="Pouco frequente" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>Criar listas de assinatura</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Lista do Forms para páginas de aterrissagem no Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Usar formulários em suas páginas de aterrissagem</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="Validação" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>Relatórios</strong></a>
</div>
<p>
</td>
</tr></table>

## Antes de começar {#prerequisites}

Antes de criar uma landing page, conclua estas etapas de configuração:

1. **Configurar um subdomínio** — Configure um subdomínio dedicado para hospedar suas páginas de aterrissagem. [Saiba mais](lp-subdomains.md)
1. **Criar uma predefinição de página de aterrissagem** — Uma predefinição define o subdomínio e outras configurações aplicadas às suas páginas de aterrissagem. [Saiba mais](lp-presets.md#lp-create-preset)
1. **Criar uma lista de assinaturas** (para casos de uso de assinaturas) — é necessário se você deseja que os clientes assinem ou cancelem a assinatura de um serviço específico. [Saiba mais](subscription-list.md)
1. **Criar um formulário** (para casos de uso de captura de dados) — Obrigatório quando você deseja incorporar um formulário em uma página de aterrissagem de **[!UICONTROL Captura de Dados]** e enviar envios para [!DNL Experience Platform]. [Saiba mais](lp-forms.md)

## Como funciona {#how-it-works}

A criação e a implantação de uma landing page seguem esta sequência:

1. **Criar e configurar sua página de aterrissagem** — Selecione uma predefinição, configure a página principal e adicione as subpáginas necessárias. [Saiba mais](create-lp.md#create-landing-page)
1. **Criar a página** — Crie o conteúdo e o formulário da página usando o editor de arrastar e soltar de [!DNL Journey Optimizer]. [Saiba mais](design-lp.md)
1. **Testar e publicar sua página de aterrissagem** — visualize a página, teste o comportamento do formulário e publique para ativá-la. [Saiba mais](create-lp.md#test-landing-page)
1. **Link em uma mensagem ou jornada** — Adicione a URL da página de aterrissagem a uma ação de email, campanha ou jornada para que os clientes possam acessá-la. [Saiba mais](../email/message-tracking.md#insert-links)

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma lista de assinaturas, configurar páginas de aterrissagem para aceitar ou recusar um serviço, integrar a opção de aceitação/recusa a uma mensagem e configurar jornadas relevantes.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
