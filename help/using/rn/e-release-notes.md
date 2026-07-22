---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 2fdc3176a79289ef505f1a8c974810f97f048f6a
workflow-type: tm+mt
source-wordcount: 2470
ht-degree: 19%

---


# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer fornece de forma contínua novos recursos, melhorias para os recursos já existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.




### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Notas de pré-lançamento de 26 de julho {#july-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas poderão ser implantadas posteriormente.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 28 de julho de 2026

### Fidelidade {#july-26-loyalty}

A Journey Optimizer apresenta o Loyalty, um novo recurso nesta versão.

<table>
<thead>
<tr>
<th><strong>Desafios de fidelidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os desafios de fidelidade transformam iniciativas de fidelidade em experiências envolventes e gamificadas que motivam os clientes a realizar ações valiosas, como fazer compras, escrever comentários, participar de redes sociais ou fazer referência a amigos.</p>
<p>Os administradores podem usar o menu Admin de fidelidade para conectar o Journey Optimizer ao seu ecossistema de fidelidade, incluindo APIs de atendimento de recompensa, definições de eventos, inventário de produtos, exclusões e configurações de identidade. Em seguida, os profissionais de marketing podem projetar desafios padrão, sequenciais ou em sequência, definir tarefas e recompensas, fornecer cartões de conteúdo e mensagens de marca e monitorar o desempenho com painéis de relatórios integrados. A Journey Optimizer gera as jornadas que organizam cada desafio em segundo plano, para que as equipes possam se concentrar na experiência do cliente e nas metas de negócios.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14019">DOCAC-14019</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Integração {#july-26-onboarding}

A Journey Optimizer apresenta o Hub de integração, um novo recurso nesta versão.

<table>
<thead>
<tr>
<th><strong>Hub de integração</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A transição para o Adobe Journey Optimizer a partir de outra plataforma de marketing agora é mais rápida e simples. O novo hub de integração apresenta um espaço de trabalho de migração que permite importar automaticamente seu conteúdo de email e jornadas existentes, evitando que você tenha que recriá-los do zero.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15180">DOCAC-15180</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Jornadas {#july-26-journeys}

Os recursos e melhorias a seguir foram adicionados às jornadas nesta versão.

<table>
<thead>
<tr>
<th><strong>Otimização de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode configurar uma ação do jornada para incluir vários canais de saída (Email, Push, SMS) e permitir que o Journey Optimizer forneça automaticamente por meio do melhor canal para cada cliente. Três modos de otimização estão disponíveis:</p>
<ul>
<li>Classificação manual: especifique a ordem de canal de sua preferência.</li>
<li>Preferência do cliente: use o canal de preferência do cliente em seu perfil (atributo Consentimentos e preferências do modelo de dados de experiência).</li>
<li>Classificação baseada em modelo de IA: use pontuações de propensão de aprendizado de máquina para inferir o canal mais eficaz por cliente.</li>
</ul>
<p>Quando o canal mais bem classificado estiver indisponível (não aceito, com limite de frequência ou não configurado), o sistema voltará para o próximo canal disponível.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14900">DOCAC-14900</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Suporte a documentos de públicos externos (valores separados por vírgulas e Composição de Público Federado) na Simulação de Jornada** - A Simulação de Jornada agora oferece suporte a Públicos Externos. Ao simular jornadas direcionadas a valores separados por vírgula ou públicos-alvo de Composição de público federado, você pode simular atributos de enriquecimento desses públicos-alvo diretamente pelo formulário da interface ou por uma importação de JSON. A interface do usuário exibe dinamicamente apenas os atributos específicos de enriquecimento usados na lógica de jornada, permitindo a validação precisa das ramificações de decisão e regras de personalização antes da ativação. ([DOCAC-15074](https://jira.corp.adobe.com/browse/DOCAC-15074)) <!-- Documentation link: TBD -->

