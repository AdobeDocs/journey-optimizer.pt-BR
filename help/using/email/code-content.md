---
solution: Journey Optimizer
product: journey optimizer
title: Desenvolva seu próprio conteúdo de email
description: Saiba como desenvolver seu próprio conteúdo de email
feature: Email Design
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: código, HTML, editor
exl-id: 5fb79300-08c6-4c06-a77c-d0420aafca31
source-git-commit: 48b3ef3d2e041ea49d1b0c91cc72ea04237a5e33
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 34%

---

# Programar seu próprio conteúdo {#code-content}

Use o modo **[!UICONTROL Desenvolver você mesmo]** para importar um HTML bruto e/ou desenvolver o conteúdo do email. Este método requer conhecimento sobre HTML.

➡️ [Conheça este recurso no vídeo](#video)

>[!CAUTION]
>
> Imagens de [Adobe Experience Manager Assets](../integrations/assets.md) não podem ser referenciadas ao usar este método. As imagens referenciadas no código HTML devem ser armazenadas em um local público.

1. Na página inicial do Email Designer, selecione **[!UICONTROL Codifique o seu próprio]**.

   ![](assets/code-your-own.png)

1. Digite ou cole seu código HTML bruto.

1. Use o painel esquerdo para aproveitar os recursos de personalização do [!DNL Journey Optimizer]. [Saiba mais](../personalization/personalize.md)

   ![](assets/code-editor.png)

   >[!NOTE]
   >
   >O editor de personalização no Email Designer tem algumas limitações de função em comparação às expressões de jornada. [Saiba mais sobre as limitações de função de data/hora](#date-time-limitations)

1. Se quiser limpar o conteúdo do email e criar um email utilizando um novo design, selecione **[!UICONTROL Alterar o design]** no menu de opções.

   ![](assets/code-editor-change-design.png)

   >[!NOTE]
   >
   >Essa ação abre o modelo selecionado no Designer de email. Em seguida, você pode concluir o design do seu email ou voltar para o editor de códigos usando a opção **[!UICONTROL Alternar para o editor de códigos]**.

1. Clique no botão **[!UICONTROL Visualizar]** para verificar o design da mensagem e a personalização usando perfis de teste. [Saiba mais](../content-management/preview-test.md)

   ![](assets/code-editor-preview.png)

1. Quando o código estiver pronto, clique em **[!UICONTROL Salvar]** e volte para a tela de criação de mensagens para finalizar a mensagem.

   ![](assets/code-editor-save.png)

## Limitações da função de data e hora {#date-time-limitations}

Ao usar a personalização no editor de código do Email Designer, a função `now()` não está disponível para cálculos de data dinâmicos.

>[!IMPORTANT]
>
>A função `now()` **não tem suporte** no idioma de expressão do Construtor de Email. Embora o `now()` esteja disponível em condições de jornada, ele não pode ser usado no conteúdo do email ou no editor de código.

**Alternativas disponíveis:**

Use as seguintes funções para trabalhar com a data e hora atuais na personalização de email:

* **`getCurrentZonedDateTime()`** - Retorna a data e a hora atuais com informações de fuso horário. Esta é a alternativa recomendada para `now()`.

  Exemplo: `{%= getCurrentZonedDateTime() %}` retorna `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

* **`currentTimeInMillis()`** - Retorna a hora atual em milissegundos da época.

  Exemplo: `{%= currentTimeInMillis() %}`

**Soluções alternativas:**

Se precisar realizar cálculos de data no conteúdo do email:

* **Pré-calcular campos de data** - Calcule os valores de data necessários no seu pipeline de dados ou atributos de perfil antes de enviar o email e, em seguida, faça referência a esses valores pré-calculados na sua personalização.

  Exemplo: `{%= profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate %}`

* **Usar funções de manipulação de data** - Use [funções de data/hora](../personalization/functions/dates.md) como `dayOfYear()` ou `diffInDays()` com valores de data de atributos de perfil.

  Exemplo: `{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}`

* **Usar atributos computados** - Crie [atributos computados](../audience/computed-attributes.md) que executam cálculos de data complexos, disponibilizando os resultados como atributos de perfil.

Saiba mais sobre [Funções de data e hora na personalização](../personalization/functions/dates.md).
