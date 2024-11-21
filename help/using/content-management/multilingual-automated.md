---
solution: Journey Optimizer
product: journey optimizer
title: Criação do conteúdo multilíngue com tradução automática
description: Saiba mais sobre o conteúdo multilíngue no Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: introdução, iniciar, conteúdo, experimento
exl-id: 38e82eb2-67d9-4a7d-8c1f-77dab20bcec4
source-git-commit: 1b48cb825eb1f3110a27389d1e780cb1d7e80fad
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 20%

---

# Criação do conteúdo multilíngue com tradução automática {#multilingual-automated}

>[!CONTEXTUALHELP]
>id="ajo_multi_add_provider"
>title="Adicionar provedor"
>abstract="Adicione provedores de tradução e códigos de idiomas conforme necessário. Isso permite gerenciar quais provedores e códigos de idioma estão ativos no projeto, proporcionando a flexibilidade para ajustar recursos e públicos-alvo com base nos requisitos e no escopo atuais do projeto."

>[!CONTEXTUALHELP]
>id="ajo_multi_edit_provider"
>title="Editar provedor"
>abstract="Modifique os provedores de tradução existentes e adicione códigos de idiomas conforme necessário. Essa funcionalidade permite controlar quais provedores e códigos de idioma estão ativos no projeto, oferecendo a flexibilidade de ajustar recursos e públicos-alvo específicos de acordo com as necessidades e metas atuais do projeto."

>[!IMPORTANT]
>
>Para o fluxo automatizado, os usuários precisam de permissões relacionadas ao recurso **[!UICONTROL Serviço de Tradução]**. [Saiba mais sobre permissões](../administration/permissions.md)

Usando o fluxo automatizado, você pode simplesmente selecionar o idioma de destino e o provedor de idioma. Seu conteúdo é então enviado diretamente para tradução, pronto para uma revisão final após a conclusão.

Siga estas etapas para criar conteúdo multilíngue usando a tradução automática:

1. [Adicionar seu provedor](multilingual-provider.md)

1. [Adicionar códigos de idiomas (opcional)](multilingual-locale.md)

