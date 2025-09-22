---
solution: Journey Optimizer
product: journey optimizer
title: Criar e usar formulários para suas páginas de destino
description: Saiba como criar e usar formulários para suas landing pages no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: landing page, landing page, criação, página, formulário
badge: label="Disponibilidade limitada" type="Informative"
hidefromtoc: true
hide: true
exl-id: c688ac5e-eb09-445b-a3f0-1627b40cddc8
source-git-commit: 45ebae048a748429a1918326526f3756a3e93c4c
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 2%

---

# Usar formulários nas páginas de aterrissagem {#lp-forms}

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.

Para capturar dados de perfil com suas páginas de aterrissagem do [!DNL Journey Optimizer] e enriquecer seus conjuntos de dados do [!DNL Experience Platform], você pode usar formulários em suas páginas de aterrissagem.

## Criação de uma predefinição de formulário {#create-form-preset}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_connection"
>title="Selecione o endpoint a ser usado"
>abstract="Defina o ponto de encerramento da transmissão para onde os dados são enviados ao enviar o formulário."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Criar uma conexão de transmissão da API HTTP"

>[!CONTEXTUALHELP]
>id="ajo_lp_form_dataset"
>title="Selecionar um conjunto de dados"
>abstract="Defina um conjunto de dados em que as respostas do formulário serão armazenadas e refletidas. Você pode digitar para pesquisar um conjunto de dados específico ou selecioná-lo na lista."

Antes de criar um formulário, é necessário criar uma predefinição dedicada em que você seleciona o ponto de extremidade da conexão para o qual os dados de envio de formulário são enviados e o conjunto de dados em que os dados capturados pelo formulário serão armazenados.

Quando os dados chegam ao endpoint de transmissão, eles são vinculados às informações do conjunto de dados. Usando as conexões de origem/destino geradas e o fluxo de origem, os dados são enviados para o conjunto de dados.

Ao criar uma predefinição:

* É possível configurar várias predefinições usando diferentes combinações de conjuntos de dados e conexões de transmissão.
* O mesmo conjunto de dados ou conexão de transmissão pode ser reutilizado em várias predefinições.
* Cada conexão de transmissão gera automaticamente recursos como:
   * **conexão Source** - de onde os dados se originam.
   * **Conexão de destino** - onde os dados são armazenados ou consumidos.
   * **Fluxo do Source** - o pipeline que move os dados da conexão de origem para [!DNL Experience Platform], manipulando o mapeamento, a transformação e a validação.

