---
solution: Journey Optimizer
product: journey optimizer
title: Migrar conteúdo e jornadas
description: Saiba como migrar modelos de conteúdo de email e importar jornadas de plataformas externas.
feature: Get Started
topic: Content Management
role: User
level: Intermediate
hide: true
source-git-commit: 8731e10c9a6278c34cd0db8ccdec112f2d5c90d8
workflow-type: tm+mt
source-wordcount: '1298'
ht-degree: 0%

---

# Migrar conteúdo e jornadas {#migrate-content-and-journeys}

Se você estiver mudando de outra plataforma de marketing para o [!DNL Journey Optimizer], não é necessário começar do zero. O Journey Optimizer inclui um espaço de trabalho dedicado que importa o conteúdo e as jornadas de email existentes. Ele os converte em [!DNL Journey Optimizer] modelos de conteúdo e jornadas, para que você possa continuar de onde parou, em vez de reconstruir tudo do zero.

Para migrar seu conteúdo e jornadas para o Journey Optimizer, você precisa das seguintes permissões: Gerenciar campanhas, Gerenciar Jornadas, Gerenciar mensagens, Gerenciar segmentos, Gerenciar itens de biblioteca, Exibir e gerenciar sandboxes e Gerenciar a configuração de integração do AJO. [Saiba mais sobre funções e permissões](../administration/permissions.md)

Você pode acessar este espaço de trabalho diretamente na página inicial [!DNL Journey Optimizer].

![Acesso ao espaço de trabalho de migração](assets/onboarding-hub-15.png)

## Configurar uma conexão {#set-up-a-connection}

>[!CONTEXTUALHELP]
>id="ajo_migration_connection_name"
>title="Nome da conexão"
>abstract="Um nome descritivo que identifica o sistema de origem (por exemplo, &quot;Marketing-Automation-Prod&quot;). Deve começar com uma letra e conter apenas alfanuméricos, sublinhados ou hifens (4 a 50 caracteres)."


>[!CONTEXTUALHELP]
>id="ajo_migration_base_api_url"
>title="URL base da API"
>abstract="O URL raiz da API, sem caminhos de recursos ou sequências de consulta, por exemplo, https://api.example.com."

>[!CONTEXTUALHELP]
>id="ajo_migration_authentication_method"
>title="Escolha de um método de autenticação"
>abstract="A Chave de API envia uma única credencial com cada solicitação, enquanto o OAuth 2.0 usa um protocolo baseado em token mais adequado para APIs corporativas e de terceiros."

>[!CONTEXTUALHELP]
>id="ajo_migration_client_id"
>title="ID de cliente"
>abstract="O identificador público do seu aplicativo, emitido quando você se registra no servidor de autorização."

>[!CONTEXTUALHELP]
>id="ajo_migration_client_secret"
>title="Segredo do cliente"
>abstract="Uma credencial confidencial conhecida somente pelo seu aplicativo e pelo servidor de autorização. Nunca o exponha no código do lado do cliente."


>[!CONTEXTUALHELP]
>id="ajo_migration_token_url"
>title="URL do token"
>abstract="O ponto de extremidade do servidor de autorização que emite tokens de acesso para o fluxo de credenciais do cliente, normalmente terminando em /oauth/token ou /token."


>[!NOTE]
>
>Uma conexão não é necessária se você fizer upload de arquivos ou capturas de tela do HTML em vez de importar por meio de uma API.

Para importar conteúdo ou jornadas por meio de uma API, primeiro conecte o [!DNL Journey Optimizer] à plataforma de origem:

1. No espaço de trabalho, selecione **[!UICONTROL Gerenciar conexões]**.

   ![Botão Gerenciar conexões](assets/onboarding-hub-14.png)

1. Clique em **[!UICONTROL Nova conexão]**.

   ![Janela Gerenciar conexões com o botão Nova conexão realçado](assets/onboarding-hub-1.png)