1. [Criar um projeto de idioma](#create-translation-project)

1. [Criar configurações de idioma](#create-language-settings)

1. [Criar um conteúdo multilíngue](#create-a-multilingual-campaign)

1. [Revisar sua tarefa de tradução (opcional)](#review-translation-project)

## Criar projeto de tradução {#translation-project}

>[!CONTEXTUALHELP]
>id="ajo_multi_create_project"
>title="Criar projeto"
>abstract="Para começar a criar conteúdo multilíngue, inicie o projeto de tradução, identifique o código do idioma de destino e selecione o idioma ou dialeto regional apropriado para o público-alvo. Depois disso, escolha um provedor de tradução que se alinhe às necessidades do seu projeto."

>[!CONTEXTUALHELP]
>id="ajo_multi_edit_project"
>title="Editar projeto"
>abstract="Atualize seu projeto de tradução para incorporar códigos de idioma adicionais, permitindo expandir o conteúdo para alcançar um público-alvo maior."

Inicie o projeto de tradução especificando o Local de destino, indicando o idioma ou a região específica para o conteúdo. Em seguida, você pode escolher seu Provedor de tradução.

1. No menu **[!UICONTROL Tradução]** em **[!UICONTROL Gerenciamento de conteúdo]**, clique em **[!UICONTROL Criar projeto]** na guia **[!UICONTROL Projetos]**.

   ![](assets/translation_project_1.png)

1. Digite um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]**.

1. Selecione a **[!UICONTROL localidade do Source]**.

   ![](assets/translation_project_2.png)

1. Escolha se deseja ativar as seguintes opções:

   * **[!UICONTROL Publicar automaticamente traduções aprovadas]**: depois que as traduções são aprovadas, elas são integradas automaticamente à campanha sem a necessidade de intervenção manual.
   * **[!UICONTROL Habilitar Fluxo de trabalho de revisão]**: aplicável somente a localidades traduzidas por humanos. Isso permite que um revisor interno avalie e aprove ou rejeite com eficiência o conteúdo traduzido. [Saiba mais](#review-translation-project)

1. Clique em **[!UICONTROL Adicionar localidade]** para acessar o menu e definir os idiomas do projeto de tradução.

   Se uma **[!UICONTROL Localidade]** estiver ausente, você poderá criá-la manualmente com antecedência a partir do menu **[!UICONTROL Tradução]** ou por API. Consulte [Criar uma nova Localidade](#create-locale).

   ![](assets/translation_project_3.png)

1. Selecione na lista sua(s) **[!UICONTROL localidade(s) de Destino]** e escolha qual **[!UICONTROL provedor de Tradução]** você deseja usar para cada localidade.

   As configurações do **[!UICONTROL Provedor de tradução]** podem ser acessadas no menu **[!UICONTROL Tradução]** da seção de menu **[!UICONTROL Administração]**.

   >[!NOTE]
   >
   >O gerenciamento de contratos com o Provedor de tradução está fora do escopo desse recurso. Verifique se você tem um contrato válido e ativo em vigor com o Parceiro de tradução designado.
   >
   ></br>O Provedor de Tradução detém a propriedade da qualidade do conteúdo traduzido.

1. Clique em **[!UICONTROL Adicionar uma localidade]** quando terminar de vincular a localidade do Target ao provedor de Tradução correto. Em seguida, clique em **[!UICONTROL Salvar]**.

   Observe que se um provedor estiver esmaecido para um local de destino, isso indica que o provedor não oferece suporte a esse local específico.

   ![](assets/translation_project_4.png)

1. Clique em **[!UICONTROL Salvar]** quando o projeto de tradução estiver configurado.

Seu projeto de tradução agora foi criado e pode ser usado em uma campanha multilíngue.

## Criar configurações de idioma {#language-settings}

>[!CONTEXTUALHELP]
>id="ajo_multi_custom_conditional"
>title="Configurações condicionais personalizadas"
>abstract="As configurações condicionais personalizadas são conjuntos de regras que determinam em qual localidade o conteúdo será exibido, com base em critérios específicos. Essas configurações permitem controlar a exibição do conteúdo com base em fatores como a localização do usuário, as preferências de idioma ou outros elementos contextuais."

>[!CONTEXTUALHELP]
>id="ajo_multi_fallback"
>title="Preferências de fallback"
>abstract="Escolher uma preferência de substituição é fundamental para aprimorar a experiência do usuário. Se você não selecionar uma substituição e o perfil não atender os requisitos necessários, o conteúdo não será entregue. Por selecionar uma substituição apropriada, você garante uma entrega de conteúdo consistente, mesmo se os perfis não corresponderem aos critérios iniciais."

Nesta seção, você pode definir suas diferentes localidades para gerenciar o conteúdo multilíngue. Você também pode escolher o atributo que deseja usar para pesquisar informações relacionadas ao idioma do perfil.

1. No menu **[!UICONTROL Administração]**, acesse **[!UICONTROL Canal]** > **[!UICONTROL Configurações gerais]**.

1. No menu **[!UICONTROL Configurações de idioma]**, clique em **[!UICONTROL Criar configurações de idioma]**.

   ![](assets/language_settings_1.png)

1. Digite o nome das **[!UICONTROL Configurações de idioma]** e escolha **[!UICONTROL Projeto de tradução]**.

1. No campo **[!UICONTROL Projeto de tradução]**, clique em **[!UICONTROL Editar]** e escolha o **[!UICONTROL Projeto de tradução]** criado anteriormente.

   As **[!UICONTROL Localidades]** configuradas anteriormente são importadas automaticamente.

1. Selecione uma **[!UICONTROL Preferências de fallback]** para definir uma opção de backup para quando um perfil não atender aos critérios necessários para a entrega de conteúdo.

   Observe que, se nenhuma opção de fallback for selecionada, a campanha ou a jornada não será enviada.

   ![](assets/language_settings_2.png)

1. Escolha sua preferência de envio entre as seguintes opções:

   * **[!UICONTROL Selecionar atributos de preferência de idioma de perfil]**
   * **[!UICONTROL Criar regras condicionais personalizadas]**

1. Se você selecionar **[!UICONTROL Selecionar atributos de preferência de idioma de perfil]**, escolha o atributo relevante no menu **[!UICONTROL Atributos de preferência de idioma de perfil]** para pesquisar informações de idioma de perfil.

   ![](assets/multilingual-settings-3.png)

1. Se você selecionar **[!UICONTROL Criar regras condicionais personalizadas]**, selecione a localidade para a qual deseja criar condições. Em seguida, crie regras com base em fatores como localização do usuário, preferências de idioma ou outros elementos contextuais.

   ![](assets/language_settings_3.png)

1. Comece a criar condições adicionando um atributo, evento ou público-alvo para definir seu grupo-alvo.

   >[!IMPORTANT]
   >
   >Os dados contextuais estão disponíveis exclusivamente para canais de cartões de Experiência e Conteúdo na Web, no aplicativo e com base em código. Se usada para canais de email, SMS, notificação por push ou correspondência direta, sem atributos adicionais, a campanha ou jornada será enviada no idioma da primeira opção na lista.

   ![](assets/multilingual-settings-6.png)

   +++Pré-requisitos para usar eventos contextuais em suas condições

   Quando os usuários exibem seu conteúdo, uma solicitação de personalização é enviada juntamente com o evento de experiência. Para aproveitar dados contextuais em suas condições, você deve anexar dados adicionais à carga da solicitação de personalização. Para fazer isso, é necessário criar uma regra na Coleção de dados do Adobe Experience Platform para especificar: SE uma solicitação de personalização for enviada, ANEXE dados extras à solicitação e defina o atributo para corresponder ao campo de idioma no esquema.

   >[!NOTE]
   >
   >Esses pré-requisitos são necessários apenas para os canais de cartões no aplicativo e de Conteúdo.

   1. Na Coleção de dados da Adobe Experience Platform, acesse o menu **[!UICONTROL Regras]** e crie uma nova regra. Informações detalhadas sobre como criar regras estão disponíveis na [!DNL Adobe Experience Platform] [Documentação da Coleção de Dados](https://experienceleague.adobe.com/en/docs/experience-platform/collection/e2e#create-a-rule){target="_blank"}

   2. Na seção **[!UICONTROL IF]** da regra, adicione um evento configurado conforme abaixo:

      ![](assets/multilingual-experience-events-rule-if.png)

      * Escolha a **[!UICONTROL Extensão]** com a qual você está trabalhando.
      * No campo **[!UICONTROL Tipo de evento]**, selecione &quot;Evento de solicitação AEP&quot;.
      * No painel direito, selecione &quot;Tipo de evento XDM é igual a personalization.request&quot;
      * Clique no botão **[!UICONTROL Manter alterações]** para confirmar.

   3. Na seção **[!UICONTROL THEN]** da regra, adicione uma ação configurada conforme abaixo:

      ![](assets/multilingual-experience-events-rule-then.png)

      * Escolha a **[!UICONTROL Extensão]** com a qual você está trabalhando.
      * No campo **[!UICONTROL Tipo de ação]**, selecione &quot;Anexar dados&quot;.
      * Na seção de carga JSON, verifique se o atributo usado para recuperar o idioma a ser usado (no exemplo abaixo &quot;idioma&quot;) corresponde ao nome do atributo especificado no esquema para o qual a sequência de dados da coleção de dados está fluindo.

        ```JSON
        {
            "xdm":{
                "application":{
                    "_dc":{
                        "language":"{%%Language%%}"
                    }
                }
            }
        }
        ```

      * Clique no botão **[!UICONTROL Manter alterações]** para confirmar e salvar sua regra.

+++

1. Arraste e solte as localidades para reordená-las e gerenciar sua prioridade na lista.

1. Clique em **[!UICONTROL Enviar]** para criar suas **[!UICONTROL configurações de idioma]**.

Observe que, após configurar suas preferências de idioma, você não terá mais a opção de editá-las.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.


1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Criar um conteúdo multilíngue {#create-multilingual-campaign}

>[!AVAILABILITY]
>
> A visualização de experiências baseadas em código e de cartões de Conteúdo está indisponível no momento com o fluxo automatizado.

Depois de definir o projeto de Tradução e as configurações de Idioma, você estará pronto para criar a campanha ou jornada e personalizar o conteúdo para as diferentes localidades.

1. Comece criando e configurando sua [campanha](../campaigns/create-campaign.md) ou [jornada](../building-journeys/journeys-message.md) de email, SMS ou notificação por push de acordo com suas necessidades.

1. Depois que o conteúdo principal for criado, clique em **[!UICONTROL Salvar]** e volte para a tela de configuração da campanha.

1. Clique em **[!UICONTROL Adicionar idiomas]**.  [Saiba mais](#create-language-settings)

   ![](assets/multilingual-campaign-automated-1.png)

1. Selecione as **[!UICONTROL configurações de idioma]** criadas anteriormente.

   ![](assets/multilingual-campaign-automated-2.png)

1. Agora que suas Localidades foram importadas, clique em **[!UICONTROL Enviar para tradução]** para encaminhar seu conteúdo para o provedor de Tradução selecionado anteriormente.

   ![](assets/multilingual-campaign-automated-3.png)

1. Depois que o conteúdo é enviado para tradução, ele não pode mais ser editado. Para fazer alterações no conteúdo original, clique no ícone de bloqueio.

   Observe que, se quiser fazer alterações nesse conteúdo, será necessário criar um novo projeto de tradução e reenviá-lo para tradução.

   ![](assets/multilingual-campaign-automated-4.png)

1. Clique em **[!UICONTROL Abrir tradução]** para acessar seu projeto de tradução e revisá-lo.

   ![](assets/multilingual-campaign-automated-5.png)

1. Nesta página, siga o status do projeto de tradução:

   * **[!UICONTROL Tradução em andamento]**: seu provedor de serviços está trabalhando ativamente na tradução.

     Se você selecionou **Insourcing** ao definir suas **configurações de idioma**, será possível traduzir o conteúdo diretamente no projeto de Tradução. [Saiba mais](#manage-ht-project)

   * **[!UICONTROL Pronto para revisão]**: o processo de revisão está pronto para começar, fornecendo a capacidade de acessar a tradução e rejeitá-la ou aprová-la.

     Se você selecionou **[!UICONTROL Habilitar fluxo de trabalho de revisão]** em seu **[!UICONTROL projeto de Tradução]**, será possível revisar a tradução diretamente no Journey Optimizer após a conclusão pelo provedor de Tradução selecionado. [Saiba mais](#review-translation-project)

   * **[!UICONTROL Revisado]**: a tradução foi aprovada e está pronta para ser enviada à campanha.

   * **[!UICONTROL Pronto para publicar]**: a tradução automática foi concluída e agora pode ser enviada para a sua campanha.

   * **[!UICONTROL Concluído]**: a tradução agora está disponível em sua campanha.

   ![](assets/multilingual-campaign-automated-6.png)

1. Depois que a tradução for concluída, o conteúdo multilíngue estará pronto para ser enviado.

   ![](assets/translation_review_9.png)

1. Clique em **[!UICONTROL Revisar para ativar]** para exibir um resumo da campanha.

   O resumo permite modificar a campanha, se necessário, e verificar se algum parâmetro está incorreto ou ausente.

1. Navegue pelo conteúdo multilíngue para ver a renderização em cada idioma.

   ![](assets/multilingual-campaign-automated-7.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Ativar]**.

   >[!IMPORTANT]
   >
   > Se a campanha estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para enviar a campanha multilíngue. [Saiba mais](../test-approve/gs-approval.md)

Agora você pode ativar sua campanha ou jornada. Depois de enviado, você pode medir o impacto da sua jornada ou campanha multilíngue nos relatórios.

## Gerenciar projeto de tradução interno {#manage-ht-project}

>[!CONTEXTUALHELP]
>id="ajo_multi_insourcing_project"
>title="Projeto de tradução interno"
>abstract="O projeto de tradução interno permite gerenciar e executar traduções diretamente do projeto de tradução, simplificando o processo e garantindo maior controle sobre a qualidade e a consistência da tradução."

Se você selecionou Insourcing ao definir as configurações de idioma, é possível traduzir o conteúdo diretamente no projeto de tradução.

1. No seu **[!UICONTROL projeto de Tradução]**, acesse o menu **[!UICONTROL Mais ações]** e selecione **[!UICONTROL Insourcing]**.

   ![](assets/inhouse-translation-1.png)

1. Você pode exportar seu arquivo CSV para tradução usando um software de tradução externo. Como alternativa, você pode importar o arquivo CSV de volta para o projeto de tradução clicando no botão **[!UICONTROL Importar CSV]**.

   ![](assets/inhouse-translation-3.png)

1. Clique em **[!UICONTROL Editar]** para adicionar o conteúdo da tradução.

   ![](assets/inhouse-translation-2.png)

1. Se você estiver pronto para publicar o texto traduzido, clique em **[!UICONTROL Finalizar]**.

## Revisar o projeto de tradução {#review-translation-project}

>[!CONTEXTUALHELP]
>id="ajo_multi_review_project"
>title="Revisar o projeto de tradução"
>abstract="Depois que o provedor escolhido concluir a tradução, é possível revisar os resultados diretamente no Journey Optimizer. Isso permite avaliar a precisão e a qualidade da tradução, garantindo que ela se alinhe às suas expectativas e aos requisitos do projeto antes de finalizá-la."

>[!CONTEXTUALHELP]
>id="ajo_multi_preview_project"
>title="Visualizar o projeto de tradução"
>abstract="A janela Visualizar permite ver como o conteúdo traduzido aparece em cada idioma. Esse recurso ajuda a examinar a renderização e garantir que o conteúdo seja exibido de forma correta e efetiva em todos os idiomas selecionados."

Se você selecionou **[!UICONTROL Habilitar fluxo de trabalho de revisão]** em seu **[!UICONTROL projeto de Tradução]**, será possível revisar a tradução diretamente no Journey Optimizer após a conclusão pelo provedor de Tradução selecionado.

Observe que se essa opção estiver desabilitada, quando a tradução for concluída pelo seu provedor, o status da tarefa de tradução será automaticamente definido como **[!UICONTROL Revisado]**, permitindo que você continue rapidamente clicando em **[!UICONTROL Publish]**.

1. Assim que a tradução for concluída pelo seu provedor de serviços, você poderá acessar a tradução para revisão a partir do seu **[!UICONTROL Projeto de tradução]** ou diretamente da sua **[!UICONTROL Campanha]**.

   No menu **[!UICONTROL Mais ações]**, clique em **[!UICONTROL Revisão]**.

   ![](assets/translation_review_1.png)

1. Na janela Revisar, navegue pelo conteúdo traduzido e aceite ou rejeite cada cadeia de caracteres de tradução.

   ![](assets/translation_review_3.png)

1. Clique em **[!UICONTROL Editar]** para alterar o conteúdo da sua cadeia de caracteres de tradução.

   ![](assets/translation_review_2.png)

1. Insira sua tradução atualizada e clique em **[!UICONTROL Confirmar]** quando terminar.

   ![](assets/translation_review_4.png)

1. Você também pode optar por **[!UICONTROL Rejeitar tudo]** ou **[!UICONTROL Aprovar tudo]** diretamente.

   Ao selecionar **[!UICONTROL Rejeitar tudo]**, adicione um comentário e clique em **[!UICONTROL Rejeitar]**.

1. Clique em **[!UICONTROL Visualizar]** para verificar a renderização do conteúdo traduzido em cada idioma.

1. Se você estiver pronto para publicar o texto traduzido, clique em **[!UICONTROL Finalizar]**.

   ![](assets/translation_review_5.png)

1. Em seu **[!UICONTROL projeto de tradução]**, selecione um dos projetos para acessar mais detalhes. Se você rejeitou a tradução, pode optar por enviá-la de volta para a tradução.

   ![](assets/translation_review_6.png)

1. Depois que o status do **[!UICONTROL Projeto de tradução]** for definido como Revisado, você poderá enviá-lo para a sua Campanha.

   No menu **[!UICONTROL Mais ações]**, clique em **[!UICONTROL Publish]**.

   ![](assets/translation_review_7.png)

1. Em sua Campanha, verifique se o status da tradução foi alterado para **[!UICONTROL Conclusão da tradução]**. Agora você pode enviar seu conteúdo multilíngue. Consulte a etapa 10 em [esta seção](#create-multilingual-campaign).

   ![](assets/translation_review_9.png)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.


-->
