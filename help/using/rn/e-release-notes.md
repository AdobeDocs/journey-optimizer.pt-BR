---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1a5f6be689c9e91ee0dc0b5f024dbe8020424337
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 29%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).


## Notas de pré-lançamento de 25 de outubro {#25-10-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas notas de versão na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 21-22 de outubro de 2025

### Novos recursos {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Canal de correspondência direta no jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a Campanhas, o canal de correspondência direta agora está disponível na tela de jornada, permitindo que você incorpore a correspondência direta às suas jornadas. A correspondência direta agora pode ser usada em cenários de jornada em lote e 1:1, com suporte para configuração de extração de arquivos e configurações de frequência baseadas em tempo.</p>
<p> Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nova API para recuperar Campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova API do Journey Optimizer agora está disponível, permitindo recuperar e inspecionar programaticamente dados relacionados à campanha, como detalhes, versões e configurações.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento e relatórios de ação personalizada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esse recurso fornece melhor visibilidade sobre a integridade e a execução da jornada, incluindo status do ciclo de vida e alertas de desempenho. Agora você pode entender rapidamente quando, onde e por que uma situação anômala está ocorrendo em uma ação personalizada.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mensagens básicas do RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a nova oferta complementar RCS Basic, agora é possível fornecer mensagens básicas RCS (Rich Communication Services) no Journey Optimizer, habilitando os seguintes recursos aprimorados de mensagens, sujeitos ao suporte geográfico e do provedor:</p>
<ul>
<li><strong>Suporte a remetente marcado e verificado:</strong> Envie mensagens usando perfis comerciais verificados com elementos de marca (logotipo, nome do remetente etc.).</li>
<li><strong>Insights de entrega de mensagens:</strong> receba relatórios de entrega detalhados, incluindo atualizações de status de mensagens (por exemplo, enviado, entregue, lido).</li>
<li><strong>Rastreamento de link:</strong> incorpore e rastreie URLs em mensagens do RCS para análise de envolvimento.</li>
<li><strong>Fallback para SMS:</strong> Fallback automático para SMS quando o dispositivo do destinatário não dá suporte a RCS ou está temporariamente inacessível via RCS.</li>
<li><strong>Composição básica de mensagem:</strong> envia mensagens básicas baseadas em texto RCS.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correspondência direta em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O canal de correspondência direta agora está disponível em campanhas orquestradas. A Atividade correspondência direta facilita o envio de correspondência direta na campanha orquestrada, tanto para mensagens únicas quanto recorrentes. Ela serve para automatizar o processo de geração do arquivo de extração exigido pelos provedores de correspondência direta. É possível combinar atividades de canal na tela da campanha orquestrada para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos conectores de origem para aplicativos de fidelidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Novos conectores de origem agora estão disponíveis no Adobe Experience Platform para os aplicativos de fidelidade Talon.One, Capillary e Kobie. Esses conectores permitem transmitir dados de fidelidade facilmente para o Adobe Experience Platform e aproveitar esses dados no Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, você pode adicionar políticas de decisão a campanhas e jornadas por email. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
<p> Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo de alta taxa de transferência para campanhas de email acionadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo modo de taxa de transferência alta está disponível agora em campanhas acionadas por API. Este modo foi projetado para mensagens em larga escala e em tempo real (até 5.000 transações por segundo) e oferece maior disponibilidade com menor latência.</p>
<p>Esse recurso está disponível somente para o canal de email e para organizações que adquiriram a oferta complementar de mensagens transacionais de alta transferência da Adobe. Entre em contato com seu representante da Adobe para obter mais informações.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Período de Silêncio/Exclusões Baseadas no Tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Quiet hours permite definir exclusões com base no tempo para canais de email, SMS, push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade.</p>
<p>Você pode aplicar horas de silêncio por meio de conjuntos de regras, que podem ser atribuídas a ações individuais em campanhas ou jornadas para obter um controle preciso. Simplificando esses processos.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nova função Auxiliar de metadados de execução</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova função auxiliar de executionMetadata está disponível no editor de personalização. Ele permite anexar informações contextuais a qualquer ação nativa e capturá-las em um conjunto de dados para exportação para sistemas externos.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Data de disponibilidade: 13 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Agente de experimento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Agente de experimentação é uma ferramenta alimentada por IA que moderniza como você pode executar e gerenciar experimentos digitais em sites, emails, mensagens por push e aplicativos. Criado com base na plataforma de IA do Adobe Experience Platform e em ferramentas de experimentação, o Agente de experimentação ajuda a executar experimentos com mais eficiência, organizar metas comerciais e gerar insights acionáveis, destacando o que funcionou, o que não funcionou e onde experimentar em seguida.</p>
<p>Como parte do novo recurso do Experimentation Accelerator, o agente oferece:</p>
<ul>
<li><strong>Desempenho:</strong> uma visão clara do que aconteceu no experimento</li>
<li><strong>Insights:</strong> uma explicação do motivo pelo qual os resultados ocorreram</li>
<li><strong>Oportunidades:</strong> orientação sobre as próximas ações a serem realizadas</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Data de disponibilidade: 9 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API pública para recuperar jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova API do Journey Optimizer agora está disponível para recuperar jornadas e seus objetos associados, como campanhas e superfícies.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Data de disponibilidade: 25 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos

