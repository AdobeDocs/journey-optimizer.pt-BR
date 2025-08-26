---
solution: Journey Optimizer
product: journey optimizer
title: Copiar objetos Journey Optimizer entre sandboxes
description: Saiba como copiar jornadas, modelos de conteúdo e fragmentos entre sandboxes.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: sandbox, jornada, cópia, ambiente
exl-id: 356d56a5-9a90-4eba-9875-c7ba96967da9
source-git-commit: f8134fd1e030fb969747a37acd657f62fd398c75
workflow-type: tm+mt
source-wordcount: '1701'
ht-degree: 4%

---

# Exportar objetos para outra sandbox {#copy-to-sandbox}

Você pode copiar objetos como jornadas, ações personalizadas, modelos de conteúdo ou fragmentos em várias sandboxes usando recursos de exportação e importação de pacotes. Um pacote pode consistir em um único objeto ou em vários objetos. Todos os objetos incluídos em um pacote precisam ser da mesma sandbox.

Esta página descreve o caso de uso de ferramentas de sandbox no contexto do Journey Optimizer. Para obter mais informações sobre o recurso propriamente dito, consulte o [Guia de ferramentas de sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects){target="_blank"} do Adobe Experience Platform.

>[!NOTE]
>
>Este recurso requer as seguintes permissões do recurso **Administração de sandbox**: Gerenciar sandboxes (ou Exibir sandboxes) e Gerenciar pacotes. [Saiba mais](../administration/ootb-permissions.md)

O processo de cópia é realizado por meio de uma exportação e importação de pacotes entre as sandboxes de origem e de destino. Estas são as etapas gerais para copiar uma jornada de uma sandbox para outra:

