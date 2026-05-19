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
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b19d9237-76be-466d-a869-aacf2d72205fid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 1e0a06dddba6c5ca4c53e4b143eb7fa7763ded6b
workflow-type: tm+mt
source-wordcount: 735
ht-degree: 96%

---

# Introdução às páginas de destino {#get-started-lp}

Uma página de destino é uma página da Web independente para a qual o usuário é direcionado depois de clicar em um email, site, anúncio ou qualquer outro local digital.

O [!DNL Journey Optimizer] permite criar e projetar páginas de destino para direcionar seus usuários a formulários online, onde estes podem aceitar ou recusar receber suas comunicações ou um serviço específico, como um boletim informativo.

➡️ [Saiba como configurar assinaturas e criar páginas de destino neste vídeo](#video)

## Quando usar páginas de destino {#when-to-use}

Use páginas de destino quando quiser:

* Permitir que os clientes **aceitem ou recusem** comunicações de marketing, um serviço específico ou boletim informativo a partir de um link em um email ou campanha, incluindo listas de assinaturas para serviços direcionados. [Leia mais](lp-use-cases.md#subscription-to-a-service)
* **Obter consentimento** antes de enviar comunicações e enviar um **email de confirmação** após optar por participar ou não. [Leia mais](lp-use-cases.md#send-confirmation-email)
* **Capturar ou atualizar dados de perfil** usando formulários em páginas de destino de **[!UICONTROL Captura de dados]** — para criação progressiva de perfis, preferências, registros e cenários semelhantes. [Leia mais](#data-capture-lp)
* Redirecionar usuários para um **formulário Web dedicado** sem criar uma página externa fora do [!DNL Journey Optimizer]
* Criar **páginas de destino responsivas** usando os recursos de design de conteúdo do [!DNL Journey Optimizer]

### Captura de dados com páginas de destino {#data-capture-lp}

As páginas de destino da **[!UICONTROL Captura de dados]** permitem que você insira formulários publicados para que os visitantes possam enviar atributos gravados no seu conjunto de dados da [!DNL Adobe Experience Platform] por meio da conexão de streaming configurada na predefinição do formulário. [Saiba como criar e incorporar formulários em uma página de destino](lp-forms.md)

>[!NOTE]
>
>A captura de dados por meio de formulários de página de destino tem suporte para **perfis conhecidos** (perfis existentes identificados na [!DNL Adobe Experience Platform]). A página de destino deve ser aberta a partir de um **link personalizado** (por exemplo, de uma campanha de email) para que a identidade do perfil possa ser resolvida quando a página for carregada.

Veja a seguir exemplos de casos de uso:

1. **Enriquecimento progressivo de perfil**: colete atributos adicionais de clientes conhecidos, como número de telefone, data de nascimento ou local, por meio de uma página de destino personalizada para enriquecer o perfil da [!DNL Experience Platform] existente para segmentação e personalização.

2. **Atualização da central de preferências**: permita que assinantes conhecidos gerenciem suas preferências de comunicação (canal, interesses de tópico) por meio de uma página de destino, com alterações normalmente refletidas no perfil da [!DNL Experience Platform] em cerca de 15 minutos.

3. **Registro de evento ou webinário**: capture dados específicos de eventos de perfis conhecidos em uma página de registro, atualize o perfil com atributos de registro e acione uma jornada de confirmação.

4. **Fidelidade ou inscrição no programa**: permita que os clientes existentes se inscrevam em programas de fidelidade ou níveis de associação enviando detalhes adicionais por meio de uma página de destino, enriquecendo o perfil para direcionamento downstream.

5. **Participação em competições ou concursos**: permita que clientes conhecidos participem de competições ou sorteios por meio de um formulário em uma página de destino; capture detalhes específicos da participação (respostas, preferências ou declarações) e registre-os no perfil para dar suporte à elegibilidade, seleção de vencedores e jornadas de acompanhamento.

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
<img alt="Lista de formulários para páginas de destino no Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Use formulários em suas páginas de destino</strong></a>
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

Antes de criar uma página de destino, conclua estas etapas de configuração:

1. **Configurar um subdomínio**: configure um subdomínio dedicado para hospedar suas páginas de destino. [Saiba mais](lp-subdomains.md)
1. **Criar uma predefinição de página de destino**: uma predefinição define o subdomínio e outras configurações aplicadas às suas páginas de destino. [Saiba mais](lp-presets.md#lp-create-preset)
1. **Criar uma lista de assinaturas** (para casos de uso de assinaturas): é necessário se você deseja que os clientes assinem ou cancelem a assinatura de um serviço específico. [Saiba mais](subscription-list.md)
1. **Criar um formulário** (para casos de uso de captura de dados): obrigatório quando você deseja incorporar um formulário em uma página de destino de **[!UICONTROL Captura de dados]** e fazer envios para a [!DNL Experience Platform]. [Saiba mais](lp-forms.md)

## Como funciona {#how-it-works}

A criação e a implantação de uma página de destino seguem esta sequência:

1. **Criar e configurar a página de destino**: selecione uma predefinição, configure a página principal e adicione as subpáginas necessárias. [Saiba mais](create-lp.md#create-landing-page)
1. **Criar a página**: crie o conteúdo e o formulário da página usando o editor de arrastar e soltar do [!DNL Journey Optimizer]. [Saiba mais](design-lp.md)
1. **Testar e publicar a página de destino**: visualize a página, teste o comportamento do formulário e publique para ativá-la. [Saiba mais](create-lp.md#test-landing-page)
1. **Link em uma mensagem ou jornada**: adicione o URL da página de destino a uma ação de email, campanha ou jornada para que os clientes possam acessá-la. [Saiba mais](../email/message-tracking.md#insert-links)

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma lista de assinaturas, configurar páginas de destino para oferecer assinaturas ou cancelar assinaturas de um serviço, integrar a opção de assinatura ou cancelamento a uma mensagem e configurar jornadas relevantes.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)

➡️ **Veja na prática:** Conheça os [casos de uso da página de aterrissagem](lp-use-cases.md) para obter exemplos passo a passo sobre gerenciamento de assinatura, emails de confirmação e cenários de captura de dados.
