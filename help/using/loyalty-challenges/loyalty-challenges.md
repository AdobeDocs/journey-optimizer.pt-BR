---
solution: Journey Optimizer
product: journey optimizer
title: Desafios de fidelidade
description: Saiba como criar e gerenciar desafios de fidelidade no Adobe Journey Optimizer para criar programas de fidelidade envolventes.
feature: Loyalty challenges
topic: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privado" type="Informative"
version: Journey Orchestration
source-git-commit: 48ccfc4047251fa97777d3fb2f160c33797a113e
workflow-type: tm+mt
source-wordcount: '5146'
ht-degree: 1%

---


# Desafios de fidelidade {#loyalty-challenges}

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Entre em contato com o representante da Adobe para obter acesso.

Os Desafios de fidelidade permitem criar ofertas de envolvimento personalizadas para seus clientes, ajudando você a organizar programas de fidelidade em escala. Você pode projetar desafios com tarefas e marcos específicos, recompensar os clientes por concluí-los e fornecer a experiência por meio de canais da Adobe Journey Optimizer.

>[!BEGINSHADEBOX]
>
>**Neste guia:**
>
>* [Visão geral](#overview) - Entenda quais desafios de fidelidade oferecem
>* [Como funciona](#how-it-works) - Fluxo de trabalho passo a passo, da configuração ao monitoramento
>* [Pré-requisitos](#prerequisites) - Configurar assimilação e permissões de dados
>* [Acessar Desafios de Fidelidade](#access) - Abra o menu e visualize os desafios
>* [Criar desafios](#create-challenges) - Criar novos desafios de fidelidade
>* [Criar tarefas](#create-tasks) - Defina o que os clientes devem fazer
>* [Gerenciar desafios](#manage-challenges) - Editar, monitorar e otimizar
>
>[!ENDSHADEBOX]

## Visão geral {#overview}

Os Desafios de fidelidade permitem projetar e implantar ofertas de envolvimento personalizadas que motivam os clientes a realizar ações específicas e receber recompensas. O recurso fornece uma solução completa para a criação de programas de fidelidade em escala, desde a definição de tarefas e marcos até o fornecimento de conteúdo e o rastreamento do desempenho em todos os canais. Você pode criar três tipos de experiências de desafio, configurar recompensas, enviar notificações de vários canais em estágios-chave do ciclo de vida e monitorar o desempenho por meio de jornadas geradas automaticamente — tudo isso enquanto mantém a integração com seu sistema externo de gerenciamento de fidelidade.

## Como funciona {#how-it-works}

A criação e o lançamento de um desafio de fidelidade seguem este fluxo de trabalho:

1. **Configurar assimilação de dados** - Configure os conectores de origem do Experience Platform (como Capilar) para assimilar dados do evento de fidelidade que controlam as ações e o progresso do cliente.

2. **Criar um desafio** - Defina as propriedades básicas do desafio, incluindo nome, tipo (Padrão, Streak ou Sequencial), público-alvo e intervalo de datas.

3. **Adicionar tarefas** - Defina as ações específicas que os clientes devem concluir, incluindo tipos de tarefas (compra, gastos, visitas, etc.), quantidades, filtros de produtos e recompensas.

4. **Criar cartões de conteúdo** - Crie a representação visual do seu desafio usando cartões de conteúdo do Journey Optimizer exibidos em dispositivos do cliente.

5. **Configurar mensagens** (Opcional) - Configure mensagens multicanais (no aplicativo, email, push) para estágios principais: inicialização, em andamento e conclusão.

6. **Revisar e publicar** - Teste seu desafio com perfis de teste e publique-o para disponibilizá-lo para seu público-alvo.

7. **jornada gerada automaticamente** - Quando você publica, o Journey Optimizer cria automaticamente uma jornada que orquestra a entrega de cartões de conteúdo e mensagens.

8. **Ativar jornada** - A jornada gerada automaticamente é ativada na data de início do desafio e gerencia todas as interações com os clientes.

9. **Monitorar desempenho** - Acompanhe a participação, as taxas de conclusão, a distribuição de recompensas e o envolvimento com mensagens por meio de relatórios internos e da tela de jornada.

>[!NOTE]
>
>A jornada gerada automaticamente é exibida no inventário de jornadas e pode ser personalizada, se necessário. No entanto, as alterações feitas diretamente na jornada não são sincronizadas com a configuração de desafio.

## Principais recursos

Use os desafios de fidelidade para:

* **Crie três tipos de desafios**:
   * **Padrão**: os clientes concluem qualquer número de tarefas para receber recompensas.
   * **Streak**: os clientes concluem a mesma tarefa várias vezes.
   * **Sequencial**: os clientes concluem as tarefas em uma ordem específica.

* **Criar conteúdo de desafio**: use cartões de conteúdo do Journey Optimizer para criar a representação visual de seu desafio em dispositivos do cliente. Os cartões de conteúdo exibem as informações de desafio, o progresso e as recompensas no dispositivo do cliente.

* **Configurar requisitos da tarefa**: defina o que os clientes devem fazer para receber recompensas, incluindo:
   * Tipos de tarefa (compra, valor de gasto, visita etc.)
   * Requisitos de quantidade
   * Inclusões/exclusões de produto usando SKUs
   * Atributos e condições personalizados

* **Configurar recompensas**: defina recompensas que os clientes ganharão ao concluir a tarefa ou após concluir todo o desafio

* **Enviar notificações**: entregar mensagens em vários canais (no aplicativo, email, push) em estágios-chave:
   * **Inicialização**: quando o desafio começa
   * **Em andamento**: quando os clientes estão em processo
   * **Concluído**: quando os clientes concluírem o desafio

* **Acompanhe o desempenho**: monitore jornadas geradas automaticamente e analise o desempenho do desafio

### Limitações importantes {#limitations}

* **Nenhum sistema de razão**: os Desafios de Fidelidade não rastreiam valores monetários ou saldos de pontos. Quando os clientes concluem um desafio e ganham uma recompensa, a Journey Optimizer chama seu sistema de gerenciamento de fidelidade externo para lidar com a alocação de pontos.

* **Somente seleção de público-alvo**: você pode selecionar públicos-alvo existentes, mas não pode criar novos públicos-alvo na interface de desafios de fidelidade.

## Pré-requisitos {#prerequisites}

Antes de usar os desafios de fidelidade, verifique se você tem:

* Configuração de assimilação de dados

  Os desafios de fidelidade dependem dos dados assimilados pelos conectores de origem do Experience Platform para rastrear o progresso do cliente e a conclusão das tarefas.

   1. **Configurar um conector de origem com suporte**: atualmente, o Conector Capilar está disponível. Conectores adicionais estão planejados.

   2. **Validar assimilação de dados**: verifique se os eventos de fidelidade e os dados do cliente estão fluindo para o Experience Platform e disponíveis no Journey Optimizer.

  Para obter instruções detalhadas, consulte:

   * [Documentação de origens do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
   * [Configurar conectores de origem no Journey Optimizer](../start/get-started-sources.md)

* Permissões necessárias {#required-permissions}

Para usar os Desafios de fidelidade, você precisa das permissões apropriadas no Journey Optimizer. Entre em contato com o administrador se não conseguir acessar o recurso.

## Desafios de fidelidade de acesso {#access}

Para acessar os desafios de fidelidade:

1. No Adobe Journey Optimizer, selecione **[!UICONTROL Desafios de fidelidade]** no menu de navegação esquerdo.

   <!--![Loyalty challenges menu in left navigation](assets/loyalty-challenges-menu.png)-->

2. O inventário de desafios de fidelidade exibe todos os desafios existentes com informações como:
   * Nome e descrição do desafio
   * Status (Rascunho, Ao vivo, Interrompido etc.)
   * Tipo de desafio (Padrão, Streak, Sequencial)
   * Datas iniciais e finais
   * Data da última modificação

   <!--![Loyalty challenges inventory showing list of challenges](assets/loyalty-challenges-inventory.png)-->

3. Selecione **[!UICONTROL Criar desafio]** para começar a criar um novo desafio.

### Pesquisar e filtrar desafios {#search-filter}

Use os recursos de pesquisa e filtragem para encontrar rapidamente desafios específicos:

#### Pesquisa {#search}

Insira o nome do desafio ou palavras-chave para encontrar desafios correspondentes no campo **[!UICONTROL Pesquisar]**.

#### Filtrar por status {#filter-by-status}

Exibir desafios com status específicos em **[!UICONTROL Filtrar por status]**:

* Rascunho
* Agendado
* Ativado
* Concluído
* Parado
* Arquivado

#### Filtrar por tipo {#filter-by-type}

Mostrar apenas desafios Padrão, Streak ou Sequenciais usando **[!UICONTROL Filtrar por tipo]**.

#### Filtrar por data {#filter-by-date}

Exibir desafios em um intervalo de datas específico usando **[!UICONTROL Filtrar por data]**.

#### Filtrar por tags {#filter-by-tags}

Mostre desafios com marcas específicas aplicadas usando **[!UICONTROL Filtrar por marcas]**.


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

#### Exemplo de configuração de recompensa {#reward-example}

**Desafio**: &quot;Desafio do amante do café&quot;

**Tarefa 1**: Compre 3 cafés

* Recompensa: 30 pontos (10 pontos por café)
* Intervalo: após a conclusão da tarefa

**Tarefa 2**: Experimente 2 novas bebidas sazonais

* Recompensa: 50 pontos
* Intervalo: após a conclusão da tarefa

**Prêmio de conclusão do desafio**:

* Recompensa: Café grátis + 100 pontos bônus
* Intervalo: após a conclusão de todas as tarefas

**Total de recompensas possíveis**: 180 pontos + 1 café gratuito

### Atributos avançados de tarefa {#advanced-attributes}

Para casos de uso avançados, é possível configurar atributos de tarefa adicionais:

**[!UICONTROL Condições personalizadas]**: adicione lógica ou condições personalizadas além dos tipos de tarefa padrão usando segmentos ou regras do Experience Platform.

**[!UICONTROL Geofencing]**: (para tarefas de Visita) requer visitas a locais específicos definidos por coordenadas geográficas e raio.

**[!UICONTROL Requisitos com base no tempo]**: requerem que as tarefas sejam concluídas durante horas, dias ou intervalos de datas específicos.

**[!UICONTROL Período de controle]**: Defina um tempo mínimo entre as conclusões de tarefas para evitar ações repetidas rápidas.

**[!UICONTROL Dependências de tarefa]**: (para desafios sequenciais) defina os pré-requisitos que devem ser concluídos antes que esta tarefa fique disponível.

## Criar desafios {#create-challenges}

Crie um desafio de fidelidade para definir a oferta de engajamento, configure cartões de conteúdo para entrega, adicione tarefas, configure recompensas e, opcionalmente, configure mensagens entre canais.

### Antes de começar {#before-you-start}

Antes de criar um desafio, verifique se você tem:

* Assimilação de dados configurada e validada pelos conectores de origem
* Criação de todos os públicos-alvo necessários no Experience Platform
* Ativos de conteúdo preparados (imagens, texto etc.) para seu desafio
* Definiu as tarefas e recompensas que deseja oferecer

### Criar um desafio {#create-a-challenge}

Para criar um novo desafio de fidelidade:

1. No Journey Optimizer, selecione **[!UICONTROL Desafios de fidelidade]** no menu de navegação esquerdo.

2. Selecione **[!UICONTROL Criar desafio]** no canto superior direito.

   <!--![Create challenge button in loyalty challenges inventory](assets/create-challenge-button.png)-->

3. Na tela de propriedades do desafio, configure o seguinte:

#### Propriedades básicas {#basic-properties}

**[!UICONTROL Nome]**: insira um nome descritivo para o desafio. Esse nome aparece no inventário e está incluído no nome da jornada gerada automaticamente.

**[!UICONTROL Descrição]**: (opcional) adicione uma descrição para ajudar você e sua equipe a entender a finalidade e os detalhes deste desafio.

**[!UICONTROL Tipo de desafio]**: selecione o tipo de desafio que deseja criar:

* **[!UICONTROL Padrão]**: os clientes podem concluir qualquer número de tarefas especificadas em qualquer ordem para ganhar a recompensa. Exemplo: &quot;Faça 5 compras este mês&quot;.

* **[!UICONTROL Streak]**: os clientes devem concluir a mesma tarefa repetidamente. Exemplo: &quot;Visite nossa loja 10 vezes seguidas&quot;.

* **[!UICONTROL Sequencial]**: os clientes devem concluir as tarefas em uma ordem específica. Exemplo: &quot;Primeiro, faça uma compra, em seguida, escreva uma avaliação e depois indique um amigo.&quot;

<!--![Challenge type selection showing Standard, Streak, and Sequential options](assets/challenge-type-selection.png)-->

**[!UICONTROL Data de início]**: selecione quando o desafio se tornará ativo e disponível para os clientes.

**[!UICONTROL Data de término]**: selecione quando o desafio expirará. Os clientes que não concluírem o desafio até essa data não poderão mais receber a recompensa.

#### Seleção de público-alvo {#audience-selection}

**[!UICONTROL Selecionar público-alvo]**: escolha o público-alvo que está qualificado para este desafio. Você só pode selecionar públicos existentes; não é possível criar novos públicos na interface dos Desafios de fidelidade.

Para criar ou refinar públicos, consulte [Criar públicos no Journey Optimizer](../audience/about-audiences.md).

1. Selecione **[!UICONTROL Salvar como rascunho]** para continuar configurando seu desafio.

## Criar tarefas {#create-tasks}

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

   <!--![Tasks section in challenge creation interface](assets/tasks-section.png)-->

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

<!--![Task type selection dropdown showing available task types](assets/task-type-selection.png)-->

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

   <!--![Add product criteria button in task configuration](assets/add-product-criteria.png)-->

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
## Configurar cartões de conteúdo {#configure-content-cards}

Os cartões de conteúdo são a principal forma de exibir os desafios para os clientes em seus dispositivos. Você deve configurar um cartão de conteúdo para seu desafio.

1. Em seu desafio, navegue até a guia **[!UICONTROL Conteúdo]**.

2. Selecione **[!UICONTROL Editar conteúdo]** para abrir o editor de cartão de conteúdo.

   <!--![Content tab with Edit content button](assets/content-tab-edit.png)-->

3. Configure as propriedades do cartão de conteúdo:

   **[!UICONTROL Nome da configuração]**: insira um nome para esta configuração de cartão de conteúdo.

   **[!UICONTROL Configuração]**: selecione ou crie uma configuração de cartão de conteúdo. Isso define as configurações técnicas para como o cartão de conteúdo é entregue.

4. No editor de cartão de conteúdo, crie seu cartão de desafio:

   * Adicionar texto para descrever o desafio, as tarefas e as recompensas
   * Incluir imagens ou outros elementos visuais
   * Use a personalização para incluir informações específicas do cliente
   * Exibir indicadores de progresso, se aplicável
   * Adicionar botões do call-to-action

   O editor de cartão de conteúdo fornece os mesmos recursos que outros canais do Journey Optimizer. Para obter orientações detalhadas, consulte [Criar cartões de conteúdo](../content-card/design-content-card.md).

5. Selecione **[!UICONTROL Salvar]** para salvar a configuração do cartão de conteúdo.

>[!NOTE]
>
>O cartão de conteúdo é entregue por meio da jornada gerada automaticamente. Ele é exibido para membros do público-alvo qualificados quando o desafio está ativo.

## Configurar mensagens {#configure-messaging}

Você pode, opcionalmente, configurar mensagens para serem enviadas aos clientes em estágios-chave do ciclo de vida de desafio. As mensagens estão disponíveis para três estágios:

* **[!UICONTROL Iniciar]**: enviar uma mensagem quando o desafio se tornar ativo
* **[!UICONTROL Em andamento]**: enviar uma mensagem quando os clientes estiverem participando do desafio
* **[!UICONTROL Concluído]**: envia uma mensagem quando os clientes concluem o desafio

### Adicionar mensagens {#add-messages}

1. Em seu desafio, navegue até a guia **[!UICONTROL Mensagens]**.

   <!--![Messaging tab showing Launch, In progress, and Complete stages](assets/messaging-tab-stages.png)-->

2. Selecione o estágio no qual deseja adicionar uma mensagem: Inicialização, Em andamento ou Concluído.

3. Selecione **[!UICONTROL Adicionar mensagem]**.

4. Escolha o canal da mensagem:
   * **[!UICONTROL No aplicativo]**: exibir uma mensagem no aplicativo
   * **[!UICONTROL Email]**: enviar uma notificação por email
   * **[!UICONTROL Push]**: enviar uma notificação por push

5. Selecione **[!UICONTROL Editar conteúdo]** para abrir o editor de conteúdo para o canal selecionado.

6. Projete a mensagem usando o editor de conteúdo padrão:
   * Adicionar texto, imagens e outros elementos de conteúdo
   * Use a personalização para incluir informações específicas do cliente
   * Incluir detalhes do desafio como progresso ou recompensas
   * Adicionar conteúdo dinâmico com base em atributos ou comportamentos do cliente

   Para obter orientações específicas do canal, consulte:
   * [Criar mensagens no aplicativo](../in-app/create-in-app.md)
   * [Criar emails](../email/create-email.md)
   * [Criar notificações por push](../push/create-push.md)

7. Selecione **[!UICONTROL Salvar]** para salvar sua mensagem.

8. Repita essas etapas para adicionar mensagens para outros estágios ou canais, conforme necessário.

>[!NOTE]
>
>É possível adicionar várias mensagens por estágio, permitindo alcançar clientes em diferentes canais. Por exemplo, você pode enviar um email e uma notificação por push quando um desafio é iniciado.

### Acionadores e tempo de mensagem {#message-timing}

**Mensagens de inicialização**: enviadas quando o desafio se torna ativo para o público qualificado.

**Mensagens em andamento**: acionadas quando os clientes atingem um ponto de andamento especificado. Você pode configurar as condições do acionador com base em:

* Número de tarefas concluídas
* Porcentagem de desafio concluído
* Conclusão de tarefa específica
* Tempo decorrido desde o início do desafio

**Mensagens concluídas**: enviadas quando os clientes concluem com êxito todas as tarefas necessárias.

>[!TIP]
>
>**Práticas recomendadas para mensagens**:
>
>* Mantenha as mensagens concisas e concentradas no desafio
>* Comunicar claramente o valor e as recompensas
>* Usar identidade visual e tom consistentes
>* Incluir chamadas para ação claras
>* Testar mensagens antes de publicar seu desafio

## Gerar e personalizar jornadas {#generate-journey}

Ao salvar um desafio com conteúdo e mensagens configurados, o Journey Optimizer gera automaticamente uma jornada no back-end.

### Como funciona a geração de jornadas {#journey-generation-process}

1. Ao salvar um desafio e selecionar **[!UICONTROL Gerar jornada]**, o Journey Optimizer cria uma nova jornada.

2. A jornada é nomeada automaticamente com base no nome do desafio (por exemplo, &quot;Desafio: [Seu nome de desafio]&quot;).

3. A tela de jornada inclui:
   * Atividade **[!UICONTROL Ler público]** com o público selecionado
   * Ação de entrega **Cartão de conteúdo**
   * **Atividades de mensagem** para qualquer mensagem que você tenha configurado (Inicialização, Em andamento, Concluído)
   * **Aguardar** e **Condição** atividades conforme necessário com base em sua configuração

   <!--![Auto-generated journey canvas showing content card and message activities](assets/generated-journey-canvas.png)-->

4. A jornada aparece no inventário de jornadas e é visível a todos os usuários com permissões apropriadas.

### Exibir a jornada gerada {#view-journey}

Para exibir a jornada gerada automaticamente:

1. Navegue até **[!UICONTROL Jornadas]** no menu de navegação esquerdo.

2. Pesquise a jornada por nome de desafio ou filtre por tags, se você as atribuiu.

3. Selecione a jornada para visualizar sua tela e configuração.

### Personalizar a jornada {#customize-journey}

Você pode editar a jornada gerada automaticamente para adicionar lógica personalizada, atividades adicionais ou configurações avançadas.

>[!IMPORTANT]
>
>**Considerações importantes ao editar jornadas**:
>
>* As alterações feitas na tela de jornada **não são sincronizadas novamente** com a interface de Desafios de Fidelidade
>* O desafio continua sendo a fonte da verdade para a definição da experiência principal
>* O Journey Optimizer exibe um aviso quando você entra no modo de edição personalizado
>* Se você precisar fazer alterações em tarefas, recompensas ou propriedades de desafio principais, edite-as na interface de desafios de fidelidade, não na jornada
>* As edições de jornada personalizadas são apropriadas para lógica avançada de roteamento, cronometragem ou integração

Para personalizar a jornada:

1. Abra a jornada gerada no inventário de jornadas.

2. O Journey Optimizer exibe um aviso sobre edição personalizada. Leia o aviso cuidadosamente e confirme-o.

3. Faça as alterações desejadas usando a tela de jornada:
   * Adicionar atividades adicionais (esperas, condições, ações)
   * Configurar regras avançadas de tempo ou frequência
   * Adicionar ações ou integrações personalizadas
   * Modificar as condições de entrada do público

4. Teste suas alterações minuciosamente antes de publicar.

5. Publicar a jornada quando estiver pronta.

Para obter orientações detalhadas sobre edição de jornadas, consulte [Criar jornadas](../building-journeys/journey-gs.md).

### Jornada considerações sobre a tela {#journey-considerations}

Ao trabalhar com jornadas geradas automaticamente:

* **Não é possível editar o público-alvo na jornada**: se você precisar alterar o público-alvo, faça isso na interface dos Desafios de Fidelidade e gere a jornada novamente.

* **Atualizações de conteúdo da mensagem**: as alterações no conteúdo da mensagem devem ser feitas na interface do usuário de Desafios de Fidelidade para manter a consistência.

* **Status da Jornada**: o status da jornada (Rascunho, Ao Vivo, Interrompido) é gerenciado independentemente do status de desafio.

* **Testes**: teste toda a experiência de desafio, não apenas a jornada, para garantir que todos os componentes funcionem corretamente juntos.

## Revisar e publicar {#review-and-publish}

Antes de publicar seu desafio:

1. **Examinar todos os componentes**:
   * Propriedades e datas do desafio
   * Tarefas e requisitos da tarefa
   * Configuração de prêmios
   * Design do cartão de conteúdo
   * Tempo e conteúdo de mensagens
   * Estrutura de jornada gerada

2. **Testar a experiência**:
   * Usar perfis de teste para validar a renderização do conteúdo
   * Verifique se as tarefas são acionadas corretamente com base nos dados de teste
   * Verificar lógica de alocação de premiação
   * Testar mensagens em todos os canais configurados
   * Revisar a execução da jornada com públicos de teste

3. **Publicar seu desafio**:
   * Quando estiver pronto, selecione **[!UICONTROL Publicar]** nas propriedades de desafio
   * O desafio se torna ativo na data de início especificada
   * A jornada gerada automaticamente é ativada
   * Os membros do público-alvo qualificados podem ver e participar do desafio

## Gerenciar desafios {#manage-challenges}

Depois de criar e publicar os desafios de fidelidade, você pode visualizá-los, editá-los, monitorá-los e otimizá-los para garantir que eles forneçam os resultados desejados para o seu programa de fidelidade.

### Status de desafio {#challenge-statuses}

Cada desafio passa por um ciclo de vida refletido por seu status:

**[!UICONTROL Rascunho]**: o desafio está sendo criado ou editado, mas ainda não foi publicado. É possível fazer qualquer alteração nos desafios de rascunho.

**[!UICONTROL Agendado]**: o desafio foi publicado e se torna ativo em sua data de início. Os clientes ainda não podem ver ou participar dos desafios programados.

**[!UICONTROL Live]**: o desafio está ativo e os clientes no público qualificado podem vê-lo e participar dele. Esse status aparece quando a data atual está entre as datas inicial e final.

**[!UICONTROL Concluído]**: o desafio ultrapassou sua data final ou todos os objetivos foram atingidos. Os clientes não podem mais participar, mas você pode visualizar dados históricos e resultados.

**[!UICONTROL Parado]**: o desafio foi interrompido manualmente antes da conclusão. Os clientes não podem mais participar. Para reativar um desafio interrompido, você deve duplicá-lo e criar uma nova versão.

**[!UICONTROL Arquivado]**: o desafio foi arquivado para fins organizacionais. Os desafios arquivados podem ser recuperados usando filtros, mas estão ocultos na exibição padrão.

### Exibir detalhes do desafio {#view-details}

Para exibir informações detalhadas sobre um desafio:

1. No inventário, clique no nome do desafio ou selecione o menu **[!UICONTROL Mais ações]** (três pontos) e escolha **[!UICONTROL Exibir detalhes]**.

   <!--![Challenge inventory with More actions menu highlighted](assets/challenge-more-actions.png)-->

2. A tela de detalhes do desafio é exibida:

   Guia **[!UICONTROL Visão geral]**:
   * Propriedades básicas (nome, descrição, tipo, datas)
   * Status atual e informações do ciclo de vida
   * Informações do público
   * Histórico de criação e modificação

   Guia **[!UICONTROL Tarefas]**:
   * Lista de todas as tarefas do desafio
   * Tipos de tarefa, requisitos e condições
   * Recompensas configuradas por tarefa

   Guia **[!UICONTROL Conteúdo]**:
   * Configuração e visualização do cartão de conteúdo
   * Renderização visual de como o desafio aparece para os clientes

   Guia **[!UICONTROL Mensagens]**:
   * Mensagens configuradas para os estágios Inicialização, Em andamento e Concluído
   * Atribuições de canal e visualizações de conteúdo

   Guia **[!UICONTROL Desempenho]** (para desafios Live e Completados):
   * Métricas de participação
   * Taxas de conclusão
   * Distribuição de recompensas
   * Estatísticas de engajamento de mensagem

### Editar desafios {#edit-challenges}

É possível editar os desafios dependendo de seu status atual.

#### Editar desafios de rascunho {#edit-draft}

Para desafios no status **[!UICONTROL Rascunho]**:

1. Clique no nome do desafio ou selecione **[!UICONTROL Editar]** no menu de ações.

2. Modifique qualquer aspecto do desafio:
   * Propriedades básicas
   * Tarefas e recompensas
   * Cartões de conteúdo
   * Mensagens
   * Seleção de público-alvo

3. Selecione **[!UICONTROL Salvar como rascunho]** para salvar as alterações sem publicação ou **[!UICONTROL Publicar]** para ativar o desafio.

#### Editar desafios publicados {#edit-published}

Para desafios que estão **[!UICONTROL Agendados]** ou **[!UICONTROL Ativos]**:

>[!IMPORTANT]
>
>**Impacto da edição de desafios dinâmicos**: as alterações nos desafios dinâmicos podem afetar os clientes que já estão participando. Considere o seguinte antes de fazer alterações:
>
>* Modificar os requisitos da tarefa pode invalidar o progresso do cliente
>* Alterar as recompensas pode criar inconsistências para clientes que já ganharam recompensas
>* As alterações de público-alvo podem excluir clientes que foram qualificados anteriormente
>* As alterações de conteúdo aparecem imediatamente para os clientes
>
>Para alterações significativas, considere interromper o desafio atual e criar uma nova versão.

**Edição limitada para desafios em tempo real**:

Você pode fazer essas alterações em desafios reais sem interrompê-las:

* Atualizar descrição do desafio (voltado para o interior)
* Modificar visuais e texto do cartão de conteúdo
* Atualizar conteúdo de mensagens
* Ajustar data final (apenas estender, não pode encurtar)
* Adicionar ou modificar tags

**Alterações que exigem duplicação de desafio**:

Para alterar essas propriedades, você deve duplicar o desafio e criar uma nova versão:

* Tipo de desafio (Padrão, Streak, Sequencial)
* Requisitos e condições da tarefa
* Valores de premiação e regras de alocação
* Data de início (para desafios em tempo real)
* Público (grandes alterações)

### Duplicar um desafio {#duplicate-challenge}

A duplicação cria uma cópia de um desafio existente que você pode modificar e publicar como um novo desafio:

1. No inventário, selecione o menu **[!UICONTROL Mais ações]** (três pontos) para o desafio que deseja duplicar.

2. Selecione **[!UICONTROL Duplicar]**.

3. Na caixa de diálogo de duplicação:
   * Inserir um novo nome para o desafio duplicado
   * Opcionalmente, modifique a descrição
   * Escolha se deseja copiar as configurações de público
   * Escolha se as configurações de mensagens devem ser copiadas

4. Selecione **[!UICONTROL Duplicar]**.

5. O desafio duplicado é aberto no modo de rascunho, em que você pode fazer alterações antes de publicar.

**Cenários de duplicação comuns**:

* Executar novamente um desafio bem-sucedido por um novo período
* Criar variações de um desafio para públicos diferentes
* Atualizar requisitos ou recompensas da tarefa para uma nova versão
* Reativar um desafio interrompido ou concluído

### Interromper um desafio {#stop-challenge}

Para interromper um desafio em tempo real ou programado antes de sua data de término natural:

1. Selecione o desafio no estoque.

2. Selecione **[!UICONTROL Parar desafio]** no menu de ações.

3. Na caixa de diálogo de confirmação, analise o impacto:
   * Os clientes que participam atualmente não podem mais progredir
   * Os clientes que concluíram as tarefas, mas não concluíram o desafio completo, não receberão recompensas finais
   * A jornada associada foi interrompida
   * O desafio não pode ser reiniciado (deve ser duplicado para reutilização)

4. Selecione **[!UICONTROL Parar]** para confirmar.

>[!NOTE]
>
>**Parando vs. concluindo**: um desafio interrompido termina prematuramente e não segue o processo normal de conclusão. Os clientes recebem recompensas parciais já alocadas, mas não recebem recompensas finais de conclusão de desafio. Considere comunicar a extremidade inicial aos clientes afetados.

### Desafios de arquivamento {#archive}

Arquive os desafios concluídos ou interrompidos para manter o inventário organizado:

1. Selecione o menu **[!UICONTROL Mais ações]** (três pontos) para o desafio.

2. Selecione **[!UICONTROL Arquivar]**.

3. O desafio muda para o status arquivado e fica oculto na visualização de inventário padrão.

Para exibir desafios arquivados:

1. No inventário, aplique o filtro **[!UICONTROL Status]**.

2. Selecione **[!UICONTROL Arquivado]**.

3. Os desafios arquivados são exibidos com as mesmas informações que os desafios ativos.

Para desarquivar um desafio:

1. Encontre o desafio arquivado usando filtros.

2. Selecione **[!UICONTROL Desarquivar]** no menu de ações.

3. O desafio retorna ao status anterior (Concluído ou Interrompido).

### Excluir desafios {#delete}

Exclua os desafios que não são mais necessários:

>[!IMPORTANT]
>
>**A exclusão é permanente**: os desafios excluídos não podem ser recuperados. Exclua apenas os desafios que você não precisará mais no futuro. Considere o arquivamento em vez da exclusão para manter registros históricos.

**Regras de exclusão**:

* Você só pode excluir desafios no status **[!UICONTROL Rascunho]**
* Desafios publicados, agendados, online ou concluídos não podem ser excluídos
* Para remover um desafio publicado, primeiro você deve pará-lo e depois arquivá-lo

Para deletar um desafio de rascunho:

1. Selecione o menu **[!UICONTROL Mais ações]** (três pontos) para o desafio.

2. Clique em **[!UICONTROL Excluir]**.

3. Na caixa de diálogo de confirmação, confirme a exclusão.

## Monitorar desempenho {#monitor-performance}

Acompanhe o modo como os clientes se envolvem com seus desafios usando métricas de desempenho integradas.

### Métricas de desempenho {#performance-metrics}

A guia Desempenho mostra as métricas principais para desafios ativos e concluídos:

<!--![Performance metrics dashboard showing participation and completion data](assets/performance-metrics-dashboard.png)-->

**[!UICONTROL Métricas de participação]**:

* **Total de clientes qualificados**: Número de clientes no público alvo
* **Clientes inscritos**: número de clientes que visualizaram ou participaram do desafio
* **Taxa de inscrição**: porcentagem de clientes qualificados que se inscreveram
* **Participantes ativos**: número de clientes que estão fazendo progresso no momento

**[!UICONTROL Métricas de conclusão]**:

* **Clientes concluídos**: número de clientes que concluíram todas as tarefas
* **Taxa de conclusão**: porcentagem de clientes inscritos que concluíram o desafio
* **Tempo médio de conclusão**: Tempo médio desde a inscrição até a conclusão
* **Tarefas concluídas**: Número total de tarefas individuais concluídas em todos os clientes

**[!UICONTROL Métricas de recompensa]**:

* **Total de recompensas distribuídas**: Soma de todas as recompensas alocadas
* **Recompensas por tipo**: detalhamento por pontos, descontos, itens gratuitos, etc.
* **Média de recompensa por cliente**: valor médio de recompensa para clientes participantes

**[!UICONTROL Métricas de envolvimento]**:

* **Impressões do cartão de conteúdo**: Número de vezes que o desafio foi exibido
* **Cliques no cartão de conteúdo**: número de vezes que os clientes interagiram com o cartão de desafio
* **Entrega de mensagem**: número de mensagens enviadas para os estágios Inicialização, Em andamento e Conclusão
* **Engajamento na mensagem**: taxas de abertura, taxas de clique para mensagens por estágio e canal

### Exibir relatórios de desempenho {#view-reports}

Para acessar dados detalhados de desempenho:

1. Abra o desafio e navegue até a guia **[!UICONTROL Desempenho]**.

2. Selecione o intervalo de datas para relatórios (Hoje, Últimos 7 dias, Últimos 30 dias, Intervalo personalizado).

3. Revisar métricas por:
   * **Visão geral**: resumo de alto nível das métricas principais
   * **Linha do tempo**: Tendências de desempenho ao longo do tempo
   * **Detalhamento**: métricas segmentadas por atributos, canais ou tarefas do cliente

4. Exporte relatórios usando o botão **[!UICONTROL Exportar]** para análise adicional.

### Monitorar a jornada gerada {#monitor-journey}

A jornada gerada automaticamente contém dados de execução valiosos:

1. Nos detalhes do desafio, selecione **[!UICONTROL Exibir jornada]** para abrir a jornada associada.

2. Na tela de jornada, revise:
   * **Relatório de Jornadas**: estatísticas gerais de execução
   * **Relatórios de atividade**: desempenho de atividades individuais
   * **Métricas de entrada e saída**: quantos clientes entraram e saíram
   * **Logs de erros**: quaisquer problemas ou falhas de execução

3. Use o monitoramento do jornada para identificar:
   * Gargalos em que os clientes caem
   * Problemas técnicos que afetam a entrega
   * Desempenho da mensagem por canal
   * Oportunidades de otimização de tempo

Para obter orientações detalhadas sobre o monitoramento de jornadas, consulte [Monitorar suas jornadas](../building-journeys/report-journey.md).

### Otimizar desafios {#optimize}

Use os dados de desempenho para melhorar os desafios atuais e futuros:

**[!UICONTROL Variações de teste]**: crie desafios duplicados com tarefas, recompensas ou mensagens diferentes para comparar o desempenho.

**[!UICONTROL Ajustar tempo]**: modifique a duração do desafio ou os prazos finais da tarefa com base nos padrões de conclusão.

**[!UICONTROL Refinar público-alvo]**: amplie ou restrinja a seleção de público-alvo com base nas taxas de participação e conclusão.

**[!UICONTROL Atualizar conteúdo]**: atualize os cartões de conteúdo e as mensagens para manter o interesse e a clareza.

**[!UICONTROL Otimização da recompensa]**: ajuste os valores da recompensa para equilibrar custo e participação.

**[!UICONTROL Dificuldade da tarefa]**: modifique os requisitos da tarefa se eles forem muito fáceis ou muito difíceis com base nos dados de conclusão.

## Validação e teste de tarefa {#validation-testing}

Antes de publicar seu desafio, valide se as tarefas estão configuradas corretamente:

1. **Verificar lógica da tarefa**:
   * Verificar se os requisitos de quantidade são realistas
   * Verifique se os critérios de filtragem de produtos estão corretos
   * Confirme se os prêmios estão configurados corretamente

2. **Testar com perfis de teste**:
   * Criar perfis de teste que representem cenários de clientes diferentes
   * Enviar eventos de teste por meio do pipeline de assimilação de dados
   * Verifique se as tarefas são acionadas corretamente
   * Confirme se as recompensas foram alocadas conforme esperado

3. **Revisar mapeamento de dados**:
   * Verifique se os dados de entrada do evento são mapeados corretamente aos requisitos da tarefa
   * Validar se as SKUs, categorias e atributos correspondem entre seu sistema de origem e a Journey Optimizer
   * Casos de borda de teste (dados ausentes, valores inválidos etc.)

## Práticas recomendadas {#best-practices}

### Criação de desafios

**Comece simples**: para seu primeiro desafio, comece com um desafio padrão simples para se familiarizar com o processo.

**Teste completamente**: sempre teste seu desafio com perfis de teste e públicos-alvo antes de publicar em sua base de clientes completa.

**Comunicações claras**: certifique-se de que os clientes entendam o que precisam fazer, o que ganharão e quando.

**Tempo realista**: defina datas de início e término apropriadas, permitindo que os clientes tenham tempo suficiente para concluir o desafio.

**Recompensas atraentes**: torne as recompensas valiosas e relevantes para seu público-alvo, gerando maior participação.

### Configuração de tarefa

**Limpar requisitos**: torne os requisitos da tarefa claros e realizáveis. Evite condições excessivamente complexas.

**Dificuldade apropriada**: equilibrar a dificuldade da tarefa com o valor de recompensa. Tarefas mais difíceis devem oferecer maiores recompensas.

**Precisão da filtragem de produtos**: verifique novamente as SKUs, as categorias e os atributos para garantir uma correspondência precisa dos produtos.

**Recompensas progressivas**: use as recompensas por marcos (após a conclusão da tarefa) para manter o engajamento do cliente durante todo o desafio.

**Flexibilidade**: para desafios Padrão, permita flexibilidade na forma como os clientes concluem tarefas para acomodar diferentes comportamentos e preferências.

### Gerenciamento e monitoramento

**Monitoramento regular**: verifique o desempenho do desafio pelo menos uma vez por semana se há desafios em tempo real para identificar problemas antecipadamente.

**Limpar nomenclatura**: use nomes descritivos que indiquem a finalidade do desafio, o público-alvo ou o período para facilitar a organização.

**Usar marcas**: aplique marcas consistentes para categorizar desafios por campanha, temporada, segmento de público-alvo ou outros atributos relevantes.

**Alterações de documento**: anote por que você fez alterações nos desafios para referência e aprendizado futuros.

**Arquive de forma consistente**: arquive regularmente os desafios concluídos para manter o inventário gerenciável.

**Comunicar alterações**: se você modificar um desafio em tempo real, informe aos clientes afetados sobre as alterações que afetam sua participação.

**Analisar após a conclusão**: analise o desempenho após o término de cada desafio para identificar as lições aprendidas para desafios futuros.

**Implantação gradual**: para novos tipos de desafios ou alterações significativas, considere começar com um público menor antes da implantação completa.

**Controle de versão**: use controle de versão limpo em nomes de desafio ao criar iterações (por exemplo, &quot;Holiday Challenge 2024 - v2&quot;).

## Solução de problemas {#troubleshooting}

**Desafio não exibido aos clientes**:

* Verifique se o desafio está no status Live
* Verificar se os clientes estão no público qualificado
* Confirme se a configuração do cartão de conteúdo está correta
* Revisar os logs de execução da jornada para problemas de entrega

**Baixas taxas de participação**:

* Revisar a visibilidade e o apelo do cartão de conteúdo
* Verifique se as mensagens comunicam claramente o valor
* Garantir que as tarefas sejam realizáveis e que as recompensas sejam atraentes
* Verifique se o direcionamento de público-alvo é apropriado

**Tarefas não acionadas**:

* Verifique se os dados estão sendo assimilados corretamente dos conectores de origem
* Verifique se os atributos de evento correspondem aos requisitos da tarefa
* Revisar qualificação do público

**Recompensas não alocadas**:

* Confirmar se a configuração de premiação está correta
* Verificar conexão com o sistema de gerenciamento de fidelidade externo
* Verificar se há erros nos logs de entrega de gratificação

**A filtragem de produtos não está funcionando**:

* Validar códigos SKU e nomes de categoria
* Verifique se o mapeamento de atributos está correto
* Teste com dados de compra de amostra

**Jornada não gerando**:

* Confirme se toda a configuração necessária está concluída
* Verifique se há erros na guia Mensagens
* Verificar se o cartão de conteúdo está configurado
* Revisar logs de erros do sistema

**Dados de desempenho não exibidos**:

* Permitir que os dados sejam propagados (até 24 horas)
* Verificar se os eventos estão sendo acompanhados corretamente
* Verificar status de assimilação de dados
* Garantir que os clientes tenham começado a participar

## Feedback do Beta {#beta-feedback}

Durante a fase beta, seus comentários são valiosos para nos ajudar a melhorar os Desafios de fidelidade. Compartilhe sua experiência, suas perguntas e suas sugestões com o representante da Adobe ou pelos canais de feedback beta fornecidos no início.

## Tópicos relacionados {#related-topics}

* [Criar públicos no Journey Optimizer](../audience/about-audiences.md)
* [Design de cartões de conteúdo](../content-card/design-content-card.md)
* [Criar mensagens no aplicativo](../in-app/create-in-app.md)
* [Criar emails](../email/create-email.md)
* [Criar notificações por push](../push/create-push.md)
* [Criar jornadas](../building-journeys/journey-gs.md)
* [Monitorar suas jornadas](../building-journeys/report-journey.md)
* [Documentação de origens do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Configurar conectores de origem no Journey Optimizer](../start/get-started-sources.md)
