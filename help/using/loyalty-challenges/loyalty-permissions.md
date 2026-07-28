---
solution: Journey Optimizer
product: journey optimizer
title: Permissões para desafios de fidelidade
description: Saiba quais permissões são necessárias para acessar, configurar e usar os Desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Administration
role: Admin
level: Intermediate
exl-id: 7d6d4f18-8c5d-4c9c-9f7d-2d6c5f9a8b31
feature_v2: []
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 967
ht-degree: 6%

---

# Permissões para desafios de fidelidade {#loyalty-permissions}

## Visão geral {#overview}

A fidelidade [!DNL Adobe Journey Optimizer] usa o controle de acesso baseado em função (RBAC) do Adobe Admin Console para gerenciar o acesso do usuário.

A atribuição de função é necessária antes que os usuários possam executar operações de Fidelidade. Os usuários sem uma função atribuída têm acesso negado aos pontos de acesso do serviço de fidelidade. Antes de integrar usuários ao programa de fidelidade, atribua uma função apropriada a cada usuário que usará o serviço.

As funções podem ser atribuídas diretamente a usuários individuais ou por meio de grupos de usuários. [Saiba como atribuir funções a usuários](#assign-roles).

## Funções recomendadas {#recommended-roles}

A fidelidade fornece três funções padrão pré-configuradas para a sandbox **Prod**. Novos clientes podem usar essas funções como estão.

### Administrador de fidelidade {#loyalty-administrator}

A função de **Administrador de Fidelidade** fornece acesso administrativo total a todos os recursos de Fidelidade: desafios, configuração, catálogo de produtos e insights.

| Permissão | Descrição |
| - | - |
| Gerenciar desafios de fidelidade | Crie, edite, exclua, publique, cancele a publicação e arquive desafios; acione a geração de jornadas |
| Gerenciar configuração principal de fidelidade | Criar, editar e excluir a configuração da organização principal |
| Gerenciar configurações avançadas de fidelidade | Gerenciar pontos de extremidade de premiação e configurações de transformação de evento, incluindo acesso de leitura/gravação a valores confidenciais de credenciais |
| Gerenciar Catálogo de Produtos de Fidelidade | Exibir, importar e editar entradas do catálogo de produtos |
| Gerenciar Insights de Fidelidade | Exibir insights, atualizar a configuração de KPI e acionar o pipeline de insights |

### Profissional de fidelidade {#loyalty-practitioner}

A função de **Profissional de fidelidade** foi projetada para proprietários de empresas que gerenciam o ciclo de vida de desafio completo e editam a configuração principal. A configuração de recompensa, a configuração de eventos e o acesso ao catálogo de produtos são somente leitura. A exclusão e as gravações de configuração avançadas não são permitidas.

| Permissão | Descrição |
| - | - |
| Gerenciar desafios de fidelidade | Crie, edite, exclua, publique, cancele a publicação e arquive desafios; acione a geração de jornadas |
| Configurar a configuração principal do Loyalty | Criar e editar a configuração da organização principal. A exclusão não é permitida |
| Exibir Configuração de Recompensa de Fidelidade | Exibir configuração de premiação, incluindo provedores, definições e proxies. Os valores confidenciais são excluídos |
| Exibir Configuração de Evento de Fidelidade | Exibir definições de evento e mapeamentos de transformação de evento |
| Exibir Catálogo de Produtos de Fidelidade | Exibir entradas do catálogo de produtos e status do trabalho de importação |
| Desenvolver insights de fidelidade | Exibir dados de insights e atualizar cartões da insight |

### Analista de fidelidade {#loyalty-analyst}

A função de **Analista de Fidelidade** fornece acesso somente leitura a desafios, catálogos de produtos e insights. Use essa função para fins de relatório e auditoria.

| Permissão | Descrição |
| - | - |
| Exibir desafios de fidelidade | Exibir desafios |
| Exibir Catálogo de Produtos de Fidelidade | Exibir entradas do catálogo de produtos e status do trabalho de importação |
| Exibir Insights de Fidelidade | Visualize cartões insight gerados por IA, dados vitais de integridade e dados de desempenho de desafio |

## Recursos de função {#role-capabilities}

| Operação | Administrador | Profissional | Analista |
| - | - | - | - |
| Desafios - exibir | Sim | Sim | Sim |
| Desafios - criar ou editar | Sim | Sim | Não |
| Desafios - excluir | Sim | Sim | Não |
| Desafios — publicar, cancelar a publicação ou arquivar | Sim | Sim | Não |
| Desafios - acionar a geração de jornadas | Sim | Sim | Não |
| Configuração da organização principal - exibir | Sim | Sim | Não |
| Configuração da organização principal - criar ou editar | Sim | Sim | Não |
| Configuração da organização principal - excluir | Sim | Não | Não |
| Configuração de recompensa - exibição, valores confidenciais excluídos | Sim | Sim | Não |
| Configuração de recompensa - gravar ou acessar valores confidenciais | Sim | Não | Não |
| Configuração do evento - exibir | Sim | Sim | Não |
| Configuração do evento - gravação | Sim | Não | Não |
| Catálogo de produtos - exibição | Sim | Sim | Sim |
| Catálogo de produtos - importar ou editar | Sim | Não | Não |
| Insights - exibir | Sim | Sim | Sim |
| Insights - gravar ou atualizar configuração de KPI | Sim | Não | Não |

## Escopo de função padrão {#default-role-scope}

>[!IMPORTANT]
>
>As funções de Fidelidade padrão têm escopo somente para a sandbox **Prod**.

Para conceder aos usuários acesso a uma sandbox de não produção, como uma sandbox de preparo ou desenvolvimento, crie uma função personalizada para essa sandbox e atribua as mesmas permissões que a função padrão correspondente.

## Permissões disponíveis para funções personalizadas {#custom-role-permissions}

Ao criar uma função personalizada para uma sandbox de não produção, selecione uma das permissões abaixo. Para replicar uma função padrão, consulte as permissões listadas na seção função relevante acima.

| Permissão | Descrição |
| - | - |
| Gerenciar desafios de fidelidade | Operações completas de desafio: criar, editar, excluir, publicar, desfazer a publicação, arquivar e acionar a geração de jornadas |
| Desenvolver desafios de fidelidade | Crie e edite desafios por meio da API. Ações de exclusão e ciclo de vida não são permitidas |
| Exibir desafios de fidelidade | Exibir somente desafios |
| Gerenciar configuração principal de fidelidade | Criar, editar e excluir a configuração da organização principal |
| Configurar a configuração principal do Loyalty | Criar e editar a configuração da organização principal. A exclusão não é permitida |
| Gerenciar configurações avançadas de fidelidade | Gerenciar pontos de extremidade de premiação e configurações de transformação de evento, incluindo acesso de leitura/gravação a valores confidenciais de credenciais |
| Exibir Configuração de Recompensa de Fidelidade | Exibir provedores de recompensa, definições de recompensa e proxies de recompensa. Os valores confidenciais são excluídos |
| Exibir Configuração de Evento de Fidelidade | Exibir definições de evento e mapeamentos de transformação de evento |
| Gerenciar Catálogo de Produtos de Fidelidade | Visualize, importe de CSV e edite entradas do catálogo de produtos, incluindo inclusões e exclusões; monitore o status do trabalho de importação |
| Exibir Catálogo de Produtos de Fidelidade | Exibir entradas do catálogo de produtos e status do trabalho de importação. Ações de carregamento e edição não são permitidas |
| Gerenciar Insights de Fidelidade | Exibir insights, atualizar a configuração de KPI e acionar o pipeline de insights |
| Desenvolver insights de fidelidade | Exibir dados de insights e atualizar cartões da insight |
| Exibir Insights de Fidelidade | Visualize cartões insight gerados por IA, dados vitais de integridade e dados de desempenho de desafio somente |

## Atribuir funções a usuários {#assign-roles}

>[!IMPORTANT]
>
>Somente administradores de produtos e administradores de sistemas podem gerenciar usuários, grupos e funções.

O Adobe Admin Console oferece suporte a duas abordagens para associar funções a usuários.

### Atribuir usuários diretamente a uma função {#assign-users-directly}

Adicionar usuários individuais diretamente a uma função. Essa abordagem é mais adequada para equipes pequenas ou tarefas pontuais.

### Usar grupos de usuários {#use-user-groups}

Crie um grupo de usuários e atribua a eles uma função e a ambos. Essa abordagem é mais adequada para gerenciar o acesso por departamento ou função em escala.

Para obter instruções passo a passo sobre o gerenciamento de funções, grupos e usuários, consulte a documentação de controle de acesso do Adobe Journey Optimizer:

* [Gerenciar usuários e funções](../administration/permissions.md)
* [Permissões integradas](../administration/ootb-permissions.md)

## Solução de problemas de acesso {#troubleshooting}

Se um usuário não conseguir acessar os Desafios de fidelidade ou um recurso relacionado, verifique o seguinte:

* O usuário é atribuído a uma função de Fidelidade.
* A função inclui a sandbox onde os Desafios de fidelidade estão ativados.
* A função inclui a permissão necessária para a ação que o usuário está tentando executar.
* Para sandboxes de não produção, uma função personalizada foi criada para essa sandbox.
* A organização e a sandbox estão habilitadas para desafios de fidelidade.

Se os problemas de acesso persistirem depois que as permissões forem atualizadas, entre em contato com o representante da Adobe.

