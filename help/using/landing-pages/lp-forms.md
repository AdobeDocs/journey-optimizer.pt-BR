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
exl-id: c688ac5e-eb09-445b-a3f0-1627b40cddc8
source-git-commit: 58565932ccd2ecf95bafece71bf182fa9082cec6
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 9%

---

# Usar formulários nas páginas de aterrissagem {#lp-forms}

>[!AVAILABILITY]
>
>No momento, esse recurso está na disponibilidade limitada para clientes nos Estados Unidos e na Austrália. Entre em contato com o representante da Adobe para obter acesso.

Para capturar dados de perfil com suas páginas de aterrissagem do [!DNL Journey Optimizer] e enriquecer seus conjuntos de dados do [!DNL Experience Platform], você pode usar formulários em suas páginas de aterrissagem.

## Criar uma predefinição de formulário {#create-form-preset}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_connection"
>title="Selecionar o ponto de acesso a ser usado"
>abstract="Defina o ponto de acesso de transmissão para onde os dados serão mandados ao enviar o formulário."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Criar uma conexão de transmissão com a API HTTP"

>[!CONTEXTUALHELP]
>id="ajo_lp_form_dataset"
>title="Selecionar um conjunto de dados"
>abstract="Defina um conjunto de dados em que as respostas do formulário serão armazenadas e refletidas. É possível digitar para pesquisar um conjunto de dados específico ou selecioná-lo na lista."

Antes de criar um formulário, é necessário criar uma predefinição dedicada em que você seleciona o ponto de extremidade da conexão para o qual os dados de envio de formulário são enviados e o conjunto de dados em que os dados capturados pelo formulário serão armazenados.

Quando os dados chegam ao endpoint de transmissão, eles são vinculados às informações do conjunto de dados. Usando as conexões de origem/destino geradas e o fluxo de origem, os dados são enviados para o conjunto de dados.

Ao criar uma predefinição:

* É possível configurar várias predefinições usando diferentes combinações de conjuntos de dados e conexões de transmissão.
* O mesmo conjunto de dados ou conexão de transmissão pode ser reutilizado em várias predefinições.
* Cada conexão de transmissão gera automaticamente recursos como:
   * **conexão Source** - de onde os dados se originam.
   * **Conexão de destino** - onde os dados são armazenados ou consumidos.
   * **Fluxo do Source** - o pipeline que move os dados da conexão de origem para [!DNL Experience Platform], manipulando o mapeamento, a transformação e a validação.

