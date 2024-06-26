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
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 5%

---

# Projetar o conteúdo da Web no aplicativo {#in-app-web-design}

>[!BEGINSHADEBOX]

**Índice**

* [Configurar o canal da Web no aplicativo](configure-in-app-web.md)
* [Criar sua campanha de mensagens no aplicativo da Web](create-in-app-web.md)
* Projetar o conteúdo da Web no aplicativo

>[!ENDSHADEBOX]

Para editar o conteúdo da mensagem no aplicativo, clique no link **[!UICONTROL Editar conteúdo]** botão no **[!UICONTROL Ação]** do Campaign.

![](assets/in_app_web_surface_7.png)

A variável **[!UICONTROL Formatação avançada]** ativar/desativar ativa opções adicionais para personalizar a experiência.

Depois que a mensagem no aplicativo for criada e o conteúdo definido e personalizado, você poderá revisá-la e ativá-la. As notificações serão enviadas de acordo com o agendamento da campanha. Saiba mais [nesta página](send-in-app.md).

## Layout da mensagem {#message-layout}

No **[!UICONTROL Layout da mensagem]** selecione uma das quatro opções diferentes de layout a serem escolhidas, dependendo das suas necessidades.

![](assets/in_app_web_design_1.png)

* **[!UICONTROL Tela cheia]**: esse tipo de layout cobre a tela inteira do dispositivo do público-alvo.

  É compatível com mídias (imagem, vídeo), texto e componentes de botão.

* **[!UICONTROL Modal]**: esse layout aparece em uma janela grande com estilo de alerta. O aplicativo ainda fica visível em segundo plano.

  É compatível com mídias (imagem, vídeo), texto e componentes de botão.

* **[!UICONTROL Banner]**: esse tipo de layout é exibido como uma mensagem de alerta de SO nativo.

  Você só pode adicionar um **[!UICONTROL Cabeçalho]** e uma **[!UICONTROL Corpo]** à sua mensagem.

* **[!UICONTROL Personalizado]**: o modo de mensagem personalizada permite importar e editar diretamente uma de suas mensagens HTML pré-configuradas.

   * Selecionar **[!UICONTROL Compor]** para inserir ou colar seu código de HTML bruto.

     Use o painel esquerdo para aproveitar os recursos de personalização do Journey Optimizer. Para obter mais informações, consulte [esta seção](../personalization/personalize.md).

   * Selecionar **[!UICONTROL Importar]** para importar o arquivo HTML ou .zip que contenha o conteúdo HTML.

## Guia Conteúdo {#content-tab}

No **Conteúdo** é possível definir e personalizar o conteúdo da notificação e o estilo da notificação **Fechar** botão. Você também pode adicionar uma mídia à notificação no aplicativo e adicionar botões de ação nesta guia.

### Botão Fechar {#close-button}

![](assets/in_app_web_design_2.png)

Escolha o **[!UICONTROL Estilo]** do seu **[!UICONTROL Botão Fechar]**.

Os estilos disponíveis são:

* **[!UICONTROL Simples]**
* **[!UICONTROL Círculo]**
* **[!UICONTROL Imagem personalizada]** de um URL de mídia ou de seus Ativos.

+++Mais opções com formatação avançada

Se a variável **[!UICONTROL Modo de formatação avançado]** estiver ativada, você poderá verificar a **[!UICONTROL Cor]** para escolher a cor e a opacidade do botão.

+++

### Mídia {#add-media}

A variável **[!UICONTROL Mídia]** permite adicionar mídia à mensagem no aplicativo para criar uma experiência atraente para o usuário final.

![](assets/in_app_web_design_3.png)

Digite o URL de mídia ou clique no link **[!UICONTROL Selecionar ativos]** ícone para adicionar diretamente os ativos armazenados na biblioteca de Ativos à mensagem no aplicativo. [Saiba mais sobre o gerenciamento de ativos](../content-management/assets-essentials.md).
Você também pode adicionar um **[!UICONTROL Texto alternativo]** para aplicativos de leitura de tela.

