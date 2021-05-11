---
title: contextos de personalização no Journey Optimizer
description: Saiba em quais contextos você pode adicionar personalização
translation-type: tm+mt
source-git-commit: 568b37f0bbcb663cf7062f26b90d57d89452e862
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 2%

---

# Áreas de personalização {#personalization-areas}

![](../assets/do-not-localize/badge.png)

O conteúdo e a exibição de mensagens entregues pelo Journey Optimizer podem ser personalizados de várias maneiras diferentes.

Todos os campos associados ao ícone do editor podem abrir o editor de personalização e receber conteúdo de personalização.

![](assets/perso_icon.png)

## Personalize seus emails

Durante a criação da mensagem do canal de email, o campo **Assunto do email** é personalizável.

![](assets/perso_subject.png)

No Designer de email, é possível personalizar o conteúdo:

* Na **mensagem**: clique dentro de um bloco de texto, clique no ícone **Personalizar** na barra de ferramentas contextual e selecione **Inserir personalização** campo. Para obter mais informações sobre a interface do Designer de email, consulte esta [seção](../design-emails.md).

   ![](assets/perso_insert.png)

* Para um **link**: selecione algum texto ou imagem dentro de um bloco de texto, clique no ícone **Insert link** na barra de ferramentas contextual. Na janela , é possível adicionar um bloco de personalização clicando no ícone **Add personalization**.

   ![](assets/perso_link.png)

## Personalizar notificações por push

No **Push channel**, a personalização permite ajustar a notificação por push.

Você pode adicionar personalização nos seguintes campos:

* **Title**
* **Corpo**
* **Som personalizado**
* **Etiquetas**
* **Dados personalizados**

![](assets/perso_push.png)

Para obter uma documentação completa sobre a configuração da notificação por push, consulte [esta seção](../configure-push.md).


## Usar o editor de expressão

O editor de expressão é a peça central da personalização no Journey Optimizer.

Ela está disponível em todos os contextos onde é necessário definir personalização como emails, push e ofertas.

Na interface do editor de expressão, você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

![](assets/perso_ee1.png)

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização.

* **Perfil** : lista todas as referências associadas ao esquema de perfil descrito na documentação do  [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR).
* **Associação**  de segmento: lista todos os segmentos criados no serviço de Segmentação da Adobe Experience Platform. Mais informações sobre segmentação disponíveis [aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **Ofertas** : lista todas as ofertas associadas a uma disposição específica. Selecione a disposição e insira as ofertas no seu conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](https://experienceleague.adobe.com/docs/customer-journey-management/using/create-messages/deliver-personalized-offers.html?lang=en#about-offer-decisioning)

Na seleção, a referência é adicionada no editor.

>[!NOTE]
>
>O ícone de informações ao lado do ícone &quot;+&quot; abre uma dica de ferramenta que fornece mais detalhes para cada variável.

No exemplo a seguir, o editor de expressão permite selecionar os perfis que fazem aniversário hoje e concluir a personalização inserindo uma oferta específica correspondente a este dia.

![](assets/perso_ee2.png)




