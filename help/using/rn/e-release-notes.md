---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 8d5e3584ff2dc7cf9c00043e1a67f9a4c23255d9
workflow-type: tm+mt
source-wordcount: '2726'
ht-degree: 8%
---

# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer fornece de forma contínua novos recursos, melhorias para os recursos já existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

## Notas de pré-lançamento de 26 de setembro {#sep-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas podem ser lançadas posteriormente — consulte a “Data de disponibilidade” listada de cada entrada para obter detalhes.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 22 a 23 de setembro de 2026

>[!BEGINSHADEBOX]

**Novo no CX Enterprise Coworker este mês**

Esta versão traz vários recursos e habilidades novos e aprimorados do [Coworker](../start/ai-features.md#cx-coworker), listados aqui para visibilidade. Cada uma delas também é detalhada em sua seção relevante abaixo.

* [Plug-in de Conteúdo do Canal CE](#sep-26-content-management) - Um novo plug-in que reúne habilidades de HTML em cópia de campanha, imagem e email no Coworker, desde um resumo da campanha até a cópia pronta para produção e o HTML.
* [Habilidade de recomendação de fidelidade](#sep-26-loyalty) - Solicite oportunidades de desafio diretamente na interface de conversa do Colaborador e transforme-as em desafios ao vivo sem sair do chat.
* [Simulação de Jornada](#sep-26-journeys) - Automatize a validação de jornada de ponta a ponta e interprete os resultados diretamente no Colaborador.
* [Criação de Jornadas no painel do Colaborador](#sep-26-journeys) - Gere jornadas com IA diretamente no painel direito do Colaborador, substituindo a experiência anterior do Assistente de IA.
* [Comparar versões do jornada](#sep-26-journeys) - Obtenha uma diferença estruturada e de fidelidade completa entre duas versões de uma jornada por meio do Chat do Colaborador.
* [Habilidade da Análise de Higiene](#sep-26-journeys) - Examine jornadas ativas e de rascunho em busca de configurações corrompidas, falhas silenciosas e ativos em decomposição ou não utilizados, com correções recomendadas.
* [Habilidade em Análise de Desempenho de Negócios](#sep-26-journeys) - Analise o desempenho da jornada e obtenha recomendações concretas de otimização, diretamente do chat.

>[!ENDSHADEBOX]

### Gerenciamento de conteúdo {#sep-26-content-management}

O recurso a seguir está chegando ao gerenciamento de conteúdo nesta versão.

<table>
<thead>
<tr>
<th><strong>Plug-in de Conteúdo do Canal no Colaborador</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo plug-in de <strong>Conteúdo do Canal</strong> já está disponível no Co-worker, que reúne as habilidades de cópia da campanha, imagem e email montado no HTML em um plug-in, da estratégia à implantação. As seguintes habilidades estão disponíveis no plug-in **Conteúdo do canal**:</p>
<ul>
<li><strong>Orquestrar Criação De Conteúdo</strong>.</li>
<li><strong>Explorar a estratégia de conteúdo</strong></li>
<li><strong>Resumo do conteúdo</strong></li>
<li><strong>Gerar conteúdo</strong></li>
<li><strong>Verificar prontidão do conteúdo</strong></li>
<li><strong>Revisar e regenerar conteúdo</strong></li>
<li><strong>Gerar imagem</strong></li>
<li><strong>Avaliar o design de conteúdo</strong></li>
<li><strong>Salvar conteúdo do canal</strong></li>
<li><strong>Criar e-mail no Figma</strong></li>
<li><strong>Pesquisa de marca</strong> </li>
</ul>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Integrações {#sep-26-integrations}

Os recursos a seguir estão chegando às integrações nesta versão.

* **Substituição dinâmica de token para fragmentos de Experience Manager** - As referências de Fragmento de Conteúdo do Experience Manager agora oferecem suporte a um atributo **tokenSubstitution**. Quando definido como `false`, a personalização dentro dos campos do fragmento é resolvida diretamente, sem um mapa de token na referência. O padrão é `true`, que mantém o comportamento existente.

  Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.

* **Suporte a fragmentos de conteúdo do AEM Managed Services na Decisão** - Os fragmentos de conteúdo do AEM Managed Services agora são aceitos na Decisão ao gerenciar itens de decisão.

### Fidelidade {#sep-26-loyalty}

Os seguintes recursos e melhorias estão chegando ao Fidelidade nesta versão.

<table>
<thead>
<tr>
<th><strong>Oportunidades de desafio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O menu de Desempenho de Fidelidade agora inclui uma <strong>guia Oportunidades</strong>, que mostra tendências e lacunas detectadas pela IA, como atrito de progressão de nível ou queda de tarefa de desafio, cada uma com um impacto projetado e uma ação "Criar com IA" de um clique para gerar um desafio que atenda a isso.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Domínio de desafios no editor de personalização de Cartão de Conteúdo** - O editor de personalização de Cartão de Conteúdo agora aceita **Desafios** como um domínio, permitindo que você acesse metadados de desafio ao criar a personalização de cartão de conteúdo. Isso facilita a criação de conteúdo personalizado para cada estágio de um desafio — Início, Em andamento e Término — sem código personalizado.

<!--
### Onboarding {#sep-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A <strong>dedicated workspace</strong> lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

-->

### Jornadas {#sep-26-journeys}

Os recursos e melhorias a seguir estão chegando às jornadas nesta versão.

<table>
<thead>
<tr>
<th><strong>Criação de jornada do painel Colaborador</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>criação de Jornadas com IA</strong> agora está disponível diretamente no painel direito Colaborador, substituindo a experiência anterior do Assistente de IA por um ponto de entrada integrado e reformulado para geração de jornadas.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Cartões de recomendação de IA para alertas de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A página inicial da Journey Optimizer agora exibe um <strong>cartão de recomendação de IA</strong> quando um alerta de jornada é acionado, cobrindo os alertas <strong>Falha da ação personalizada de Jornada</strong> e <strong>Anomalia de Jornada detectada</strong>. Selecionar a placa abre a jornada com o painel direito pré-preenchido com a análise já realizada.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade de entrada do jornada de desativação de atividade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova atividade de <strong>Desativação de atividade de entrada</strong> na tela de jornada permite remover um perfil de até cinco atividades ou experiências de entrada diretamente de uma jornada, dissociando a desqualificação de entrada da saída do jornada para uma orquestração entre canais mais avançada.</p>
</td>
</tr>
</tbody>
</table>

* **O suporte à ID complementar na simulação de Jornada** - **A ID complementar** agora tem suporte na simulação de Jornada, permitindo que você teste cenários de usuário complexos para jornadas acionadas por evento e público-alvo de leitura.

* **Suporte de salto para jornadas de Qualificação de Público-Alvo** - As Jornadas que começam com uma **Qualificação de Público-Alvo** agora podem usar uma atividade de **Salto** para entrar em uma jornada de início baseada em evento; não há suporte para salto para uma jornada baseada em Qualificação de Público-Alvo.

* **Comparar versões do jornada com o Colaborador** - Hoje, examinar o que foi alterado entre duas versões de uma jornada requer compará-las manualmente dentro do nó do Journey Optimizer por nó. Não há diferença estruturada, o que torna as verificações de revisão de alteração, auditoria e pré-publicação lentas e propensas a erros, especialmente porque o jornada se torna mais complexo. Esse recurso permite que um cliente ou agente de IA compare duas versões de uma jornada por meio do Chat do Colaborador e obtenha uma comparação de fidelidade completa **estruturada** - nós adicionados/removidos/modificados/movidos com detalhes em nível de campo, conexões alteradas, alterações de propriedade em nível de jornada e contagens acumuladas - sem abrir o Journey Optimizer.

* **Eventos de etapa reduzidos para atividades de espera e de evento** - Os eventos de etapa não são mais gerados para atividades de **espera** e **evento** quando o perfil não foi realmente processado nessa atividade. <!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

* **Supressão de evento de etapa de execução seca para relatórios personalizados** - Como parte da otimização de evento de etapa, o Journey Optimizer agora interrompe a geração de determinados eventos de etapa não reportáveis durante as Execuções Secas de Jornada. Isso só afeta relatórios personalizados criados nesses tipos de evento de etapa de execução segura. Se você for afetado, acione novamente a simulação para gerar dados novamente.

* **Habilidade do Coworker para Análise de Higiene** - Uma nova habilidade de Análise de Higiene no Coworker verifica as jornadas ativas e de rascunho em busca de configurações com falha, falhas silenciosas e ativos em decomposição ou não utilizados — como jornadas de rascunho obsoletas, fontes de dados órfãs e erros persistentes de ação personalizada — e apresenta correções recomendadas diretamente do chat. <!-- Documentation link: TBD -->

* **Habilidade do Colaborador para Análise de Desempenho de Negócios** - Uma nova habilidade **Análise de Desempenho de Negócios** no Colaborador analisa o desempenho de suas jornadas, explica áreas de baixo desempenho e recomenda otimizações concretas, como esperas de reengajamento, escalonamento de canal e Otimização de Tempo de Envio.  <!-- Documentation link: TBD -->

* **Tempo limite de recuperação automática de evento nas Propriedades de Jornada** - As Propriedades de Jornada agora incluem uma configuração **Definir tempo limite de recuperação de evento**: por padrão, os eventos de jornada afetados são repetidos automaticamente por até 72 horas após uma interrupção de serviço sem a necessidade de nenhuma ação. Você pode ativar essa configuração para controlar a janela de repetição (0-72 horas) para jornadas sensíveis ao tempo. O campo existente **Tempo limite ou erro** também foi renomeado para **Tempo limite de Ação Personalizada/Ação de IDS** para evitar confusão entre as duas configurações.

### Canais {#sep-26-channels}

Os seguintes recursos e melhorias estão chegando aos canais nesta versão.

<table>
<thead>
<tr>
<th><strong>Atividades ativas para atualizações do Android Live</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Journey Optimizer agora expande seus recursos de personalização móvel em tempo real estendendo o suporte à <strong>Atividade em tempo real para o Android</strong>. Você pode fornecer atualizações de progresso em tempo real diretamente aos usuários, como rastreamento de pedidos, status de voo, atualizações de eventos ao vivo e pontuações de esportes em tempo real.</p>
<p>Além do suporte às atividades do iOS Live, a Journey Optimizer agora gerencia tokens de push temporários para atualizações do Android Live em todas as configurações da plataforma. Ele é compatível com fluxos de atualização transacionais e de transmissão usando campanhas acionadas por API e APIs headless.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de saída personalizado (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Os </strong> canais de saída personalizados permitem que os administradores levem qualquer canal de mensagens baseado em HTTP de saída — como WeChat, Kakao Talk, Messenger ou um provedor proprietário — diretamente para a Journey Optimizer por meio de um Channel Builder sem código. Depois de configurados, os canais personalizados ficam disponíveis em campanhas, jornadas e campanhas orquestradas, com o mesmo conjunto completo de recursos dos canais nativos: personalização com o editor de expressão, experimentação de conteúdo, pré-visualização e prova, relatórios prontos para uso e aplicação de consentimento e governança.</p>
<p>Com esta versão, os canais de saída personalizados também ganham vários novos recursos:</p>
<ul>
<li>Use o Journey Optimizer Decisioning na carga útil do canal personalizado por meio do Editor do Personalization, da mesma forma que nas experiências baseadas em código.</li>
<li>Aplique regras de negócios a canais personalizados, da mesma forma que já é possível em canais nativos.</li>
<li>Selecione canais personalizados na lista de canais para campanhas acionadas por API, o que não era possível anteriormente.</li>
<li>Defina um webhook de relatórios para um canal personalizado e anexe-o a uma configuração de canal, para que você possa enriquecer seus relatórios do Journey Optimizer com eventos de interação.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Melhorias nos modelos de notificações por push do Android</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As notificações por push do Android eram renderizadas anteriormente com um layout único e fixo: as imagens sempre eram cortadas ao centro e o texto do corpo longo era truncado. Essa versão apresenta um seletor de modelo no momento da criação, permitindo que os profissionais de marketing controlem o layout das notificações por push do Android.</p>
<p>As seguintes melhorias estão disponíveis:</p>
<ul>
<li><b>Seleção de layout</b>: novo seletor de layout de notificação por push (Padrão/Expandido) ao criar um push do Android.</li>
<li><b>Layout padrão com "Mostrar imagem inteira"</b>: escolha recortado para preenchimento vs. dimensionado para ajuste.</li>
<li><b>Layout expandido</b>: corpo de texto multilinha sem truncamento, além de miniatura de ícone grande opcional.</li>
<li><b>Corpo recolhido (Layout expandido)</b>: defina um texto de corpo separado e mais curto para o estado recolhido.</li>
</ul>
</td>
</tr>
</tbody>
</table>


* **Flexibilidade de autenticação BYOP de SMS personalizado** - Agora você pode configurar **cabeçalhos de autenticação personalizados** ao conectar a configuração OAuth do seu provedor de SMS, incluindo onde o token é colocado nas mensagens de saída e como a própria solicitação de token é formatada.

* **Correspondência direta - Dividir arquivos grandes automaticamente** - Os arquivos de Correspondência Direta agora podem ser divididos em várias partes automaticamente quando excedem aproximadamente 20 GB ou manualmente escolhendo um tamanho de arquivo de destino na configuração de roteamento de arquivos.

* **Correspondência direta - Aumento do limite de público-alvo** - O limite de público-alvo do canal de correspondência direta aumentou de 3 milhões para 100 milhões de perfis, permitindo que você direcione públicos-alvo muito maiores sem encontrar erros de criação de arquivos.

### Canal de email {#sep-26-email-channel}

Os seguintes recursos e melhorias estão chegando ao canal de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Substituir configurações do canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ao criar suas jornadas e campanhas, agora é possível substituir os parâmetros de email derivados da configuração de canal selecionada diretamente no nível de jornada ou ação de campanha.</p>
<p>Isso permite personalizar os campos de cabeçalho de email (<strong>Do nome</strong>, <strong>Do prefixo de email</strong>, <strong>Responder ao nome</strong> e <strong>Responder ao email</strong>), o endereço de execução e os valores de cancelamento de inscrição na lista, usando atributos de perfil ou dados contextuais para obter um controle mais preciso. Especificamente, isso permite que os detalhes do remetente reflitam o supervisor, o local ou a ramificação relevante para cada recipient, em vez de rotear todos os envios por meio de um único endereço corporativo.</p>
</td>
</tr>
</tbody>
</table>

* **Substituição da lista de supressão no nível de ação de email** - o Journey Optimizer agora permite substituir o comportamento da lista de supressão diretamente no nível de ação de email em jornadas e campanhas. Isso proporciona às equipes mais flexibilidade para comunicações operacionais ou críticas para conformidade que exigem uma configuração de envio dedicada, preservando os controles de lista de supressão global existentes para todos os outros envios. Esse aprimoramento ajuda as organizações a lidar com cenários de exceção com precisão sem alterar seu modelo de governança de supressão mais amplo.

* **Validação da sintaxe de URL na criação de email** - o Journey Optimizer agora valida URLs anteriormente no fluxo de criação de email e fornece orientações mais claras quando sintaxe mal formada é detectada. Isso ajuda os autores a identificar problemas antes da finalização, reduzir erros de publicação e melhorar a confiança do delivery.

### Designer de email {#sep-26-email-designer}

Os seguintes recursos e melhorias estão chegando ao Designer de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte ao modo escuro para variantes de tema de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os temas de email agora oferecem suporte ao modo escuro, para que cada variante de cor possa ser renderizada com uma aparência personalizada para os recipients que visualizam seu email em um cliente habilitado para o modo escuro.</p>
<p>Quando habilitada, uma paleta escura padrão é gerada automaticamente para cada variante, e você pode personalizá-la ainda mais com uma paleta diferente ou com suas próprias cores personalizadas, independentemente do design do modo claro. Portanto, as alterações feitas em um modo não afetam o outro.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Importar modelos do Dynamic Media diretamente de arquivos do PSD no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O componente Dynamic Media do Designer de email agora permite importar um arquivo do Photoshop (PSD) diretamente como um novo modelo, além de navegar pelos modelos existentes do Dynamic Media. Arraste e solte um arquivo do PSD no componente e o Adobe Journey Optimizer o converte automaticamente em um modelo do Dynamic Media armazenado no Dynamic Media — não é necessária nenhuma conversão manual ou viagem de ida e volta pelo Adobe Experience Manager. Após a importação, o modelo é editado com o editor dinâmico de mídia integrado, a mesma experiência usada para o conteúdo Adobe Express no Designer de email.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novo componente de tabela no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Designer de email agora inclui um <strong>componente de Tabela</strong> interno, permitindo que você estruture o conteúdo em linhas e colunas diretamente no seu email. Arraste e solte o componente na tela, personalize o número de linhas e colunas e estilize cada célula independentemente para criar layouts claros e organizados sem depender de HTML personalizados.</p>
</td>
</tr>
</tbody>
</table>

* **Fontes substitutas para fontes personalizadas em temas de email** - Agora é possível definir uma fonte substituta para qualquer fonte personalizada (da Web) aplicada por temas de email. Se o cliente de email de um assinante não oferecer suporte à fonte personalizada, o Adobe Journey Optimizer exibirá automaticamente a fonte de fallback especificada, em vez de deixar a opção para o padrão do cliente de email. Isso mantém a tipografia de email mais próxima das diretrizes da sua marca e reduz as inconsistências de renderização de fonte nos clientes de email.

### Campanhas orquestradas {#sep-26-oc}

Os recursos e melhorias a seguir estão chegando às campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>OU participe de atividades para campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>Atividade de ingresso</strong> em campanhas orquestradas agora oferece suporte às condições de ingresso AND e OR. Com a lógica OR, um perfil que conclui qualquer ramificação upstream, em vez de todas, continua ao longo de um único caminho downstream compartilhado. Isso permite modelar "se A ou B ou C, faça isso" padrões diretamente na tela sem duplicar etapas downstream em ramificações separadas.</p>
</td>
</tr>
</tbody>
</table>

* **Canal LINE para campanhas orquestradas** - O LINE agora está disponível como um canal de saída nativo em campanhas orquestradas, junto com email, SMS e push. Você pode criar e entregar mensagens LINE diretamente da tela da campanha, incluindo texto, adesivos, imagens, vídeos, dados de localização e mensagens do Flex, apoiando casos de uso de engajamento promocional, transacional e contínuo em mercados dominados pelo LINE, como Japão e APAC. Lançado anteriormente com disponibilidade limitada, esse recurso agora está disponível no mercado.

* **Novas APIs de monitoramento de Campanhas Orquestradas** - Novas **especificações de API** estão disponíveis para campanhas orquestradas, permitindo que você crie, gerencie e acione campanhas orquestradas de forma programática, permitindo uma integração mais profunda com sistemas externos e pipelines de automação.

* **Melhorias no UX de junção direta** - Ao adicionar um atributo de uma coleção relacionada, agora é possível escolher entre três modos de junção — um novo padrão que avisa sobre o impacto potencial no desempenho de produtos cartesianos, além dos modos Agregado e Avançado existentes — facilitando a compreensão das compensações da consulta antes da compilação.

* **Monitoramento da Orquestração de Campanha** — Uma nova interface de usuário está disponível para rastrear o status de assimilação e a atualização dos dados do armazenamento relacional usados pela Segmentação Orquestrada do Campaign. Ele oferece visibilidade direta da integridade dos dados que alimentam os públicos-alvo em lote. Uma nova guia Orquestração de campanha no painel Monitoramento da Adobe Experience Platform exibe a integridade dos fluxos de dados do armazenamento relacional (registros assimilados/atualizados/excluídos/com falha/ignorados), com gráficos detalhados e um detalhamento por fluxo de dados/conjunto de dados, incluindo linhagem.


### Relatório {#sep-26-reporting}

O recurso a seguir está chegando aos relatórios nesta versão.

<table>
<thead>
<tr>
<th><strong>Novos gráficos de monitoramento de entrada no Gerenciamento de dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível monitorar a integridade dos dados de entrada diretamente em <strong>Gerenciamento de Dados &gt; Monitoramento &gt; Edge</strong>, com seis novos gráficos que abrangem eventos de taxa de transferência, latência e proposta:</p>
<ul>
<li><strong>Taxa de Transferência de Entrada do AJO</strong> — taxa de transferência de entrada geral (registros por segundo) ao longo do tempo.</li>
<li><strong>Detalhamento de Taxa de Transferência de Entrada do AJO</strong> — taxa de transferência de entrada dividida por localização.</li>
<li><strong>Latência de Entrada do AJO</strong> — latência de solicitação de entrada (em milissegundos), dividida pela distribuição de valores (P50, P90 e mais).</li>
<li><strong>Taxa de Transferência de Eventos de Apresentação de Entrada do AJO</strong> — taxa de transferência de eventos de apresentação (sinais de rastreamento gerados quando um usuário interage com o, visualiza ou aciona ofertas personalizadas) ao longo do tempo.</li>
<li><strong>Taxa de Transferência de Eventos de Apresentação de Entrada do AJO por Canal</strong> — a taxa de transferência de eventos de apresentação é dividida por canal de entrada (CBE, no aplicativo, cartões de conteúdo).</li>
<li><strong>Taxa de Transferência de Eventos de Apresentação de Entrada do AJO por Tipo de Evento</strong> — a taxa de transferência de eventos de apresentação é dividida por tipo de evento (descartada, suprimida, exibida, acionada, interagida, enviada).</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Melhorias de usabilidade {#sep-26-usability}

* **Melhorias de usabilidade na experiência de Simulação de conteúdo** - A nova experiência de Simulação de conteúdo agora permite nomear e organizar suas variantes para facilitar a comparação, copiar ou excluir detalhes da variante diretamente de cada cartão, exibir caminhos completos de atributos e configuração de canal por cartão sob demanda e carregar seus próprios perfis CSV, JSON ou JSONL com um botão de carregamento mais destacado.

* **Calendário unificado para Campanhas, Jornadas e campanhas orquestradas** - A exibição de calendário para jornadas e campanhas agora sai de inventários separados em um menu unificado acessível no painel esquerdo que mostra ambos em uma exibição combinada.

