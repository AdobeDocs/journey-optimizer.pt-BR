---
title: Testar o e-mail rendering
description: Saiba como testar a renderização de email e entender limitações de renderização conhecidas em clientes e ambientes de email.
feature: Preview
role: User
level: Beginner
exl-id: fe077a8b-9788-4723-a1e7-32816a879af9
feature_v2: []
subfeature_v2: id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
source-git-commit: ca053767a216de5f43415c94eb7dd24cffe9dff7
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 1%

---

# Testar o e-mail rendering {#email-rendering}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como conectar sua conta Litmus ao Adobe Journey Optimizer para testar a renderização de email em clientes de email populares e entender as limitações de renderização conhecidas, incluindo ambientes de navegador da Web para dispositivos móveis.

>[!ENDSHADEBOX]

Você pode aproveitar sua conta do **Litmus** no [!DNL Journey Optimizer] para visualizar instantaneamente sua **renderização de email** em clientes de email populares. Em seguida, você pode garantir que seu conteúdo de email tenha uma ótima aparência e funcione corretamente em cada caixa de entrada.

Para verificar a renderização de email, siga estas etapas:

1. Na tela de edição de conteúdo da sua mensagem ou no Designer de email, clique em **[!UICONTROL Simular conteúdo]** e selecione **[!UICONTROL Simular conteúdo (perfis do AEP)]** na lista suspensa.

1. Selecione o botão **[!UICONTROL Renderizar email]**.

   ![](../email/assets/email-rendering-button.png)

1. Clique em **Conectar sua conta Litmus** na seção superior direita.

   ![](../email/assets/email-rendering-litmus.png)

1. Insira suas credenciais e faça logon.

   ![](../email/assets/email-rendering-credentials.png)

1. Clique no botão **Executar teste** para gerar visualizações de email.

1. Verifique seu conteúdo de email em clientes populares de desktop, móveis e baseados na Web.

   ![](../email/assets/email-rendering-previews.png)

>[!CAUTION]
>
>Ao conectar sua conta do **Litmus** com o [!DNL Journey Optimizer], você concorda que as mensagens de teste são enviadas para Litmus: uma vez enviadas, esses emails não serão mais gerenciados pelo Adobe. Como consequência, a política de retenção de dados do Litmus se aplica a esses emails, incluindo dados de personalização que podem ser incluídos nessas mensagens de teste.

## Limitações do navegador web para dispositivos móveis {#rendering-limitations}

A renderização de email pode ser diferente quando os destinatários abrem o Gmail ou o Outlook **por meio de um navegador da Web móvel** (por exemplo, Chrome em um telefone), em vez de usar um aplicativo móvel nativo ou cliente de desktop. Essa é uma limitação conhecida dos ambientes de webmail móvel e não é específica do Journey Optimizer.

Essa diferença de renderização vem de como os clientes de webmail se comportam dentro de um navegador móvel. O navegador renderiza a interface do usuário do webmail de desktop completa primeiro, colocando o email em duas camadas, além do alcance de qualquer CSS responsivo ou consulta de mídia. O Gmail Web também desmonta blocos CSS `<style>` e envolve conteúdo de email em seu próprio `<div>`, o que pode substituir seus estilos e criar conflitos de alinhamento.

Os sintomas típicos incluem deslocamento de alinhamento de texto (texto alinhado à esquerda que aparece centralizado), linhas separadoras brancas extras entre seções de conteúdo e um layout geral que difere do design do modelo.

Esses problemas só ocorrem no Gmail Web e no Outlook Web quando acessados por um navegador móvel. Os aplicativos móveis nativos do Outlook e do Gmail, bem como todos os clientes de desktop, não são afetados.

>[!TIP]
>
>Para minimizar o impacto:
>
>* Use layouts simples baseados em tabela com CSS totalmente incorporado.
>
>* Evite depender de consultas de mídia ou blocos `<style>` para propriedades críticas de layout, como alinhamento de texto.
