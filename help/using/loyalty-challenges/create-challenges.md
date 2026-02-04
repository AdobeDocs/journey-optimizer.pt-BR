---
solution: Journey Optimizer
product: journey optimizer
title: Criar desafios de fidelidade
description: Saiba como criar e configurar desafios de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 1%

---


# Criar desafios {#create-challenges}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos Desafios de Fidelidade](get-started.md) - Visão geral, fluxo de trabalho, pré-requisitos
* [Acessar Desafios de Fidelidade](access-loyalty-challenges.md) - Inventário e filtragem
* **Criar desafios** ◀︎ **Você está aqui** - Criar e configurar desafios
* [Gerenciar desafios](manage-challenges.md) - Editar, monitorar, otimizar

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_create_challenge"
>title="Criar um desafio de fidelidade"
>abstract="Crie um desafio de fidelidade para definir a oferta de engajamento, configure cartões de conteúdo para entrega, adicione tarefas, configure recompensas e, opcionalmente, configure mensagens entre canais."

## Antes de começar {#before-you-start}

Antes de criar um desafio, verifique se você tem:

* Assimilação de dados configurada e validada pelos conectores de origem
* Criação de todos os públicos-alvo necessários no Experience Platform
* Ativos de conteúdo preparados (imagens, texto etc.) para seu desafio
* Definiu as tarefas e recompensas que deseja oferecer

## Criar um desafio {#create-a-challenge}

Para obter etapas detalhadas sobre como criar desafios, incluindo:
* Configuração de propriedades de desafio
* Tipos de desafio (padrão, Streak, sequencial)
* Seleção de público-alvo
* Configuração de data

## Adicionar tarefas {#add-tasks}

As tarefas definem as ações ou marcos específicos que os clientes devem concluir para ganhar recompensas em um desafio de fidelidade. Você pode configurar tipos de tarefa, quantidades, requisitos de produto e valores de recompensa para criar experiências de fidelidade envolventes e personalizadas.

### Visão geral da tarefa {#task-overview}

Cada tarefa representa uma ação mensurável que contribui para a conclusão do desafio. Dependendo do tipo de desafio (Padrão, Streak ou Sequencial), os clientes concluem as tarefas de forma diferente:

* **Desafios padrão**: os clientes concluem qualquer número especificado de tarefas em qualquer ordem
* **Distribuir desafios**: os clientes concluem a mesma tarefa várias vezes consecutivamente
* **Desafios sequenciais**: os clientes concluem as tarefas em uma ordem definida

### Adicionar uma tarefa {#add-task}

Para adicionar uma tarefa ao seu desafio:

1. Abra seu desafio ou crie um novo.

2. Navegue até a seção **[!UICONTROL Tarefas]**.

3. Selecione **[!UICONTROL Adicionar tarefa]** ou **[!UICONTROL Criar nova tarefa]**.

4. Na tela de criação da tarefa, configure as seguintes propriedades.

### Propriedades da tarefa {#task-properties}

#### Informações básicas sobre tarefas {#basic-info}

**[!UICONTROL Nome da tarefa]**: digite um nome descritivo para a tarefa. Esse nome pode ser visto por você e sua equipe, mas pode não ser mostrado aos clientes dependendo do design do cartão de conteúdo.

**[!UICONTROL Descrição da tarefa]**: (opcional) adicione detalhes sobre a finalidade ou os requisitos da tarefa.

**[!UICONTROL Tipo de tarefa]**: selecione o tipo de ação que os clientes devem executar. Os tipos de tarefa disponíveis incluem:

* **[!UICONTROL Compra]**: o cliente faz uma transação de compra
* **[!UICONTROL Valor dos gastos]**: o cliente gasta um valor monetário especificado
* **[!UICONTROL Visita]**: o cliente visita um local físico ou uma propriedade digital
* **[!UICONTROL Compromisso]**: o cliente se envolve com o conteúdo, como visualizar um vídeo ou ler um artigo
* **[!UICONTROL Evento personalizado]**: o cliente aciona um evento personalizado rastreado pela sua assimilação de dados

#### Requisitos de quantidade {#quantity-requirements}

**[!UICONTROL Quantidade necessária]**: especifique quantas vezes o cliente deve executar a tarefa para concluí-la.

Por exemplo:

* Para uma tarefa de Compra: &quot;Comprar 2 itens&quot; (quantidade = 2)
* Para uma tarefa de Quantia de gasto: &quot;Gasto de US$ 50&quot; (quantidade = 50)
* Para uma tarefa de Visita: &quot;Visita 5 vezes&quot; (quantidade = 5)

**[!UICONTROL Período de rastreamento]**: (opcional) defina a janela de tempo para concluir esta tarefa:

* Por duração de desafio (padrão)
* Por dia
* Por semana
* Por mês
* Intervalo de datas personalizado

### Filtragem de produto e SKU {#product-filtering}

Para tarefas de Quantidade de compras e gastos, você pode especificar quais produtos se qualificam para a conclusão da tarefa.

#### Inclusões de produto {#product-inclusions}

Defina quais produtos ou categorias contam para a tarefa:

1. Selecione **[!UICONTROL Adicionar critérios de produto]**.

2. Escolha como definir produtos qualificados:
   * **[!UICONTROL Por SKU]**: insira códigos SKU específicos do produto
   * **[!UICONTROL Por categoria]**: selecione categorias de produtos do catálogo
   * **[!UICONTROL Por atributo]**: filtrar por atributos de produto, como marca, tamanho, cor ou atributos personalizados

