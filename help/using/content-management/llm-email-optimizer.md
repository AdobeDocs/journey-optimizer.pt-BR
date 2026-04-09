---
title: Otimizar texto de email para caixas de entrada de IA
description: Refine a camada de texto simples do email no Journey Optimizer para que os clientes da caixa de entrada assistida por IA possam usar suas ofertas e CTAs quando resumirem a intenção de email ou extração — no Designer de email com Otimizar com IA.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# Otimizar texto de email para caixas de entrada de IA {#email-text-optimizer}

O [!DNL Adobe Journey Optimizer] vem com um recurso de canal de email que ajuda a estruturar a [versão do texto](../email/text-version-email.md) de suas mensagens para experiências aprimoradas de caixa de entrada assistida por IA, como [!DNL Apple Intelligence] e [!DNL Google Gemini] em [!DNL Gmail], para que eles possam responder às perguntas e resumir os emails com base no seu conteúdo com mais precisão, com melhores resultados.

>[!NOTE]
>
>Esse recurso altera somente o texto sem formatação, não a versão HTML do seu conteúdo de email.

Com esse otimizador de texto de email, você pode garantir que a versão em texto simples do seu conteúdo de email seja aprimorada para experiências de caixa de entrada assistida por IA, para que as informações fornecidas aos recursos de IA desses provedores de caixa de entrada de email sejam exatamente as que você deseja fornecer.

## Como funciona {#how-it-works}

As perguntas mais comuns que os destinatários podem fazer na caixa de entrada assistida por IA são *Sobre o que se trata este email?* ou *Quais são estas ofertas?*.

* As respostas fornecidas por esses assistentes de IA podem ser um breve resumo (por exemplo, que a mensagem é promocional, menciona acesso antecipado e uma venda do VIP e inclui links para categorias de produto), mas ainda omitem objetivos com os quais o profissional de marketing se preocupou, pois os assistentes estão inferindo de qualquer texto que veem efetivamente, não necessariamente a história completa que você pretendia.

* Além disso, os assistentes podem pesquisar proativamente por descontos ou cupons relacionados à marca e dobrá-los na resposta, para que o usuário não esteja mais olhando apenas para o que a sua mensagem realmente prometeu. Esse comportamento é útil para usuários finais, mas dilui o controle para profissionais de marketing que precisam de respostas para rastrear os termos reais no envio.

Para evitar esses problemas, [!DNL Journey Optimizer] reescreve o texto sem formatação para que cupons, intervalos de desconto, planos de ação e outras prioridades apareçam antecipadamente em uma cópia linear clara. O objetivo é usar a IA da caixa de entrada para criar resumos e perguntas e respostas em suas ofertas e ações definidas, em vez de se apoiar em uma parte de texto padrão fina ou em resultados da Web não relacionados.

