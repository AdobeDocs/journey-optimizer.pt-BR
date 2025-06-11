---
solution: Journey Optimizer
product: journey optimizer
title: Crie sua primeira regra
description: Saiba como criar regras para suas campanhas orquestradas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 5e956a6a-0b89-4d78-8f16-fe9fceb25674
source-git-commit: 435b4a7eee9428c7f0efeb62c72b39c0e2aaabba
workflow-type: tm+mt
source-wordcount: '1801'
ht-degree: 7%

---

# Crie sua primeira regra {#build-query}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Acessar e gerenciar campanhas orquestradas](access-manage-orchestrated-campaigns.md) | [Etapas principais para a criação de campanha orquestrada](gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/><b>[Criar a primeira consulta](build-query.md)</b><br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

As principais etapas para criar regras para suas campanhas orquestradas são as seguintes:

1. **Adicionar condições** - Crie condições personalizadas para filtrar sua consulta criando sua própria condição com atributos do banco de dados e expressões avançadas.
1. **Combinar condições** - Organize as condições na tela usando grupos e operadores lógicos.
1. **Verificar e validar a regra** - Verifique os dados resultantes da regra antes de salvá-la.

## Adicionar uma condição {#conditions}

Para adicionar condições em sua query, siga estas etapas:

1. Acesse o construtor de regras de uma atividade **[!UICONTROL Criar público-alvo]**.

1. Clique no botão **Adicionar condição** para criar uma primeira condição para sua consulta.

   Você também pode iniciar seu query usando um filtro predefinido. Para fazer isso, clique no botão **[!UICONTROL Selecionar ou salvar filtro]** e escolha **[!UICONTROL Selecionar filtro predefinido]**.

   ![imagem mostrando o construtor de regras](assets/rule-builder-add.png)

1. Identifique o atributo do banco de dados a ser usado como critério para a sua condição. O ícone &quot;i&quot; ao lado de um atributo fornece informações sobre a tabela em que ele está armazenado e seu tipo de dados.

   ![imagem mostrando a seleção de um atributo](assets/rule-builder-select-attribute.png)

   >[!NOTE]
   >
   >O botão **Editar expressão** permite usar o editor de expressão para definir manualmente uma expressão usando campos do banco de dados e funções auxiliares. [Saiba como editar expressões](../orchestrated/edit-expressions.md)

1. Clique na ![imagem que mostra o botão Mais ações](assets/do-not-localize/rule-builder-icon-more.svg) ao lado de um atributo para acessar estas opções adicionais:

+++ Distribuição de valores

   Analise a distribuição de valores para um determinado atributo dentro da tabela. Esse recurso é útil para entender os valores disponíveis, suas contagens e porcentagens. Isso também ajuda a evitar problemas como inconsistências no uso de maiúsculas e minúsculas ou na ortografia ao criar consultas ou expressões.

   Para atributos com um grande número de valores, a ferramenta exibe apenas os primeiros vinte. Nesses casos, uma notificação de **[!UICONTROL Carregamento parcial]** é exibida para indicar essa limitação. Aplique filtros avançados para refinar os resultados exibidos e se concentrar em valores ou subconjuntos de dados específicos.

   ![imagem mostrando a interface de Distribuição de valores](assets/rule-builder-distribution-values.png)

+++

+++ Adicionar aos favoritos

   Adicionar atributos ao menu de favoritos fornece acesso rápido aos atributos usados com mais frequência. Você pode adicionar até 20 atributos aos favoritos. Atributos favoritos e recentes são associados a cada usuário dentro de uma organização, garantindo acessibilidade em diferentes computadores e proporcionando uma experiência contínua em todos os dispositivos.

   Para acessar os atributos que você adicionou aos favoritos, use o menu **[!UICONTROL Favoritos e recentes]**. Os atributos favoritos aparecem primeiro, seguido pelos usados recentemente, facilitando a localização dos atributos necessários. Para remover um atributo dos favoritos, clique no ícone de estrela novamente.

   ![imagem mostrando a interface de favoritos](assets/rule-builder-favorites.png)

+++

1. Clique em **[!UICONTROL Confirmar]** para adicionar o atributo selecionado à sua condição.

1. Um painel de propriedades é exibido, onde você pode configurar o valor desejado para o atributo.

   ![imagem mostrando o construtor de regras com uma condição adicionada](assets/rule-builder-condition.png)