3. Insira ou selecione os identificadores de produto:

   **Exemplo - Por SKU**:

   ```text
   SKU001, SKU002, SKU003
   ```

   **Exemplo - Por categoria**:

   * Bebidas > Café
   * Padaria > Pastas

   **Exemplo - Por atributo**:

   * Marca = &quot;Marca Premium&quot;
   * Categoria = &quot;Itens da estação&quot;
   * Preço > US$ 20

4. Selecione **[!UICONTROL Adicionar]** para salvar os critérios do produto.

#### Exclusões de produto {#product-exclusions}

Opcionalmente, exclua produtos específicos da contagem para a tarefa:

1. Selecione **[!UICONTROL Adicionar exclusões]**.

2. Use os mesmos métodos de filtragem que as inclusões de produto para especificar quais produtos devem ser excluídos.

3. Cenários de exclusão comuns:

   * Venda ou itens de compensação
   * Cartões-presente
   * Itens promocionais ou gratuitos
   * Marcas ou categorias específicas

>[!NOTE]
>
>**Lógica de inclusão e exclusão**: quando inclusões e exclusões são definidas:
>
>* Os produtos devem corresponder aos critérios de inclusão
>* Os produtos que correspondem aos critérios de exclusão são removidos, mesmo que correspondam às inclusões
>* Se nenhuma inclusão for definida, todos os produtos serão qualificados, exceto os explicitamente excluídos

#### Exemplos de filtragem de produtos {#product-filtering-examples}

##### Exemplo 1: Desafio do café {#example-1}

* Tipo de tarefa: Compra
* Quantidade necessária: 3
* Inclusões: Categoria = &quot;Bebidas > Café&quot;
* Resultado: Cliente deve comprar 3 bebidas de café

##### Exemplo 2: gasto com prêmio {#example-2}

* Tipo de tarefa: valor do gasto
* Quantidade necessária: US$ 100
* Inclusões: Marca = &quot;Marca Premium&quot;
* Exclusões: Categoria = &quot;Apuramento&quot;
* Resultado: o cliente deve gastar US$ 100 em itens de Marca Premium, excluindo itens de compensação

##### Exemplo 3: compra de produto específico {#example-3}

* Tipo de tarefa: Compra
* Quantidade necessária: 1
* Inclusões: SKU = &quot;NEWPRODUCT2024&quot;
* Resultado: o cliente deve comprar o produto específico com o SKU &quot;NEWPRODUCT2024&quot;

### Configurar recompensas {#configure-rewards}

Defina o que os clientes ganham ao concluir tarefas. As recompensas podem ser concedidas no nível da tarefa ou no nível do desafio depois que todas as tarefas forem concluídas.

#### Tempo de recompensa {#reward-timing}

Escolha quando os clientes receberão recompensas:

**[!UICONTROL Após a conclusão da tarefa]**: os clientes recebem uma recompensa imediatamente após a conclusão desta tarefa específica (também chamada de &quot;recompensas progressivas&quot; ou &quot;recompensas por etapas&quot;).

**[!UICONTROL Após a conclusão do desafio]**: os clientes recebem uma recompensa somente após concluírem todas as tarefas necessárias no desafio (também chamadas de &quot;recompensas finais&quot; ou &quot;grandes prêmios&quot;).

>[!TIP]
>
>Você pode combinar ambos os tipos de recompensa em um único desafio para manter o engajamento durante toda a jornada do cliente. Por exemplo:
>
>* Atribuir 10 pontos após a conclusão de cada tarefa (recompensas progressivas)
>* Dar mais 100 pontos depois de completar todo o desafio (recompensa final)

#### Tipos e valores de recompensa {#reward-types}

**[!UICONTROL Pontos]**: o prêmio de fidelidade aponta para a conta do cliente.

* Insira o número de pontos (por exemplo, 100)
* Os pontos são comunicados ao seu sistema externo de gerenciamento de fidelidade por meio da API

**[!UICONTROL Desconto]**: forneça um código ou valor de desconto.

* Inserir tipo de desconto (porcentagem ou valor fixo)
* Inserir valor de desconto
* Opcionalmente, especifique o código de desconto ou deixe o sistema gerar um

**[!UICONTROL Item gratuito]**: conceda um produto ou serviço gratuito.

* Especificar o SKU ou a descrição do item
* Indicar como o item gratuito deve ser reivindicado

**[!UICONTROL Premiação personalizada]**: defina um tipo de premiação personalizada.

* Inserir descrição da premiação
* Fornecer códigos ou identificadores relevantes
* Configurar como a recompensa é entregue ou reclamada

## Configurar cartões de conteúdo {#configure-content-cards}

Para obter etapas detalhadas sobre como configurar cartões de conteúdo, incluindo:
* Configuração do cartão de conteúdo
* Design e personalização
* Pré-visualização e teste

## Configurar mensagens {#configure-messaging}

Para obter etapas detalhadas sobre como configurar mensagens multicanais, incluindo:
* Canais de mensagem (no aplicativo, email, push)
* Estágios de mensagem (inicialização, em andamento, concluído)
* Acionadores e tempo de mensagem

## Revisar e publicar {#review-and-publish}

Antes de publicar seu desafio:

1. **Revise todos os componentes**: desafiar propriedades, tarefas, recompensas, conteúdo, mensagens
2. **Testar a experiência**: use perfis de teste para validar disparadores de conteúdo e tarefa
3. **Publicar**: tornar o desafio ativo para o público-alvo

A jornada gerada automaticamente é ativada na data de início especificada.

## Próximas etapas {#next-steps}

* [Gerenciar desafios](manage-challenges.md) - Saiba como editar, monitorar e otimizar desafios
* [Entender os Desafios de Fidelidade](get-started.md) - Examinar recursos e funcionalidades
