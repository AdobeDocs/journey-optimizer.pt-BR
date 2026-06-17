---
solution: Journey Optimizer
product: journey optimizer
title: Uso de integrações externas
description: Integre integrações externas ao processo de criação de canal para enriquecer o conteúdo com informações personalizadas e dinâmicas
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: integração
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: d16f7424-4847-4b90-a37c-4b52cbdabee5
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 836
ht-degree: 1%

---


# Uso de integrações externas para personalização {#integrations-personalization}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como os profissionais de marketing aplicam integrações configuradas para personalizar conteúdo de email, SMS e push e encadear uma chamada de API para outra com mensagens dinâmicas e mais avançadas.

>[!ENDSHADEBOX]

Antes de usar integrações externas em seu conteúdo, confirme se um administrador **configurou e ativou** cada integração (ponto de extremidade, autenticação, políticas, carga de resposta e ativação) conforme descrito em [Trabalhar com integrações](integrations.md).

Você pode adicionar até **3** integrações por **[!UICONTROL Fragmento]** e até **5** na mensagem. As integrações provenientes apenas de fragmentos não contam no **5**.

## Aplicar personalização da integração ao seu conteúdo {#apply-integration-personalization}

Como profissional de marketing, você pode usar integrações configuradas para personalizar seu conteúdo. Siga estas etapas:

