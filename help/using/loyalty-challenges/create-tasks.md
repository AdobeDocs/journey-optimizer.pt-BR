---
solution: Journey Optimizer
product: journey optimizer
title: Criar tarefas para desafios de fidelidade
description: Saiba como criar e configurar tarefas para desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: c1e49173-69cc-4729-9f9a-afea2ccff3fa
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 1203
ht-degree: 10%

---

# Criar tarefas {#create-tasks}

>[!BEGINSHADEBOX]

**Sumário**

[Introdução aos desafios de fidelidade](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Criar e gerenciar desafios**

* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md)
* [Criar desafios](create-challenges.md)
* **Criar tarefas** ◀︎ **Você está aqui**
* [Monitorar o desempenho de desafio de fidelidade](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configurar desafios de fidelidade](loyalty-admin.md)
* [Guia de definição de recompensa](reward-definition-guide.md)
* [Guia do Transformador de eventos](event-transformer-guide.md)
* [Dados e conjuntos de dados de fidelidade](loyalty-data-and-datasets.md)
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../rn/releases.md).

As tarefas definem as ações ou marcos específicos que os clientes devem concluir para ganhar recompensas em um desafio de fidelidade. Você pode configurar tarefas de compras e gastos, ou tarefas de **[!UICONTROL Eventos personalizados]** que rastreiam eventos de experiência do Adobe Experience Platform que sua organização já captura.

Cada tarefa representa uma ação mensurável que contribui para a conclusão do desafio. As tarefas são componentes reutilizáveis que podem ser criados de forma independente e depois adicionados a um ou mais desafios, ou criados diretamente dentro de um desafio.

## Criar uma tarefa {#create-task}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_create"
>title="Criar uma tarefa"
>abstract="Selecione uma atividade de cliente (compra, gasto ou evento personalizado) e configure atributos específicos da atividade. No painel Propriedades, defina o nome e a descrição da tarefa."

É possível criar tarefas a partir de dois pontos de entrada. O processo de configuração é o mesmo, independentemente de onde você começa.

>[!BEGINTABS]

>[!TAB Do inventário de tarefas]

Selecione a guia **[!UICONTROL Tarefas]** e selecione **[!UICONTROL Criar tarefa]**. As tarefas criadas no inventário são salvas e disponibilizadas para reutilização em vários desafios.

![](assets/task-create-inventory.png)

>[!TAB De dentro de um desafio]

Abrir um desafio existente ou criar um novo. Selecione **[!UICONTROL Adicionar tarefa]** e clique no botão **[!UICONTROL Novo]**. Tarefas criadas dessa maneira são automaticamente adicionadas ao seu desafio e também salvas no inventário de Tarefas para reutilização em outros desafios.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## Escolher atividade do cliente {#choose-activity}

Selecione o tipo de atividade que os clientes devem executar para concluir esta tarefa:

