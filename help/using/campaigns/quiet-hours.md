---
solution: Journey Optimizer
product: journey optimizer
title: Período de Silêncio
description: Saiba como impedir que comunicações sejam enviadas durante períodos específicos usando regras de horas silenciosas
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: quiet hours, exclusões de tempo, regras de negócios, conjuntos de regras, programação, campanhas
exl-id: [TO BE GENERATED]
hide: yes
hidefromtoc: yes
source-git-commit: 11bccd63afa1bf5aafcd1dff70c8193ea754d256
workflow-type: tm+mt
source-wordcount: 980
ht-degree: 9%

---

# Período de Silêncio {#quiet-hours}

>[!AVAILABILITY]
>
>As regras do período de silêncio estão disponíveis atualmente apenas para algumas organizações (disponibilidade limitada). Para a adição na lista de espera, entre em contato com o representante da Adobe.

O Período de silêncio permite definir exclusões com base no tempo para canais de email, SMS, Push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando a respeitar as preferências do cliente e os requisitos de conformidade.

É possível aplicar o período de silêncio por meio de conjuntos de regras que podem ser atribuídas a ações individuais em campanhas ou jornadas para obter um controle preciso.

## Por que usar o Quiet Hours {#why-quiet-hours}

O Quiet hours ajuda a melhorar a experiência do cliente e a manter a conformidade de várias maneiras:

* **Respeitar as preferências do cliente**: evite enviar mensagens em horários inconvenientes (por exemplo, tarde da noite ou madrugada), o que pode afetar negativamente a reputação da marca e a fidelidade do cliente.

* **Melhore o engajamento**: ao enviar mensagens quando os clientes tiverem mais probabilidade de vê-las e interagir com elas, você aumenta a eficácia de suas comunicações.

* **Conformidade legal**: certos estados e regiões proíbem mensagens de marketing por SMS durante horas específicas. O Período de silêncio ajuda você a manter a conformidade com regulamentos como o TCPA e as leis de SMS específicas do estado.

* **Otimizar tempo**: se muito tempo se passou desde que uma mensagem foi agendada, ela pode não ser mais relevante. As horas de silêncio permitem descartar mensagens desatualizadas ou mantê-las até um momento adequado.

## Como funcionam as Horas de Silêncio {#how-quiet-hours-work}

O Quiet hours é implementado por meio de regras de negócios criadas e aplicadas às campanhas e jornadas usando conjuntos de regras.

Quando uma mensagem é agendada para ser enviada durante um período de silêncio, o [!DNL Adobe Journey Optimizer] executa uma das duas ações a seguir com base na sua configuração:

* **Descartar**: a mensagem é suprimida permanentemente e nunca é enviada.
* **Fila**: a mensagem é mantida e enviada automaticamente assim que o período de silêncio termina.

O sistema avalia as horas de silêncio com base no fuso horário do recipient, que pode ser:

* O fuso horário especificado no perfil do cliente
* Um fuso horário inferido com base em outros dados de perfil e evento
* Um fuso horário fixo especificado na regra

>[!NOTE]
>
>Janela de pré-supressão: o sistema começa a suprimir as comunicações 30 minutos antes do início do horário de silêncio, garantindo que nenhuma mensagem seja entregue assim que o período de silêncio começar.

## Criar uma regra de Silêncio {#create-quiet-hours-rule}

Para criar uma regra de horas de silêncio:

1. Navegue até **[!UICONTROL Administração]** > **[!UICONTROL Regras de Negócios]**.

1. Na seção **[!UICONTROL Conjuntos de regras]**, crie um novo conjunto de regras ou selecione um existente ao qual deseja adicionar a regra de horas sem atividade.

1. Clique em **[!UICONTROL Criar regra]** e selecione **[!UICONTROL Período de Silêncio]** como o tipo de regra.

