---
solution: Journey Optimizer
product: journey optimizer
title: Considerações e solução de problemas dos fragmentos de conteúdo do Adobe Experience Manager
description: Considerações e problemas comuns para fragmentos de conteúdo do AEM no Journey Optimizer.
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# Considerações e solução de problemas {#aem-fragments-limitations}

## Principais considerações {#considerations}

Lembre-se do seguinte ao usar Fragmentos de conteúdo de [!DNL Adobe Experience Manager] em [!DNL Journey Optimizer]:

* **Tipos de fragmento de conteúdo**
   * Fragmentos de conteúdo simples, fragmentos de conteúdo aninhados e **variações de fragmento de conteúdo** são suportados. Escolha a variação ao inserir o fragmento em [!DNL Journey Optimizer]. Se você não selecionar uma variação, a variação **Principal** (o conteúdo principal do fragmento em [!DNL Adobe Experience Manager]) será usada.

* **Conteúdo multilíngue**
   * Cada variação deve ser criada, marcada e publicada em [!DNL Adobe Experience Manager]. Em [!DNL Journey Optimizer], selecione a variação de fragmento que corresponde a cada idioma ou localidade da mensagem.
   * Não há resolução automática de idioma ou fallback entre variações.

* **Acesso ao repositório**
   * [!DNL Journey Optimizer] integra-se somente à camada [!DNL Adobe Experience Manager] **Publicar** (Sites, Fragmentos de conteúdo). Os fragmentos de conteúdo estão disponíveis por meio de um endpoint público não autenticado.
   * Repositórios de autor podem aparecer no seletor de repositório, mas somente fragmentos publicados em **Publicar** podem ser usados em [!DNL Journey Optimizer].

* **Status do fragmento de conteúdo**
   * Os fragmentos podem mostrar o status **[!UICONTROL Publicado]** ou **[!UICONTROL Modificado]**; [!DNL Journey Optimizer] sempre usa a **última versão publicada**.
   * As alterações feitas após a publicação não são refletidas em [!DNL Journey Optimizer] até que o fragmento seja republicado em [!DNL Adobe Experience Manager]. Não há reconciliação automática de versão entre os dois produtos.

* **Personalização**
   * Compatível: atributos de perfil, atributos contextuais, cadeias de caracteres estáticas e variáveis pré-declaradas.
   * Não suportado: atributos derivados ou computados.

* **Atualizações e controle de versão**
   * As atualizações exigem republicação manual de [!DNL Adobe Experience Manager]. Não há reconciliação automática de versão.
   * Quando um Fragmento de Conteúdo é publicado ou republicado em [!DNL Adobe Experience Manager], o [!DNL Journey Optimizer] atualiza esse fragmento e atualiza **todas as variações desse fragmento referenciadas** em campanhas ou jornadas ativas.
   * A [!DNL Adobe Experience Manager] [ação de publicação](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-publication) pode ser atrasada. Quando a tarefa for concluída, [!DNL Journey Optimizer] receberá um evento e atualizará o conteúdo.
   * Após uma atualização bem-sucedida, as alterações normalmente ficam disponíveis em cerca de **5 minutos** para jornadas unitárias e no **próximo lote** para casos de uso em lote.

* **Armazenamento em cache e revisão de texto**
   * Quando um fragmento é adicionado pela primeira vez a uma campanha ou jornada, o [!DNL Journey Optimizer] o armazena em cache. Se você selecionar um fragmento que já foi usado em outro lugar por meio do **[!UICONTROL Abrir seletor de CF do AEM]**, ele será carregado do cache [!DNL Journey Optimizer].
   * Depois de republicar um fragmento modificado no [!DNL Adobe Experience Manager], o [!DNL Journey Optimizer] acompanha o evento e atualiza o cache.
   * As provas sempre refletem a **versão publicada mais recentemente**; não é possível bloquear uma versão histórica para revisão.

## Solução de problemas {#troubleshooting}

Se você encontrar problemas ao trabalhar com fragmentos de conteúdo do Adobe Experience Manager no Journey Optimizer, consulte os seguintes problemas e resoluções comuns:

| Problema | Causa | Resolução |
|-|-|-|
| **Tag não encontrada** ou **Fragmento de Conteúdo não visível no seletor** | A sintaxe da marca Adobe Experience Manager não corresponde ao formato necessário `ajo-enabled:{OrgId}/{SandboxName}` | Valide se a ID da marca usa a **ID da Organização** e o **Nome da Sandbox** corretos. Verifique se não há espaços ou separadores incorretos. Publique novamente o fragmento de conteúdo depois de corrigir a tag. |
| **O fragmento do conteúdo não aparece na lista** | O fragmento de conteúdo está em estado de rascunho ou não foi publicado | Somente os Fragmentos de conteúdo aprovados e publicados são exibidos no seletor do Journey Optimizer. Publique o fragmento de conteúdo no Adobe Experience Manager e verifique se ele tem o status publicado. |
| **Erro indefinido de variável** | Espaço reservado do Personalization não declarado na tag auxiliar do fragmento | Adicione todos os parâmetros necessários na tag auxiliar do fragmento. Cada espaço reservado usado no fragmento de conteúdo deve ser declarado explicitamente com seu mapeamento. |
| **A prova exibe um conteúdo inesperado** | A prova usa a versão publicada mais recente do Adobe Experience Manager | As provas sempre refletem a publicação mais recente do fragmento de conteúdo no Adobe Experience Manager. Se você tiver feito alterações recentes no Adobe Experience Manager, republique o fragmento e atualize a prova. |
| **Erro de CPES (Acesso negado)** | Função de usuário não autorizada a acessar determinados atributos | Entre em contato com o administrador do sistema para verificar se sua função tem as permissões apropriadas para o perfil ou atributos contextuais usados na personalização. |
| **O fragmento exibe conteúdo em branco ou ausente** | Parâmetros de personalização obrigatórios ou valores de fallback ausentes | Verifique se todos os parâmetros necessários foram fornecidos e considere adicionar valores de fallback para atributos opcionais. |
| **A imagem não é renderizada ou parece corrompida** | O URL da imagem no fragmento de conteúdo é um caminho relativo ou não está acessível pelo canal | Use URLs **absolutos** (`https://...`) para campos de imagem. Os caminhos relativos do Adobe Experience Manager não são compatíveis. Confirme o URL em um navegador ou pré-visualização de mensagem. |
| **O link do Experience League AEM retorna 404** | Favorito obsoleto, pré-visualização da criação ou página de ajuda não publicada do AEM | Abra o tópico [Fragmentos de conteúdo com o Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} da documentação do Live Experience Manager e navegue a partir do sumário na página ou pesquise o nome da seção (por exemplo, **Configuração do Dispatcher**). |

Se o problema persistir, entre em contato com o representante da Adobe com detalhes sobre a ID do fragmento de conteúdo, a campanha ou a ID da jornada e quaisquer mensagens de erro exibidas.
