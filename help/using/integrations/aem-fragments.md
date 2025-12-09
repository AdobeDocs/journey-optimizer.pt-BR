---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de conteúdo do AEM
description: Saiba como acessar e gerenciar fragmentos de conteúdo do AEM
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: e292d584e3c3d1997c2c3e6bb3675758ff530bf9
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 5%

---

# Fragmentos de conteúdo do Adobe Experience Manager {#aem-fragments}

Ao integrar o Adobe Experience Manager as a Cloud Service com o Adobe Journey Optimizer, agora é possível incorporar facilmente os Fragmentos de conteúdo do AEM ao conteúdo do Journey Optimizer. Essa conexão simplifica o processo de acesso e aproveitamento do conteúdo do AEM, permitindo a criação de campanhas e jornadas personalizadas e dinâmicas.

Para saber mais sobre os Fragmentos de conteúdo do AEM, consulte [Trabalho com fragmentos de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} na documentação do Experience Manager.

## Antes de começar {#start}

>[!AVAILABILITY]
>
>Para clientes da área de saúde, a integração é habilitada somente mediante o licenciamento das ofertas complementares Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

### Limitações {#limitations}

Observe as seguintes limitações ao trabalhar com Fragmentos de conteúdo do Adobe Experience Manager no Journey Optimizer:

* **Tipos de Fragmento de Conteúdo**: somente Fragmentos de Conteúdo simples são suportados. No momento, não há suporte para variações e fragmentos aninhados.

* **Conteúdo multilíngue**: há suporte apenas para o fluxo manual.

* **Personalization**: somente atributos de perfil, atributos contextuais, cadeias de caracteres estáticas e variáveis pré-declaradas têm suporte. Não há suporte para atributos derivados ou computados.

* **Atualizações e controle de versão**: as atualizações de Fragmentos de conteúdo exigem republicação manual da Adobe Experience Manager. Não há reconciliação automática de versão entre o Adobe Experience Manager e o Journey Optimizer.

* **Armazenamento em cache**: o Journey Optimizer busca fragmentos de conteúdo em tempo real na publicação do Adobe Experience Manager. Não há cache pré-renderização.

* **Revisão**: a prova de campanhas e jornadas publicadas reflete os dados da publicação mais recente de Fragmento de Conteúdo do Experience Manager. Não há bloqueio de versão histórica.

* **Acesso do usuário**: é recomendável limitar o número de usuários com acesso para publicar Fragmentos de conteúdo para reduzir o risco de erros acidentais.

### Fluxo de sincronização de conteúdo {#content-sync-flow}

A integração entre o Adobe Experience Manager e o Journey Optimizer segue esse fluxo de dados:

1. **[Criar e criar](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**: o conteúdo é criado e configurado no Adobe Experience Manager como Fragmentos de Conteúdo.

1. **[Marcação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**: os fragmentos de conteúdo devem ser marcados com a marca específica da Journey Optimizer (`ajo-enabled:{OrgId}/{SandboxName}`).

1. **[Publicar](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**: os fragmentos de conteúdo são publicados no Adobe Experience Manager, tornando-os disponíveis para o Journey Optimizer.

1. **[Acesso](#aem-add)**: o Journey Optimizer busca e exibe os Fragmentos de conteúdo disponíveis da instância de publicação do Adobe Experience Manager em tempo real.

1. **[Integração](#aem-add)**: os Fragmentos de conteúdo são selecionados e integrados em campanhas ou jornadas.

## Criar e atribuir uma tag no Experience Manager

Antes de usar o fragmento de conteúdo no Journey Optimizer, é necessário criar uma tag especificamente para o Journey Optimizer:

1. Acesse seu ambiente **Experience Manager**.

1. No menu **Ferramentas**, selecione **Marcação**.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Clique em **Criar Marca**.

1. Verifique se a ID segue a seguinte sintaxe: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Clique em **Criar**.

1. Defina seu Modelo de fragmento de conteúdo conforme detalhado na [documentação do Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} e atribua a tag do Journey Optimizer recém-criada.

Essa conexão em tempo real garante que o conteúdo esteja sempre atualizado, mas também significa que quaisquer alterações nos fragmentos publicados afetarão imediatamente as campanhas e jornadas ativas.

Agora você pode começar a criar e configurar o fragmento de conteúdo para uso posterior no Journey Optimizer. Saiba mais em [documentação do Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Adicionar fragmentos de conteúdo do Experience Manager {#aem-add}

Depois de criar e personalizar os fragmentos de conteúdo do AEM, você pode importá-los para a campanha ou jornada do otimizador de Jornadas.

1. Crie sua [Campanha](../campaigns/create-campaign.md) ou [Jornada](../building-journeys/journey-gs.md).

1. Para acessar o fragmento de conteúdo do AEM, clique no ![ícone do Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) em qualquer campo de texto ou abra o código-fonte por meio de um componente de conteúdo do HTML.

   ![](assets/aem_campaign_2.png)

1. No menu **[!UICONTROL Fragmento de Conteúdo do AEM]** no painel esquerdo, clique em **[!UICONTROL Abrir seletor de CF do AEM]**.

   ![](assets/aem_campaign_3.png)

1. Selecione um **[!UICONTROL Fragmento de conteúdo]** na lista disponível para importar para o conteúdo do Journey Optimizer.

1. Clique em **[!UICONTROL Mostrar filtros]** para ajustar a lista de Fragmentos de conteúdo.

   Por padrão, o filtro de Fragmento de conteúdo é predefinido para exibir somente conteúdo aprovado.

   ![](assets/aem_campaign_4.png)

1. Depois de selecionar seu **[!UICONTROL Fragmento do conteúdo]**, clique em **[!UICONTROL Selecionar]** para abri-lo.

   ![](assets/aem_campaign_5.png)

1. Clique em **[!UICONTROL Exibir fragmento]** para exibir as informações do fragmento. Observe que abrir o menu **[!UICONTROL Informações do fragmento]** coloca o editor no modo somente leitura.

   Selecione **[!UICONTROL Visualizar]** no menu à direita para exibir seu fragmento no Adobe Experience Manager.

   ![](assets/aem_campaign_7.png)

1. Clique no ícone ![Mais ações](assets/do-not-localize/Smock_MoreSmallList_18_N.svg) para acessar o menu avançado do Fragmento:

   * **[!UICONTROL Trocar fragmento]**
   * **[!UICONTROL Explorar referências]**
   * **[!UICONTROL Abrir no AEM]**

   ![](assets/aem_campaign_8.png)

1. Escolha os campos desejados em seu **[!UICONTROL Fragmento]** para adicionar ao conteúdo.
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Para habilitar a personalização em tempo real, todos os espaços reservados usados em um **[!UICONTROL Fragmento de conteúdo]** devem ser declarados explicitamente pelo usuário como parâmetros na marca auxiliar do fragmento. Você pode mapear esses espaços reservados para atributos de perfil, atributos contextuais, cadeias de caracteres estáticas ou variáveis predefinidas usando os seguintes métodos:

   1. **Mapeamento de Perfil ou de Atributo Contextual**: atribua o espaço reservado a um perfil ou atributo contextual, por exemplo: name = profile.person.name.firstName.

   1. **Mapeamento de Cadeia de Caracteres Estática**: atribua um valor de cadeia de caracteres fixo colocando-o entre aspas duplas; por exemplo: name = &quot;John&quot;.

   1. **Mapeamento de Variáveis**: faça referência a uma variável declarada anteriormente na mesma HTML, por exemplo, name = &#39;variableName&#39;.
Nesse caso, verifique se **_variableName_** está declarado antes de adicionar a ID do fragmento, usando a seguinte sintaxe:

      ```html
      {% let variableName = attribute name %} 
      ```

   No exemplo abaixo, o espaço reservado **_name_** é mapeado para o atributo **_profile.person.name.firstName_** dentro do fragmento.

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**. Agora você pode testar e verificar o conteúdo da sua mensagem conforme detalhado em [esta seção](../content-management/preview.md).
Depois de executar os testes e validar o conteúdo, você pode [enviar a campanha](../campaigns/review-activate-campaign.md) ou [publicar a jornada](../building-journeys/publish-journey.md) para o público-alvo.

O Adobe Experience Manager permite identificar as campanhas ou jornadas do Journey Optimizer em que um fragmento de conteúdo está sendo usado. Saiba mais em [documentação do Adobe Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references).

## Solução de problemas {#troubleshooting}

Se você encontrar problemas ao trabalhar com fragmentos de conteúdo do Adobe Experience Manager no Journey Optimizer, consulte os seguintes problemas e resoluções comuns:

| Problema | Causa | Resolução |
|-|-|-|
| **Tag não encontrada** ou **Fragmento de Conteúdo não visível no seletor** | A sintaxe da marca Adobe Experience Manager não corresponde ao formato necessário `ajo-enabled:{OrgId}/{SandboxName}` | Valide se a ID da marca usa a **ID da Organização** e o **Nome da Sandbox** corretos. Verifique se não há espaços ou separadores incorretos. Publique novamente o fragmento de conteúdo depois de corrigir a tag. |
| **O fragmento do conteúdo não aparece na lista** | O fragmento de conteúdo está em estado de rascunho ou não foi aprovado | Somente os Fragmentos de conteúdo aprovados e publicados são exibidos no seletor do Journey Optimizer. Publique o fragmento de conteúdo no Adobe Experience Manager e verifique se ele tem o status aprovado. |
| **Erro indefinido de variável** | Espaço reservado do Personalization não declarado na tag auxiliar do fragmento | Adicione todos os parâmetros necessários na tag auxiliar do fragmento. Cada espaço reservado usado no fragmento de conteúdo deve ser declarado explicitamente com seu mapeamento. |
| **A prova exibe um conteúdo inesperado** | A prova usa a versão publicada mais recente do Adobe Experience Manager | As provas sempre refletem a publicação mais recente do fragmento de conteúdo no Adobe Experience Manager. Se você tiver feito alterações recentes no Adobe Experience Manager, republique o fragmento e atualize a prova. |
| **Erro de CPES (Acesso negado)** | Função de usuário não autorizada a acessar determinados atributos | Entre em contato com o administrador do sistema para verificar se sua função tem as permissões apropriadas para o perfil ou atributos contextuais usados na personalização. |
| **O fragmento exibe conteúdo em branco ou ausente** | Parâmetros de personalização obrigatórios ou valores de fallback ausentes | Verifique se todos os parâmetros necessários foram fornecidos e considere adicionar valores de fallback para atributos opcionais. |

Se o problema persistir, entre em contato com o representante da Adobe com detalhes sobre a ID do fragmento de conteúdo, a campanha ou a ID da jornada e quaisquer mensagens de erro exibidas.