1. [Adicionar o objeto para exportar como um pacote na sandbox de origem](#export)
1. [Publicar o pacote](#publish)
1. [Importar o pacote na sandbox de destino](#import)

## Objetos exportados e práticas recomendadas {#objects}

O Journey Optimizer permite exportar jornadas, ações personalizadas, modelos de conteúdo, fragmentos e outros objetos para outra sandbox. As seções a seguir fornecem informações e práticas recomendadas para cada tipo de objeto.

### Práticas recomendadas gerais {#global}

* Ao copiar um objeto, todas as dependências (como fragmentos aninhados, públicos-alvo do jornada ou ações) são atualizadas corretamente no objeto principal, garantindo o mapeamento adequado na sandbox de destino.

* Se um objeto exportado contiver personalização de perfil, verifique se o esquema apropriado existe na sandbox de destino para evitar qualquer problema de personalização.

* Atualmente, as landing pages não são compatíveis com a migração entre sandboxes. Ao copiar uma jornada para outra sandbox, todas as referências às páginas de aterrissagem na jornada ou no conteúdo de email ainda apontarão para as IDs da página de aterrissagem da sandbox original (fonte). Após a migração, você deve atualizar manualmente todas as referências de página de aterrissagem em sua jornada e conteúdo de email para usar as IDs de página de aterrissagem corretas na sandbox de destino (destino). Consulte [Criar e publicar páginas de destino](../landing-pages/create-lp.md).

+++ Jornadas

* **Dependências copiadas** - Ao exportar uma jornada, além da própria jornada, o Journey Optimizer jornada também copia a maioria dos objetos dos quais ela depende: públicos-alvo, ações personalizadas, esquemas, eventos e ações. Para obter mais detalhes sobre objetos copiados, consulte o [Guia de ferramentas de sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects){target="_blank"} do Adobe Experience Platform.

* **Validação manual recomendada** - Não garantimos que todos os elementos vinculados sejam copiados para a sandbox de destino. É altamente recomendável executar uma verificação completa, por exemplo, antes de publicar uma jornada. Isso permite identificar qualquer objeto ausente em potencial.

* **Exclusividade e modo de rascunho** - Os objetos copiados na sandbox de destino são exclusivos e não há risco de substituir elementos existentes. A jornada jornada e qualquer mensagem dentro dela é trazida no modo de rascunho. Isso permite executar uma validação completa antes da publicação na sandbox de destino.

* **Metadados** - O processo de cópia copia apenas os metadados sobre a jornada e os objetos nessa Jornada. Nenhum dado de perfil ou conjunto de dados está sendo copiado como parte desse processo.

* **Ações personalizadas**

   * Ao exportar ações personalizadas, a configuração de URL e os parâmetros de carga são copiados. No entanto, por motivos de segurança, os parâmetros de autenticação não são copiados e, em vez disso, são substituídos por &quot;INSERIR SEGREDO AQUI&quot;. Os valores constantes do cabeçalho da solicitação e do parâmetro de consulta também são substituídos por &quot;INSERIR SEGREDO AQUI&quot;.

     Isso inclui as ações personalizadas com finalidade especial ([!DNL Adobe Campaign Standard], [!DNL Campaign Classic], [!DNL Marketo Engage]).

   * Ao copiar uma jornada para outra sandbox, se você selecionar &quot;usar existente&quot; para uma ação personalizada durante o processo de importação, a ação personalizada existente selecionada deverá ser a mesma que a ação personalizada de origem (ou seja, mesma configuração, parâmetros etc.). Caso contrário, a nova cópia da jornada terá erros que não poderão ser resolvidos na tela.

* **Fontes de dados, grupos de campos e eventos** - Ao copiar uma jornada que usa eventos, fontes de dados ou grupos de campos, o processo de importação verifica automaticamente se já existem componentes com o mesmo nome e tipo na sandbox de destino. Por exemplo, um evento unitário será substituído por um evento unitário na sandbox do target com o mesmo nome. O mesmo se aplica a eventos comerciais, fontes de dados personalizadas e grupos de campos baseados em API e esquema usados em jornadas. Se um evento unitário da sandbox de origem tiver o mesmo nome que uma sandbox de destino de evento comercial, ele não será copiado nem criado, isso se aplica a todos os outros componentes também.

+++

+++ Campanhas

As campanhas são copiadas junto com todos os itens relacionados ao perfil, público-alvo, esquema, mensagens em linha e objetos dependentes. No entanto, os seguintes itens **não** foram copiados:

* Variantes multilíngues e configurações de idioma,
* Regras comerciais,
* Tags,
* Rótulos de DULE (Label Usage Labeling and Enforcement, Rotulagem e aplicação de uso de dados).

Ao copiar campanhas, verifique se o objeto listado abaixo está validado na sandbox de destino para evitar configurações incorretas:

* **Configurações de canal**: as configurações de canal são copiadas junto com as campanhas. Depois que as campanhas são copiadas, as configurações de canal devem ser selecionadas manualmente na sandbox de destino.
* **Variantes e configurações de experimentação**: as variantes e configurações de experimentos estão incluídas no processo de cópia da campanha. Valide essas configurações na sandbox de destino após a importação.
* **Decisão unificada**: as políticas de decisão e os itens de decisão têm suporte para exportação e importação. Certifique-se de que as dependências relacionadas à decisão estejam mapeadas corretamente na sandbox de destino.

+++

+++ Decisão

* Os objetos abaixo devem estar presentes na sandbox de destino antes de copiar objetos do Decisioning:

   * Atributos de perfil usados em objetos de Decisão,
   * O grupo de campos de atributos de oferta personalizados,
   * Os esquemas de sequências de dados usados para atributos de contexto em regras, classificação ou limite.

* No momento, não há suporte para cópia de sandbox para fórmulas de classificação com Modelos de IA.

* Ao copiar uma campanha, os itens de decisão (itens de oferta) não são copiados automaticamente. Certifique-se de copiá-los individualmente usando a opção &quot;Adicionar ao pacote&quot;.

* Se uma Política de decisão tiver uma estratégia de seleção, os itens de decisão deverão ser adicionados separadamente. Se tiver itens de decisão manuais/substitutos, eles serão adicionados automaticamente como dependências diretas.

* Ao copiar entidades de Decisão, copie os itens de decisão **antes** de qualquer outro objeto. Por exemplo, se você copiar uma coleção primeiro e não houver ofertas na nova sandbox, essa nova coleção permanecerá vazia.

* Ao copiar entidades com dependências (por exemplo, esquema, segmentos), clique em &quot;Criar novo&quot; na entidade para desmarcá-la e revelar a opção &quot;Usar existente&quot; para artefatos dependentes. Dependências adicionais podem exigir a repetição dessa etapa mais abaixo na hierarquia.

  Exemplo: ao importar uma campanha, para reutilizar um esquema de sequência de dados em uma regra, clique em &quot;Criar novo&quot; em DECISIONING_STRATEGY e, em seguida, em DECISIONING_RULES, para revelar a opção &quot;Usar existente&quot; para o esquema de sequência de dados.

* Para entidades dependentes de um esquema de contexto de sequência de dados, verifique se a sequência de dados é criada antes e selecione um esquema existente para essa sequência de dados.

* Se clicar diretamente em &quot;Concluir&quot; durante a importação, todas as dependências serão criadas novamente.

+++

+++ Modelos de conteúdo

* Ao exportar um template de conteúdo, todos os fragmentos aninhados também são copiados junto com ele.

* Às vezes, a exportação de modelos de conteúdo pode resultar na duplicação do fragmento. Por exemplo, se dois modelos compartilharem o mesmo fragmento e forem copiados em pacotes separados, ambos os modelos precisarão reutilizar o mesmo fragmento na sandbox de destino. Para evitar a duplicação, selecione a opção &quot;Use existing&quot; durante o processo de importação. [Saiba como importar um pacote](#import)

* Para evitar ainda mais a duplicação, é recomendável exportar modelos de conteúdo em um único pacote. Isso garante que o sistema gerencie a desduplicação com eficiência.

+++

+++ Fragmentos

* Os fragmentos podem ter vários status, como Em tempo real, Rascunho e Em tempo real com rascunho em andamento. Ao exportar um fragmento, seu estado de rascunho mais recente é copiado para a sandbox de destino.

* Ao exportar um fragmento, todos os fragmentos aninhados também são copiados junto com ele.

+++

## Adicionar objetos como um pacote {#export}

Para copiar objetos para outra sandbox, primeiro é necessário adicioná-los como um pacote na sandbox de origem. Siga estas etapas:

1. Navegue até o inventário onde o primeiro objeto que deseja copiar está armazenado, como a lista jornadas. Clique no ícone **Mais ações** (os três pontos ao lado do nome do objeto) e clique em **Adicionar ao pacote**.

   ![](assets/journey-sandbox1.png)

1. Na janela **Adicionar ao pacote**, escolha se deseja adicionar o objeto a um pacote existente ou criar um novo pacote:

   ![](assets/journey-sandbox2.png)

   * **Pacote existente**: selecione o pacote no menu suspenso.
   * **Criar um novo pacote**: digite o nome do pacote. Você também pode adicionar uma descrição.

1. Repita essas etapas para adicionar todos os objetos que você deseja exportar com seu pacote.

## Publicar o pacote a ser exportado {#publish}

Quando o pacote estiver pronto para ser exportado, siga estas etapas para publicá-lo:

1. Navegue até o menu **[!UICONTROL Administração]** > **[!UICONTROL Sandboxes]**, selecione a guia **Pacotes**.

1. Abra o pacote que deseja exportar, selecione os objetos que deseja exportar e clique em **Publicar**.

   Neste exemplo, queremos exportar uma jornada, um template de conteúdo e um fragmento.

   ![](assets/journey-sandbox4.png)

1. Para acompanhar o status da publicação do pacote na guia **[!UICONTROL Trabalhos]**. Para obter mais detalhes sobre um trabalho, selecione-o na lista e clique no botão **[!UICONTROL Exibir detalhes da importação]**.

   ![](assets/journey-sandbox9.png)

## Importar o pacote na sandbox de destino {#import}

Depois que o pacote for publicado, é necessário importá-lo para a sandbox de destino. Siga estas etapas:

1. Navegue até o menu **[!UICONTROL Sandboxes]** e selecione a guia **[!UICONTROL Procurar]**.

1. Procure a sandbox em que deseja importar o pacote e clique no ícone + ao lado do nome.

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >Somente as sandboxes da sua organização estão disponíveis.

1. No campo **Sandbox de destino**, verifique se as sandboxes de destino corretas estão selecionadas e selecione o pacote a ser importado na lista suspensa **[!UICONTROL Nome do pacote]**. Clique em **Next**.

   ![](assets/journey-sandbox6.png)

1. Revise os objetos e as dependências do pacote. Esta é a lista de objetos que foram adicionados ao pacote, juntamente com outros objetos dos quais as jornadas dependem, como públicos, esquemas, eventos ou ações.

   Para cada objeto, você pode optar por criar um novo ou usar um existente na sandbox de destino. Isso permite, por exemplo, evitar a duplicação de fragmentos que pode ocorrer ao importar modelos de conteúdo usando fragmentos comuns.

   ![](assets/journey-sandbox7.png)

1. Clique no botão **Concluir**, no canto superior direito, para começar a copiar o pacote para a sandbox de destino. O processo de cópia varia de acordo com a complexidade dos objetos e com quantos objetos precisam ser copiados.

1. Clique no trabalho de importação para revisar o resultado da cópia:

   * Clique no botão **Exibir objetos importados** para exibir cada objeto individual copiado.
   * Clique no botão **Exibir detalhes da importação** para verificar os resultados da importação para cada objeto.

   ![](assets/journey-sandbox8.png)

1. Acesse sua sandbox de destino e execute uma verificação completa de todos os objetos copiados.
