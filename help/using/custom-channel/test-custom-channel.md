---
title: Testar seu canal personalizado
description: Saiba como testar a conexão, simular o conteúdo e revisar suas mensagens de canal personalizadas no Adobe Journey Optimizer antes de ativar.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 2%

---


# Testar seu canal personalizado {#test-custom-channel}

Antes de ativar uma jornada ou campanha que use um canal personalizado, valide se o endpoint pode ser acessado, se a autenticação funciona e se os tokens de personalização são resolvidos corretamente para os perfis de destino.

## Testar a conexão do Channel Builder {#test-connection}

Enquanto um canal personalizado estiver com o status de **[!UICONTROL Rascunho]**, use o botão **[!UICONTROL Testar]** no Construtor de Canais para enviar uma solicitação de teste para o seu ponto de extremidade e validar a conexão ponta a ponta antes da ativação. [Saiba mais](create-custom-channel.md#test-connection)

Este teste confirma:

* Que o ponto de extremidade pode ser acessado dos IPs de saída de [!DNL Journey Optimizer].
* Verifique se as credenciais de autenticação configuradas são válidas.
* Que o endpoint retorna uma resposta HTTP 2xx.

Verifique os logs do sistema externo para confirmar se a solicitação de teste foi recebida com os cabeçalhos e a estrutura de carga esperados.

## Simular conteúdo com perfis de teste {#simulate-content}

O recurso **[!UICONTROL Simular conteúdo]** resolve expressões de personalização em relação a perfis de teste para que você possa inspecionar a carga exata que seria enviada antes que qualquer mensagem real fosse entregue.

1. Na tela de ação de jornada ou de edição de campanha, clique em **[!UICONTROL Simular conteúdo]**.

1. Clique em **[!UICONTROL Adicionar perfil de teste]** e selecione um ou mais perfis. [Saiba como criar perfis de teste](../audience/creating-test-profiles.md)

1. Revise a carga resolvida no painel de visualização. Para cada perfil de teste, verifique:

   * Todos os tokens de personalização (por exemplo, `{{profile.person.name.firstName}}`) foram substituídos pelos valores esperados do perfil.
   * Nenhum token não resolvido permanece (exibido como cadeias de caracteres vazias ou sintaxe `{{...}}` literal).
   * Os campos de carga obrigatórios são preenchidos.
   * As funções auxiliares produzem a saída formatada esperada.

>[!TIP]
>
>Teste com vários perfis que representam segmentos de público-alvo diferentes para capturar casos de borda, por exemplo, perfis com atributos opcionais ausentes, conjuntos de caracteres não latinos ou valores nulos em campos personalizados.

## Enviar uma prova {#send-proof}

Para validar o delivery de ponta a ponta antes da ativação, envie uma prova para um conjunto de recipients de teste:

1. No painel **[!UICONTROL Simular conteúdo]**, alterne para a guia **[!UICONTROL Enviar prova]**.

1. Adicione os perfis que deseja usar. Você pode carregar um arquivo CSV com perfis que não estão definidos como perfis de teste no [!DNL Journey Optimizer].

1. Clique em **[!UICONTROL Enviar prova]**. [!DNL Journey Optimizer] chama seu ponto de extremidade externo com a carga personalizada de cada perfil selecionado.

1. Verifique o sistema externo para confirmar se as cargas úteis de prova foram recebidas. Para canais de mensagens (por exemplo, WeChat ou Kakao Talk), verifique se a mensagem aparece no dispositivo ou aplicativo de mensagens de destino.

O resultado da prova é exibido usando os mesmos padrões de validação que a prova de email: os campos obrigatórios, as incompatibilidades de tipo e os erros de validação de esquema são exibidos antes do envio da prova.

Saiba mais sobre como enviar provas em [campanhas](../campaigns/create-campaign.md#send-proof) e [jornadas](../building-journeys/testing-the-journey.md).

## Testar no modo de teste do jornada {#test-journey}

Para validação de jornada de ponta a ponta, ative a jornada no **[!UICONTROL Modo de teste]**:

1. Na tela de jornada, clique em **[!UICONTROL Testar]** na área superior direita.

1. Configure o evento de acionador ou selecione um perfil de teste para uma jornada acionada pelo público-alvo.

1. Clique em **[!UICONTROL Acionar um evento]** ou permitir que o perfil entre por meio de uma atividade **[!UICONTROL Ler público]**.

1. Observe o fluxo na tela. Quando um perfil atinge o nó de ação do canal personalizado, o [!DNL Journey Optimizer] chama seu ponto de extremidade externo com a carga personalizada.

1. Verifique os logs do sistema externo para confirmar se a solicitação foi recebida corretamente.

1. Clique em **[!UICONTROL Parar teste]** quando terminar.

Saiba mais sobre como testar jornadas no [modo de teste](../building-journeys/testing-the-journey.md).

## Simular uma jornada {#simulate-journey}

O modo **Simulação** de [!DNL Journey Optimizer] permite validar sua jornada de ponta a ponta usando usuários simulados (entidades temporárias semelhantes a perfis que não persistem no Adobe Experience Platform) sem exigir perfis de teste pré-criados.

Para canais personalizados, a simulação resolve expressões de personalização e renderiza a pré-visualização de carga para cada usuário simulado, para que você possa verificar se o conteúdo correto seria entregue antes de entrar em funcionamento.

Para simular uma jornada usando um canal personalizado:

1. Na tela de jornada, clique em **[!UICONTROL Simular]** na área superior direita.

1. Adicione manualmente os usuários simulados ou gere-os usando a opção **[!UICONTROL Simulação rápida]** baseada em IA.

1. Configure todos os eventos de entrada necessários e acione os usuários simulados por meio da jornada.

1. Quando um usuário simulado atinge o nó de ação do canal personalizado, inspecione a carga resolvida no painel de visualização para confirmar se os tokens de personalização e a estrutura de carga estão corretos.

>[!NOTE]
>
>A simulação está disponível para jornadas de rascunho e ativas e usa usuários temporários simulados que não contam para cotas de perfil ou chamadas de endpoint reais.

[Saiba mais sobre a simulação de jornada](../building-journeys/simulate-journey-gs.md)

## Lista de verificação de pré-ativação {#checklist}

Antes de ativar sua jornada ou campanha, confirme o seguinte:

* O teste de conexão do Construtor de canais foi bem-sucedido (ponto de extremidade acessível, autenticação válida).
* As cargas simuladas mostram os valores esperados para todos os perfis de teste.
* Nenhum token de personalização não resolvido permanece na carga.
* Todos os campos de carga necessários são preenchidos.
* Uma prova foi enviada e recebida corretamente pelo sistema externo.
* Os caminhos de erro na atividade de ação de jornada (se configurados) tratam dos cenários de falha conforme esperado.

Após a conclusão dos testes, prossiga para a ativação. [Saiba como](create-custom-experience.md#activate)
