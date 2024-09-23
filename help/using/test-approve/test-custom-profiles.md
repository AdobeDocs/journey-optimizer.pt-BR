---
solution: Journey Optimizer
product: journey optimizer
title: Testar seu conteúdo usando perfis personalizados
description: Saiba como pré-visualizar seu conteúdo e enviar provas usando perfis personalizados.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6229f295b961b0535139b64928216e40c3759947
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 1%

---


# Testar seu conteúdo usando perfis personalizados {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simular usando perfis personalizados"
>abstract="Nesta tela, você pode visualizar seu conteúdo e enviar provas enquanto representa perfis personalizados que você pode carregar de um arquivo CSV ou adicionar manualmente nesta tela."

>[!AVAILABILITY]
>
>No momento, esses recursos estão disponíveis como uma versão beta somente para usuários selecionados.
>
>A renderização da caixa de entrada e os relatórios de spam não estão disponíveis na experiência atual. Para usar esses recursos, selecione o botão **[!UICONTROL Simular conteúdo]** no seu conteúdo para acessar a interface do usuário herdada.

O Jornada otimizer permite visualizar e testar o conteúdo usando perfis personalizados que você pode carregar de um arquivo CSV ou adicionar manualmente ao simular o conteúdo.

Para acessar esta experiência, clique no botão **[!UICONTROL Simular conteúdo]** e escolha **[!UICONTROL Simular com CSV(Beta)]**.

Essa tela permite que você selecione os perfis que serão usados para visualizar seu conteúdo e enviar provas. Todos os atributos usados em seu conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados para seus testes.

As principais etapas para testar seu conteúdo são as seguintes:

1. Adicione perfis personalizados fazendo upload de um arquivo CSV ou adicionando-os manualmente, um por um. [Saiba como adicionar perfis personalizados](#profiles)
1. Verifique a pré-visualização do conteúdo usando os perfis adicionados. [Saiba como visualizar seu conteúdo](#preview)
1. Envie até 10 provas para os endereços de email enquanto representa os perfis personalizados desejados. [Saiba como enviar provas](#proofs)


## Adicionar perfis personalizados {#profiles}

É possível adicionar perfis personalizados para testar o conteúdo usando um arquivo CSV ou manualmente:

* Para carregar perfis de um arquivo CSV, clique no link **[!UICONTROL Baixar modelo]** para recuperar um modelo de arquivo CSV. Esses modelos incluem uma coluna para cada atributo de personalização usado em seu conteúdo.

  Preencha o arquivo CSV e clique em **[!UICONTROL Carregar perfis de amostra]** para carregá-lo e testar seu conteúdo.

* Para adicionar um perfil manualmente, clique no botão **[!UICONTROL Criar perfil de amostra]** e preencha as informações do perfil. Um campo é exibido para cada atributo de personalização usado no conteúdo.

  ![](assets/simulate-custom-add.png)

Depois que os perfis forem selecionados, uma caixa será exibida para cada perfil no lado esquerdo da tela. Você pode usar esses perfis para pré-visualizar seu conteúdo e enviar provas.

## Pré-visualizar seu conteúdo usando perfis personalizados {#preview}

Para visualizar o conteúdo usando um dos perfis, selecione a caixa relevante para atualizar a visualização do conteúdo na seção direita com as informações inseridas para esse perfil.

Você pode remover uma caixa a qualquer momento usando o botão de reticências no canto superior direito e selecionando **[!UICONTROL Remover]**. Para editar informações de um perfil, clique no botão de reticências e selecione **[!UICONTROL Editar]**.

![](assets/simulate-custom-boxes.png)

## Enviar provas {#proofs}

O Journey Optimizer permite enviar provas para endereços de email ao representar um ou vários perfis personalizados adicionados na tela de simulação. As etapas são as seguintes:

1. Verifique se perfis personalizados foram adicionados para testar o conteúdo e clique no botão **[!UICONTROL Enviar Prova]**.

1. No campo **[!UICONTROL Recipients]**, digite o endereço de email para o qual deseja enviar a prova e clique em **[!UICONTROL Adicionar]**. Repita a operação para enviar a prova para endereços de email adicionais. Você pode adicionar até 10 recipients de prova.

1. Na seção inferior da tela, selecione os perfis personalizados que deseja representar na prova. É possível selecionar vários perfis, nesse caso, o email incluirá quantas provas forem os perfis selecionados.

   ![](assets/simulate-custom-proofs.png)

1. Clique no botão **[!UICONTROL Enviar Prova]** para começar a enviar a prova.

Você pode acompanhar o envio a qualquer momento clicando no botão **[!UICONTROL Exibir provas]** na tela de conteúdo simulado.

![](assets/simulate-custom-sent-proofs.png)