1. Preencha os detalhes abaixo:

   * **[!UICONTROL Nome da Conexão]**: um nome que identifica o sistema de origem, como `Marketing-Automation-Prod`. Os nomes devem começar com uma letra e podem conter apenas letras, números, sublinhados ou hifens com comprimento entre 4 e 50 caracteres.
   * **[!UICONTROL URL da API Base]**: a URL raiz da API do sistema de origem, sem nenhum caminho de recurso ou cadeia de caracteres de consulta, como `https://api.example.com`.
   * **[!UICONTROL Descrição]**: contexto opcional para ajudar você e outros usuários a identificar a finalidade desta conexão.
   * **[!UICONTROL Método de Autenticação]**: como [!DNL Journey Optimizer] é autenticado no sistema de origem. Escolha **Chave de API** para enviar uma única credencial com cada solicitação. Escolha **OAuth 2.0** para usar um protocolo baseado em token que seja mais adequado para APIs corporativas e de terceiros.
   * **[!UICONTROL ID do Cliente]**: o identificador público atribuído ao seu aplicativo quando você o registrou no servidor de autorização. Necessário para conexões OAuth 2.0.
   * **[!UICONTROL Segredo do Cliente]**: a credencial confidencial associada à sua ID de cliente. Mantenha-o privado, pois ele é conhecido apenas pelo seu aplicativo e pelo servidor de autorização. Necessário para conexões OAuth 2.0.
   * **[!UICONTROL URL do token]**: o ponto de extremidade do servidor de autorização que emite tokens de acesso para o fluxo de credenciais do cliente, normalmente terminando em `/oauth/token` ou `/token`. Necessário para conexões OAuth 2.0.

     ![Novo formulário de conexão com campos para nome da conexão, URL da API base e detalhes de autenticação](assets/onboarding-hub-2.png)

1. Selecione **[!UICONTROL Criar]**.

1. Depois que a conexão for configurada, use o menu avançado para excluí-la ou para marcá-la como padrão para que seja pré-selecionada na próxima vez que você importar conteúdo ou jornadas.

   ![Menu avançado com opções para excluir uma conexão ou marcá-la como padrão](assets/onboarding-hub-3.png)

## Importar conteúdo de email {#import-email-content}

Depois de ter uma origem para o conteúdo, um arquivo HTML ou uma conexão com a plataforma de origem, importe-o para o espaço de trabalho para convertê-lo em um modelo de conteúdo [!DNL Journey Optimizer].

1. Na guia **[!UICONTROL Conteúdo de email]**, escolha como deseja importar seu conteúdo de email:

   * **[!UICONTROL Carregar HTML]**: selecione um ou mais arquivos de email do HTML no computador.

   * **[!UICONTROL Procurar da conexão]**: procure e selecione emails diretamente da sua plataforma de marketing conectada, sem precisar exportar e carregar arquivos manualmente.

   ![Guia Conteúdo de email com opções para carregar o HTML ou procurar por uma conexão](assets/onboarding-hub-6.png)

1. Para um upload do HTML, procure o arquivo ou arraste e solte-o na área de upload. Clique em **[!UICONTROL Carregar]** depois de concluído.

   Os arquivos devem estar no formato `.html` ou `.htm` e não devem ter mais de 10 MB.

   ![Área de carregamento de arquivos do HTML para conteúdo de email](assets/onboarding-hub-7.png)

1. Para importar da conexão, escolha na lista Emails e clique em **[!UICONTROL Importar]**.

1. Acesse o email importado e revise o HTML importado.

1. Adicione a **[!UICONTROL Linha de assunto]** e mapeie cada espaço reservado para personalização ao atributo de perfil correspondente.

   O espaço de trabalho converte automaticamente a sintaxe do script de origem para a sintaxe Handlebars. Para obter uma lista de operadores compatíveis, consulte [Operadores](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/functions/operators).

   ![Editor de email importado com campo de linha de assunto e mapeamento de espaço reservado de personalização](assets/onboarding-hub-8.png)

1. Selecione uma pasta para carregar as imagens do email para [!DNL Experience Manager Assets] e clique em **[!UICONTROL Carregar ativos]**.

   ![Janela de seleção de pasta para carregar imagens de email no Experience Manager Assets](assets/onboarding-hub-9.png)

1. Quando o email estiver pronto, selecione **[!UICONTROL Migrar]** e **Exibir em[!DNL Journey Optimizer]** para abrir o novo modelo de conteúdo.

   ![Botão Migrar e opção Exibir no Journey Optimizer para um email concluído](assets/onboarding-hub-10.png)

