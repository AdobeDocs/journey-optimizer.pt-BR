---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao Assistente de IA
description: Saiba como acessar e trabalhar com o assistente de IA do Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 267d1850cbe30b1078f3b5b5bd228364bb63edd6
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 93%

---

# Introdução ao Assistente de IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Assistente de IA"
>abstract="Depois de criar e personalizar a entrega, use o Assistente de IA para melhorar o conteúdo. Esse recurso simplifica o processo de personalização e melhoria de conteúdo, permitindo ajustar o conteúdo com uma descrição do que deseja gerar."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Definir contexto com o Assistente de IA"
>abstract="Para usar o conteúdo selecionado na geração de conteúdo, ative a opção **Usar conteúdo original**. Também é possível fazer upload dos ativos da sua marca para usar como fonte. Se você não usar o conteúdo selecionado, o upload e a seleção de ativos de uma marca serão obrigatórios."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Termos da IA generativa da Adobe"
>abstract="O acesso a esse recurso está sujeito à aceitação das Diretrizes de usuário da IA generativa da Adobe Experience Cloud. Revise qualquer saída desse recurso para precisão e verifique se ele é apropriado para seu caso de uso."
>additional-url="https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Diretrizes do usuário da IA generativa da Adobe"

>[!BEGINSHADEBOX]

**Índice**

* Introdução ao Assistente de IA
* [Geração de email com o Assistente de IA](generative-email.md)
* [Geração de SMS com o Assistente de IA](generative-sms.md)
* [Geração de push com o Assistente de IA](generative-push.md)
* [Experimento de conteúdo com o Assistente de IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>No momento, o Assistente de IA do Adobe Journey Optimizer está disponível na versão beta somente para usuários selecionados.

O Assistente de IA do Adobe Journey Optimizer, viabilizado pelo Azure OpenAI, traz sugestões proativas de variação de conteúdo para texto e imagens. Ele está disponível para canais de email, push e SMS. Esse novo recurso fornece uma geração de texto e de imagens baseada em prompt. A geração de imagens é gerenciada pelo Adobe Firefly.

Use o assistente de IA do Journey Optimizer para otimizar o impacto da sua mensagem, experimentando diferentes títulos principais e imagens. Gere múltiplas variantes e crie um experimento para compará-las. Aproveitando o Experimento de conteúdo do Journey Optimizer, é possível definir vários tratamentos de mensagem para medir qual tem melhor desempenho para o seu público-alvo. É possível optar por variar o conteúdo da entrega ou o assunto. O público-alvo da mensagem é alocado aleatoriamente em cada tratamento para determinar qual funciona melhor de acordo com a métrica especificada. Saiba mais sobre o Experimento de conteúdo [nesta seção](../content-management/content-experiment.md).

## Medidas de proteção e limitações {#generative-guardrails}

Veja abaixo uma lista de diretrizes gerais de uso do assistente de IA para geração de email no Journey Optimizer:

* A qualidade do conteúdo gerado é fortemente influenciada pelo objetivo ou prompt de marketing definido. Use um prompt bem definido para que o modelo GenAI interprete com precisão. 
* Faça upload do ativo de marca para ter conteúdo preciso e apropriado à marca. Caso contrário, o conteúdo será baseado em informações disponíveis publicamente. O conteúdo carregado pode estar nos seguintes formatos: arquivos PDF, JPEG, PNG ou ZIP (com formatos de arquivo compatíveis).
* O tamanho máximo para o ativo de marca carregado é de 50 MB.É possível carregar arquivos maiores ou um número maior de imagens, mas o tempo de processamento aumentará.
* Use modelos de email criados no Adobe Campaign, de preferência [modelos de email incorporados](../email/use-email-templates.md), modelos específicos da marca ou modelos personalizados para criar conteúdo de email. Recomenda-se um modelo de email com 8-10 imagens, no máximo.
* Relate resultados problemáticos usando os ícones de “polegar para cima”, “polegar para baixo” ou o sinalizador ao selecionar variantes.
* O uso do assistente de IA está sujeito às Diretrizes de usuário da IA generativa da Adobe Experience Cloud. [Saiba mais](https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

As seguintes limitações se aplicam ao assistente de IA no Journey Optimizer:

* Apenas o idioma inglês é compatível.
* Disponível somente para os canais de email, push e SMS.
* O conteúdo de GenAI nem sempre é preciso: compartilhe seu feedback para que a equipe de engenheiros(as) possa refinar os modelos.
* É possível fazer upload de vários ativos de marca, mas aproveitando apenas um para uma geração específica.

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
