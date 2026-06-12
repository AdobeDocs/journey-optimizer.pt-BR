---
solution: Journey Optimizer
product: journey optimizer
title: Publicar a jornada
description: Saiba como publicar uma jornada no Adobe Journey Optimizer, criar novas versões, gerenciar os status da jornada e entender os requisitos de republicação.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Hhvwpfq0phAjvzIGgv-NMnnhWhYJ-PpLOL0F4Q-CnqA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: cec8851784af46ce97f5bce843e970c82b4aa3ed
workflow-type: tm+mt
source-wordcount: 1272
ht-degree: 20%

---

# Publicar a jornada {#publishing-the-journey}

A publicação de uma jornada a ativa: ela muda para o status **[!UICONTROL Live]**, torna-se disponível para entrada de novos perfis e alterna para o modo somente leitura. Não é possível publicar uma jornada que contém erros.

>[!NOTE]
>
>Ao salvar ou publicar uma jornada, o Journey Optimizer valida o tamanho total do conteúdo da jornada e pode avisar ou bloquear a publicação se você se aproximar ou exceder o limite. Saiba mais em [validação do tamanho da carga da Jornada](../start/guardrails.md#journey-payload-size).

➡️ [Conheça este recurso no vídeo](#video)

## Antes de publicar {#before-you-publish}

Antes de publicar, verifique se sua jornada atende aos seguintes pré-requisitos:

* **Nenhum erro de validação** — Não é possível publicar uma jornada que contenha erros. [Teste sua jornada](testing-the-journey.md) primeiro e [solucione quaisquer erros de atividade](../building-journeys/troubleshooting.md#activity-errors).
* **Permissão de publicação** — a publicação requer a permissão de alto nível **[!DNL Publish journeys]**. Saiba mais sobre [gerenciamento de direitos de acesso](../administration/permissions-overview.md).
* **Carga dentro do limite** — A carga da jornada deve estar dentro do limite configurado (4 MB por padrão). Consulte [validação do tamanho da carga da Jornada](../start/guardrails.md#journey-payload-size).
* **Aprovação obtida** — Se a sua jornada estiver sujeita a uma política de aprovação, solicite e obtenha aprovação antes de publicar. [Saiba mais](../test-approve/gs-approval.md).

>[!TIP]
>
>Antes de publicar, valide sua jornada usando uma das opções de teste disponíveis:
>
>* [Simulação](simulate-journey-gs.md) — teste com usuários simulados, sem usar perfis de teste persistentes no Adobe Experience Platform.
>* [Modo de teste](testing-the-journey.md) — teste com perfis persistentes sinalizados como perfis de teste no Adobe Experience Platform.
>* [Execução a seco](journey-dry-run.md) — teste com dados de produção reais, sem entrar em contato com os perfis.

## Processo de publicação {#journey-publication}

As etapas para publicar uma jornada são detalhadas abaixo:

1. Verifique se a jornada é válida e não apresenta erros, e se atende aos [pré-requisitos acima](#before-you-publish).

1. Para publicar a jornada, clique na opção **[!UICONTROL Publicar]**, localizada no menu suspenso no canto superior direito.

   >[!NOTE]
   >
   > Se sua jornada estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para publicar sua jornada. [Saiba mais](../test-approve/gs-approval.md)

   ![Botão Publicar na barra de ferramentas do jornada para ativar a jornada](assets/journeyuc1_18.png)

Quando a jornada é publicada, ela está no modo **somente leitura**. No modo somente leitura, você só pode modificar os rótulos e as descrições da atividade, o nome da jornada e a descrição da jornada. Se precisar fazer modificações adicionais em uma jornada publicada, crie [uma nova versão](journey-ui.md#journey-filter) da jornada.

### Jornada status {#journey-statuses}

Após a publicação, uma jornada passa por vários status:

* **[!UICONTROL Ao vivo]** — A jornada é publicada e os perfis podem inseri-la.
* **[!UICONTROL Fechado]** — Uma versão anterior que foi encerrada automaticamente quando uma nova versão foi publicada. Nenhuma entrada pode acontecer.
* **[!UICONTROL Concluído]** — A jornada foi concluída de acordo com seus critérios finais. Para obter a definição exata de quando uma jornada é considerada concluída, consulte [Como o jornada termina](end-journey.md#journey-finished-definition).

### Parar uma jornada {#stop-journey}

Quando você interrompe uma jornada, ela é interrompida permanentemente. Todos os indivíduos que fluem pela jornada são permanentemente interrompidos e a jornada para de permitir novas entradas. Se precisar executar a jornada novamente, duplique-a e publique a nova jornada. Para obter mais informações sobre como as jornadas terminam, consulte [Como as jornadas terminam](end-journey.md).

### Requisitos de republicação {#republishing}

Em alguns casos, é necessário republicar uma jornada para que as alterações ou os ativos permaneçam em vigor:

>[!IMPORTANT]
>
>* Se forem feitas alterações em uma decisão de oferta usada na mensagem de uma jornada, será necessário desfazer a publicação da jornada e republicá-la. Isso garante que as alterações sejam incorporadas à mensagem da jornada e que ela seja consistente com as atualizações mais recentes.
>
>* O Assets/Images pode ser acessado em conteúdo entregue por até 2 anos (730 dias) desde sua primeira publicação em qualquer fragmento/mensagem em linha. A republicação é necessária após esse período de expiração (a qualquer momento após 730 dias) para mantê-las acessíveis por mais 2 anos. Qualquer republicação feita dentro de 730 dias da primeira publicação não estenderá a expiração de ativos/imagens para os próximos 730 dias.

## Versões de jornada {#journey-versions}

Na lista da jornada, todas as versões da jornada são exibidas com o número da versão. Quando você pesquisa uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida na parte superior da interface de edição da jornada, acima da tela.

![Lista de versões do Jornada mostrando versões publicadas e de rascunho](assets/journeyversions1.png)

>[!NOTE]
>
>Normalmente, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo, para todas as versões ativas da jornada. Se a reentrada estiver habilitada, um perfil poderá ser inserido em uma jornada novamente, mas não poderá fazer isso até que tenha saído totalmente da instância anterior da jornada. [Leia mais](entry-management.md).

### Criar uma nova versão de uma jornada {#journey-create-new-version}

Se precisar modificar para uma jornada em tempo real, crie uma nova versão da jornada. Para criar uma nova versão de uma jornada existente, siga as etapas abaixo:

1. Abra a versão mais recente da jornada ativa, clique em **[!UICONTROL Criar uma nova versão]** e confirme.

   ![Caixa de diálogo Criar nova versão para duplicar a jornada](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Só é possível criar uma nova versão com base na versão mais recente de uma jornada.

1. Faça as modificações, clique em **[!UICONTROL Publicar]** e confirme.

A partir do momento em que a jornada for publicada, pessoas físicas começarão a acessar a versão mais recente da jornada. As pessoas que já acessaram uma versão anterior permanecerão nela até que concluam a jornada. Se mais tarde entrarem novamente na mesma jornada, a versão mais recente será acessada.

As versões da jornada podem ser interrompidas individualmente. Todas as versões das jornadas possuem o mesmo nome.

Ao publicar uma nova versão de uma jornada, a versão anterior encerra automaticamente e alterna para o status **Fechado**. Nenhuma entrada na jornada pode acontecer. Mesmo que você interrompa a versão mais recente, a versão anterior permanecerá fechada.


>[!NOTE]
>
>Medidas de proteção e limitações específicas se aplicam ao controle de versão das jornadas. Saiba mais [nesta página](../start/guardrails.md#journey-versions-g).


## Perguntas frequentes {#faq}

**Por que não posso publicar minha jornada?**

O motivo mais comum é que a jornada contém erros de validação — não é possível publicar uma jornada com erros. Outros bloqueadores incluem exceder o [limite de tamanho de carga](../start/guardrails.md#journey-payload-size), permissão **[!DNL Publish journeys]** ausente ou uma [aprovação](../test-approve/gs-approval.md) pendente. Consulte [Antes de publicar](#before-you-publish) e [solucionar erros de atividade](../building-journeys/troubleshooting.md#activity-errors).

**É possível editar uma jornada após sua publicação?**

Uma jornada publicada está no modo somente leitura. Você só pode alterar os rótulos e as descrições da atividade, o nome da jornada e a descrição da jornada. Para qualquer outra alteração, [crie uma nova versão](#journey-create-new-version) da jornada.

**O que acontece com os perfis que já estão na jornada quando eu publicar uma nova versão?**

Novos perfis fluem para a versão mais recente. Os perfis que já estão em uma versão anterior ficam lá até que sejam concluídos; se forem inseridos novamente mais tarde, eles entrarão na versão mais recente. A versão anterior alterna automaticamente para **[!UICONTROL Fechada]** e não aceita novas entradas. Consulte [versões do Jornada](#journey-versions).

**Como executar novamente uma jornada interrompida?**

Interromper uma jornada é permanente. Para executá-la novamente, duplique-a e publique a nova jornada. Consulte [Parar uma jornada](#stop-journey).

**Preciso republicar depois de alterar uma decisão de oferta ou atualizar os ativos?**

Sim. Se você alterar uma decisão de oferta usada na mensagem de uma jornada, desfaça a publicação e republique a jornada para que a alteração seja aplicada. O Assets e as imagens expiram 730 dias após a primeira publicação; republique após esse período para mantê-las acessíveis. Consulte [Republicação de requisitos](#republishing).

**Posso publicar uma jornada que exija aprovação?**

Se a jornada estiver sujeita a uma política de aprovação, será necessário solicitar aprovação antes de publicar. [Saiba mais sobre aprovação](../test-approve/gs-approval.md).

## Tópicos relacionados {#related-topics}

* [Testar sua jornada](testing-the-journey.md) - Valide sua jornada com perfis de teste antes de publicar
* [Simulação de Jornada](simulate-journey-gs.md) - Valide sua jornada com usuários simulados antes de publicar
* [Jornada execução seca](journey-dry-run.md) - Testar com dados de produção reais sem contatar perfis
* [Solução de problemas](../building-journeys/troubleshooting.md#activity-errors) - Resolver erros de atividade e publicação
* [Como o jornada termina](end-journey.md#journey-finished-definition) - Entender a conclusão e os status da jornada
* [Gerenciamento de entrada de perfil](entry-management.md) - Configure como os perfis entram e entram novamente nas jornadas
* [medidas de proteção e limitações de Jornada](../start/guardrails.md#journeys-guardrails-journeys) - Revise as medidas de proteção de publicação e controle de versão

## Vídeo tutorial {#video}

Saiba como publicar uma jornada neste vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)
