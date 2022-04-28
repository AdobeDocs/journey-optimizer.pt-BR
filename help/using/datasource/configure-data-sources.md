---
title: Configurar uma fonte de dados
description: Saiba como configurar uma fonte de dados
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: 5596c851b70cc38cd117793d492a15fd4ce175ef
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 10%

---

# Configurar uma fonte de dados {#configure-data-source}

Estas são as etapas principais de configuração da fonte de dados:

>[!NOTE]
>
>A configuração da fonte de dados é sempre executada por um **usuário técnico**.

1. Na seção do menu ADMINISTRATION (ADMINISTRAÇÃO), selecione **[!UICONTROL Configurations]**. No  **[!UICONTROL Data Sources]** seção , clique em **[!UICONTROL Manage]**. A lista das fontes de dados é exibida. Consulte [esta página](../start/user-interface.md) para obter mais informações sobre a interface.

   ![](assets/journey18.png)

1. Em seguida, é possível adicionar grupos de campos à fonte de dados integrada (consulte [esta página](../datasource/adobe-experience-platform-data-source.md)) ou criar uma nova fonte de dados externa (consulte [esta página](../datasource/external-data-sources.md)) e grupos de campos associados (consulte [esta página](../datasource/configure-data-sources.md#define-field-groups)).

   ![](assets/journey23.png)

1. Clique em **[!UICONTROL Save]**.

   A fonte de dados agora está configurada e pronta para ser usada em suas jornadas.

## Definir grupos de campos {#define-field-groups}

Grupos de campos são conjuntos de campos que podem ser recuperados de uma fonte de dados e usados em uma jornada.

Para cada fonte de dados, você pode definir vários grupos de campos.

Por exemplo, você pode criar um grupo de campos com o número de telefone, o email, o nome e o endereço do perfil. Você poderá usar esses dados na jornada para criar condições. Por exemplo, você pode decidir enviar uma notificação por push somente se o cliente tiver instalado o aplicativo móvel. Se estiver vazio, você pode enviar um email.

Mesmo que um nome padrão seja adicionado automaticamente, recomendamos que você dê um nome ao seu grupo de campos. Na verdade, o nome do grupo de campos estará visível para outros usuários em [!DNL Journey Optimizer]. Fornecer um nome relevante para grupos de campos é uma prática recomendada.

Quando um campo de fonte de dados é usado em uma jornada, o sistema recuperará todos os campos definidos para esse grupo de campos. Portanto, selecionar apenas os campos necessários para suas jornadas é uma prática recomendada. Isso reduzirá a latência de solicitação em suas jornadas, aumentando assim o desempenho. Observe que é possível adicionar mais campos facilmente posteriormente em grupos de campos.

O número de jornadas que usam um grupo de campos é exibido na variável **[!UICONTROL Used in]** campo. Você pode clicar no botão **[!UICONTROL View journeys]** para exibir a lista de jornadas usando esse grupo de campos.

>[!NOTE]
>
>Observe que, se um grupo de campos não tiver um campo, ele não será exibido no editor de expressão.

![](assets/journey3bis.png)

## Ciclo de vida do grupo de campos {#field-group-lifecycle}

Você pode adicionar ou remover campos de um grupo de campos que não é usado em nenhum rascunho ou jornada ativa.

É possível adicionar, mas não é possível remover um campo de um grupo de campos usado em uma ou mais jornadas de rascunho ou ativas. Isso evitará quebrar jornadas.

Para excluir um campo de um grupo de campos usado em uma ou mais jornadas, siga estas etapas. Vamos usar um exemplo de um grupo de campos chamado &quot;Grupo de campos A&quot;.

1. Na lista de grupos de campos, coloque o cursor em &quot;Grupo de campos A&quot; e clique na guia **[!UICONTROL Duplicate]** ícone localizado à direita. Nomeie o grupo de campos duplicados como &quot;Grupo de campos B&quot;, por exemplo.
1. Em &quot;Grupo de campos B&quot;, remova os campos que não deseja mais.
1. Em &quot;Grupo de campos A&quot;, verifique onde esse grupo de campos é usado. Essas informações são exibidas na **[!UICONTROL Used in]** campo.
1. Abra todas as jornadas que usam &quot;Grupo de campos A&quot;.
1. Crie novas versões de cada uma dessas jornadas. Edite todas as atividades usando &quot;Grupo de campos A&quot; e selecione &quot;Grupo de campos B&quot;.
1. Pare as versões antigas de jornadas que usam o &quot;Grupo de campos A&quot;. Você não deve ter jornada usando &quot;Grupo de campos A&quot;.
1. Remova &quot;Grupo de campos A&quot; como ele não é mais usado.