* **[!UICONTROL Compra]**: os clientes devem comprar um ou mais itens para concluir esta tarefa
* **[!UICONTROL Gastos]**: os clientes devem gastar um valor especificado para concluir esta tarefa
* **[!UICONTROL Evento personalizado]**: os clientes devem executar uma atividade representada por um evento de experiência do Adobe Experience Platform. Por exemplo, check-in de hotel, ação de aplicativo móvel ou envio de revisão. O evento subjacente já deve ter sido capturado no Experience Platform e mapeado por meio de uma definição de evento no menu **[!UICONTROL Administrador de fidelidade]**. [Saiba como configurar definições de evento](loyalty-admin.md#event-definitions)

Para selecionar uma atividade, clique no ícone **+** e selecione a atividade de cliente que melhor se alinha às suas metas de resultado. Cada tipo de atividade tem atributos configuráveis específicos para definir e moldar ainda mais os requisitos da tarefa.
![](assets/task-create-activity.png)

## Definir os atributos da tarefa {#define-attributes}

Configure os atributos da tarefa com base no tipo de atividade selecionado. Navegue pelas guias abaixo para ver os atributos disponíveis para cada tipo de atividade:

>[!BEGINTABS]

>[!TAB Atividade de compra]

Atributos disponíveis para atividades de **Compra**:

* **[!UICONTROL Quantidade]**: insira o número de itens que devem ser comprados para concluir esta tarefa.
* **[!UICONTROL Itens qualificados e exclusões]**: defina itens ou grupos de itens que contam para a conclusão da tarefa e aqueles que não são qualificados, ou escolha **[!UICONTROL Trazer seus próprios dados]** para impulsionar a qualificação de seus dados externos. [Saiba mais](#eligible-items-exclusions)
* **[!UICONTROL Valor mínimo de gasto]**: defina um requisito de valor mínimo de compra.
* **[!UICONTROL Número máximo de transações]**: limite quantas transações podem ser usadas para concluir a tarefa.

![](assets/task-create-purchase.png)

>[!TAB Gastar atividade]

Atributos disponíveis para atividades de **Gasto**:

* **[!UICONTROL Valor]**: insira o valor total de gastos necessário para concluir a tarefa.
* **[!UICONTROL Itens qualificados e exclusões]**: defina itens ou grupos de itens que contam para a conclusão da tarefa e os que não contam. [Saiba mais sobre itens qualificados e exclusões](#eligible-items-exclusions)
* **[!UICONTROL Número máximo de transações]**: especifique quantas transações podem atender ao requisito de gastos. Você pode ativar esse atributo no ícone de parâmetros.

![](assets/task-create-spend.png)

>[!TAB Atividade de evento personalizada]

Atributos disponíveis para atividades de **[!UICONTROL Evento personalizado]**:

* **[!UICONTROL Valores de evento personalizados]**: insira os valores para o evento personalizado que os clientes devem concluir. Use uma vírgula para separar cada valor. Esses valores devem corresponder às definições de evento configuradas no menu **[!UICONTROL Administrador de fidelidade]**. [Saiba como configurar definições de evento](loyalty-admin.md#event-definitions)

![](assets/task-create-custom.png)

>[!ENDTABS]

## Defina itens elegíveis e exclusões {#eligible-items-exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_eligible_items_exclusion"
>title="Itens elegíveis e exclusões"
>abstract="Nas atividades **Compra** e **Gasto**, use o atributo **[!UICONTROL Itens elegíveis e exclusões]** para selecionar quais itens e grupos contam para a conclusão da tarefa e quais são excluídos. Pesquise itens ou grupos no inventário de produtos configurado por administradores e, em seguida, inclua-os ou exclua-os conforme necessário."

<!-- SCREENSHOT: Eligible items & exclusions picker showing the item and group table with Include and Exclude actions -->

Para atividades de **Compra** e **Gasto**, é possível usar a seção **[!UICONTROL Itens qualificados e exclusões]** para definir quais itens e grupos estão qualificados e quais foram excluídos. Isso permite direcionar produtos, categorias ou locais específicos para alinhar às metas do desafio.

Os itens e grupos disponíveis no seletor são definidos por usuários administradores no menu **[!UICONTROL Administrador de fidelidade]**. Os administradores carregam o inventário de produtos usado para itens elegíveis e configuram exclusões em toda a organização que são aplicadas automaticamente quando os profissionais de marketing criam tarefas. [Saiba como configurar o inventário de produtos](loyalty-admin.md#product-inventory) e [exclusões](loyalty-admin.md#exclusions)

As tarefas **[!UICONTROL Evento personalizado]** não usam itens e exclusões qualificados; a conclusão é orientada pelos **[!UICONTROL Valores de evento personalizado]** que você configurar.

Por exemplo, é possível limitar uma tarefa a categorias de produto específicas ou excluir cartões-presente ou itens promocionais da contagem até a conclusão da tarefa.

![](assets/task-create-eligible.png)

### Definir itens qualificados para a tarefa

Para definir itens qualificados, selecione **[!UICONTROL Adicionar]** na seção **[!UICONTROL Itens qualificados e exclusões]**.

No seletor, selecione os itens ou grupos que devem contar para a conclusão da tarefa e selecione **[!UICONTROL Incluir]**. Os itens e grupos incluídos são adicionados à lista elegível.

![](assets/task-create-eligible-add.png)

Se nenhum item ou grupo elegível for selecionado, as compras não estarão limitadas a um conjunto de inventário específico, a menos que as exclusões estejam configuradas.

### Excluir itens da tarefa

Para excluir itens da tarefa, selecione **[!UICONTROL Adicionar]** na seção **[!UICONTROL Itens qualificados e exclusões]**.

Selecione os itens ou grupos que não devem ser incluídos na conclusão da tarefa e selecione **[!UICONTROL Excluir]**.

![](assets/task-create-exclusion-add.png)

Os itens da lista de exclusões globais são adicionados automaticamente como exclusões. As exclusões têm prioridade sobre as inclusões: os itens listados como excluídos não contam, mesmo se também fizerem parte de um grupo incluído.

### Traga seus próprios dados para elegibilidade e exclusões {#byod-personalization}

>[!AVAILABILITY]
>
>A opção **[!UICONTROL Trazer seus próprios dados]** está disponível atualmente para um conjunto restrito de organizações e será disponibilizada de forma mais ampla em uma versão futura.

Além de selecionar itens e grupos no Journey Optimizer, você também pode impulsionar a qualificação de seus dados externos de Desafios de Fidelidade em tempo de execução usando a opção **[!UICONTROL Trazer seus próprios dados]**.

Quando **[!UICONTROL Trazer seus próprios dados]** é selecionado, a qualificação por participante é resolvida no tempo de execução a partir dos dados sincronizados com seu ambiente de Desafios de Fidelidade, em vez de uma lista de IDs de item.

Para usar essa opção, selecione o ícone de personalização em **[!UICONTROL Itens qualificados e exclusões]** e escolha **[!UICONTROL Trazer seus próprios dados]**.

![](assets/tasks-create-eligible-bring.png)

>[!IMPORTANT]
>
>Ao atribuir esta tarefa a um desafio, selecione **[!UICONTROL Padrão]** como o tipo de desafio. Não selecione **[!UICONTROL Trazer seus próprios dados]** no nível do desafio, pois essa opção é reservada para desafios totalmente orientados por dados, em que toda a estrutura, incluindo tarefas e recompensas, é fornecida externamente.

## Definir propriedades da tarefa {#define-task-properties}

No painel de tarefas **[!UICONTROL Propriedades]**, configure as informações básicas da tarefa:

* **[!UICONTROL Nome da tarefa]**: digite um nome descritivo para a tarefa.
* **[!UICONTROL Descrição da tarefa]**: a descrição é gerada automaticamente com base na atividade e nos atributos configurados. Para inserir uma descrição personalizada, desative a opção de geração automática e insira sua descrição no campo de texto.

![](assets/tasks-create-properties.png)

Após configurar todos os atributos e propriedades, selecione **[!UICONTROL Criar]** para salvar a tarefa. A tarefa é salva no inventário de tarefas e, se criada a partir de um desafio, é automaticamente adicionada a esse desafio.