>[!IMPORTANT]
>
>Os comportamentos exatos do assistente de IA dependem do provedor da caixa de entrada e da versão do modelo. Após o email ser entregue, as respostas e os resumos fornecidos pelos clientes externos de IA podem estar incorretos, incompletos ou misturados com os resultados da Web.
>
>O recurso Otimizar texto de email para caixas de entrada de IA melhora apenas o texto simples criado no Journey Optimizer; não garante como um assistente de terceiros interpretará ou exibirá a mensagem. Leia mais sobre as [limitações e riscos da IA de caixa de entrada de terceiros](#inbox-ai-risks).

## Casos de uso recomendados {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **Texto denso ou fragmentado gerado automaticamente** — Quando é difícil digitalizar o texto sem formatação padrão, a otimização pode produzir uma narrativa linear mais clara com ofertas e links explícitos.

* **Controlando perguntas e respostas da caixa de entrada** — Quando você espera que os destinatários perguntem aos assistentes *sobre o que é o email* ou *quais são as ofertas*, uma versão de texto sem formatação forte reduz os resumos parciais e reduz a dependência de respostas fornecidas pela Web que não estão vinculadas à sua cópia aprovada.

## Otimizar para experiências na caixa de entrada de IA {#optimize-with-ai}

>[!IMPORTANT]
>
>Antes de começar a usar este recurso, leia os [Riscos e limitações relacionados](#inbox-ai-risks).
>
>Para acessar este recurso, você deve concordar com um contrato de usuário que exiba a primeira vez que usar a IA gerativa no [!DNL Journey Optimizer]. Para obter mais informações, leia as [Diretrizes de usuário da IA gerativa da Adobe Experience Cloud](https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

Para otimizar a versão em texto sem formatação do seu email para caixas de entrada da IA com o [!DNL Journey Optimizer], siga as etapas abaixo.

1. Abra seu email no [Designer de Email](../email/content-from-scratch.md) (de uma campanha, jornada ou modelo, dependendo do seu fluxo de trabalho).

1. Selecione o ícone de **[!UICONTROL Texto sem formatação]** para abrir a versão de texto do seu email. [Saiba mais](../email/text-version-email.md)

   ![Selecione o ícone de texto sem formatação para abrir a versão de texto do seu email](assets/text-optimizer-text-icon.png){zoomable="yes"}

1. A versão de texto do email é exibida. Clique no botão **[!UICONTROL Otimizar para Caixa de Entrada de IA]** para gerar uma versão de texto simples aprimorada que destaque as principais informações para leitura e resumo assistidos por IA.

   ![Botão Otimizar para Caixa de Entrada de IA na exibição de versão de texto](assets/text-optimizer-for-ai-button.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >Ao clicar no botão **[!UICONTROL Otimizar para Caixa de Entrada de IA]**, a opção **[!UICONTROL Sincronizar com o HTML]** é automaticamente desabilitada. [Saiba mais](../email/text-version-email.md#plain-text-custom)

1. Se esta for a primeira vez que você está usando a IA Gerativa em [!DNL Journey Optimizer], você será solicitado a concordar com o contrato de usuário. Para saber mais, confira as [Diretrizes de usuário da IA gerativa da Adobe](https://www.adobe.com/br/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Caixa de diálogo de contrato de usuário de IA gerativa no Journey Optimizer](assets/text-optimizer-agreement.png){width=50%}

   Clique em **[!UICONTROL Concordar]** para continuar.

1. O texto gerado é exibido. Revise as alterações, edite-as se necessário e salve seu email como de costume.

   ![Texto gerado na exibição de versão de texto](assets/text-optimizer-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >O otimizador de texto de email atualiza somente o corpo de texto simples. Isso não altera o design, o layout ou as imagens do HTML.

1. Você pode voltar para a versão HTML do seu email a qualquer momento clicando no ícone **[!UICONTROL Alternar para o modo de exibição de Área de Trabalho]**. As alterações feitas na versão em texto são preservadas.

   >[!CAUTION]
   >
   >Se você habilitar novamente a opção **[!UICONTROL Sincronizar com o HTML]**, suas alterações serão perdidas e substituídas pelo conteúdo de texto gerado da versão do HTML.

## Riscos e limitações da IA da caixa de entrada de terceiros {#inbox-ai-risks}

O recurso Otimizar texto de email para caixas de entrada de IA ajuda a preparar texto sem formatação sobre como os provedores de caixa de correio podem processar os envios do [!DNL Journey Optimizer]. Não abrange os produtos desses fornecedores. Depois que uma mensagem é entregue, todos os recursos de IA em [!DNL Gmail], [!DNL Apple] Email, [!DNL Outlook] ou outros clientes operam sob seus termos, modelos e políticas, não a Adobe.

* **Apresentação imprevisível** — Resumos, notificações e respostas de conversas podem omitir ofertas, preços ou datas incorretos, mesclar conteúdo com resultados da Web não relacionados ou parafrasear de maneiras que não correspondem mais à sua cópia aprovada. O comportamento muda quando os fornecedores atualizam os modelos ou a interface do usuário sem aviso prévio.

* **Nenhuma garantia de paridade com o HTML** — Destinatários que dependem de visualizações ou respostas de assistentes podem nunca ver o design, as imagens ou os rodapés legais completos do HTML. O que eles acreditam na mensagem &quot;diz&quot; pode vir apenas de um resumo curto gerado por IA.

* **Uso de privacidade, conformidade e dados** — a IA da Caixa de Entrada pode processar o conteúdo de mensagens na infraestrutura do provedor de acordo com a política de privacidade, retenção e regras regionais desse provedor. As organizações de setores regulamentados devem avaliar se o uso desses recursos pelo recipient afeta suas obrigações, independentemente de como o email foi criado em [!DNL Journey Optimizer].

* **Exposição legal e de marca** — Resumos de IA incorretos ou incompletos ainda podem gerar confusão no cliente ou disputas sobre promoções, termos ou linguagem de recusa. O otimizador melhora a camada de texto fornecida; ele não garante que o modelo de terceiros a reproduza fielmente.

* **[!UICONTROL Otimizar para a caixa de entrada de IA]** em [!DNL Journey Optimizer] — A ação de tempo de criação no Designer de Email é um sistema separado dos assistentes da caixa de entrada do usuário final. Sempre revise o texto simples gerado antes de enviar.

## Tópicos relacionados {#related-topics}

* [Gerenciar a versão de texto de um email](../email/text-version-email.md)
* [Introdução ao design de email](../email/get-started-email-design.md)
* Para obter os recursos gerativos do Adobe de forma mais ampla, consulte [Introdução ao Assistente de IA para criar conteúdo](gs-generative.md).
