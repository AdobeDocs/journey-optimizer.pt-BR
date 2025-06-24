---
solution: Journey Optimizer
product: journey optimizer
title: Usar dados do Adobe Experience Platform para a tomada de decisão (Beta)
description: Saiba como usar os dados do Adobe Experience Platform para a tomada de decisões.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor
exl-id: 46d868b3-01d2-49fa-852b-8c2e2f54292f
source-git-commit: ebefeb59a19e831ec7f86cee690a35fe71e14554
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 2%

---

# Usar dados do Adobe Experience Platform para a tomada de decisão {#aep-data}

>[!CONTEXTUALHELP]
>id="ajo_exd_rules_dataset_lookup"
>title="Pesquisa de conjunto de dados"
>abstract="Usar dados do Adobe Experience Platform em regras de decisão permite definir critérios de qualificação com base em atributos dinâmicos e externos, garantindo que os itens de decisão sejam exibidos somente quando relevantes. Crie um mapeamento para definir como o conjunto de dados do Adobe Experience Platform se une aos dados em [!DNL Journey Optimizer]. Selecione o conjunto de dados com os atributos necessários e escolha uma chave de ligação que exista nos atributos do item de decisão e no conjunto de dados."

>[!CONTEXTUALHELP]
>id="ajo_exd_formula_dataset_lookup"
>title="Pesquisa de conjunto de dados"
>abstract="As fórmulas de classificação definem a prioridade dos itens de decisão. Ao usar atributos de conjunto de dados do [!DNL Adobe Experience Platform], você pode ajustar dinamicamente a lógica de classificação para refletir condições reais. Crie um mapeamento para definir como o conjunto de dados do Adobe Experience Platform se une aos dados em [!DNL Journey Optimizer]. Selecione o conjunto de dados com os atributos necessários e escolha uma chave de ligação que exista nos atributos do item de decisão e no conjunto de dados"

>[!AVAILABILITY]
>
>Esse recurso está atualmente disponível para todos os clientes como uma versão beta pública. Entre em contato com o representante de sua conta se desejar obter acesso.

[!DNL Journey Optimizer] permite que você aproveite os dados de [!DNL Adobe Experience Platform] para a tomada de decisão. Isso permite estender a definição dos atributos de decisão para dados adicionais nos conjuntos de dados para atualizações em massa que mudam periodicamente, sem precisar atualizar manualmente os atributos, um de cada vez. Por exemplo, disponibilidade, tempos de espera etc.

## Restrições e diretrizes do Beta {#guidelines}

Antes de começar, observe as seguintes restrições e diretrizes:

* Uma política de decisão pode fazer referência a até três conjuntos de dados no total, em todas as suas regras de decisão e fórmulas de classificação combinadas. Por exemplo, se as regras usarem dois conjuntos de dados, as fórmulas poderão usar apenas um conjunto de dados adicional.
* Uma regra de decisão pode usar três conjuntos de dados.
* Uma fórmula de classificação pode usar três conjuntos de dados.
* Quando uma política de decisão é avaliada, o sistema executa até 1000 consultas (pesquisas) de conjunto de dados no total. Cada mapeamento do conjunto de dados usado por um item de decisão conta como uma consulta. Exemplo: se um item de decisão usar dois conjuntos de dados, avaliar essa oferta contará como duas consultas para o limite de 1000 consultas.

## Ativar um conjunto de dados para pesquisa de dados {#enable}

Para usar dados de um conjunto de dados [!DNL Adobe Experience Platform] para a tomada de decisão, primeiro você deve habilitá-lo para a pesquisa por meio de uma chamada de API. Para obter instruções detalhadas, consulte esta seção: [Aproveitar conjuntos de dados do Adobe Experience Platform no Journey Optimizer](../data/lookup-aep-data.md).

## Usar dados do Adobe Experience Platform para a tomada de decisão

Depois que um conjunto de dados é ativado para pesquisa, você pode usar seus atributos para enriquecer a lógica de decisão com dados externos. Isso é especialmente útil para atributos que mudam com frequência, como disponibilidade de produtos ou preços em tempo real.

