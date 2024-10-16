---
title: Projetar o conteúdo da Web no aplicativo
description: Saiba como criar conteúdo da Web no aplicativo
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: no aplicativo, mensagem, criação, iniciar
hide: true
hidefromtoc: true
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Projetar o conteúdo da Web no aplicativo {#in-app-web-design}

>[!BEGINSHADEBOX]

**Índice**

* [Configurar o canal da Web no aplicativo](configure-in-app-web.md)
* [Criar sua campanha de mensagens no aplicativo da Web](create-in-app-web.md)
* Projetar o conteúdo da Web no aplicativo

>[!ENDSHADEBOX]

Para editar o conteúdo da mensagem no aplicativo, clique no botão **[!UICONTROL Editar conteúdo]** no menu **[!UICONTROL Ação]** da sua campanha.

![](assets/in_app_web_surface_7.png)

O botão de alternância **[!UICONTROL Formatação avançada]** ativa opções adicionais para personalizar a experiência.

Depois que a mensagem no aplicativo for criada e o conteúdo definido e personalizado, você poderá revisá-la e ativá-la. As notificações serão enviadas de acordo com o agendamento da campanha. Saiba mais [nesta página](send-in-app.md).

## Layout da mensagem {#message-layout}

Na seção **[!UICONTROL Layout da Mensagem]**, selecione uma das quatro opções de layout diferentes a serem escolhidas, dependendo das suas necessidades.

![](assets/in_app_web_design_1.png)

* **[!UICONTROL Tela cheia]**: esse tipo de layout cobre a tela inteira do dispositivo do público-alvo.

  É compatível com mídias (imagem, vídeo), texto e componentes de botão.

* **[!UICONTROL Modal]**: esse layout aparece em uma janela grande com estilo de alerta. O aplicativo ainda fica visível em segundo plano.

  É compatível com mídias (imagem, vídeo), texto e componentes de botão.

* **[!UICONTROL Banner]**: esse tipo de layout aparece como uma mensagem de alerta de SO nativo.

  Você só pode adicionar um **[!UICONTROL Cabeçalho]** e um **[!UICONTROL Corpo]** à sua mensagem.

* **[!UICONTROL Personalizado]**: o modo de mensagem personalizada permite importar e editar diretamente uma de suas mensagens HTML pré-configuradas.

   * Selecione **[!UICONTROL Compor]** para inserir ou colar seu código de HTML bruto.

     Use o painel esquerdo para aproveitar os recursos de personalização do Journey Optimizer. Para obter mais informações, consulte [esta seção](../personalization/personalize.md).

   * Selecione **[!UICONTROL Importar]** para importar o arquivo HTML ou .zip que contenha o conteúdo HTML.

## Guia Conteúdo {#content-tab}

Na guia **Conteúdo**, é possível definir e personalizar o conteúdo da notificação e o estilo do botão **Fechar**. Você também pode adicionar uma mídia à notificação no aplicativo e adicionar botões de ação nesta guia.

### Botão Fechar {#close-button}

![](assets/in_app_web_design_2.png)

Escolha o **[!UICONTROL Estilo]** do seu **[!UICONTROL botão Fechar]**.

Os estilos disponíveis são:

* **[!UICONTROL Simples]**
* **[!UICONTROL Círculo]**
* **[!UICONTROL Imagem personalizada]** de uma URL de mídia ou de sua Assets.

+++Mais opções com formatação avançada

Se o **[!UICONTROL Modo de formatação avançado]** estiver ativado, você poderá marcar a opção **[!UICONTROL Cor]** para escolher a cor e a opacidade do botão.

+++

### Mídia {#add-media}

O campo **[!UICONTROL Mídia]** permite adicionar mídia à mensagem no aplicativo para criar uma experiência atraente para o usuário final.

![](assets/in_app_web_design_3.png)

Digite sua URL de mídia ou clique no ícone **[!UICONTROL Selecionar Assets]** para adicionar diretamente os ativos armazenados na biblioteca do Assets à mensagem no aplicativo. [Saiba mais sobre o gerenciamento de ativos](../content-management/assets-essentials.md).
Você também pode adicionar um **[!UICONTROL texto alternativo]** para aplicativos de leitura de tela.

+++Mais opções com formatação avançada

Se o **[!UICONTROL Modo de formatação avançado]** estiver ativado, você poderá personalizar a **[!UICONTROL Altura máxima]** e a **[!UICONTROL Largura máxima]** da mídia.

+++

### Conteúdo {#title-body}

Para redigir a mensagem, insira o conteúdo nos campos **[!UICONTROL Cabeçalho]** e **[!UICONTROL Corpo]**.

![](assets/in_app_web_design_4.png)

Use o ícone **[!UICONTROL Personalization]** para adicionar personalização. Saiba mais sobre a personalização no editor de personalização do Adobe Journey Optimizer [nesta seção](../personalization/personalize.md).

+++Mais opções com formatação avançada

Se o **[!UICONTROL Modo de formatação avançado]** estiver ativado, você poderá escolher para seu **[!UICONTROL Cabeçalho]** e **[!UICONTROL Corpo]**:

* a **[!UICONTROL Fonte]**
* o **[!UICONTROL Pt tamanho]**
* a **[!UICONTROL Cor da Fonte]**
* o **[!UICONTROL Alinhamento]**
+++

### Botões {#add-buttons}

Adicione botões para a interação com mensagens no aplicativo.

![](assets/in_app_web_design_5.png)

Para personalizar o botão:

1. Edite o campo Button #1 text (primary). Você também pode usar o ícone **[!UICONTROL Personalization]** para definir dados de conteúdo e personalização.

1. Escolha o **[!UICONTROL Interagir evento]** que define a ação do botão depois que os usuários interagiram com ele.

1. Insira sua URL da Web ou deep link no campo **[!UICONTROL Target]**.

1. Para adicionar vários botões, clique em **[!UICONTROL Botão Adicionar]**.

+++Mais opções com formatação avançada

Se o **[!UICONTROL Modo de formatação avançado]** estiver ativado, você poderá escolher para seus **[!UICONTROL Botões]**:

* a **[!UICONTROL Fonte]**
* o **[!UICONTROL Pt tamanho]**
* a **[!UICONTROL Cor da Fonte]**
* o **[!UICONTROL Alinhamento]**
* o **[!UICONTROL estilo do botão]**
* o **[!UICONTROL Raio]**
* a **[!UICONTROL cor do botão]**

+++

## Guia Configurações {#settings-tab}

Na guia **Configurações**, é possível definir o layout da mensagem e pré-visualizar a mensagem no aplicativo. Você também pode acessar opções avançadas de formatação.

### Layout {#layout-options}

![](assets/in_app_web_design_6.png)

O campo **[!UICONTROL Imagem de plano de fundo]** permite adicionar um plano de fundo à mensagem no aplicativo:

* Uma mídia de um link de URL.

* Uma cor de fundo.

### Mensagem {#message-tab}

![](assets/in_app_web_design_7.png)

A opção de controle de interface do usuário, habilitada por padrão, permite escurecer o plano de fundo por trás da mensagem no aplicativo para enfatizar o foco no conteúdo.

+++Mais opções com formatação avançada

Se o **[!UICONTROL Modo de formatação avançado]** estiver ativado, você poderá personalizar ainda mais sua mensagem com as seguintes opções:

* **[!UICONTROL Personalizar tomada de controle da interface do usuário]**: permite selecionar uma cor para exibir no plano de fundo e sua opacidade.

* **[!UICONTROL Personalizar tamanho]**: permite ajustar a largura e a altura das notificações no aplicativo.

* **[!UICONTROL Personalizar posição]**: permite personalizar a posição das mensagens no aplicativo na tela dos usuários. É possível alterar os alinhamentos Vertical e Horizontal.

* **[!UICONTROL Canto arredondado da mensagem]**: permite que você adicione o canto arredondado à sua notificação no aplicativo alterando o **[!UICONTROL Raio do canto]**.

+++

**Tópicos relacionados:**

* [Teste e envie sua mensagem no aplicativo](send-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report-cja-inapp.md)
* [Configuração no aplicativo](inapp-configuration.md)