+++Mais opções com formatação avançada

Se a variável **[!UICONTROL Modo de formatação avançado]** estiver ativada, você poderá personalizar a variável **[!UICONTROL Altura máxima]** e **[!UICONTROL Largura máxima]** de sua mídia.

+++

### Conteúdo {#title-body}

Para redigir a mensagem, insira o conteúdo nas **[!UICONTROL Cabeçalho]** e **[!UICONTROL Corpo]** campos.

![](assets/in_app_web_design_4.png)

Use o **[!UICONTROL Personalização]** ícone para adicionar personalização. Saiba mais sobre a personalização no editor de personalização do Adobe Journey Optimizer [nesta seção](../personalization/personalize.md).

+++Mais opções com formatação avançada

Se a variável **[!UICONTROL Modo de formatação avançado]** estiver ativada, você poderá escolher para sua **[!UICONTROL Cabeçalho]** e **[!UICONTROL Corpo]**:

* o **[!UICONTROL Fonte]**
* o **[!UICONTROL Tamanho Pt]**
* o **[!UICONTROL Cor da fonte]**
* o **[!UICONTROL Alinhamento]**
+++

### Botões {#add-buttons}

Adicione botões para a interação com mensagens no aplicativo.

![](assets/in_app_web_design_5.png)

Para personalizar o botão:

1. Edite o campo Button #1 text (primary). Você também pode usar a variável **[!UICONTROL Personalização]** ícone para definir o conteúdo e os dados de personalização.

1. Escolha o seu **[!UICONTROL Interagir evento]** que define a ação do botão depois que os usuários interagiram com ele.

1. Insira o URL da Web ou deep link na **[!UICONTROL Target]** campo.

1. Para adicionar vários botões, clique em **[!UICONTROL Botão Adicionar]**.

+++Mais opções com formatação avançada

Se a variável **[!UICONTROL Modo de formatação avançado]** estiver ativada, você poderá escolher para sua **[!UICONTROL Botões]**:

* o **[!UICONTROL Fonte]**
* o **[!UICONTROL Tamanho Pt]**
* o **[!UICONTROL Cor da fonte]**
* o **[!UICONTROL Alinhamento]**
* o **[!UICONTROL Estilo do botão]**
* o **[!UICONTROL Raio]**
* o **[!UICONTROL Cor do botão]**

+++

## Guia Configurações {#settings-tab}

No **Configurações** defina o layout da mensagem e visualize a mensagem no aplicativo. Você também pode acessar opções avançadas de formatação.

### Layout {#layout-options}

![](assets/in_app_web_design_6.png)

A variável **[!UICONTROL Imagem de fundo]** permite adicionar um plano de fundo à mensagem no aplicativo:

* Uma mídia de um link de URL.

* Uma cor de fundo.

### Mensagem {#message-tab}

![](assets/in_app_web_design_7.png)

A opção de controle de interface do usuário, habilitada por padrão, permite escurecer o plano de fundo por trás da mensagem no aplicativo para enfatizar o foco no conteúdo.

+++Mais opções com formatação avançada

Se a variável **[!UICONTROL Modo de formatação avançado]** estiver ativada, você poderá personalizar ainda mais sua mensagem com as seguintes opções:

* **[!UICONTROL Personalizar tomada de controle da interface]**: permite selecionar uma cor para exibir no plano de fundo e sua opacidade.

* **[!UICONTROL Personalizar tamanho]**: permite ajustar a largura e a altura das notificações no aplicativo.

* **[!UICONTROL Personalizar posição]**: permite personalizar a posição das mensagens no aplicativo na tela dos usuários. É possível alterar os alinhamentos Vertical e Horizontal.

* **[!UICONTROL Canto arredondado da mensagem]**: permite adicionar um canto redondo à notificação no aplicativo alterando o **[!UICONTROL Raio do canto]**.

+++

**Tópicos relacionados:**

* [Teste e envie sua mensagem no aplicativo](send-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)
* [Configuração no aplicativo](inapp-configuration.md)