1. Acesse o conteúdo da campanha e clique em **[!UICONTROL Adicionar personalização]** a partir do Texto ou dos **[!UICONTROL Componentes]** do HTML.

   [Saiba mais sobre componentes](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Navegue até a seção **[!UICONTROL Integrações]** e clique em **[!UICONTROL Abrir integrações]** para exibir todas as integrações ativas.

   Observe que os **Fragmentos de Journey Optimizer** estão disponíveis com Integrações, mas oferecem suporte somente a canais de saída. Depois que um fragmento é publicado, a adição e o salvamento de novas integrações são desativados para evitar impacto nas jornadas e campanhas existentes.

   ![](assets/external-integration-content-2.png)

1. Selecione uma integração e clique em **[!UICONTROL Salvar]**.

   ![](assets/external-integration-content-3.png)

1. Habilite o modo **[!UICONTROL Pills]** para desbloquear o menu de integração avançado.

   ![](assets/external-integration-content-4.png)

1. Ao criar a personalização da integração, o Auxiliar de integrações inclui um campo **`required`** que define como as falhas ou os dados ausentes interagem com o conteúdo padrão:

   * **`required=true`** (padrão): a renderização para essa mensagem. O envio é excluído com **`ExternalDataLookupExclusion`**, e essa exclusão é registrada no **conjunto de dados de comentários da mensagem**.
   * **`required=false`**: A variável de resultado está definida como **`null`** e a renderização continua. Use texto padrão, fallbacks ou lógica condicional no modelo para que os perfis não recebam conteúdo vazio quando a integração não retornar dados.

     ![](assets/external-integration-content-8.png)

1. Para concluir a configuração de integração, defina os atributos de integração, que foram especificados anteriormente durante a [configuração](integrations.md#configure).

   Você pode designar valores a esses atributos usando valores estáticos, que permanecem constantes, ou atributos de perfil, que extraem dinamicamente informações dos perfis do usuário.

   ![](assets/external-integration-content-5.png)

1. Depois que os atributos de integração forem definidos, você poderá usar os campos de integração no seu conteúdo para mensagens personalizadas clicando no ícone ![adicionar](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >Os tokens no modelo devem usar somente campos expostos pelo administrador na configuração de integração. Por exemplo, `{{weatherResponse.temperature}}` é válido quando `temperature` é exposto; `{{weatherResponse.humidity}}` é rejeitado no editor se `humidity` não foi exposto.

1. Clique em **[!UICONTROL Salvar]**.

A personalização da sua integração agora é aplicada com sucesso ao seu conteúdo, garantindo que cada recipient receba uma experiência personalizada e relevante com base nos atributos configurados.

![](assets/external-integration-content-7.png)

## Mapear uma chamada de API para outra {#map-integration-chain}

É possível encadear integrações para que os resultados de uma chamada alimentem a próxima, por exemplo, segmentos de caminho, cabeçalhos ou parâmetros de consulta. As chamadas são executadas em ordem na mesma mensagem, que aceita personalização mais avançada sem código personalizado.

Antes de começar, verifique se:

* Um administrador configurou e ativou todas as integrações necessárias. Consulte [Configurar a integração](integrations.md).
* Espaços reservados para caminhos de variáveis, cabeçalhos e parâmetros de consulta são configurados na configuração de integração com rótulos voltados para o profissional de marketing.
* O administrador expôs os campos de resposta necessários na **[!UICONTROL carga de resposta]** de cada integração para que apareçam ao criar.

O exemplo abaixo usa uma integração de reserva que retorna um número de voo da reserva do perfil e, em seguida, uma integração de informações de voo que usa esse número para o status ativo (atrasos, destino). Você mapeia as entradas da segunda integração para a resposta da primeira chamada.

1. Abra a mensagem ou fragmento e abra o editor de personalização.

   ![](assets/uc-integrations-1.png)

1. Em **[!UICONTROL Integrações]**, clique em **[!UICONTROL Abrir integrações]**.

   ![](assets/uc-integrations-2.png)

1. Adicione a integração cuja resposta alimentará a próxima chamada, por exemplo, dados de reserva ou reserva que incluem o identificador de voo.

   ![](assets/uc-integrations-3.png)

1. (Opcional) Abra o menu da **[!UICONTROL função auxiliar]** e adicione um auxiliar, por exemplo, a função `Let`, se desejar vincular uma variável nomeada à resposta de reserva.

   >[!NOTE]
   >
   > Somente os campos expostos na **[!UICONTROL carga de resposta]** definida pelo administrador estão disponíveis. Você não pode fazer referência a propriedades que não foram expostas na configuração.

1. Se você usar uma variável auxiliar, mapeie essa variável para o campo que a integração de reservas retorna para uso downstream, por exemplo, o número do voo na carga do passageiro ou da reserva.

   ![](assets/uc-integrations-4.png)

1. No menu **[!UICONTROL Abrir integrações]**, adicione a segunda integração, por exemplo, status de voo.

   ![](assets/uc-integrations-5.png)

1. Na segunda integração, abra **[!UICONTROL Atributos de integrações]**. Para cada entrada que deve reutilizar dados da primeira chamada, como uma variável de caminho, cabeçalho ou parâmetro de consulta, selecione uma origem de mapeamento da primeira resposta de integração.

   Na experiência **[!UICONTROL Pills]**, você pode mapear a saída da primeira chamada diretamente para a entrada da segunda chamada sem uma instrução `Let`. Se você usou `Let`, é possível mapear através dessa variável.

   ![](assets/uc-integrations-6.png)

1. Insira tokens da segunda integração em seu conteúdo com o controle ![add](assets/do-not-localize/Smock_Add_18_N.svg), por exemplo, destino da resposta de informações de voo.

   ![](assets/uc-integrations-8.png)

1. Salve o conteúdo.

Em **[!UICONTROL Simulação]** ou enviar, o Journey Optimizer executa integrações em ordem: a primeira chamada usa o contexto do perfil configurado, e seu resultado cria a segunda solicitação. A execução de uma determinada integração na simulação ou no momento do envio depende da configuração e do canal.

![](assets/uc-integrations-7.png)

## Vídeo tutorial {#video}

Este vídeo mostra como as **Integrações** conectam o Adobe Journey Optimizer a APIs externas para que você possa receber dados e conteúdo em **canais de saída**, email, SMS e push, para personalizações mais relevantes.

>[!VIDEO](https://video.tv.adobe.com/v/3484118/?learn=on)
