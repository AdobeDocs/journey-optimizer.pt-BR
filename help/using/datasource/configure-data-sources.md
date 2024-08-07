---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma fonte de dados
description: Saiba como configurar uma fonte de dados
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: dados, fonte, configuração, campo
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 8%

---

# Configurar uma fonte de dados {#configure-data-source}

>[!NOTE]
>
>A configuração da fonte de dados é sempre executada por um **usuário técnico**.

Para configurar uma fonte de dados, siga as etapas abaixo:

1. Na seção de menu ADMINISTRAÇÃO, selecione **[!UICONTROL Configurações]**. Na seção **[!UICONTROL Fontes de Dados]**, clique em **[!UICONTROL Gerenciar]**. A lista das fontes de dados é exibida. Consulte [esta página](../start/user-interface.md) para obter mais informações sobre a interface.

   ![](assets/journey18.png)

1. Você pode adicionar grupos de campos à fonte de dados interna (consulte [esta página](../datasource/adobe-experience-platform-data-source.md)) ou criar uma nova fonte de dados externa (consulte [esta página](../datasource/external-data-sources.md)) e grupos de campos associados (consulte [esta página](../datasource/configure-data-sources.md#define-field-groups)).

   ![](assets/journey23.png)

1. Clique em **[!UICONTROL Salvar]**.

   A fonte de dados agora está configurada e pronta para ser usada em suas jornadas.

## Definir grupos de campos {#define-field-groups}

Grupos de campos são conjuntos de campos que você pode recuperar de uma fonte de dados e usar em uma jornada.

Para cada fonte de dados, é possível definir vários grupos de campos.

Por exemplo, você pode criar um grupo de campos com o número de telefone, o email, o nome e o endereço do perfil. Você poderá usar esses dados na jornada para criar condições. Por exemplo, você pode decidir enviar uma notificação por push somente se o cliente tiver instalado o aplicativo móvel. Se estiver vazio, você poderá enviar um email.

Embora um nome padrão seja adicionado automaticamente, recomendamos que você dê um nome ao seu grupo de campos. Na verdade, o nome do grupo de campos ficará visível para outros usuários em [!DNL Journey Optimizer]. Dar um nome relevante aos grupos de campo é uma prática recomendada.

Quando um campo de fonte de dados é usado em uma jornada, o sistema recupera todos os campos definidos para esse grupo de campos. Portanto, selecionar apenas os campos necessários para suas jornadas é uma prática recomendada. Isso reduzirá a latência de solicitação em suas jornadas, aumentando o desempenho. Observe que mais tarde é possível adicionar facilmente mais campos em grupos de campos.

O número de jornadas que usam um grupo de campos é exibido no campo **[!UICONTROL Usado em]**. Você pode clicar no botão **[!UICONTROL Exibir jornadas]** para exibir a lista de jornadas usando este grupo de campos.

>[!NOTE]
>
>Observe que, se um grupo de campos não tiver um campo, ele não será exibido no editor de expressão.

![](assets/journey3bis.png)

## Ciclo de vida do grupo de campos {#field-group-lifecycle}

Você pode adicionar ou remover campos de um grupo de campos que não é usado em nenhum rascunho ou jornada em tempo real.

Você pode adicionar, mas não pode remover, um campo de um grupo de campos usado em uma ou mais jornadas de rascunho ou ativas. Isso evitará quebrar as jornadas.

Para excluir um campo de um grupo de campos usado em uma ou mais jornadas, siga estas etapas. Vamos usar um exemplo de um grupo de campos chamado &quot;Grupo de campos A&quot;.

1. Na lista de grupos de campos, coloque o cursor em &quot;Grupo de campos A&quot; e clique no ícone **[!UICONTROL Duplicar]**, localizado à direita. Nomeie o grupo de campos duplicado como &quot;Grupo de campos B&quot;, por exemplo.
1. Em &quot;Grupo de campos B&quot;, remova os campos que não deseja mais.
1. Em &quot;Grupo de campos A&quot;, verifique onde esse grupo de campos é usado. Essas informações são exibidas no campo **[!UICONTROL Usado em]**.
1. Abra todas as jornadas que usam &quot;Grupo de campos A&quot;.
1. Crie novas versões de cada uma dessas jornadas. Edite todas as atividades usando &quot;Grupo de campos A&quot; e selecione &quot;Grupo de campos B&quot;.
1. Interrompa versões antigas de jornadas que usam &quot;Grupo de campos A&quot;. Você não deve ter nenhuma jornada usando o &quot;Grupo de campos A&quot;.
1. Remova o &quot;Grupo de campos A&quot; pois ele não é mais usado.
