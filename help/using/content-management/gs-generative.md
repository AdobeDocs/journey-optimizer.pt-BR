---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao Assistente de IA no Journey Optimizer - Acelerador de conteúdo
description: Saiba como acessar e trabalhar com o Assistente de IA no Journey Optimizer - Acelerador de conteúdo
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 448568ff9ee96d4fa6dbaaa43ce2d45e38d6b920
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 42%

---

# Introdução ao Assistente de IA no Journey Optimizer - Acelerador de conteúdo {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Assistente de IA no Journey Optimizer para aceleração de conteúdo"
>abstract="Depois de criar e personalizar seu delivery, você pode usar o Assistente de IA no Journey Optimizer para aceleração de conteúdo para aprimorar seu conteúdo. Esse recurso simplifica o processo de personalização e melhoria de conteúdo, permitindo ajustar o conteúdo com uma descrição do que deseja gerar."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Fazer upload do ativo da marca"
>abstract="O menu Upload do ativo de marca permite adicionar qualquer ativo de marca com conteúdo que possa fornecer contexto adicional para o Assistente de IA no Journey Optimizer para aceleração de conteúdo ou selecionar um ativo carregado anteriormente. Essa opção garante que o Assistente de IA tenha acesso a todos os materiais necessários para aprimorar sua funcionalidade e relevância."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Termos da IA generativa da Adobe"
>abstract="O acesso a esse recurso está sujeito à aceitação das Diretrizes de usuário da IA generativa da Adobe Experience Cloud. Você deve verificar os resultados desse recurso quanto à precisão para garantir que sejam apropriados para seu caso de uso"
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Diretrizes do usuário da IA generativa da Adobe"

>[!INFO]
>
>Mergulhe na experiência prática com a [nossa demonstração interativa](https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator), criada para permitir que você explore seus recursos em primeira mão e entenda totalmente suas capacidades.


O Assistente de IA no Adobe Journey Optimizer para aceleração de conteúdo, desenvolvido pelo Microsoft Azure OpenAI e Adobe Firefly, traz sugestões proativas de variação de conteúdo para texto e imagens. Ele está disponível para canais de email, push e SMS. Esse novo recurso fornece uma geração de texto e de imagens baseada em prompt. A geração de imagens é gerenciada pelo Adobe Firefly.

Use o Assistente de IA no Adobe Journey Optimizer para aceleração de conteúdo para otimizar o impacto da sua mensagem, experimentando com diferentes títulos e imagens principais. Gere múltiplas variantes e crie um experimento para compará-las. Aproveitando o Experimento de conteúdo do Journey Optimizer, é possível definir vários tratamentos de mensagem para medir qual tem melhor desempenho para o seu público-alvo. É possível optar por variar o conteúdo da entrega ou o assunto. O público-alvo da mensagem é alocado aleatoriamente em cada tratamento para determinar qual funciona melhor de acordo com a métrica especificada. Saiba mais sobre o Experimento de conteúdo [nesta seção](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Antes de começar a usar esse recurso, leia as [Medidas de Proteção e Limitações](#generative-guardrails) relacionadas.
>
>
>* Você deve concordar com um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) antes de usar o Assistente de IA no Adobe Journey Optimizer para Aceleração de Conteúdo. Para obter mais informações, entre em contato com o seu representante da Adobe.

## Acesse o Acelerador de conteúdo do assistente de IA {#generative-access}

Para acessar o Assistente de IA no Adobe Journey Optimizer para o recurso de Aceleração de Conteúdo, os usuários precisam ter a permissão **Gerar Conteúdo**. [Saiba mais](../administration/permissions.md)

+++  Saiba como atribuir permissões relacionadas à geração de conteúdo

1. No produto **Permissões**, vá para a guia **Funções** e selecione a **Função** desejada.

1. Clique em **Editar** para modificar as permissões.

1. Adicione o recurso **Assistente de IA** e selecione **Gerar conteúdo** no menu suspenso.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Clique em **Salvar** para aplicar as alterações.

   Todos os usuários já atribuídos a esta função terão suas permissões automaticamente atualizadas.

1. Para atribuir esta função a novos usuários, navegue até a guia **Usuários** no painel **Funções** e clique em **Adicionar Usuário**.

1. Insira o nome de usuário, endereço de email ou escolha na lista e clique em **Salvar**.

1. Se o usuário não tiver sido criado anteriormente, consulte [esta documentação](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

O usuário receberá um email com instruções para acessar sua instância.

+++

## Medidas de proteção e limitações {#generative-guardrails}

As diretrizes gerais para usar o Assistente de IA no Adobe Journey Optimizer para aceleração de conteúdo para geração de email estão listadas abaixo:

* A qualidade do conteúdo gerado é fortemente influenciada pelo objetivo ou prompt de marketing definido. Use um prompt bem definido para que o modelo GenAI interprete com precisão. 
* Faça upload do ativo de marca para ter conteúdo preciso e apropriado à marca. Caso contrário, o conteúdo será baseado em informações disponíveis publicamente. O conteúdo carregado pode estar nos seguintes formatos: arquivos PDF, JPEG, PNG ou ZIP (com formatos de arquivo compatíveis).
* O tamanho máximo para o ativo de marca carregado é de 50 MB.É possível carregar arquivos maiores ou um número maior de imagens, mas o tempo de processamento aumentará.
* Use um modelo específico da marca ou personalizado para criar seu conteúdo de email usando o Assistente de IA no Adobe Journey Optimizer para aceleração de conteúdo. Modelos de e-mail com até 8-10 imagens são recomendados.
* Relate resultados problemáticos usando os ícones de “polegar para cima”, “polegar para baixo” ou o sinalizador ao selecionar variantes.
* O uso do assistente de IA está sujeito às Diretrizes de usuário da IA generativa da Adobe Experience Cloud. [Saiba mais](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Adobe Como parte do compromisso de promover a transparência no uso de ferramentas de IA gerativa na criação de mídia, o Adobe aplicará Contents credentials quando o conteúdo ou um projeto que inclui um ativo gerado por Firefly for baixado ou exportado. [Saiba mais](https://helpx.adobe.com/firefly/using/content-credentials.html)

As seguintes limitações se aplicam ao Assistente de IA no Adobe Journey Optimizer para aceleração de conteúdo:

* O idioma suportado é somente em inglês. Entradas em outros idiomas podem produzir resultados inconsistentes ou errôneos. Questões decorrentes de respostas em outros idiomas não serão tratadas ou melhoradas no momento.
* Disponível somente para os canais de email, push, web e SMS.
* O conteúdo de GenAI nem sempre é preciso: compartilhe seu feedback para que a equipe de engenheiros(as) possa refinar os modelos.
* É possível fazer upload de vários ativos de marca, mas aproveitando apenas um para uma geração específica.


## Recursos de geração de conteúdo do AI Assistant {#generative-features}


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
<td>
<a href="generative-web.md">
<img alt="Geração na Web" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>Geração de página da Web</strong>
</div>
<p>
</td>
</tr></table>