Seu modelo de conteúdo agora está disponível no [!DNL Journey Optimizer] e pronto para uso em suas jornadas.

➡️ [Saiba mais sobre o Modelo de conteúdo](../content-management/use-content-templates.md)

## Importar jornadas {#import-journeys}

Recrie suas jornadas importando uma captura de tela do fluxo de jornada ou conectando-se à plataforma de origem.

1. Na guia **[!UICONTROL Jornadas]**, escolha como deseja importar suas jornadas:

   * **[!UICONTROL Carregar capturas de tela]**: selecione uma ou mais capturas de tela do jornada no computador.

   * **[!UICONTROL Procurar da conexão]**: procure e selecione jornadas diretamente da sua plataforma de marketing conectada, sem precisar exportar e carregar capturas de tela manualmente.

   ![Guia Jornadas com opções para carregar capturas de tela ou navegar a partir de uma conexão](assets/onboarding-hub-11.png)

1. Para um upload do HTML, procure o arquivo ou arraste e solte-o na área de upload. Clique em **[!UICONTROL Carregar]** depois de concluído.

   Os arquivos devem estar no formato .png, .jpg, .gif, .webp e não devem ter mais de 5 MB.

   ![Área de carregamento de captura de tela para imagens do jornada](assets/onboarding-hub-13.png)

1. Para importar da conexão, escolha na lista jornada e clique em **[!UICONTROL Importar]**.

1. Visualize a jornada gerada pelo espaço de trabalho a partir da origem.

1. No painel **[!UICONTROL Itens de ação]**, resolva cada item com base no tipo de atividade à qual ele pertence:

   * Para cada etapa de mensagem, selecione uma configuração de canal e um modelo de conteúdo.
   * Para cada atividade do **[!UICONTROL Público]**, selecione o público.

1. Selecione **[!UICONTROL Aplicar alterações]** e **Exibir em[!DNL Journey Optimizer]** para abrir a tela de jornada.

   ![Painel de itens de ação com atividades resolvidas e o botão Aplicar alterações](assets/onboarding-hub-12.png)

Sua jornada agora está disponível no [!DNL Journey Optimizer], onde você pode revisar a tela, fazer os ajustes finais e ativá-la quando estiver pronto para entrar no ar.

➡️ [Saiba mais sobre a criação de Jornadas](../building-journeys/journey-gs.md)

## Rastrear migração {#track-migration-progress}

A visão geral do espaço de trabalho ajuda você a acompanhar cada email importado e localizar rapidamente os que ainda estão aguardando ação. Cada email importado mostra um status de necessidades revisadas, migradas ou com falha, para que você possa ver rapidamente sua posição. Um conjunto de KPIs na parte superior da tela fornece uma contagem rápida de itens em cada status:

* **Total de emails** (ou **Total de jornadas**): o número geral de itens importados para o espaço de trabalho.
* **Em andamento**: itens que ainda estão sendo revisados ou mapeados antes de serem migrados.
* **Migrado**: itens convertidos com êxito e disponíveis em [!DNL Journey Optimizer].
* **Falha**: itens que não puderam ser migrados e precisam de atenção.

![Visão geral do Workspace com KPIs para itens totais, em andamento, migrados e com falha](assets/onboarding-hub-4.png)

Um conjunto de filtros permite restringir a lista de conteúdo de email importado para que você possa se concentrar em um subconjunto específico em vez de percorrer cada item. Combine um ou mais dos seguintes filtros para encontrar o que está procurando:

* **[!UICONTROL Status]**: mostrar apenas emails com um status específico, como **[!UICONTROL Precisa de revisão]**, **[!UICONTROL Migrado]** ou **[!UICONTROL Falha]**.
* **[!UICONTROL Criado]**: mostra emails importados dentro de um intervalo de datas específico.
* **[!UICONTROL Atualizado]**: mostrar os emails modificados pela última vez em um intervalo de datas específico.

![Opções de filtro para status, data de criação e data de atualização no espaço de trabalho](assets/onboarding-hub-5.png)


