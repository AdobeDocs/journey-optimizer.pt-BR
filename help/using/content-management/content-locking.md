---
solution: Journey Optimizer
product: journey optimizer
title: Bloquear conteúdo em modelos de email
description: Saiba como bloquear conteúdo em seus modelos de email.
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 2a666364144cf320a9ed20741da7d6f5d22b0d96
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 3%

---


# Bloquear conteúdo em modelos de email {#lock-content-email-templates}

O Journey Optimizer permite bloquear o conteúdo em modelos de email, bloqueando todo o modelo ou estruturas e componentes específicos. Isso permite evitar edições ou exclusões não intencionais, dando a você maior controle sobre a personalização do modelo e melhorando a eficiência e a confiabilidade de suas campanhas de email.

>[!AVAILABILITY]
>
>Os usuários com permissões para criar modelos de conteúdo podem ativar o bloqueio.

O bloqueio de conteúdo pode ser aplicado no nível **estrutura** ou no nível **componente**. Estes são os principais princípios que se aplicam no nível da estrutura e do componente ao bloquear o conteúdo no seu modelo.

* Quando uma estrutura está bloqueada:

   * Todo o conteúdo dessa estrutura também é bloqueado por padrão.
   * Nenhum conteúdo pode ser adicionado à estrutura.
   * Por padrão, não é possível excluir a estrutura. É possível substituir essa restrição ativando a opção &quot;Permitir exclusão&quot;.
   * Componentes de conteúdo individuais dentro da estrutura bloqueada podem ser definidos como editáveis.

* Quando uma estrutura é editável (estrutura não bloqueada):

   * Os componentes de conteúdo individuais podem ser bloqueados dentro dessa estrutura.
   * Por padrão, não é possível excluir um componente se ele estiver bloqueado ou se a opção &quot;Somente bloqueio de conteúdo editável&quot; estiver selecionada. É possível substituir essa restrição ativando a opção &quot;Permitir exclusão&quot;.

## Bloquear um modelo de email {#define}

### Habilitar bloqueio de conteúdo {#enable}

Você pode ativar o bloqueio de conteúdo para um modelo de email diretamente no Designer de email, independentemente de você estar criando um novo modelo ou editando um existente. Siga estas etapas:

1. Abra ou crie um modelo de email e acesse a tela de edição de conteúdo no Designer de email.

1. No painel **[!UICONTROL Corpo]** à direita, alterne a opção **[!UICONTROL Governança]**.

1. Na lista suspensa **[!UICONTROL Modo]**, selecione o modo de bloqueio desejado para o modelo:

   * **[!UICONTROL Bloqueio de conteúdo]**: bloquear seções específicas de conteúdo no modelo. Por padrão, todas as estruturas e componentes se tornam editáveis. Em seguida, você pode bloquear seletivamente elementos individuais.
   * **[!UICONTROL Somente leitura]**: bloqueia todo o conteúdo do modelo, impedindo modificações.

   ![](assets/template-lock-enable.png)

1. Se você selecionou o modo **[!UICONTROL Bloqueio de conteúdo]**, poderá definir ainda mais como os usuários podem interagir com o modelo. Ative a opção **[!UICONTROL Habilitar edição de conteúdo]** e escolha uma das seguintes opções:

   * **[!UICONTROL Permitir adição de estrutura e conteúdo]**: os usuários podem adicionar estruturas entre as existentes e adicionar componentes ou fragmentos de conteúdo em estruturas editáveis.

   * **[!UICONTROL Permitir somente adição de conteúdo]**: os usuários podem adicionar componentes ou fragmentos de conteúdo dentro de estruturas editáveis, mas não podem adicionar ou duplicar estruturas.