1. Selecione o **[!UICONTROL Operador]** a ser aplicado na lista suspensa. Vários operadores estão disponíveis para uso. Os operadores disponíveis na lista suspensa dependem do tipo de dados do atributo.

   +++Lista de operadores disponíveis

   | Operador | Finalidade | Exemplo |
   |---|---|---|
   | Igual a | Retorna um resultado idêntico aos dados inseridos na segunda coluna de valor. | Last name (@lastName) equal to &#39;Jones&#39; retornará apenas destinatários cujo sobrenome seja Jones. |
   | Não é igual a | Retorna todos os valores não idênticos ao valor inserido. | Idioma (@language) não é igual a &#39;English&#39;. |
   | Maior que | Retorna um valor maior que o valor digitado. | Age (@age) greater than 50 retornará todos os valores maiores que &#39;50&#39;, como &#39;51&#39;, &#39;52&#39;. |
   | Menor que | Retorna um valor menor que o valor digitado. | Creation date (@created) before &#39;DaysAgo(100)&#39; retornará todos os destinatários criados menos de 100 dias atrás. |
   | Maior que ou igual a | Retorna todos os valores iguais ou maiores que o valor inserido. | Age (@age) greater than or equal to &#39;30&#39; retornará todos os destinatários maiores de 30 anos ou mais. |
   | Menor que ou igual a | Retorna todos os valores iguais ou inferiores ao valor inserido. | Age (@age) less than or equal to &#39;60&#39; retornará todos os destinatários com 60 anos ou menos. |
   | Incluído em | Retorna resultados incluídos nos valores indicados. Esses valores devem ser separados por vírgula. | Birth date (@birthDate) is included in &#39;12/10/1979,12/10/1984&#39; retornará os destinatários nascidos entre essas datas. |
   | Não está em | Funciona como o operador Is included in. Aqui, os recipients são excluídos com base nos valores inseridos. | A data de nascimento (@birthDate) não está incluída em &#39;12/10/1979,12/10/1984&#39;. Os recipients nascidos nessas datas não serão retornados. |
   | Está vazio | Retorna os resultados que correspondem a um valor vazio na segunda coluna de valor. | Mobile (@mobilePhone) is empty retorna todos os destinatários que não têm número de celular. |
   | Não está vazio | Funciona de forma inversa ao operador Is empty. Não é necessário inserir dados na segunda coluna de valor. | O email (@email) não está vazio. |
   | Começa com | Retorna resultados iniciando com o valor inserido. | Account # (@account) começa com &#39;32010&#39;. |
   | Não inicia com | Retorna resultados que não começam com o valor inserido. | Account # (@account) não começa com &#39;20&#39;. |
   | Contains | Retorna resultados contendo pelo menos o valor inserido. | Email domain (@domain) contains &#39;mail&#39; retornará todos os nomes de domínio que contêm &#39;mail&#39;, como &#39;gmail.com&#39;. |
   | Não contém | Retorna resultados não contendo o valor inserido. | O domínio de email (@domain) não contém &#39;vo&#39;. Nomes de domínio contendo &#39;vo&#39;, como &#39;voila.fr&#39;, não aparecerão nos resultados. |
   | Curtir | Semelhante ao operador Contains, permite inserir um caractere curinga % no valor. | Sobrenome (@lastName) como &#39;Jon%s&#39;. O caractere curinga atua como um &quot;joker&quot; para encontrar nomes como &quot;Jones&quot;. |
   | Not like | Semelhante ao operador Contains, permite inserir um caractere curinga % no valor. | Sobrenome (@lastName) diferente de &#39;Smi%h&#39;. Os destinatários que têm &#39;Smith&#39; como sobrenome não serão retornados. |

   +++

1. No campo **Value**, defina o valor esperado. Você também pode usar o editor de expressão para definir manualmente uma expressão usando campos do banco de dados e funções auxiliares. Para fazer isso, clique no ícone ![imagem mostrando o ícone do editor de expressão](assets/do-not-localize/rule-builder-icon-editor.svg). [Saiba como editar expressões](../orchestrated/edit-expressions.md)

   Para atributos do tipo data, os valores predefinidos estão disponíveis usando a opção **[!UICONTROL Predefinições]**.

   +++Veja o exemplo

   ![imagem mostrando a opção de predefinição](assets/rule-builder-attribute-preset.png)

   +++

### Condições personalizadas em tabelas vinculadas (links 1-1 e 1-N){#links}

As condições personalizadas permitem consultar tabelas vinculadas à tabela usada atualmente pela regra. Isso inclui tabelas com um link de cardinalidade 1-1 ou tabelas de coleção (link 1-N).

Para um link **1-1**, navegue até a tabela vinculada, selecione o atributo desejado e defina o valor esperado.

Você também pode selecionar diretamente um link de tabela no seletor de **Valor** e confirmar. Nesse caso, os valores disponíveis para a tabela selecionada precisam ser selecionados usando um seletor dedicado, como mostrado no exemplo abaixo.

+++Exemplo de consulta

Aqui, a consulta está direcionando marcas cujo rótulo é &quot;running&quot;.

1. Navegue dentro da tabela **Marca** e selecione o atributo **Etiqueta**.

   ![Captura de tela da tabela Marca](assets/rule-builder-1-1-attribute.png)

1. Defina o valor esperado para o atributo.

   ![Captura de tela da tabela Marca](assets/rule-builder-1-1-attribute-value.png)

Esta é uma amostra de consulta em que um link de tabela foi selecionado diretamente. Os valores disponíveis para esta tabela devem ser selecionados em um seletor dedicado.

![Captura de tela da tabela Marca](assets/rule-builder-1-1-attribute-table.png)

+++

