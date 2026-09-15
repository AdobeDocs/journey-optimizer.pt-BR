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
source-git-commit: f4e6891fa1821333a87a5477472b473d23df3eb5
workflow-type: tm+mt
source-wordcount: '3342'
ht-degree: 10%
---

# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer fornece de forma contínua novos recursos, melhorias para os recursos já existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

## Notas de pré-lançamento de 26 de setembro {#sep-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas podem ser lançadas posteriormente — consulte a “Data de disponibilidade” listada de cada entrada para obter detalhes.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 22 a 23 de setembro de 2026

### Gerenciamento de conteúdo {#sep-26-content-management}

O recurso a seguir está chegando ao gerenciamento de conteúdo nesta versão.

<table>
<thead>
<tr>
<th><strong>Plug-ins de cópia de mensagens e design de e-mail no CX Co-worker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dois novos plug-ins agora estão disponíveis no CX Co-worker para simplificar seus <strong>fluxos de trabalho de mensagens e email</strong>, desde a estratégia até a implantação:</p>
<p><strong>Plug-in de cópia de mensagem</strong>:</p>
<ul>
<li>Captura resumos da campanha e define mapas de mensagens, arcos narrativos e funções de canal.</li>
<li>Cria uma matriz de conteúdo multidimensional personalizada em canais, pontos de contato, localidades, públicos-alvo e variantes.</li>
<li>Produz uma cópia totalmente nova e aproveita o Adobe Firefly para gerar, cortar e adaptar visuais de campanha.</li>
<li>Permite a avaliação de conteúdo no local e sincroniza diretamente os ativos aprovados de volta para o Journey Optimizer, Adobe Campaign V8 e Marketo.</li>
</ul>
<p><strong>Plug-in de design de email</strong>:</p>
<ul>
<li>Converte metas de marketing, capturas de tela de referência ou links de design do Figma em planos de layout personalizados e HTML de email prontos para produção.</li>
<li>Gerencia ativos de marca reutilizáveis, tokens de design e modelos de email estruturais.</li>
<li>Auditorias montadas no código de email para conformidade corporativa, qualidade de design visual e padrões de acessibilidade WCAG 2.1 AA.</li>
<li>Exporta HTML aprovados diretamente para o Adobe Journey Optimizer e Adobe Campaign.</li>
</ul>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

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

<table>
<thead>
<tr>
<th><strong>Atualizações de mapeamento de evento de fidelidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A criação ou edição de um Mapeamento de evento agora usa um novo **construtor de mapeamento visual**: selecione um esquema, escolha campos de um seletor de campo pesquisável, mapeie cada campo para um campo de evento de fidelidade com status de conexão por linha e visualize a expressão JSONata gerada automaticamente, com a opção de alternar para a edição JSONata manual a qualquer momento.</p><p>Além disso, as "Definições de evento" no Admin de fidelidade foram renomeadas para "Mapeamentos de evento", com uma exibição de lista atualizada que mostra o nome de esquema do evento de experiência legível.</p>
</td>
</tr>
</tbody>
</table>

* **Habilidade de recomendação de fidelidade do CX Coworker** - Os profissionais de marketing agora podem solicitar **oportunidades de desafio** diretamente na interface de conversação do CX Coworker, obtendo ideias de desafio baseadas em tendências reais do programa de fidelidade e transformando-as em desafios ao vivo sem sair do chat.

* **Domínio de desafios no editor de personalização de Cartão de Conteúdo** - O editor de personalização de Cartão de Conteúdo agora aceita **Desafios** como um domínio, permitindo que você acesse metadados de desafio ao criar a personalização de cartão de conteúdo. Isso facilita a criação de conteúdo personalizado para cada estágio de um desafio — Início, Em andamento e Término — sem código personalizado.

### Integração {#sep-26-onboarding}

O recurso a seguir está sendo integrado nesta versão.

