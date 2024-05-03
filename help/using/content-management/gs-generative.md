---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao assistente de IA
description: Saiba como acessar e trabalhar com o assistente de IA do Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 98ce21578d30ac50665561438715d19d1723f4a7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 47%

---

# Introdução ao assistente de IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_content_generation"
>title="Criar o conteúdo do email"
>abstract="O assistente de IA do Adobe Journey Optimizer traz sugestões proativas de variação de conteúdo para textos e imagens. Ele está disponível para canais de email, push, SMS e web. Esse novo recurso fornece uma geração de texto e de imagens baseada em prompt."

>[!BEGINSHADEBOX]

**Índice**

* **[Introdução ao assistente de IA](gs-generative.md)**
* [Geração de email com o Assistente de IA](generative-email.md)
* [Geração de SMS com o Assistente de IA](generative-sms.md)
* [Geração de push com o Assistente de IA](generative-push.md)
* [Experimento de conteúdo com o Assistente de IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>No momento, o assistente de IA do Adobe Journey Optimizer está disponível na versão beta somente para usuários selecionados. Para participar do programa beta, entre em contato com o atendimento ao cliente da Adobe.

O assistente de IA do Adobe Journey Optimizer traz sugestões proativas de variação de conteúdo para textos e imagens. Ele está disponível para canais de email, push e SMS. Esse novo recurso fornece uma geração de texto e de imagens baseada em prompt. A geração de imagens é gerenciada pelo Adobe Firefly.

Use o assistente de IA do Journey Optimizer para otimizar o impacto da sua mensagem, experimentando diferentes títulos principais e imagens. Gere múltiplas variantes e crie um experimento para compará-las. Aproveitando o Experimento de conteúdo do Journey Optimizer, é possível definir vários tratamentos de mensagem para medir qual tem melhor desempenho para o seu público-alvo. É possível optar por variar o conteúdo da entrega ou o assunto. O público-alvo da mensagem é alocado aleatoriamente em cada tratamento para determinar qual funciona melhor de acordo com a métrica especificada. Saiba mais sobre o Experimento de conteúdo [nesta seção](../campaigns/content-experiment.md).

## Medidas de proteção e limitações {#generative-guardrails}

As diretrizes gerais para o uso do Assistente de IA no Journey Optimizer para geração de email estão listadas abaixo:

* A qualidade do conteúdo gerado é fortemente influenciada pelo objetivo/prompt de marketing definido por você. Use um prompt bem definido para que o modelo GenAI seja interpretado com precisão. 
* Faça upload do ativo da marca para ter informações precisas sobre o conteúdo da marca. Caso contrário, o conteúdo será baseado em informações disponíveis publicamente. O conteúdo carregado pode estar nos seguintes formatos: arquivos PDF, JPEG, PNG ou ZIP (com formatos de arquivo compatíveis).
* O tamanho máximo para o ativo de marca carregado é de 50 MB. Arquivos maiores ou muitas imagens podem funcionar, mas o tempo de processamento é aumentado.
* Use modelos de email criados no Adobe Campaign, de preferência [modelos de email incorporados](../email/use-email-templates.md), um modelo específico da marca ou um modelo personalizado para criar seu conteúdo de email. Modelo de e-mail com até 8-10 imagens recomendado.
* Relate quaisquer saídas problemáticas usando os ícones de miniatura para cima, miniatura para baixo ou sinalizador ao selecionar variantes.
* O uso do assistente de IA está sujeito às Diretrizes de usuário da IA gerativa da Adobe Experience Cloud. [Saiba mais](https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

As seguintes limitações se aplicam ao Assistente de IA no Journey Optimizer:

* O idioma suportado é somente em inglês.
* Disponível somente para os canais de email, push e SMS.
* O conteúdo da GenAI pode nem sempre ser preciso: compartilhe seu feedback para que nossos engenheiros possam refinar os modelos.
* Você pode fazer upload de vários ativos de marca, mas pode aproveitar apenas um para uma geração específica.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Geração de email" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>Geração de email</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="Geração de SMS" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>Geração de SMS</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Geração de push" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Geração de notificação por push</strong></a>
</div>
<p></td>
</tr></table>