Para um link **1-N**, você pode definir subcondições para refinar sua consulta, como mostrado no exemplo abaixo.

+++Exemplo de consulta

Aqui, o query é direcionado a recipients que fizeram compras relacionadas ao produto Brewmsaster, por mais de 100$.

1. Selecione a tabela **Compras** e confirme.

1. Clique em **[!UICONTROL Adicionar condição]** para definir as subcondições a serem aplicadas à tabela selecionada.

   ![Captura de tela da tabela Compra](assets/rule-builder-1-n-purchase.png)

1. Adicione subcondições para atender às suas necessidades.

   ![Captura de tela da tabela Compra](assets/rule-builder-1-n-collection.png)

+++

### Condições personalizadas com dados agregados {#aggregate}

As condições personalizadas permitem executar operações agregadas. Para fazer isso, você precisa selecionar diretamente um atributo de uma tabela de coleção:

1. Navegue dentro da tabela de coleção desejada e selecione o atributo no qual deseja executar uma operação agregada.

1. No painel de propriedades, alterne a opção **Aggregate data** e selecione a função de agregação desejada.

   ![Captura de tela da opção Dados agregados](assets/rule-builder-aggregate.png)

## Combinar condições usando operadores {#operators}

Cada vez que você adiciona uma nova condição à regra, ela é automaticamente vinculada à condição existente por um operador **AND**. Isso significa que os resultados das duas condições são combinados.

Para alterar o operador entre condições, clique nele e selecione o operador desejado.

![Exemplo de uma consulta](assets/rule-builder-change-operator.png)

Os operadores disponíveis são:

* **AND (Interseção)**: combina resultados que correspondem a todos os componentes de filtragem nas transições de saída.
* **OR (União)**: inclui resultados que correspondem a pelo menos um dos componentes de filtragem nas transições de saída.
* **EXCETO (Exclusão)**: exclui resultados que correspondem a todos os componentes de filtragem na transição de saída.

## Manipular condições {#manipulate}

A barra de ferramentas da tela do construtor de regras fornece opções para manipular facilmente as condições em sua regra:

| Ícone da barra de ferramentas | Descrição |
|--- |--- |
| ![Ícone Mover seleção para cima](assets/do-not-localize/rule-builder-icon-up.svg) | Mova o componente uma linha para cima. |
| ![Ícone Mover seleção para baixo](assets/do-not-localize/rule-builder-icon-down.svg) | Mova o componente uma linha para baixo. |
| ![Ícone de seleção de grupo](assets/do-not-localize/rule-builder-icon-group.svg) | Coloque dois componentes em um grupo. |
| ![Ícone Desagrupar seleção](assets/do-not-localize/rule-builder-icon-ungroup.svg) | Separe os componentes de um único grupo. |
| ![Ícone Expandir tudo](assets/do-not-localize/rule-builder-icon-expand.svg) | Expanda todos os grupos. |
| ![Recolher todo o ícone](assets/do-not-localize/rule-builder-icon-collapse.svg) | Recolher todos os grupos. |
| ![Ícone Remover tudo](assets/do-not-localize/rule-builder-icon-delete.svg) | Remova todos os grupos e componentes. |

Dependendo das suas necessidades, talvez seja necessário criar grupos intermediários de componentes, agrupando os componentes em um mesmo grupo e vinculando-os.

* Para agrupar duas condições existentes, selecione uma das duas condições e clique no botão ![Mover ícone de seleção para cima](assets/do-not-localize/rule-builder-icon-up.svg) ou ![Mover ícone de seleção para baixo](assets/do-not-localize/rule-builder-icon-down.svg) para agrupá-lo com a condição acima ou abaixo.

* Para agrupar uma condição existente com uma nova, selecione a condição, clique na ![imagem que mostra o botão Mais ações](assets/do-not-localize/rule-builder-icon-more.svg) e selecione **[!UICONTROL Adicionar grupo]**. Selecione o novo atributo a ser adicionado ao grupo e confirme.

  ![](assets/rule-builder-edit-groups.png)

No exemplo abaixo, criamos um grupo intermediário para clientes-alvo que compraram o produto BrewMaster ou VanillaVelvet.

![](assets/rule-builder-groups.png)

## Verificar e validar sua consulta

Depois de criar a consulta na tela, você pode verificá-la usando o painel **Propriedades da regra**. As operações disponíveis são:

* **Exibir resultados:** Exibe os dados resultantes da sua consulta.
* **Visualização de código**: exibe uma versão baseada em código da consulta no SQL.
* **Calcular**: atualiza e exibe o número de registros direcionados pela sua regra.
* **Selecionar ou salvar filtro**: escolha um filtro predefinido existente para usar na tela ou salve sua consulta como um filtro predefinido para reutilização futura.

<br/>

    >[!IMPORTANT]
    >
    >Selecione um filtro predefinido no painel de propriedades Regra para substituir a regra que foi criada na tela pelo filtro selecionado.

Quando a regra estiver pronta, clique no botão **[!UICONTROL Confirmar]** no para salvá-la.