<!--
>[!NOTE]
>
> To access and edit form presets, you must have the **[!UICONTROL Manage form presets]** permission on the production sandbox. Learn more about permissions in [this section](../administration/high-low-permissions.md#administration-permissions).TBC
-->

Para criar uma predefinição de formulário, siga as etapas abaixo.

1. Para acessar o inventário **[!UICONTROL Predefinições de formulário]**, selecione **[!UICONTROL Administração]** > **[!UICONTROL Canais]** >**[!UICONTROL Configurações de formulário]** no menu esquerdo.

1. Clique em **[!UICONTROL Criar predefinição de formulário]**.

1. Atualize o nome para recuperá-lo mais facilmente e adicione uma descrição, se necessário.

   ![](assets/lp_create-form-preset.png){width=80%}

1. Selecione a **[!UICONTROL Conexão de streaming]** a ser usada para esse formulário. Este é o ponto de encerramento da transmissão para onde os dados são enviados ao enviar o formulário.

   Saiba mais sobre como criar uma conexão de origem de streaming na [documentação do Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/streaming/http){target="_blank"}.

   >[!IMPORTANT]
   >
   >Para que uma conexão de transmissão da API HTTP seja exibida na lista suspensa, ela deve atender aos seguintes requisitos quando criada no Adobe Experience Platform:
   >
   >* **O tipo de dados** deve ser definido como **XDM** (não dados brutos)
   >* A **Autenticação** deve ser **desabilitada** (conexão não autenticada)
   >
   >Se a conexão de transmissão não for exibida na lista, verifique se essas duas condições foram atendidas. <!--Learn how to [create a non-authenticated connection with XDM data type](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/streaming/http#create-a-streaming-connection){target="_blank"}.-->

1. Selecione um **[!UICONTROL Conjunto de Dados]** para vincular ao formulário. É aqui que as respostas do formulário serão armazenadas e refletidas. É possível digitar para pesquisar um conjunto de dados específico ou selecioná-lo na lista.

   >[!NOTE]
   >
   >Atualmente, apenas **Conjuntos de dados** **habilitados para perfil e** Não habilitados para perfil[!DNL Adobe Experience Platform] estão disponíveis para seleção. Um conjunto de dados pode ser selecionado de cada vez. Os conjuntos de dados do sistema não podem ser usados para salvar dados de formulário. [Saiba mais sobre conjuntos de dados](../data/get-started-datasets.md)

1. Clique em **[!UICONTROL Publicar]**. Sua predefinição agora está pronta para ser usada em um formulário.

## Acessar e gerenciar formulários {#access-forms}

Para acessar a lista de formulários, selecione **[!UICONTROL Content Management]** > **[!UICONTROL Forms]** no menu esquerdo.

Todos os formulários existentes são exibidos. Você pode filtrar formulários com base no status, data de criação ou data de modificação.

![](assets/lp_form-list.png)

## Criar e projetar um formulário {#create-form}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_preset"
>title="Selecionar uma predefinição"
>abstract="Escolha uma predefinição que contenha a conexão a ser usada e um conjunto de dados predefinido para o formulário."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/landing-pages/lp-forms#create-form-preset" text="Criar uma predefinição de formulário"

Para criar um formulário, siga as etapas abaixo.

1. Na lista **[!UICONTROL Forms]**, clique em **[!UICONTROL Criar formulário]**.

1. Adicione um nome. Você pode adicionar uma descrição, se necessário.

   ![](assets/lp_create-form.png)

1. Selecione uma **[!UICONTROL Predefinição]** que contenha a conexão a ser usada e um conjunto de dados predefinido para o seu formulário. [Saiba como criar uma predefinição de formulário](#create-form-preset)

1. Clique em **[!UICONTROL Criar]**. O designer do formulário abre, o que permite que você adicione estruturas e conteúdo [componentes](../email/content-components.md#add-content-components) para criar seu conteúdo. Você pode usar componentes de [Texto](../email/content-components.md#text) e **[!UICONTROL Campo]**.

1. Para capturar dados e atributos do perfil, adicione campos específicos ao formulário. [Saiba mais](#define-fields)

1. Configure e projete esses campos. [Saiba mais](#configure-fields)

1. Você pode ajustar o layout, estilo e dimensões do formulário conforme necessário usando o painel **[!UICONTROL Estilos]**. [Saiba mais sobre estilo](../email/get-started-email-style.md)

1. Depois de configurar todos os campos, clique em **[!UICONTROL Salvar e fechar]**.

1. Configure a página Thank you. [Saiba como](#thank-you-page)

1. **[!UICONTROL Publique]** o formulário para torná-lo disponível para seleção nas páginas de aterrissagem.

### Definir campos específicos {#define-fields}

Para adicionar campos específicos ao formulário, arraste e solte uma estrutura na tela e arraste um componente **[!UICONTROL Campo]** para dentro dela.<!--**[!UICONTROL Select field attribute]** or **[!UICONTROL Add custom field]**.-->

![](assets/lp_create-form-field.png)

Em seguida, selecione uma das seguintes opções:

>[!BEGINTABS]

>[!TAB Selecionar atributo de campo]

Use essa opção para selecionar um atributo com base no esquema do conjunto de dados vinculado ao seu formulário.

>[!NOTE]
>
>O conjunto de dados é definido na predefinição selecionada para o formulário. [Saiba mais](#create-form-preset)

![](assets/lp_select-field-attribute.png){width=100%}

Por exemplo, você pode definir a ID de email e pessoa. Quando os usuários preenchem esses campos, as informações inseridas são salvas no conjunto de dados selecionado.

![](assets/lp_create-form-field-attributes.png){width=55%}

Para mapear os dados coletados com um Perfil, selecione um campo de identidade de perfil. Os campos de identidade estão marcados como **[!UICONTROL Obrigatório]** na lista de atributos - você pode filtrá-los.

![](assets/lp_create-form-required-attributes.png){width=65%}

>[!TAB Adicionar campo personalizado]

Com essa opção, é possível definir um campo livre sem mapeá-lo para um campo no conjunto de dados vinculado.

![](assets/lp_create-form-custom-field.png){width=85%}

>[!ENDTABS]

### Configurar e projetar um campo {#configure-fields}

Depois de selecionar um atributo de campo ou adicionar um campo personalizado, você pode ajustar ainda mais seus detalhes, bem como seu comportamento ao enviar o formulário.

1. Na seção **[!UICONTROL Detalhes do campo]** da guia **[!UICONTROL Conteúdo]** à direita, você pode especificar os seguintes elementos, conforme necessário:

   * Ajuste o **[!UICONTROL Rótulo]** para que fique claro para os destinatários do seu formulário.
   * Altere o **[!UICONTROL Tipo de campo]** de acordo com suas necessidades. Pode ser uma caixa de seleção, moeda, data, controle deslizante, URL etc.

     >[!NOTE]
     >
     >Os outros detalhes do campo podem variar de acordo com o tipo de campo selecionado.

   * Adicionar um **[!UICONTROL Espaço Reservado]**.<!--To explain-->
   * Especificar **[!UICONTROL Instruções]**.<!--How will they be displayed in the form? To explain-->
   * Insira um **[!UICONTROL Valor padrão]** que será exibido antes que os usuários do formulário preencham o campo.
   * Você pode definir uma **[!UICONTROL Mensagem de validação]** personalizada.
   * Defina um **[!UICONTROL Comprimento máximo]**. Uma mensagem de erro é exibida se os recipients do formulário excederem o limite ao preencher o campo.

   ![](assets/lp_create-form-field-details.png){width=85%}

1. Na seção **[!UICONTROL Comportamentos de campo]**, você pode definir o seguinte:

   * Selecione **[!UICONTROL Obrigatório]** para tornar este campo obrigatório. Se os usuários não preencherem o campo, não poderão enviar o formulário.
   * Selecione **[!UICONTROL Diferenciar]** para fazer com que o campo diferencie maiúsculas de minúsculas. <!--To confirm - do you mean retain capitalization when added to the dataset?-->
   * Selecione **[!UICONTROL Preenchimento prévio Habilitado]** para preencher o campo com as informações de perfil, se disponíveis.<!--Even for a custom field, or a field not mapped to a profile? What happens if no data is available?-->
   * Selecione **[!UICONTROL Habilitar máscara de entrada]** para substituir a entrada dos usuários por caracteres genéricos. Você pode usar *9* para significar qualquer número, *a* para significar qualquer letra ou * para significar qualquer número ou letra.<!--Not sure how you define that in the form-->

   ![](assets/lp_create-form-field-behaviors.png){width=75%}

### Configure a página de agradecimento {#thank-you-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_forms_thankyou_page"
>title="Página de agradecimento "
>abstract="Configure o que acontece quando alguém preenche ou encaminha o formulário."

De volta aos detalhes do formulário, na **[!UICONTROL página de agradecimento]**, configure o que acontece quando um usuário preenche o formulário.

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

## Editar um formulário publicado {#edit-form}

Depois que um formulário for publicado, você ainda poderá editá-lo. Siga as etapas abaixo.

1. Acesse a [lista de formulários](#access-forms) e selecione um formulário publicado.

1. Clique no botão **[!UICONTROL Editar formulário]**.

   ![](assets/lp_edit-form-button.png){width=90%}

1. Uma nova versão do formulário é criada com o status de rascunho. Clique em **[!UICONTROL Criar versão de rascunho]**.

1. Atualize o formulário conforme necessário e clique em **[!UICONTROL Salvar]**. O formulário agora tem o status **[!UICONTROL Publicado (com rascunho)]**:

   * A versão atual continua com o status **[!UICONTROL Publicado]**, até que você publique a versão atualizada.

   * A versão atualizada tem o status **[!UICONTROL Rascunho]**.

1. De volta ao resumo do formulário, você pode navegar entre as duas versões do formulário.

   ![](assets/lp_published-with-draft-form.png){width=70%}

1. Na seção **[!UICONTROL Rascunho]**, você pode publicar ou descartar o rascunho, bem como editar os detalhes ou o conteúdo do formulário.

   ![](assets/lp_edit-draft-form.png){width=75%}

## Usar o formulário em uma página de destino {#leverage-form-in-lp}

Agora é possível incorporar este formulário em uma página de aterrissagem para capturar dados correspondentes aos atributos definidos no formulário e salvá-los no conjunto de dados selecionado. Siga as etapas abaixo.

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
   >Você pode atualizar o formulário selecionado usando o botão **[!UICONTROL Editar formulário]**. O formulário é aberto em uma nova guia. As etapas para editar o conteúdo do formulário estão detalhadas em [esta seção](#create-form).

1. Na seção **[!UICONTROL Tipo de acompanhamento]**, configure o que acontece quando um usuário preenche o formulário:

   * Escolha **[!UICONTROL Formulário definido]** para selecionar a ação que foi definida no formulário inserido. [Saiba mais](#thank-you-page)

   * Você também pode selecionar uma [página de aterrissagem](create-lp.md) publicada para a qual o usuário será redirecionado após enviar o formulário.

   * Ou defina uma **[!UICONTROL URL externa]** como a página de acompanhamento para a qual os usuários são direcionados quando enviam o formulário.

1. Salve e teste sua landing page. [Saiba como](create-lp.md#test-landing-page)

Assim que a página de aterrissagem for [publicada](create-lp.md#publish-landing-page) e usada em uma jornada, quando os usuários preencherem o formulário, as informações inseridas serão assimiladas no conjunto de dados selecionado.

>[!NOTE]
>
>Se você cancelar a publicação de um formulário usado em uma landing page, editar esse formulário e publicá-lo novamente, a landing page sempre usará a versão mais recente publicada do formulário.