>[!NOTE]
>
> Para acessar e editar predefinições de formulário, você deve ter a permissão **[!UICONTROL Gerenciar predefinições de formulário]** na sandbox de produção. Saiba mais sobre permissões em [esta seção](../administration/high-low-permissions.md#administration-permissions).<!--TBC-->

1. Para acessar o inventário **[!UICONTROL Predefinições de formulário]**, selecione **[!UICONTROL Administração]** > **[!UICONTROL Canais]** >**[!UICONTROL Configurações de formulário]** no menu esquerdo.

1. Clique em **[!UICONTROL Criar predefinição de formulário]**.

1. Atualize o nome para recuperá-lo mais facilmente e adicione uma descrição, se necessário.

   ![](assets/lp_create-form-preset.png){width=80%}

1. Selecione a **[!UICONTROL Conexão de streaming]** a ser usada para esse formulário. Este é o ponto de encerramento da transmissão para onde os dados são enviados ao enviar o formulário.

   >[!NOTE]
   >
   >Saiba mais sobre como criar uma conexão de origem de streaming na [documentação do Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/streaming/http){target="_blank"}.

1. Selecione um **[!UICONTROL Conjunto de Dados]** para vincular ao formulário. É aqui que as respostas do formulário serão armazenadas e refletidas. Você pode digitar para pesquisar um conjunto de dados específico ou selecioná-lo na lista.

   >[!NOTE]
   >
   >Atualmente, apenas [!DNL Adobe Experience Platform] conjuntos de dados estão disponíveis para seleção. Somente um conjunto de dados pode ser selecionado de cada vez.

1. Clique em **[!UICONTROL Publicar]**. Sua predefinição agora está pronta para ser usada em um formulário.

## Acessar e gerenciar formulários {#access-forms}

Para acessar a lista de formulários, selecione **[!UICONTROL Content Management]** > **[!UICONTROL Forms]** no menu esquerdo.

Todos os formulários existentes são exibidos. Você pode filtrar formulários com base no status, data de criação ou data de modificação.

## Criar um formulário {#create-form}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_preset"
>title="Selecionar uma predefinição"
>abstract="Escolha uma predefinição predefinida que contenha a conexão a ser usada e um conjunto de dados predefinido para seu formulário."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/landing-pages/lp-forms#create-form-preset" text="Criação de uma predefinição de formulário"

Para criar um formulário, siga as etapas abaixo.

1. Na lista **[!UICONTROL Forms]**, clique em **[!UICONTROL Criar formulário]**.

1. Adicione um nome. Você pode adicionar uma descrição, se necessário.

   ![](assets/lp_create-form.png)

1. Selecione uma **[!UICONTROL Predefinição]** que contenha a conexão a ser usada e um conjunto de dados predefinido para o seu formulário. [Saiba como criar uma predefinição de formulário](#create-form-preset)

1. Clique em **[!UICONTROL Criar]**.

   <!--![](assets/lp_create-form-filled.png){width=50%}-->

1. O designer do formulário é aberto. Adicione [componentes](../email/content-components.md#add-content-components) para criar o conteúdo do formulário. Você pode usar componentes de [Texto](../email/content-components.md#text) e **[!UICONTROL Campo]**.

1. Com o componente **[!UICONTROL Campo]**, é possível selecionar atributos com base no esquema do conjunto de dados selecionado.

   >[!NOTE]
   >
   >Para mapear os dados coletados com um Perfil, selecione um campo de identidade de perfil. Para identificar os campos de identidade da lista de atributos, procure os campos marcados como **[!UICONTROL Obrigatório]**.<!--Explain-->

   Por exemplo, você pode definir a ID de email e pessoa. Quando os usuários preenchem esses campos, as informações inseridas são salvas no conjunto de dados selecionado.

   ![](assets/lp_create-form-fields.png)

1. Você pode especificar cada **[!UICONTROL Detalhes do campo]**, como instruções, um valor padrão, uma mensagem de validação, comprimento máximo etc.

   ![](assets/lp_create-form-field-details.png)

1. Você pode ajustar o layout, estilo e dimensões do formulário conforme necessário usando o painel **[!UICONTROL Estilos]**. [Saiba mais sobre estilo](../email/get-started-email-style.md)

1. Clique em **[!UICONTROL Salvar e fechar]**.

1. Configure a página Thank you. [Saiba como](#thank-you-page)

1. **[!UICONTROL Publique]** o formulário para torná-lo disponível para seleção nas páginas de aterrissagem.

### Configurar a página de agradecimento {#thank-you-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_forms_thankyou_page"
>title="Página de agradecimento"
>abstract="Configure o que acontece quando alguém preenche ou encaminha o formulário."

Na seção **[!UICONTROL Página de agradecimento]**, configure o que acontece quando um usuário preenche o formulário.

![](assets/lp_create-form-thank-you.png){width=70%}

Configure uma das seguintes ações:

* **[!UICONTROL Permanecer na página]** - Essa opção mantém o visitante na mesma página quando o formulário é enviado.
* **[!UICONTROL Página de aterrissagem]** - Selecione uma [página de aterrissagem](create-lp.md) publicada para a qual o usuário será redirecionado após enviar o formulário.
* **[!UICONTROL URL Externa]** - Insira a URL completa que você deseja como página de acompanhamento. Depois que o usuário enviar o formulário, ele será direcionado para a URL especificada.
* **[!UICONTROL Redirecionamento condicional]** - Configure as regras para mostrar dinamicamente diferentes ações de acompanhamento com base nas respostas do formulário.

  É possível definir uma regra para cada público-alvo específico. Por exemplo, você pode exibir uma landing page específica para residentes dos EUA, outra página para residentes do Canadá e assim por diante. Por fim, configure uma ação padrão para usuários que não se enquadram em nenhuma regra definida por você.

  >[!NOTE]
  >
  >As condições definidas em uma regra são lidas sequencialmente.

  ![](assets/lp_create-form-thank-you-conditional.png){width=40%}

## Usar o formulário em uma página de destino {#leverage-form-in-lp}

Agora é possível incorporar esse formulário em uma página de aterrissagem para capturar dados correspondentes aos atributos definidos no formulário e salvá-los no conjunto de dados selecionado. Siga as etapas abaixo.

1. Crie uma landing page. [Saiba como](create-lp.md#create-landing-page)

1. Selecione **[!UICONTROL Captura de Dados]** como o tipo de página de aterrissagem e clique em **[!UICONTROL Criar]**.

   ![](assets/lp_create-lp-data-capture.png){width=65%}

1. Configure a página principal. [Saiba como](create-lp.md#configure-primary-page)

1. Abra o [designer da página de aterrissagem](design-lp.md).

1. Arraste e solte um **[!UICONTROL componente de Estrutura]** no seu conteúdo. Arraste e solte um componente **[!UICONTROL Formulário]** nessa estrutura.

   >[!NOTE]
   >
   >Somente formulários publicados podem ser selecionados em uma página de aterrissagem.

1. Na seção **[!UICONTROL Incorporar formulário]**, selecione o formulário criado.

   ![](assets/lp_embed-form.png)

   >[!NOTE]
   >
   >Você pode atualizar o formulário selecionado usando o botão **[!UICONTROL Editar formulário]**. O formulário é aberto em uma nova guia. As etapas para editar o conteúdo do formulário são as mesmas descritas em [esta seção](#create-form).

1. Na seção **[!UICONTROL Tipo de acompanhamento]**, configure o que acontece quando um usuário preenche o formulário:

   * Escolha **[!UICONTROL Formulário definido]** para selecionar a ação que foi definida no formulário inserido. [Saiba mais](#thank-you-page)

   * Você também pode selecionar uma [página de aterrissagem](create-lp.md) publicada para a qual o usuário será redirecionado após enviar o formulário.

   * Ou defina uma **[!UICONTROL URL externa]** como a página de acompanhamento para a qual os usuários são direcionados quando enviam o formulário.

1. Salve e teste sua landing page. [Saiba como](create-lp.md#test-landing-page)

Assim que a página de aterrissagem for [publicada](create-lp.md#publish-landing-page) e usada em uma jornada, quando os usuários preencherem o formulário, as informações inseridas serão assimiladas no conjunto de dados selecionado.

>[!NOTE]
>
>Se você cancelar a publicação de um formulário usado em uma landing page, editar esse formulário e publicá-lo novamente, a landing page sempre usará a versão mais recente publicada do formulário.
