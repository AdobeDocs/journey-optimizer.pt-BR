---
solution: Journey Optimizer
product: journey optimizer
title: Teste o conteúdo usando dados de entrada de exemplo
description: Saiba como pré-visualizar conteúdo de email e enviar provas usando dados de entrada de amostra.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 100c9ca994199a3b90650ebfbabbf0b7ac8726c2
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 7%

---


# Teste o conteúdo usando dados de entrada de exemplo {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simular usando amostra de entrada"
>abstract="Nesta tela, você pode testar diferentes variantes do seu conteúdo de email fornecendo valores para campos de personalização por meio de um modelo CSV (baixe o CSV) ou inserindo manualmente os valores."

>[!AVAILABILITY]
>
>No momento, esses recursos estão disponíveis como uma versão beta somente para usuários selecionados.

O otimizador de Jornada permite testar diferentes variantes do conteúdo de email visualizando-o e enviando provas com dados de entrada de amostra carregados de um arquivo CSV ou adicionados manualmente. Todos os atributos de perfis usados em seu conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados para seus testes criarem várias variantes.

Para acessar esta experiência, clique no botão **[!UICONTROL Simular conteúdo]** e escolha **[!UICONTROL Simular com CSV(Beta)]**.

![](assets/simulate-sample.png)

As principais etapas para testar seu conteúdo são as seguintes:

1. Adicione até 30 variantes com dados de entrada de amostra, fazendo upload de um arquivo CSV ou adicionando dados manualmente. [Saiba como adicionar variantes](#profiles)
1. Verifique a visualização do conteúdo usando as diferentes variantes. [Saiba como visualizar seu conteúdo](#preview)
1. Envie até 10 provas para endereços de email usando as diferentes variantes. [Saiba como enviar provas](#proofs)


## Medidas de proteção e limitações {#limitations}

Antes de começar a testar seu conteúdo usando exemplos de dados de entrada, considere as seguintes medidas de proteção e pré-requisitos.

* A partir de agora, o teste usando dados de entrada de amostra só está disponível para o canal de email. A experiência não pode ser acessada pelo botão &quot;Simular conteúdo&quot; no Designer de email.
* Os seguintes recursos não estão disponíveis na experiência atual: renderização da caixa de entrada, relatórios de spam, conteúdo multilíngue e experimento de conteúdo. Para usar esses recursos, selecione o botão **[!UICONTROL Simular conteúdo]** no seu conteúdo para acessar a interface de usuário anterior.
* Somente atributos de perfil são suportados no momento. Se atributos contextuais forem usados em seu conteúdo para personalização, você não poderá testar seu conteúdo usando esses atributos.
* Somente os seguintes tipos de dados são suportados ao inserir dados para suas variantes: número (inteiro e decimal), string, booleano e tipo de data. Qualquer outro tipo de dados mostrará um erro.

## Adicionar variantes {#profiles}

Você pode adicionar até 30 variantes para testar o conteúdo, usando um arquivo CSV ou manualmente:

* Para carregar dados de entrada de exemplo de um arquivo CSV, clique no link **[!UICONTROL baixar CSV]** para recuperar um modelo de arquivo CSV. Esses modelos incluem uma coluna para cada atributo de perfil usado em seu conteúdo para personalização.

  Preencha o arquivo CSV e clique em **[!UICONTROL Carregar dados de entrada]** para carregá-los e testar seu conteúdo.

* Para adicionar uma variante manualmente, clique no botão **[!UICONTROL Criar entrada de amostra]** e preencha os dados de entrada de exemplo da variante. Um campo é exibido para cada atributo de perfil usado no conteúdo para personalização.

  ![](assets/simulate-custom-add.png)

Depois que os perfis forem selecionados, uma caixa será exibida para cada variante no lado esquerdo da tela. Você pode usar esses perfis para pré-visualizar seu conteúdo e enviar provas.

>[!NOTE]
>
>As variantes adicionadas servem apenas como fins de teste para o conteúdo atual. Os não são armazenados no Adobe Experience Platform, mas na sessão do navegador do usuário, o que significa que não serão exibidos ao fazer logoff ou se estiverem trabalhando em outro dispositivo.

## Pré-visualizar suas variantes de conteúdo {#preview}

Para visualizar o conteúdo usando uma das variantes, selecione a caixa relevante para atualizar a visualização do conteúdo na seção direita com as informações inseridas para essa variante.

Você pode remover uma variante a qualquer momento usando o botão de reticências no canto superior direito e selecionando **[!UICONTROL Remover]**. Para editar informações de uma variante, clique no botão de reticências e selecione **[!UICONTROL Editar]**.

![](assets/simulate-custom-boxes.png)

## Enviar provas {#proofs}

O Journey Optimizer permite enviar provas para endereços de email enquanto representa uma ou várias variantes adicionadas na tela de simulação. As etapas são as seguintes:

1. Verifique se as variantes foram adicionadas para testar o conteúdo e clique no botão **[!UICONTROL Enviar Prova]**.

1. No campo **[!UICONTROL Recipients]**, digite o endereço de email para o qual deseja enviar a prova e clique em **[!UICONTROL Adicionar]**. Repita a operação para enviar a prova para endereços de email adicionais. Você pode adicionar até 10 recipients de prova.

1. Na seção inferior da tela, selecione a variante que deseja usar na prova. É possível selecionar várias variantes, nesse caso, o email incluirá quantas provas forem as variantes selecionadas.

   Para obter mais informações sobre uma variante, selecione o link **[!UICONTROL Exibir detalhes do perfil]**. Isso permite exibir as informações inseridas na tela anterior para as diferentes variantes.

   ![](assets/simulate-custom-proofs.png)

1. Clique no botão **[!UICONTROL Enviar Prova]** para começar a enviar a prova.

1. Para acompanhar o envio da prova, clique no botão **[!UICONTROL Exibir provas]** na tela de conteúdo simulado.

![](assets/simulate-custom-sent-proofs.png)
