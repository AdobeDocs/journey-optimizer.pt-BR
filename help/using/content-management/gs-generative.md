---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao Assistente de IA no Journey Optimizer
description: Saiba como acessar e trabalhar com o Assistente de IA no Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 076de3f8cec65ebf864131d2e405ead7596b2514
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 93%

---

# Introdução ao Assistente de IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Assistente de IA no Journey Optimizer"
>abstract="Após elaborar e personalizar a entrega, é possível usar o Assistente de IA no Journey Optimizer para aprimorar o conteúdo. Esse recurso simplifica o processo de personalização e melhoria de conteúdo, permitindo ajustar o conteúdo com uma descrição do que deseja gerar."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Fazer upload do ativo da marca"
>abstract="O menu Fazer upload do ativo da marca habilita a adição de qualquer ativo da marca com conteúdo que possa fornecer contexto adicional para o Assistente de IA no Journey Optimizer ou a seleção de um ativo enviado anteriormente. Essa opção garante que o Assistente de IA tenha acesso a todos os materiais necessários para aprimorar sua funcionalidade e relevância."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Termos da IA generativa da Adobe"
>abstract="O acesso a esse recurso está sujeito à aceitação das Diretrizes de usuário da IA generativa da Adobe Experience Cloud. Você deve verificar os resultados desse recurso quanto à precisão para garantir que sejam apropriados para seu caso de uso"
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Diretrizes do usuário da IA generativa da Adobe"

>[!INFO]
>
>Mergulhe em uma experiência prática com a [nossa prévia ao vivo do recurso](https://experienceleague.adobe.com/pt-br/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}, projetada para ajudar você a explorar esses recursos em primeira mão e entendê-los totalmente.


O Assistente de IA no Adobe Journey Optimizer, com tecnologia Microsoft Azure OpenAI e Adobe Firefly, traz sugestões proativas de variação de conteúdo para texto e imagens. Este novo recurso fornece uma **geração de texto e imagem baseada em prompt**. A geração de imagens é gerenciada pelo Adobe Firefly.

O Assistente de IA oferece suporte à geração **em vários idiomas**, permitindo que você alcance e envolva diversos públicos globais. O Assistente de IA está disponível nos seguintes idiomas:

<table style="table-layout:auto; border-collapse: collapse;">
  <tbody>
    <tr style="background-color: #FFFFFF;">
      <td>
        <ul>
          <li>Francês</li>
          <li>espanhol</li>
          <li>Alemão</li>
          <li>Italiano</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Japonês</li>
          <li>Sueco</li>
          <li>Holandês</li>
          <li>Norueguês</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

Use o Assistente de IA do Adobe Journey Optimizer para otimizar o impacto da mensagem, experimentando diferentes títulos principais e imagens. Gere múltiplas variantes e crie um experimento para compará-las. Aproveitando o **Experimento de conteúdo do Journey Optimizer**, você pode definir vários tratamentos de mensagens para medir qual tem o melhor desempenho para seu público-alvo. É possível optar por variar o conteúdo da entrega ou o assunto. O público-alvo da mensagem é alocado aleatoriamente em cada tratamento para determinar qual funciona melhor de acordo com a métrica especificada. Saiba mais sobre o Experimento de conteúdo [nesta seção](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Antes de começar a usar esse recurso, consulte as [Medidas de proteção e limitações](#generative-guardrails) relacionadas.
>
>
>* Você deve aceitar um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} antes de poder usar o Assistente de IA no Adobe Journey Optimizer. Para obter mais informações, entre em contato com o representante da Adobe.

## Acessar o Assistente de IA {#generative-access}

Para acessar o recurso Assistente de IA no Adobe Journey Optimizer, os usuários precisam receber a permissão **Gerar conteúdo**. [Saiba mais](../administration/permissions.md)

+++  Saiba como atribuir permissões relacionadas à geração de conteúdo

1. No produto **Permissões**, abra a guia **Funções** e selecione a **função** desejada.

1. Clique em **Editar** para modificar as permissões.

1. Adicione o recurso **Assistente de IA** e selecione **Gerar conteúdo** no menu suspenso.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Clique em **Salvar** para aplicar as alterações.

   As permissões de todos os usuários já atribuídos a essa função serão atualizadas automaticamente.

1. Para atribuir essa função a novos usuários, navegue até a guia **Usuários** no painel **Funções** e clique em **Adicionar usuário**.

1. Insira o nome do usuário, seu endereço de email ou escolha na lista e clique em **Salvar**.

1. Se o usuário não tiver sido criado anteriormente, consulte [esta documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/users).

O usuário receberá um email com instruções para acessar a sua instância.

+++

## Medidas de proteção e limitações {#generative-guardrails}

As diretrizes gerais para usar o Assistente de IA do Adobe Journey Optimizer na geração de emails estão listadas abaixo:

* A qualidade do conteúdo gerado é fortemente influenciada pelo objetivo ou prompt de marketing definido. Use um prompt bem definido para que o modelo GenAI interprete com precisão. 
* Faça upload do ativo de marca para ter conteúdo preciso e apropriado à marca. Caso contrário, o conteúdo será baseado em informações disponíveis publicamente. O conteúdo carregado pode estar nos seguintes formatos: arquivos PDF, JPEG, PNG ou ZIP (com formatos de arquivo compatíveis).
* O tamanho máximo para o ativo de marca carregado é de 50 MB.É possível carregar arquivos maiores ou um número maior de imagens, mas o tempo de processamento aumentará.
* Use um modelo personalizado ou específico da marca para criar seu conteúdo de email usando o Assistente de IA no Adobe Journey Optimizer. Recomenda-se um modelo de email com 8-10 imagens, no máximo.
* Relate resultados problemáticos usando os ícones de “polegar para cima”, “polegar para baixo” ou o sinalizador ao selecionar variantes.
* O uso do Assistente de IA está sujeito às diretrizes do usuário para IA generativa da Adobe Experience Cloud. [Saiba mais](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Como parte de nosso compromisso de promover a transparência no uso de ferramentas de IA generativa para a criação de mídias, a Adobe aplicará Content Credentials quando um conteúdo ou projeto que inclua um ativo gerado pelo Firefly for baixado ou exportado. [Saiba mais](https://helpx.adobe.com/firefly/using/content-credentials.html)

As seguintes limitações se aplicam ao Assistente de IA no Journey Optimizer:

* Disponível somente para os canais de email, push, web e SMS.
* O conteúdo de GenAI nem sempre é preciso: compartilhe seu feedback para que a equipe de engenheiros(as) possa refinar os modelos.
* É possível fazer upload de vários ativos de marca, mas aproveitando apenas um para uma geração específica.


## Recursos de geração de conteúdo do Assistente de IA {#generative-features}


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
<img alt="Geração para a web" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>Geração de páginas da web</strong>
</div>
<p>
</td>
</tr></table>