1. Defina as configurações de horários de silêncio:

   * **Nome da regra**: dê um nome descritivo à regra.

   * **Período**: definir quando as horas de silêncio devem ser aplicadas:
      * **Horas do dia**: definir horas específicas (por exemplo, 20:00 às 20:00):00:00
      * **Dias da semana**: selecionar dias específicos (por exemplo, fins de semana)
      * **Datas personalizadas**: escolha datas específicas do calendário (por exemplo, feriados)

   * **Fuso horário**: selecione como determinar o fuso horário:
      * **Fuso horário local do usuário**: use o fuso horário de cada perfil de destinatário
      * **Fuso horário específico**: aplique um fuso horário fixo (por exemplo, Leste, Central)

   * **Ação**: escolha o que acontece com as mensagens durante as horas de silêncio:
      * **Descartar**: as mensagens são suprimidas permanentemente
      * **Fila**: as mensagens são mantidas e enviadas quando o horário de silêncio termina

1. Clique em **[!UICONTROL Salvar]** para criar a regra.

## Aplicar Período de Silêncio a campanhas e jornadas {#apply-quiet-hours}

Depois de criar uma regra de horas de silêncio, é necessário aplicá-la às campanhas ou jornadas:

1. Abra a campanha ou jornada onde deseja aplicar as horas de silêncio.

1. Navegue até a ação (Email, SMS, Push ou WhatsApp) que deseja controlar.

1. Na configuração da ação, localize a seção **[!UICONTROL Conjunto de regras]**.

1. Selecione o conjunto de regras que contém a regra de silencioso.

1. Salve as alterações.

A regra de horas de silêncio agora se aplica a essa ação específica. Todas as mensagens enviadas por meio dessa ação respeitarão a configuração de horas de silêncio.

>[!NOTE]
>
>As regras de horário de silêncio se aplicam às comunicações programadas e acionadas por eventos. Verifique se o conjunto de regras está configurado corretamente para lidar com seu caso de uso.

## Considerações sobre fuso horário {#timezone-considerations}

Ao usar a opção **Fuso horário local do usuário**, [!DNL Adobe Journey Optimizer] procura informações de fuso horário na seguinte ordem:

1. **Atributo de fuso horário do perfil**: o fuso horário explicitamente especificado no perfil do cliente
2. **Fuso horário inferido**: um fuso horário calculado com base em outros dados de perfil e sinais comportamentais

Se nenhuma delas estiver disponível, o sistema poderá não aplicar as horas de silêncio corretamente. Verifique se os perfis do cliente incluem informações de fuso horário para obter os melhores resultados.

Ao usar um **Fuso horário específico**, todos os destinatários recebem (ou não) mensagens com base nesse único fuso horário, independentemente da localização real.

## Medidas de proteção e limitações {#guardrails-limitations}

Esteja ciente do seguinte ao usar o horário silencioso:

* **Tempo de ativação**: pode levar até 20 minutos para que uma regra ou um conjunto de regras seja totalmente ativado. Planeje adequadamente ao criar ou modificar regras.

* **Atraso na ativação de campanha**: depois de associar regras de negócios, aguarde pelo menos 10 minutos antes de ativar uma jornada ou enviar uma campanha para garantir que as regras sejam aplicadas corretamente.

* **Limites do conjunto de regras**: atualmente, você pode ter até 3 conjuntos de regras ativos para o domínio de canal e 5 para o domínio de jornada.

* **Taxa de liberação de mensagens**: quando as horas de silêncio terminam e as mensagens em fila são liberadas, elas são enviadas a uma taxa de até 5.000 mensagens por segundo por organização.

* **Sem suporte no**: as regras de horário de silêncio não estão disponíveis no momento para a Orquestração de Campanhas.

* **Execução seca**: as regras de horas de silêncio não são avaliadas durante execuções de execução seca de jornada.

## Relatórios {#reporting}

Você pode acompanhar o impacto das horas de silêncio em suas campanhas e jornadas por meio dos recursos padrão de relatórios:

* **Relatório All-time**: a seção &quot;Motivos Excluídos&quot; mostra o volume de clientes que não receberam comunicações devido a regras de horários silenciosos, juntamente com o nome do conjunto de regras específico.

* **Relatório ao vivo**: (se disponível) mostra estatísticas em tempo real sobre perfis que estão aguardando devido a horas de espera ou foram descartados devido a horas de espera.

## Próximas etapas {#next-steps}

Depois que suas regras de horários de silêncio forem configuradas e aplicadas, você poderá:

* Revise sua campanha ou jornada para garantir que as regras estejam associadas corretamente
* Ativar sua campanha ou jornada
* Monitore o impacto das horas de silêncio em seus relatórios