<table>
<thead>
<tr>
<th><strong>Recursos guiados para integração de emails e jornadas (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A transição para o Adobe Journey Optimizer a partir de outra plataforma de marketing é mais fácil com recursos guiados que ajudam a mover o conteúdo de email existente e as jornadas para o Journey Optimizer. Um <strong>espaço de trabalho dedicado</strong> permite reutilizar o que você tem, em vez de reconstruir do zero.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
</td>
</tr>
</tbody>
</table>

### Públicos-alvo {#sep-26-audiences}

O lembrete a seguir se aplica aos públicos-alvo nesta versão.

* **Futura alteração para públicos-alvo de enriquecimento da Composição de Público-alvo** - Durante a versão de outubro (fim de outubro), o Journey Optimizer interromperá jornadas e campanhas que usam ou fazem referência a um público-alvo da Composição de Público-alvo cujo conjunto de dados de origem não tem um **descritor de identidade principal**. A partir desse ponto, somente os públicos-alvo de Composição de público-alvo criados com um descritor de identidade principal são compatíveis com jornadas e campanhas. Se você precisar que essas jornadas ou campanhas permaneçam ativas, entre em contato com o representante da Adobe — nossa equipe de produtos pode ajudá-lo a migrar. <!-- Documentation link: TBD -->

### Jornadas {#sep-26-journeys}

Os recursos e melhorias a seguir estão chegando às jornadas nesta versão.

<table>
<thead>
<tr>
<th><strong>Simulação de Jornada no CX Co-worker (MCP e Chat)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>habilidade Simulação de Jornada</strong> do CX Co-worker automatiza a validação completa da jornada e permite que você interprete facilmente os resultados. Observe que esse recurso atualmente suporta apenas o fluxo de Simulação rápida e não substitui totalmente a experiência de simulação manual do Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Criação de jornada a partir do painel do CX Co-worker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>criação de Jornadas com IA</strong> agora está disponível diretamente no painel direito do CX Coworker, substituindo a experiência anterior do Assistente de IA por um ponto de entrada integrado e reformulado para gerar jornadas.</p>
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

* **Lógica de espera de avaliação de público em lote refinada** - Na **atividade de leitura de público**, a opção &quot;Acionar após avaliação de público em lote&quot; no jornada agora sempre aguarda a conclusão de uma segmentação em lote em andamento, garantindo que a jornada use os dados da execução em vez de recorrer a um instantâneo mais antigo. Se nenhuma segmentação de lote estiver em andamento, a jornada usará o instantâneo mais recente disponível imediatamente, a menos que esse instantâneo seja o mesmo lote usado na execução anterior, caso em que a jornada aguarda até a janela configurada para um lote mais recente, e ignora a execução desse dia se nenhum chegar a tempo.

* **O suporte à ID complementar na simulação de Jornada** - **A ID complementar** agora tem suporte na simulação de Jornada, permitindo que você teste cenários de usuário complexos para jornadas acionadas por evento e público-alvo de leitura.

* **Lógica de espera de avaliação de público em lote refinada** - Na **atividade de leitura de público**, a opção &quot;Acionar após avaliação de público em lote&quot; no jornada agora sempre aguarda a conclusão de uma segmentação em lote em andamento, garantindo que a jornada use os dados da execução em vez de recorrer a um instantâneo mais antigo. Se nenhuma segmentação de lote estiver em andamento, a jornada usará o instantâneo mais recente disponível imediatamente, a menos que esse instantâneo seja o mesmo lote usado na execução anterior, caso em que a jornada aguarda até a janela configurada para um lote mais recente, e ignora a execução desse dia se nenhum chegar a tempo.

* **Comparar versões do jornada com o CX Coworker** - Hoje, examinar o que foi alterado entre duas versões de uma jornada requer compará-lo manualmente dentro do nó do Journey Optimizer por nó. Não há diferença estruturada, o que torna as verificações de revisão de alteração, auditoria e pré-publicação lentas e propensas a erros, especialmente quando o jornada se torna mais complexo. Esse recurso permite que um cliente ou agente de IA compare duas versões de uma jornada por meio do CX Coworker Chat e obtenha de volta uma comparação completa e **estruturada** - nós adicionados/removidos/modificados/movidos com detalhes em nível de campo, conexões alteradas, alterações de propriedade em nível de jornada e contagens acumuladas - sem abrir o Journey Optimizer.

* **Eventos de etapa reduzidos para atividades de espera e de evento** - Os eventos de etapa não são mais gerados para atividades de **espera** e **evento** quando o perfil não foi realmente processado nessa atividade. <!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 --> <!-- Documentation link: TBD -->

* **Supressão de evento de etapa de execução seca para relatórios personalizados** - Como parte da otimização de evento de etapa, o Journey Optimizer agora interrompe a geração de determinados eventos de etapa não reportáveis durante as Execuções Secas de Jornada. Isso só afeta relatórios personalizados criados nesses tipos de evento de etapa de execução segura. Se você for afetado, acione novamente a simulação para gerar dados novamente.

* **Habilidade do Colaborador da Análise de Higiene** - Uma nova habilidade da Análise de Higiene no CX Coworker verifica as jornadas ativas e de rascunho em busca de configurações corrompidas, falhas silenciosas e ativos em decomposição ou não utilizados, como jornadas de rascunho obsoletas, fontes de dados órfãs e erros persistentes de ação personalizada, e apresenta correções recomendadas diretamente do chat. <!-- Documentation link: TBD -->

* **Habilidade do Colaborador na Análise de Desempenho de Negócios** - Uma nova habilidade **Análise de Desempenho de Negócios** na CX Coworker analisa o desempenho de suas jornadas, explica áreas de baixo desempenho e recomenda otimizações concretas, como esperas de reengajamento, escalonamento de canais e Otimização de Tempo de Envio.  <!-- Documentation link: TBD -->

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

* **Flexibilidade de autenticação BYOP de SMS personalizado** - Agora você pode configurar **cabeçalhos de autenticação personalizados** ao conectar a configuração OAuth do seu provedor de SMS, incluindo onde o token é colocado nas mensagens de saída e como a própria solicitação de token é formatada.

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

<table>
<thead>
<tr>
<th><strong>Alertas para campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As campanhas orquestradas agora oferecem suporte a <strong>alertas automatizados</strong> por meio da mesma estrutura de alertas usada em jornadas e campanhas. Os alertas são acionados quando a execução de uma campanha falha, atinge o tempo limite ou exige confirmação e cada alerta inclui o que aconteceu, quando, onde e um link direto para a exibição de monitoramento, categorizado por gravidade, para que as equipes possam priorizar sem verificações manuais da interface do usuário.</p>
</td>
</tr>
</tbody>
</table>

* **Canal LINE para campanhas orquestradas** - O LINE agora está disponível como um canal de saída nativo em campanhas orquestradas, junto com email, SMS e push. Você pode criar e entregar mensagens LINE diretamente da tela da campanha, incluindo texto, adesivos, imagens, vídeos, dados de localização e mensagens do Flex, apoiando casos de uso de engajamento promocional, transacional e contínuo em mercados dominados pelo LINE, como Japão e APAC. Lançado anteriormente com disponibilidade limitada, esse recurso agora está disponível no mercado.

* **Novas APIs de monitoramento de Campanhas Orquestradas** - Novas **especificações de API** estão disponíveis para campanhas orquestradas, permitindo que você crie, gerencie e acione campanhas orquestradas de forma programática, permitindo uma integração mais profunda com sistemas externos e pipelines de automação.

* **Melhorias no UX de junção direta** - Ao adicionar um atributo de uma coleção relacionada, agora é possível escolher entre três modos de junção — um novo padrão que avisa sobre o impacto potencial no desempenho de produtos cartesianos, além dos modos Agregado e Avançado existentes — facilitando a compreensão das compensações da consulta antes da compilação.

* **Conteúdo condicional com dados relacionais em campanhas orquestradas** - Ao criar conteúdo condicional no Designer de email para campanhas orquestradas, agora é possível criar condições diretamente em **dados relacionais** — como registros relacionados associados a um perfil — não apenas atributos de perfil padrão. Isso fecha uma lacuna da versão original, de modo que os profissionais de marketing podem criar essas condições visualmente, sem precisar de ajuda de engenharia.

* **Monitoramento da Orquestração de Campanha** — Uma nova interface de usuário está disponível para rastrear o status de assimilação e a atualização dos dados do armazenamento relacional usados pela Segmentação Orquestrada do Campaign. Ele oferece visibilidade direta da integridade dos dados que alimentam os públicos-alvo em lote. Uma nova guia Orquestração de campanha no painel Monitoramento da Adobe Experience Platform exibe a integridade dos fluxos de dados do armazenamento relacional (registros assimilados/atualizados/excluídos/com falha/ignorados), com gráficos detalhados e um detalhamento por fluxo de dados/conjunto de dados, incluindo linhagem.


### Campanhas {#sep-26-campaigns}

Os seguintes recursos e melhorias estão chegando às campanhas nesta versão.

<table>
<thead>
<tr>
<th><strong>Simulação de experiência de entrada em campanhas de ação (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível simular ações de canal de entrada em Campanhas de ação antes de entrar em atividade. Use o modo de simulação para testar sua configuração com usuários simulados e visualizar a experiência renderizada, incluindo um URL gerado e um código QR, para que você possa validar regras, decisões e renderização de conteúdo de ponta a ponta.</p>
<p>No momento, esse recurso está em Private Beta e disponível para um conjunto limitado de organizações. Entre em contato com o representante da Adobe para obter mais informações.</p>
</td>
</tr>
</tbody>
</table>

* **Pastas para campanhas** - Agora você pode organizar suas campanhas em **pastas** para melhorar a navegação e o gerenciamento na interface.

### Decisão {#sep-26-decisioning}

Os recursos e melhorias a seguir estão chegarão à Decisão nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal da Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Decisão agora está disponível no canal da web. Você pode usar políticas de decisão diretamente no editor visual da web para fornecer as ofertas mais relevantes a cada visitante.</p>
</td>
</tr>
</tbody>
</table>

* **Geração de regra de decisão do CX Coworker** - A **experiência da geração de regra de decisão assistida por IA**, anteriormente disponível por meio do painel direito, agora pode ser acessada pelo CX Coworker, que substitui o painel direito como a maneira de criar regras com IA.

* **Suporte para perfis Adobe Experience Platform na simulação de fórmula de Regra e Classificação** - Ao simular uma Regra ou Fórmula de Classificação, agora é possível selecionar um perfil Adobe Experience Platform para preencher automaticamente os atributos de uma variante de dados de teste, em vez de inseri-los manualmente.

### Correspondência direta {#sep-26-direct-mail}

Os seguintes recursos e aprimoramentos estão chegando ao Direct Mail nesta versão.

* **Dividir arquivos grandes automaticamente** - Os arquivos de Mala Direta agora podem ser divididos em várias partes automaticamente quando excedem aproximadamente 20 GB ou manualmente escolhendo um tamanho de arquivo de destino na configuração de roteamento de arquivos. Um arquivo de manifesto JSON opcional descreve todas as partes geradas.

* **Limite de público-alvo aumentado** - O limite de público-alvo do canal de correspondência direta aumentou de 3 milhões para 100 milhões de perfis, permitindo que você direcione públicos-alvo muito maiores sem encontrar erros de criação de arquivos.

### Designer de email {#sep-26-email-designer}

Os seguintes recursos e melhorias estão chegando ao Designer de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Estilo independente em modo escuro para variantes de tema de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os temas de email agora oferecem suporte ao estilo independente para o modo escuro. No construtor de temas, é possível ativar o modo escuro para uma determinada variante a fim de gerar uma folha de estilos dedicada do modo escuro que você edita separadamente dos estilos do modo claro. As alterações feitas em um modo não substituem mais o outro. No editor de email e modelo, um novo botão de visualização ao lado das opções de exibição para dispositivos móveis e desktop permite que você visualize o conteúdo no modo escuro.</p>
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

### Administração {#sep-26-administration}

O lembrete a seguir se aplica à administração nesta versão.

* **Garantia de vida útil do conjunto de dados (TTL) — sandboxes existentes** - A proteção de vida útil (TTL) para conjuntos de dados gerados pelo sistema da Journey Optimizer (90 dias no repositório de perfis, 13 meses no data lake) será aplicada às sandboxes e organizações do cliente existentes a partir de 1º de outubro de 2026.

### Melhorias de usabilidade {#sep-26-usability}

* **Melhorias de usabilidade na experiência de Simulação de conteúdo** - A nova experiência de Simulação de conteúdo agora permite nomear e organizar suas variantes para facilitar a comparação, copiar ou excluir detalhes da variante diretamente de cada cartão, exibir caminhos completos de atributos e configuração de canal por cartão sob demanda e carregar seus próprios perfis CSV, JSON ou JSONL com um botão de carregamento mais destacado.

* **Visualização de conteúdo na tela do jornada** - A revisão de conteúdo do canal hoje requer a abertura de cada nó individualmente, um de cada vez - lento e sujeito a erros no jornada com muitos nós de canal, especialmente quando a personalização significa a verificação de vários tratamentos ou variantes por nó. A **visualização de conteúdo** remove esse atrito ao exibir uma miniatura de conteúdo para cada nó de canal diretamente na tela, com um modal de tela cheia para inspecionar e alternar entre tratamentos e variantes.

* **Calendário unificado para Campanhas, Jornadas e campanhas orquestradas** - A exibição de calendário para jornadas e campanhas agora sai de inventários separados em um menu unificado acessível no painel esquerdo que mostra ambos em uma exibição combinada.

