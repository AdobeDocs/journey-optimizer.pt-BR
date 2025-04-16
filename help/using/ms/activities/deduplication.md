---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de desduplicação
description: Saiba como usar a atividade de desduplicação
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 57%

---

# Desduplicação {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Campos para identificar duplicatas"
>abstract="Na seção **Campos para identificar duplicatas**, clique no botão **Adicionar atributo** para especificar os campos nos quais os valores idênticos permitem a identificação de duplicatas, como: endereço de email, nome, sobrenome, etc. A ordem dos campos permite especificar os que devem ser processados primeiro."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Atividade Desduplicação"
>abstract="A atividade **Desduplicação** permite excluir duplicatas nos resultados das atividades de entrada. Ela é usada principalmente após atividades de direcionamento e antes de atividades que permitem o uso de dados direcionados."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **Gerar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Configurações de desduplicação"
>abstract="Para excluir duplicatas nos dados recebidos, defina o método de desduplicação nos campos abaixo. Por padrão, somente um registro é mantido. Também é necessário selecionar o modo de desduplicação com base em uma expressão ou um atributo. Por padrão, o registro a ser mantido fora das duplicatas é selecionado aleatoriamente."

A atividade **Deduplication** é uma atividade **Targeting**. Essa atividade permite excluir duplicados no(s) resultado(s) das atividades de entrada, por exemplo, perfis duplicados na lista de recipients. A atividade **Deduplication** geralmente é usada após as atividades de direcionamento e antes das atividades que permitem o uso de dados direcionados.

## Configurar a atividade de desduplicação{#deduplication-configuration}

Siga estas etapas para configurar a atividade **Desduplicação**:

![](../assets/workflow-deduplication.png)

1. Adicione uma atividade **Deduplication** à sua campanha orquestrada.

1. Na seção **Campos para identificar duplicatas**, clique no botão **Adicionar atributo** para especificar os campos nos quais os valores idênticos permitem a identificação de duplicatas, como: endereço de email, nome, sobrenome, etc. A ordem dos campos permite especificar os que devem ser processados primeiro.

1. Na seção **Configurações de desduplicação**, selecione o número de **Duplicatas exclusivas a serem mantidas**. O valor padrão para esse campo é 1. O valor 0 permite manter todas as duplicatas.

   Por exemplo, se os registros A e B forem considerados duplicatas do registro Y, e um registro C for considerado uma duplicata do registro Z:

   * Se o valor do campo for 1: somente os registros Y e Z são mantidos.
   * Se o valor do campo for 0: todos os registros são mantidos.
   * Se o valor do campo for 2: os registros C e Z são mantidos. Os dois registros de A, B e Y são mantidos por acaso ou dependendo do método de desduplicação selecionado posteriormente.

1. Selecione o **Método de desduplicação** a ser usado:

   * **Seleção aleatória**: seleciona aleatoriamente o registro a ser mantido fora das duplicatas.
   * **Usando uma expressão**: mantenha os registros nos quais o valor da expressão inserida é o menor ou o maior.
   * **Valores não vazios**: mantém os registros para os quais a expressão não está vazia.
   * **Seguindo uma lista de valores**: defina uma prioridade de valor para um ou mais campos. Para definir os valores, clique em **Atributo** para selecionar um campo ou criar uma expressão e, em seguida, adicione o(s) valor(es) à tabela apropriada. Para definir um novo campo, clique no **botão Adicionar** localizado acima da lista de valores.

1. Marque a opção **Gerar complemento** se desejar explorar a população restante. O complemento consiste de todas as duplicatas. Uma transição adicional será adicionada à atividade.

## Exemplo{#deduplication-example}

No exemplo a seguir, use uma atividade de desduplicação para excluir duplicatas do target antes de enviar um delivery. Os perfis duplicados identificados são adicionados a um público-alvo dedicado que pode ser reutilizado se necessário. Escolha o endereço de **Email** para identificar as duplicatas. Mantenha 1 entrada e selecione o método de desduplicação **Aleatório**.

![](../assets/workflow-deduplication-example.png)