* **Datas de início e término no cabeçalho da jornada** - Quando as datas de início e/ou término são configuradas em uma jornada em tempo real, elas agora são exibidas no cabeçalho da jornada ao lado da notificação de status em tempo real. O rótulo exibido se adapta com base no fato de cada data ser futura ou já ter passado. ([DOCAC-14702](https://jira.corp.adobe.com/browse/DOCAC-14702)) <!-- Documentation link: TBD -->

### Campanhas orquestradas {#july-26-oc}

Os recursos e melhorias a seguir foram adicionados às campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte Quiet Hours para campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aplicar horas de silêncio a campanhas orquestradas. As horas de silêncio permitem definir exclusões com base no tempo para evitar que as mensagens sejam enviadas durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade em casos de uso de orquestração de campanha.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo de simulação de canais de entrada de campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível simular ações de canal de entrada em Campanhas de ação antes de entrar em atividade. Use o modo de simulação para testar sua configuração com usuários simulados e visualizar a experiência renderizada, incluindo um URL gerado e um código QR, para que você possa validar regras, decisões e renderização de conteúdo de ponta a ponta.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Capacidade de Gerenciar Dimensões de Destino do Perfil** - Agora é possível excluir um Dimension de Destino do Perfil ou editar e trocar seu namespace de identidade configurado, fornecendo maior controle e flexibilidade sobre as configurações de dados. ([DOCAC-15018](https://jira.corp.adobe.com/browse/DOCAC-15018)) <!-- Documentation link: TBD -->

* **Exibir permissão de Transições de Campanha Orquestradas** - Adicionada uma nova permissão **Exibir Transições de Campanha Orquestradas** para substituir a opção herdada **Exibir Arquivo em Campanhas Orquestradas**. Essa alteração permite ocultar os resultados de visualização nas transições da campanha para oferecer suporte à conformidade com informações de identificação pessoal. ([DOCAC-14924](https://jira.corp.adobe.com/browse/DOCAC-14924)) <!-- Documentation link: TBD -->

* **Suporte para Linha** - Agora é possível adicionar ações LINE diretamente nas campanhas Orquestradas. Essa nova atividade permite criar e fornecer conteúdo altamente personalizado, incluindo texto, adesivos, imagens, vídeos, dados de localização e mensagens avançadas do Flex, para envolver seus clientes perfeitamente na plataforma LINE. Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe. ([DOCAC-14905](https://jira.corp.adobe.com/browse/DOCAC-14905)) <!-- Documentation link: TBD -->

* **Novas APIs públicas de campanhas orquestradas** - Novas especificações de API agora estão disponíveis para campanhas orquestradas. Essas APIs permitem criar, gerenciar e acionar campanhas orquestradas de forma programática, permitindo uma integração mais profunda com sistemas externos e pipelines de automação. ([DOCAC-14308](https://jira.corp.adobe.com/browse/DOCAC-14308)) <!-- Documentation link: TBD -->

* **Personalizar detalhes do remetente de email por destinatário e campanha** - As campanhas orquestradas agora oferecem suporte à personalização de campos de cabeçalho de email, incluindo Nome do remetente, Endereço do remetente e Responder para, usando atributos de perfil ou dados relacionais. Isso permite que os detalhes do remetente reflitam o consultor, o local ou a filial relevante para cada destinatário, em vez de encaminhar todos os envios por meio de um único endereço corporativo. Os valores do cabeçalho podem ser definidos no nível do canal e substituídos por campanha usando dados contextuais para obter um controle mais preciso. ([DOCAC-13761](https://jira.corp.adobe.com/browse/DOCAC-13761)) <!-- Documentation link: TBD -->

* **Simplificação da dimensão de público alvo em campanhas orquestradas** - A dimensão de direcionamento ativa agora é mostrada na tela do fluxo de trabalho, para que você possa ver qual dimensão é usada por uma atividade de canal. O fluxo de segmentação de várias entidades é mais simples, pois você não precisa mais de uma atividade &quot;Alterar dimensão&quot; separada. Além disso, agora você pode escolher explicitamente se as mensagens são enviadas no nível do perfil ou em um nível de dimensão secundário. ([DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554)) <!-- Documentation link: TBD -->

### Campanhas {#july-26-campaigns}

Os recursos e melhorias a seguir foram adicionados às campanhas nesta versão.

<table>
<thead>
<tr>
<th><strong>Anexo personalizado do PDF para mensagens transacionais em campanhas acionadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível anexar até cinco PDFs dinâmicos e personalizados por email em campanhas transacionais acionadas por API transmitindo os locais de arquivo na carga da API. Isso permite que setores como a aviação enviem cartões de embarque ou confirmações de viagem, serviços financeiros para entregar faturas ou demonstrativos individualizados e varejo para incluir recibos de pedidos ou rótulos de devolução — cada documento personalizado para o destinatário no momento do envio.</p>
<p>Anexos personalizados e estáticos do PDF compartilham a mesma cota; exceder o limite de uso aceitável exige o complemento de anexo do PDF. Este recurso não está disponível em campanhas de jornada ou ação.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Pastas para Campanhas** - Agora você pode organizar suas campanhas em pastas para melhorar a navegação e o gerenciamento na interface. ([DOCAC-15098](https://jira.corp.adobe.com/browse/DOCAC-15098)) <!-- Documentation link: TBD -->

* **Substituir o campo de execução padrão em campanhas**: agora é possível substituir o campo de execução padrão definido globalmente para suas entregas de email, SMS e WhatsApp nos parâmetros da campanha, possibilidade que antes estava disponível no nível de jornada. ([DOCAC-14718](https://jira.corp.adobe.com/browse/DOCAC-14718)) <!-- Documentation link: TBD -->

* **Pontuação de alinhamento da marca no painel do Campaign**: agora é possível avaliar a pontuação de alinhamento da marca diretamente no painel do Campaign para garantir que o conteúdo permaneça consistente com a marca. Isso permite verificar as diretrizes rapidamente sem precisar abrir o designer de conteúdo. ([DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)) <!-- Documentation link: TBD -->

### Tomada de decisão {#july-26-decisioning}

As seguintes melhorias foram adicionadas à Decisão nesta versão.

* **Criação de regras de decisão e fórmulas de classificação a partir da expressão de linguagem natural** - Agora é possível descrever a regra de decisão ou a fórmula de classificação que deseja criar em linguagem simples e permitir que o Assistente do AI a gere para você. Esse recurso está disponível para clientes com acesso aos recursos do Adobe AI. ([DOCAC-15231](https://jira.corp.adobe.com/browse/DOCAC-15231)) <!-- Documentation link: TBD -->

* **Simulação de regras de decisão e fórmulas de classificação** - Agora é possível simular suas regras de decisão e fórmulas de classificação diretamente do editor de regras ou fórmulas. Adicione variantes de teste manuais ou gere-as usando IA e, em seguida, execute a expressão com base nos dados de teste para validar a qualificação e revisar os resultados classificados, tudo antes de implantar na produção. A geração de variantes está disponível para clientes com acesso aos recursos do Adobe AI. ([DOCAC-15227](https://jira.corp.adobe.com/browse/DOCAC-15227)) <!-- Documentation link: TBD -->

* **Atributos de oferta dinâmicos** - Os atributos personalizados do item de decisão agora podem ser personalizados no momento da entrega usando dados de perfil, contextuais e de público-alvo. Isso elimina a necessidade de manter ofertas duplicadas para pequenas variações de conteúdo, permitindo que os profissionais de marketing gerenciem menos itens de decisão e mais flexíveis. ([DOCAC-14899](https://jira.corp.adobe.com/browse/DOCAC-14899)) <!-- Documentation link: TBD -->

### Gerenciamento de conteúdo {#july-26-content}

As seguintes melhorias foram adicionadas ao gerenciamento de conteúdo nesta versão.

* **Suporte a fragmentos de expressão em `<head>` de modelos de email** - Os fragmentos de expressão agora podem ser usados no `<head>` de modelos de email. Isso permite centralizar o estilo ou qualquer código personalizado em um único fragmento e reutilizá-lo em vários modelos. Quando um fragmento é atualizado e republicado, todos os emails criados a partir de modelos que fazem referência a ele herdam automaticamente o código mais recente, eliminando a necessidade de atualizar manualmente cada email individualmente. ([DOCAC-15257](https://jira.corp.adobe.com/browse/DOCAC-15257)) <!-- Documentation link: TBD -->

* **&quot;Assistente de IA&quot; renomeado para &quot;Gerar conteúdo&quot;** - O Assistente de IA foi renomeado para Gerar conteúdo em toda a Adobe Journey Optimizer. Esta atualização está limitada à nomenclatura e terminologia; nenhuma alteração funcional foi introduzida. Rótulos de navegação, botões, menus e caixas de diálogo para geração de conteúdo, geração de imagem, expressões de personalização e experimentação de conteúdo foram renomeados de &quot;Assistente de IA&quot; para &quot;Gerar conteúdo&quot;. ([DOCAC-15230](https://jira.corp.adobe.com/browse/DOCAC-15230)) <!-- Documentation link: TBD -->

* **Origem flexível de imagens para a geração de conteúdo de IA** - A geração de conteúdo no Journey Optimizer agora origina imagens aprovadas pela marca diretamente do Adobe Experience Manager Assets Essentials e superior. Três modos controlam o equilíbrio: Assets (Gerenciamento de ativos digitais-fonte, padrão), Balanceado (Gerenciamento de ativos digitais-primeiro, IA preenche lacunas) e Creative (AI-primeiro). Isso garante que cada visual seja preciso, compatível com a marca e pronto para produção para jornadas e campanhas. ([DOCAC-14761](https://jira.corp.adobe.com/browse/DOCAC-14761)) <!-- Documentation link: TBD -->

### Canal de email {#july-26-email}

Os recursos a seguir foram adicionados ao canal de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Módulos no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Designer de email agora inclui uma biblioteca de módulos de layout prontos para uso — como cabeçalhos, cartões de produto, blocos de informações e rodapés — que você pode arrastar e soltar diretamente na tela do email. Cada módulo vem pré-configurado com propriedades editáveis (imagem, título, texto, botão, links) e pode ser totalmente personalizado por meio da interface WYSIWYG, acelerando a criação de emails sem exigir a construção de estruturas do zero.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14877">DOCAC-14877</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Personalização {#july-26-personalization}

As seguintes melhorias foram adicionadas à personalização nesta versão.

* **Gerenciar domínios para personalização completa/básica da URL** - Agora é possível criar e gerenciar domínios aprovados para personalização completa e básica da URL diretamente das configurações de Administração no Adobe Journey Optimizer, sem precisar entrar em contato com o Suporte da Adobe. ([DOCAC-15187](https://jira.corp.adobe.com/browse/DOCAC-15187)) <!-- Documentation link: TBD -->

* **Novas funções auxiliares em expressões de personalização** - Novas funções auxiliares agora estão disponíveis em expressões de personalização:

  * `appendQueryParams`: anexa um parâmetro de consulta a uma URL ou a substitui se a chave já existir.
  * `dateBetween`: Verifica se uma data está dentro de um intervalo de datas inicial e final (inclusive).
  * `equalsAnyIgnoreCase`: retorna verdadeiro quando uma cadeia de caracteres corresponde a qualquer valor fornecido, ignorando maiúsculas e minúsculas.
  * `getUrlFragment`: Extrai a parte do fragmento de uma URL (a parte após #).
  * `join`: Concatena elementos de matriz em uma única cadeia de caracteres usando um separador.
  * `decode64`: Decodifica uma cadeia de caracteres codificada em Base64. Se a entrada não for Base64 válida, a cadeia de caracteres de entrada original será retornada inalterada.

  A função `concat` também foi aprimorada e agora dá suporte a dois ou mais argumentos.

  Além disso, as seguintes Funções de migração de modelo agora estão disponíveis para ajudar na migração de modelos existentes para o Journey Optimizer:

  * `ampCompare`: compara dois valores usando o operador de comparação especificado.
  * `ampSubstr`: retorna uma parte de uma cadeia de caracteres entre os índices de início e término especificados.
  * `compareTo`: compara duas cadeias de caracteres lexicograficamente.

  ([DOCAC-15099](https://jira.corp.adobe.com/browse/DOCAC-15099)) <!-- Documentation link: TBD -->

### Canais {#july-26-channels}

Os seguintes recursos e melhorias foram adicionados aos canais nesta versão.

<table>
<thead>
<tr>
<th><strong>Canal de saída personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora apresenta os Canais personalizados, um novo recurso que permite aos administradores trazer qualquer canal de mensagens baseado em HTTP de saída — como WeChat, Kakao Talk, Messenger ou um provedor proprietário — diretamente para o Journey Optimizer por meio de um Construtor de canal sem código. Depois de configurados, os canais personalizados ficam disponíveis em Campanhas, Jornadas e Campanhas orquestradas, com o mesmo conjunto completo de recursos dos canais nativos: personalização com o editor de expressão, experimentação de conteúdo, pré-visualização e prova, relatórios prontos para uso e aplicação de consentimento e governança. Isso preenche a lacuna anteriormente abordada pelas Ações personalizadas, que estavam limitadas a Jornadas e não tinham criação de conteúdo dedicado.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-11381">DOCAC-11381</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canal do WhatsApp: suporte a modelos de fluxo do WhatsApp** - Agora você pode enviar modelos de fluxo do WhatsApp no Adobe Journey Optimizer para fornecer experiências interativas em várias telas, como pesquisas e captura de leads. As respostas são capturadas no envio e armazenadas como cargas JSON brutas no novo conjunto de dados de evento de rastreamento de canal do Journey Optimizer. ([DOCAC-15223](https://jira.corp.adobe.com/browse/DOCAC-15223)) <!-- Documentation link: TBD -->

* **Complemento de desempenho para taxa de transferência - Push** - Um novo modo de mensagens transacionais de alta taxa de transferência está disponível em campanhas acionadas por API. Esse modo é projetado para mensagens transacionais em tempo real de grande escala e aceita até 5.000 transações por segundo com maior disponibilidade. Anteriormente disponível apenas para o canal de email, esse recurso agora também está disponível para o canal de push, para organizações que compraram a oferta complementar de Mensagens transacionais de alta capacidade da Adobe. Entre em contato com o representante da Adobe para obter mais informações. ([DOCAC-14717](https://jira.corp.adobe.com/browse/DOCAC-14717)) <!-- Documentation link: TBD -->

### Administração {#july-26-administration}

Os recursos a seguir foram adicionados à administração nesta versão.

<table>
<thead>
<tr>
<th><strong>Lista de permissões de IP do Firewall do Aplicativo Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora oferece suporte à lista de permissões de IP do Web Application Firewall para páginas de aterrissagem, permitindo que as organizações façam com que todas as solicitações recebidas sejam roteadas exclusivamente por meio de sua infraestrutura configurada do Web Application Firewall. Com esse aprimoramento, os clientes podem configurar o Journey Optimizer para rejeitar qualquer solicitação direta que ignore a camada do Web Application Firewall, garantindo que as políticas de segurança definidas em ferramentas como o Imperva sejam aplicadas consistentemente.</p>
<p>Esse recurso fortalece a postura de segurança para empresas com requisitos rigorosos de acesso à rede, dando a elas controle total sobre o fluxo de tráfego para as páginas de aterrissagem hospedadas pela Journey Optimizer.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">DOCAC-14814</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>