Os atributos dos conjuntos de dados do Adobe Experience Platform podem ser usados em duas partes da lógica de decisão:

* **Regras de decisão**: defina se um item de decisão está qualificado para ser exibido.
* **Fórmulas de Classificação**: priorizar itens de decisão com base em dados externos.

As próximas seções explicam como usar os dados do Adobe Experience Platform em ambos os contextos.

### Regras de decisão {#rules}

Usar dados do Adobe Experience Platform em regras de decisão permite definir critérios de qualificação com base em atributos dinâmicos e externos, garantindo que os itens de decisão sejam exibidos somente quando relevantes.

Por exemplo, digamos que uma retailer online queira promover recomendações de produto com base no inventário da loja local. Um produto só deve ser qualificado para recomendação se estiver em estoque no local mais próximo. Um conjunto de dados contendo atualizações diárias de inventário é carregado para o Adobe Experience Platform. A lógica da regra verifica se o `inventory_count` de um determinado produto é maior que 0 para a loja preferencial do cliente. Em caso afirmativo, o item de decisão é elegível.

Para usar os dados do Adobe Experience Platform em regras de decisão, siga estas etapas:

1. Vá para o menu **[!UICONTROL Configuração de estratégia]** / **[!UICONTROL Regras de decisão]** e selecione **[!UICONTROL Criar regra com conjunto de dados]**.

   ![](assets/exd-lookup-rule.png)

1. Clique em **[!UICONTROL Criar mapeamento]** para definir como o conjunto de dados do Adobe Experience Platform se une aos dados em [!DNL Journey Optimizer].

   * Selecione o conjunto de dados com os atributos necessários.
   * Escolha uma chave de associação (por exemplo, ID do produto ou ID da loja) que exista nos atributos do item de decisão e no conjunto de dados.

   ![](assets/exd-lookup-mapping.png)

   >[!NOTE]
   >
   >É possível criar até 3 mapeamentos por regra.

1. Clique em **[!UICONTROL Continuar]**. Agora você pode acessar os atributos do conjunto de dados no menu **[!UICONTROL Pesquisa de conjunto de dados]** e usá-los nas condições da regra. [Saiba como criar uma regra de decisão](../experience-decisioning/rules.md#create)

   ![](assets/exd-lookup-menu.png)

### Fórmulas de classificação

As fórmulas de classificação definem a prioridade dos itens de decisão. Ao usar atributos de conjunto de dados do [!DNL Adobe Experience Platform], você pode ajustar dinamicamente a lógica de classificação para refletir condições reais.

Por exemplo, considere que uma companhia aérea use uma fórmula de classificação para priorizar ofertas de atualização. Se um cliente tiver um nível de fidelidade alto e a disponibilidade atual de vagas for baixa (com base em um conjunto de dados atualizado por hora), ele receberá prioridade mais alta. O conjunto de dados inclui campos como `flight_number`, `available_seats` e `loyalty_score`.

Para usar os dados do Adobe Experience Platform em fórmulas de classificação, siga estas etapas:

1. Criar ou editar uma fórmula de classificação. Na seção **[!UICONTROL Pesquisa de conjunto de dados]**, clique em **[!UICONTROL Criar mapeamento]**.

1. Defina o mapeamento do conjunto de dados:

   * Selecione o conjunto de dados apropriado (por exemplo, disponibilidade de vagas por voo).
   * Escolha uma chave de associação (por exemplo, número do voo ou ID do cliente) que exista nos atributos do item de decisão e no conjunto de dados.

   ![](assets/exd-lookup-formula-mapping.png)

   >[!NOTE]
   >
   >Você pode criar até 3 mapeamentos por fórmula de classificação.

1. Use os campos do conjunto de dados para criar a fórmula de classificação como de costume. [Saiba como criar uma fórmula de classificação](../experience-decisioning/exd-ranking-formulas.md#create-ranking-formula)

   ![](assets/exd-lookup-formula-criteria.png)