- **Campanhas, Experience Decisioning, Jornadas**
   - **Selecionar regras reutilizáveis no Direcionamento** - Agora você pode aproveitar o construtor de regras ao usar as regras de Direcionamento com o recurso de Otimização de Mensagem em jornadas e campanhas. <!-- [Read more](../FILE.md) -->

- **Canal - WhatsApp**
   - **Campo de execução para canal do WhatsApp** - Além de email e SMS, agora é possível atualizar o campo de execução padrão do WhatsApp. Também é possível substituir o campo de execução definido globalmente nos parâmetros avançados da atividade de jornada do WhatsApp ou na configuração do canal do WhatsApp. <!-- [Read more](../FILE.md) -->

- **Permissões**
   - **O criador de Jornadas/Campanhas não deve ser capaz de aprovar**. Adicionada uma opção ao criar ou definir a Política de Aprovação para impedir que os criadores de Jornadas/Campanhas aprovem seus próprios objetos. <!-- [Read more](../FILE.md) -->

- **Canal - Push**
   - **Atividades móveis ao vivo - Beta privado** - As atividades ao vivo fornecem atualizações em tempo real e experiências interativas em aplicativos móveis, permitindo que os usuários permaneçam informados sobre eventos ou tarefas em andamento diretamente na tela do dispositivo. Esse recurso melhora a participação fornecendo informações em tempo real, como rastreamento de progresso, atualizações de eventos ou conteúdo interativo, sem exigir que os usuários abram o aplicativo. <!-- [Read more](../FILE.md) -->

- **Jornadas**
   - **Novos alertas de Jornada** - Data de disponibilidade: 14 de outubro de 2025
Novos alertas pré-configurados estão disponíveis para o jornada: Taxa de descarte de perfil excedida (Taxa de descartes de perfil para perfis inseridos nos últimos 5 minutos excedeu o limite), Taxa de erro de ação personalizada excedida (Taxa de erros de ação personalizada para chamadas HTTP bem-sucedidas nos últimos 5 minutos excedeu o limite), Taxa de erro de perfil excedida (Taxa de perfis com erro para perfis inseridos nos últimos 5 minutos excedeu o limite). <!-- [Read more](../FILE.md) -->

- **Configuração**
   - **Suporte a atributos personalizados com URL de cancelamento de inscrição com um clique** - Data de disponibilidade: 6 de outubro de 2025
Com o Journey Optimizer, se você estiver gerenciando o consentimento fora do Adobe, é possível definir um terminal personalizado externo definindo seu próprio link de cancelamento de inscrição com um clique na configuração do email. Quando os destinatários clicam no link de cancelamento de inscrição, o Journey Optimizer anexa alguns parâmetros específicos do perfil padrão ao evento de atualização de consentimento. Para personalizar ainda mais o endereço de email para cancelar assinatura, agora você pode definir atributos personalizados que serão anexados ao evento de consentimento. Esse recurso já está disponível para o URL personalizado de cancelamento de inscrição com um clique desde 25 de agosto e agora é lançado para a opção Mailto (cancelar inscrição) em Disponibilidade limitada. Entre em contato com seu representante da Adobe para obter acesso. <!-- [Read more](../FILE.md) -->

- **Canal - Email**
   - **Anexos do PDF para emails** - Data de disponibilidade: 30 de setembro de 2025
Agora é possível anexar um arquivo PDF estático a uma mensagem de email enviada com o Journey Optimizer. Você pode enviar até 6 mensagens com um anexo do PDF por perfil por ano. O tamanho máximo permitido para cada anexo é de 5 MB. Para qualquer tamanho ou volume adicional, você pode comprar o complemento de anexo do PDF. Para obter mais informações, entre em contato com um representante da Adobe.

  >[!AVAILABILITY]
  >
  >Anteriormente lançado com disponibilidade limitada, essa melhoria agora está disponível para todos os ambientes (disponibilidade geral).

  <!-- [Read more](../FILE.md) -->

