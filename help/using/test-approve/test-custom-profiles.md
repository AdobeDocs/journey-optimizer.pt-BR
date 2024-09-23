---
solution: Journey Optimizer
product: journey optimizer
title: Teste o conteúdo usando perfis de amostra
description: Saiba como visualizar conteúdo de email e enviar provas usando perfis de amostra.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6b3518645b9cbfbe6f728011b0889c28fa754496
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Teste o conteúdo usando perfis de amostra {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simular usando perfis de amostra"
>abstract="Nesta tela, você pode visualizar o conteúdo do email e enviar provas enquanto representa perfis de amostra que você pode carregar de um arquivo CSV ou adicionar manualmente diretamente nesta tela."


<!--ATTENTE CONFIRMATION 

- nom (custom/sample)
- campaigns/journeys ou que campaigns

-->

>[!AVAILABILITY]
>
>No momento, esses recursos estão disponíveis como uma versão beta somente para usuários selecionados.

O Jornada otimizer permite visualizar e testar o conteúdo de email usando perfis de amostra que você pode fazer upload de um arquivo CSV ou adicionar manualmente diretamente ao simular o conteúdo. Esse recurso permite que você selecione perfis de amostra a serem usados para visualizar seu conteúdo e enviar provas. Todos os atributos de perfis usados em seu conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados para seus testes.

Para acessar esta experiência, clique no botão **[!UICONTROL Simular conteúdo]** e escolha **[!UICONTROL Simular com CSV(Beta)]**.

![](assets/simulate-sample.png)


As principais etapas para testar seu conteúdo são as seguintes:

1. Adicione até 30 perfis de amostra, fazendo upload de um arquivo CSV ou adicionando-os manualmente, um por um. [Saiba como adicionar perfis de exemplo](#profiles)
1. Verifique a pré-visualização do conteúdo usando os perfis adicionados. [Saiba como visualizar seu conteúdo](#preview)
1. Envie até 10 provas para os endereços de email enquanto representa os perfis de amostra desejados. [Saiba como enviar provas](#proofs)


## Medidas de proteção e limitações {#limitations}

Antes de começar a testar seu conteúdo usando perfis de amostra, considere as seguintes medidas de proteção e pré-requisitos.

* Até o momento, o teste usando perfis de amostra só está disponível em campanhas e para o canal de email.
* Os seguintes recursos não estão disponíveis na experiência atual: renderização da caixa de entrada, relatórios de spam, conteúdo multilíngue e experimento de conteúdo. Para usar esses recursos, selecione o botão **[!UICONTROL Simular conteúdo]** no seu conteúdo para acessar a interface de usuário anterior.
* Somente atributos de perfil são suportados no momento. Se atributos contextuais forem usados em seu conteúdo para personalização, você não poderá testar seu conteúdo usando esses atributos.
* Somente os seguintes tipos de dados são suportados ao inserir dados para seus perfis de amostra: number (inteiro e decimal), string, boolean e date type. Qualquer outro tipo de dados mostrará um erro.

## Adicionar perfis de amostra {#profiles}

Você pode adicionar até 30 perfis de amostra para testar o conteúdo usando um arquivo CSV ou manualmente:

* Para carregar perfis de um arquivo CSV, clique no link **[!UICONTROL Baixar modelo]** para recuperar um modelo de arquivo CSV. Esses modelos incluem uma coluna para cada atributo de perfil usado em seu conteúdo para personalização.

  Preencha o arquivo CSV e clique em **[!UICONTROL Carregar perfis de amostra]** para carregá-lo e testar seu conteúdo.

* Para adicionar um perfil manualmente, clique no botão **[!UICONTROL Criar perfil de amostra]** e preencha as informações do perfil. Um campo é exibido para cada atributo de perfil usado no conteúdo para personalização.

  ![](assets/simulate-custom-add.png)

Depois que os perfis forem selecionados, uma caixa será exibida para cada perfil no lado esquerdo da tela. Você pode usar esses perfis para pré-visualizar seu conteúdo e enviar provas.

>[!NOTE]
>
>Os perfis de amostra adicionados servem apenas como fins de teste para o conteúdo atual. Os não são armazenados no Adobe Experience Platform, mas na sessão do navegador do usuário, o que significa que não serão exibidos ao fazer logoff ou se estiverem trabalhando em outro dispositivo.

## Pré-visualize seu conteúdo usando perfis de amostra {#preview}

Para visualizar o conteúdo usando um dos perfis, selecione a caixa relevante para atualizar a visualização do conteúdo na seção direita com as informações inseridas para esse perfil.

Você pode remover uma caixa a qualquer momento usando o botão de reticências no canto superior direito e selecionando **[!UICONTROL Remover]**. Para editar informações de um perfil, clique no botão de reticências e selecione **[!UICONTROL Editar]**.

![](assets/simulate-custom-boxes.png)

## Enviar provas {#proofs}

O Journey Optimizer permite enviar provas para endereços de email enquanto representa um ou vários perfis de amostra adicionados na tela de simulação. As etapas são as seguintes:

1. Verifique se perfis de exemplo foram adicionados para testar seu conteúdo e clique no botão **[!UICONTROL Enviar Prova]**.

1. No campo **[!UICONTROL Recipients]**, digite o endereço de email para o qual deseja enviar a prova e clique em **[!UICONTROL Adicionar]**. Repita a operação para enviar a prova para endereços de email adicionais. Você pode adicionar até 10 recipients de prova.

1. Na seção inferior da tela, selecione os perfis de amostra que deseja representar na prova. É possível selecionar vários perfis, nesse caso, o email incluirá quantas provas forem os perfis selecionados.

   Para obter mais informações sobre um perfil, selecione o link **[!UICONTROL Exibir detalhes do perfil]**. Isso permite exibir as informações inseridas na tela anterior para os diferentes atributos de perfil.

   ![](assets/simulate-custom-proofs.png)

1. Clique no botão **[!UICONTROL Enviar Prova]** para começar a enviar a prova.

Você pode acompanhar o envio a qualquer momento clicando no botão **[!UICONTROL Exibir provas]** na tela de conteúdo simulado.

![](assets/simulate-custom-sent-proofs.png)
