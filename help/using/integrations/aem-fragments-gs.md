---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de conteúdo do AEM
description: Saiba como acessar e gerenciar fragmentos de conteúdo do AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: b06229e7a2fc64fbe28154c798b152cca8203a86
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 6%

---

# Introdução aos fragmentos de conteúdo do Adobe Experience Manager {#aem-fragments}

Ao integrar o Adobe Experience Manager as a Cloud Service com o Adobe Journey Optimizer, agora é possível incorporar facilmente os Fragmentos de conteúdo do AEM ao conteúdo do Journey Optimizer. Essa conexão simplifica o processo de acesso e aproveitamento do conteúdo do AEM, permitindo a criação de campanhas e jornadas personalizadas e dinâmicas.

Para saber mais sobre os Fragmentos de conteúdo do AEM, consulte [Trabalho com fragmentos de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} na documentação do Experience Manager.

## Antes de começar {#start}

>[!AVAILABILITY]
>
>Para clientes da área de saúde, a integração é habilitada somente mediante o licenciamento das ofertas complementares Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

### Limitações {#limitations}

Observe as seguintes limitações ao trabalhar com Fragmentos de conteúdo do Adobe Experience Manager no Journey Optimizer:

* **Tipos de Fragmento de Conteúdo**: Fragmentos de Conteúdo Simples e Fragmentos de Conteúdo aninhados são suportados. As variações de Fragmento de conteúdo não são compatíveis no momento.

* **Conteúdo multilíngue**: há suporte apenas para o fluxo manual. Cada variante de idioma deve ser criada independentemente no Adobe Experience Manager, marcada, publicada e selecionada manualmente no Journey Optimizer. Não há resolução automática de idioma ou mecanismo de fallback.

* **Acesso ao repositório**: o Journey Optimizer integra-se exclusivamente com a camada de Publicação do Adobe Experience Manager, em que os Fragmentos de conteúdo estão disponíveis por meio de um ponto de extremidade público não autenticado. Embora os repositórios de Autor possam aparecer no seletor de repositório, somente os Fragmentos de conteúdo publicados no nível de Publicação podem ser usados no Journey Optimizer.

* **Status do Fragmento do Conteúdo**: o Journey Optimizer exibe Fragmentos de Conteúdo com status **Publicado** e **Modificado**. Em todos os casos, somente a versão publicada mais recente é usada. Se um fragmento for modificado após a publicação, essas alterações não serão refletidas no Journey Optimizer até que o fragmento de conteúdo seja republicado no Adobe Experience Manager. Não há reconciliação automática de versão entre o Adobe Experience Manager e o Journey Optimizer.

* **Personalization**: somente atributos de perfil, atributos contextuais, cadeias de caracteres estáticas e variáveis pré-declaradas têm suporte. Não há suporte para atributos derivados ou computados.

* **Atualizações e controle de versão**: as atualizações de Fragmentos de conteúdo exigem republicação manual da Adobe Experience Manager. Não há reconciliação automática de versão entre o Adobe Experience Manager e o Journey Optimizer. Quando um fragmento de conteúdo é publicado no Adobe Experience Manager, o Journey Optimizer recebe um evento e as atualizações no Journey Optimizer. Se for bem-sucedida, a atualização estará disponível após 5 minutos para Jornadas unitárias e no próximo lote para casos de uso de lote.

* **Armazenamento em cache e revisão**: os fragmentos de conteúdo são recuperados em tempo real da camada de Publicação do Adobe Experience Manager. Não há pré-renderização ou armazenamento em cache de instantâneos. As provas para campanhas e jornadas sempre refletem a versão publicada mais recentemente do fragmento de conteúdo, e as versões históricas não podem ser bloqueadas para prova.

* **Acesso do usuário**: é recomendável limitar o número de usuários com acesso para publicar Fragmentos de conteúdo para reduzir o risco de erros acidentais.


### Ciclo de vida do fragmento de conteúdo

![](assets/do-not-localize/AEM_CF.png)

Os fragmentos de conteúdo seguem diferentes estágios do ciclo de vida, dependendo do nível do Adobe Experience Manager em que estão. [Saiba mais na documentação do Adobe Experience Manager](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

O conteúdo é criado e gerenciado na **camada do Autor**, onde os fragmentos podem ter status Novo, Rascunho, Publicado, Modificado ou Não publicado. Esses status se aplicam somente na **camada do autor** e oferecem suporte à criação e revisão de conteúdo.

Quando um fragmento de conteúdo é publicado, uma cópia é criada na **camada de publicação** e exposta por meio de um ponto de extremidade público não autenticado. O Journey Optimizer integra-se exclusivamente com esta **Camada de publicação**.

Como resultado, o Journey Optimizer exibe apenas os Fragmentos de conteúdo publicados ou modificados e sempre usa a versão publicada mais recente. Quaisquer alterações feitas após a publicação não serão refletidas no Journey Optimizer até que o fragmento de conteúdo seja republicado.


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
