---
solution: Journey Optimizer
product: journey optimizer
title: Jornada fragmentos
description: Saiba como criar e usar fragmentos de jornada para salvar e reutilizar conjuntos de nós de jornada em várias jornadas no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: fragmentos, jornada, reutilizar, nós, tela, inventário, reutilizável
badge: label="Disponibilidade limitada" type="Informative"
version: Journey Orchestration
source-git-commit: 4b514dea522be3648542a868be7c26b63715a1ff
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%

---


# Jornada fragmentos {#journey-fragments}

>[!AVAILABILITY]
>No momento, esse recurso está com a Disponibilidade limitada. Para solicitar acesso, entre em contato com o representante da Adobe.

Os fragmentos de jornada são conjuntos reutilizáveis de nós de jornada que você pode criar uma vez e soltar em qualquer jornada na sandbox. Seja uma verificação de elegibilidade, uma lógica de roteamento de canal preferencial ou uma sequência de boas-vindas, os fragmentos ajudam as equipes a se moverem mais rápido e a permanecerem consistentes, sem reconstruir a mesma lógica do zero todas as vezes. [Consulte exemplos de caso de uso.](#examples)

Depois de criados, os fragmentos são armazenados em um **[!UICONTROL Inventário de Fragmentos]** dedicado e podem ser inseridos em qualquer jornada usando a atividade **[!UICONTROL Fragmentos de Jornada]**.

>[!NOTE]
>Os fragmentos de jornada usam um **comportamento de cópia**: inserir um fragmento em uma jornada cria uma cópia estática dos nós originais. As atualizações feitas no fragmento original não são refletidas nas jornadas que já o usaram.

## Permissões {#journey-fragments-permissions}

Para trabalhar com fragmentos de jornada, você precisa das [permissões](../administration/permissions.md) a seguir:

* **Gerenciar Jornadas** — necessário para criar, editar e excluir fragmentos.
* **Publicar Jornadas** — necessário para ativar um fragmento.

## Acessar o inventário de fragmentos {#journey-fragments-inventory}

Os fragmentos de jornada podem ser acessados na seção **[!UICONTROL Jornada]**. Abra a guia **[!UICONTROL Fragmentos]** para procurar todos os fragmentos disponíveis na sandbox.

Você pode filtrar a lista por nome do fragmento, status, data de criação, criador, data da última modificação ou tag.

## Criar um fragmento de jornada {#create-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_create_canvas"
>title="Salvar como fragmento de jornada"
>abstract="Insira um nome exclusivo para o fragmento e clique em Salvar. Os nós selecionados serão salvos como um fragmento reutilizável disponível no Inventário de fragmentos."

Você pode criar um fragmento de jornada de duas maneiras: diretamente da tela de jornada (recomendado) ou do Inventário de fragmentos.

>[!BEGINTABS]

>[!TAB Na tela de jornada]

Para salvar nós de jornada como um fragmento diretamente da tela de jornada:

1. Abra uma jornada e selecione um ou mais nós conectados na tela.
1. Clique no ícone **[!UICONTROL Salvar como fragmento]** na barra de ferramentas.

   ![Ícone para inserir um fragmento de jornada](assets/journey-fragment-icon.png)

1. Insira um nome exclusivo para o fragmento na sandbox.

   ![Salvar nós como um fragmento da tela de jornada](assets/journey_fragment_create_canvas.png)

1. Clique em **[!UICONTROL Salvar]**. O fragmento é salvo como um rascunho.

>[!TIP]
>
>Se você criar um fragmento a partir de uma jornada, [teste ou simule sua jornada](testing-the-journey.md) **antes** de salvar o fragmento para garantir que os nós selecionados se comportem conforme esperado.

>[!TAB Do inventário de fragmentos]

Para criar um fragmento diretamente do inventário:

1. Navegue até **[!UICONTROL Jornada]** > **[!UICONTROL Fragmentos]** guia.
1. Clique em **[!UICONTROL Criar fragmento]**.
1. Na tela de criação do fragmento, adicione e configure atividades de jornada.
1. Quando terminar, clique em **[!UICONTROL Salvar]** para salvar o fragmento como rascunho.

>[!CAUTION]
>
>O modo de teste e a simulação não estão disponíveis no editor de fragmentos. Isso significa que não é possível validar o comportamento das atividades configuradas antes que o fragmento seja ativado e inserido em uma jornada. Para fragmentos em que a precisão lógica é crítica, considere [criar e testar ou simular os nós em uma jornada completa](testing-the-journey.md) primeiro e, em seguida, salvá-los como um fragmento da guia da tela acima.

>[!ENDTABS]

## Editar um fragmento {#edit-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_properties"
>title="Jornada propriedades do fragmento"
>abstract="Abra um fragmento do inventário para modificar seus nós, propriedades, tags ou rótulos. Os fragmentos ativos devem ser desativados antes de serem editados."

Para editar um fragmento, abra-o no **[!UICONTROL Inventário de fragmentos]** clicando no nome dele. Na interface de criação do fragmento, é possível:

* Adicionar, remover ou modificar atividades.
* Definir ou atualizar propriedades do fragmento: nome, tags e rótulos.

>[!NOTE]
>
>* Somente fragmentos de **[!UICONTROL Rascunho]** podem ser editados. Para modificar um fragmento **[!UICONTROL Ativo]**, desative-o primeiro.
>
>* O modo de teste e a simulação não estão disponíveis no editor de fragmentos. Teste ou simule qualquer lógica em nível de jornada na jornada completa antes de salvar nós como um fragmento.
>
>* Atividades de [Jump](jump.md) não são permitidas dentro de um fragmento.

## Gerenciar fragmentos {#manage-journey-fragments}

### Status dos fragmentos {#fragment-statuses}

Os fragmentos de jornada seguem um ciclo de vida com os seguintes status:

| Status | Descrição |
|---|---|
| **[!UICONTROL Rascunho]** | O fragmento está sendo criado e ainda não está disponível para uso no jornada. |
| **[!UICONTROL Ativo]** | O fragmento está pronto para ser usado no jornada. |
| **[!UICONTROL Arquivado]** | O fragmento foi arquivado e não está mais disponível para uso no jornada. |

As seguintes regras se aplicam às transições de status do fragmento:

* Somente fragmentos de **[!UICONTROL Rascunho]** podem ser ativados. Abra um fragmento de rascunho e use o ícone **[!UICONTROL Ativar]**.
* Somente fragmentos **[!UICONTROL Ativos]** podem ser desativados ou arquivados.
* Somente fragmentos **[!UICONTROL Arquivados]** podem ser desarquivados. Desarquivar um fragmento o retorna ao estado **[!UICONTROL Rascunho]**.
* Somente fragmentos de **[!UICONTROL Rascunho]** podem ser excluídos.

>[!NOTE]
>Ao ativar um fragmento, a maioria das mesmas verificações de validação executadas durante a publicação do jornada é aplicada. No entanto, **os atributos contextuais não são validados** e **as políticas de governança não são aplicadas** no momento da ativação — ambos são avaliados quando o fragmento é inserido e usado em uma jornada.

### Ações de fragmento {#fragment-actions}

No inventário de fragmentos, é possível executar as seguintes ações em um fragmento:

* **[!UICONTROL Abrir]**: edite o fragmento clicando em seu nome.
* **[!UICONTROL Duplicar]**: criar uma cópia do fragmento a partir de **[!UICONTROL Mais ações]** (...) ícone.
* **[!UICONTROL Arquivar]**: arquivar um fragmento (disponível somente para fragmentos **[!UICONTROL Ativos]**) de **[!UICONTROL Mais ações]** (...) ícone. Os fragmentos arquivados não estão mais disponíveis no seletor de fragmentos.
* **[!UICONTROL Desarquivar]**: restaurar um fragmento arquivado (disponível somente para fragmentos **[!UICONTROL Arquivados]**), a partir de **[!UICONTROL Mais ações]** (...) ícone. O fragmento retorna ao estado **[!UICONTROL Rascunho]**.
* **[!UICONTROL Excluir]**: excluir permanentemente um fragmento (disponível somente para fragmentos de **[!UICONTROL Rascunho]**), de **[!UICONTROL Mais ações]** (...) ícone.
* **[!UICONTROL Editar marcas]**: adicionar ou remover marcas de um fragmento, de **[!UICONTROL Mais ações]** (...) ícone.

## Usar um fragmento em uma jornada {#use-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_add"
>title="Adicionar um fragmento de jornada"
>abstract="Somente fragmentos **[!UICONTROL Ativos]** estão disponíveis no seletor. Inserir um fragmento cria uma **cópia estática** de seus nós — as atualizações do fragmento original não são refletidas na jornada."

Para inserir um fragmento em uma jornada:

1. Abra a jornada e arraste a atividade **[!UICONTROL Fragmentos de Jornada]** do painel esquerdo.
1. Solte-o em uma ramificação existente ou em uma tela vazia. Um seletor de fragmentos é exibido.
1. Procure ou pesquise o fragmento que deseja usar. Você pode visualizar um fragmento ou abri-lo em outra guia antes de inseri-lo.
1. Selecione o fragmento. Seus nós são copiados para a tela no ponto de soltar.

>[!NOTE]
>Somente fragmentos **[!UICONTROL Ativos]** estão disponíveis no seletor. Inserir um fragmento cria uma **cópia estática** de seus nós — todas as atualizações subsequentes do fragmento original não serão refletidas na jornada.
>
>Ao soltar um fragmento em uma tela vazia, ele deve começar com um nó **[!UICONTROL Ler público]**, **[!UICONTROL Qualificação de público]** ou **[!UICONTROL Evento]** (a mesma regra de quando se inicia qualquer jornada).

## Medidas de proteção e limitações {#guardrails}

As seguintes medidas de proteção se aplicam aos fragmentos de jornada:

**Criação de fragmento**

* Os nomes dos fragmentos devem ser **exclusivos por sandbox**.
* Um fragmento só pode ter **um caminho de entrada**. Seleções com mais de um ponto de entrada não podem ser salvas como um fragmento.
* Somente **nós conectados** podem ser salvos juntos como um fragmento.
* Um fragmento **não pode conter uma atividade [Jump](jump.md)**.
* Um fragmento pode conter **no máximo 20 nós**.
* Uma sandbox pode ter no máximo **200 fragmentos ativos**.

**Uso do fragmento**

* Somente fragmentos **[!UICONTROL Ativos]** podem ser inseridos em uma jornada.
* Inserir um fragmento cria uma **cópia estática** de seus nós. As atualizações do fragmento original não são propagadas para jornadas em que ele foi usado.
* Um fragmento pode ser solto em uma ramificação existente ou em uma tela vazia. Quando solto em uma tela vazia, o fragmento deve começar com um nó **[!UICONTROL Ler público]**, **[!UICONTROL Qualificação de público]** ou **[!UICONTROL Evento]**.

**Geral**

* Os fragmentos podem ser encontrados usando a barra de [Pesquisa Unificada](../start/search-filter-categorize.md) na categoria **[!UICONTROL Fragmentos de Jornada]**.
* Há suporte para [Marcas](tags.md) e **Rótulos** nos fragmentos.
* Há suporte para [Logs de Auditoria](../privacy/audit-logs.md).
* As jornadas em execução na pilha antiga (usando Campanhas em linha) não são compatíveis com fragmentos de jornada. Duplique essa jornada para passar para a nova pilha antes de usar esse recurso.

## Exemplos de caso de uso {#examples}

Os exemplos a seguir ilustram padrões comuns de jornada que podem ser salvos e reutilizados como fragmentos de jornada.

**Verificações de qualificação**

Um padrão de entrada, como um nó [Read Audience](read-audience.md) seguido de filtros de qualificação, pode ser encapsulado em um fragmento. Isso permite que as equipes mantenham a consistência em como os perfis entram nas jornadas enquanto reduzem o tempo de configuração. O fragmento pode ser somente a atividade [Otimizar](optimize.md) ou as atividades Ler público e Otimizar juntas.

![Exemplo de fragmento de verificação de qualificação](assets/journey-fragments-uc-eligibility-check.png)

**Canal preferencial**

Um fragmento pode avaliar o canal de comunicação preferido de um perfil — email, push ou SMS — e rotear o perfil de acordo. Essa lógica pode ser reutilizada em qualquer jornada que envolva mensagens de saída, garantindo um gerenciamento consistente das preferências do canal. O fragmento pode incluir a atividade [Otimizar](optimize.md) e todas as três ramificações de canal.

![Exemplo de fragmento de canal preferencial](assets/journey-fragments-uc-preferred-channel.png)

**Sequência de boas-vindas de integração**

Uma sequência de boas-vindas cronometrada — como uma série de três mensagens que apresentam um produto ou serviço — pode ser salva como um fragmento. Isso é útil para integrar novos usuários em diferentes segmentos de público-alvo ou linhas de produto. O fragmento pode incluir as atividades [Wait](wait-activity.md) e os nós de mensagem.

![Exemplo de fragmento da sequência de boas-vindas de integração](assets/journey-fragments-uc-welcome-sequence.png)

**Lembrete e espera baseados em reação**

Um fragmento pode encapsular uma atividade Email seguida por uma [Reação](reaction-events.md), aguardando que o perfil abra o email em um número definido de dias e enviando um lembrete caso não o faça. Essa lógica é comumente reutilizada em promover jornadas e fluxos de conversão de avaliação. O fragmento pode incluir as atividades Email e Reaction.

![Exemplo de fragmento de lembrete baseado em reação](assets/journey-fragments-uc-reminder.png)