1. Após selecionar o modo de bloqueio, é possível definir quais estruturas e/ou componentes serão bloqueados se você tiver selecionado o modo **[!UICONTROL Bloqueio de conteúdo]**:

   * [Saiba como bloquear estruturas](#lock-structures)
   * [Saiba como bloquear componentes](#lock-components)

   Se você escolher o modo **[!UICONTROL Somente leitura]**, poderá prosseguir com a finalização e salvamento do modelo como de costume.

Você pode ajustar as configurações de **[!UICONTROL Governança]** a qualquer momento ao criar o modelo selecionando o corpo do modelo. Para fazer isso, clique no link **[!UICONTROL Corpo]** no painel de navegação localizado na parte superior do painel do lado direito.

![](assets/template-lock-body.png)

### Bloquear estruturas {#lock-structures}

Para bloquear uma estrutura no modelo:

1. Selecione a estrutura que deseja bloquear.

1. Na lista suspensa **[!UICONTROL Tipo de bloqueio]**, escolha **[!UICONTROL Bloqueado]**.

   ![](assets/template-lock-structure.png)

   >[!NOTE]
   >
   >Por padrão, os usuários não podem excluir estruturas bloqueadas. Você pode substituir essa restrição habilitando a opção **[!UICONTROL Permitir exclusão]**.

Depois de bloquear uma estrutura, nenhum componente ou fragmento de conteúdo adicional pode ser duplicado ou adicionado dentro dela. Todos os componentes em uma estrutura bloqueada também são bloqueados por padrão. Para tornar um componente editável em uma estrutura bloqueada:

1. Selecione o componente que deseja desbloquear.

1. Ative a opção **[!UICONTROL Usar bloqueio específico]**.

1. Na lista suspensa **[!UICONTROL Tipo de bloqueio]**, escolha **[!UICONTROL Editável]**. Para permitir a edição de conteúdo ao bloquear estilos, selecione **[!UICONTROL Somente conteúdo editável]**. [Saiba como bloquear componentes](#lock-components)

   ![](assets/template-lock-editable-component.png)

### Bloquear componentes {#lock-components}

Para bloquear um componente específico em uma estrutura:

1. Selecione o componente e habilite a opção **[!UICONTROL Usar bloqueio específico]** no painel direito.

1. Na lista suspensa **[!UICONTROL Tipo de bloqueio]**, selecione sua opção de bloqueio preferencial:

   ![](assets/template-lock-component.png)

   * **[!UICONTROL Bloqueio de conteúdo editável somente]**: bloqueia os estilos do componente, mas permite a edição de conteúdo.
   * **[!UICONTROL Bloqueado]**: bloqueia totalmente o conteúdo e os estilos do componente.

   >[!NOTE]
   >
   >O tipo de bloqueio **[!UICONTROL Editável]** permite que os usuários editem um componente, mesmo dentro de uma estrutura bloqueada. [Saiba como bloquear estruturas](#lock-structures)

1. Por padrão, os usuários não podem excluir componentes bloqueados. Você pode habilitar a exclusão ativando a opção **[!UICONTROL Permitir exclusão]**.

### Identificar conteúdo bloqueado {#identify}

Para identificar facilmente as estruturas e os componentes bloqueados no modelo, use a **[!UICONTROL Árvore de navegação]**, localizada no menu do lado esquerdo. Esse menu fornece uma visão geral visual de todos os elementos do modelo, destacando itens bloqueados com um ícone de bloqueio e itens editáveis com um ícone de lápis.

No exemplo abaixo, a governança é ativada para o corpo do template. A *Estrutura 2* está bloqueada com o *Componente 1* editável, enquanto a *Estrutura 3* está totalmente bloqueada.

![](assets/template-lock-navigation.png)

## Usar modelos com conteúdo bloqueado {#use}

Ao usar um modelo com conteúdo bloqueado, a mensagem **[!UICONTROL Governança habilitada]** é exibida no painel direito.

Dependendo do tipo de bloqueio aplicado ao modelo, você pode executar ações diferentes nas estruturas e nos componentes do modelo. Para identificar rapidamente todas as áreas editáveis no modelo, alterne as **[!UICONTROL opções Realçar áreas editáveis]**.

Por exemplo, no modelo abaixo, todas as áreas são editáveis, exceto a imagem superior que foi bloqueada, o que significa que não é possível editá-la nem removê-la.

![](assets/template-lock-highlight.png)

Informações detalhadas sobre os diferentes tipos de bloqueio que podem ser aplicados. Consulte estas seções:

* [Bloquear estruturas](#lock-structures)
* [Bloquear componentes](#lock-components)

Estes são alguns exemplos de edição de emails e a configuração de bloqueio de conteúdo associada que foi configurada:


| Tipo de bloqueio de conteúdo | Configuração do modelo | Edição de email |
| ------- | ------- | ------- |
| Modelo de conteúdo somente leitura | ![](assets/locking-sample-read-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-read-only.png){zoomable="yes"} |
| O conteúdo completo é editável, mas os usuários não podem adicionar nenhuma estrutura ou componente | ![](assets/locking-sample-no-addition-conf.png){zoomable="yes"} | ![](assets/locking-sample-no-addition.png){zoomable="yes"} |
| Estrutura bloqueada que não pode ser excluída | ![](assets/locking-sample-structure-locked-conf.png){zoomable="yes"} | ![](assets/locking-sample-structure-locked.png){zoomable="yes"} |
| Componente com estilos bloqueados e que não pode ser excluído. Os usuários só podem modificar o conteúdo. | ![](assets/locking-sample-content-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-content-only.png){zoomable="yes"} |
| Componente editável em uma estrutura bloqueada. | ![](assets/locking-sample-editable-component-conf.png){zoomable="yes"} | ![](assets/locking-sample-editable-component.png){zoomable="yes"} |
