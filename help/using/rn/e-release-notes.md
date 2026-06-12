---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 02ce60020012083981c5599789b9e86804190627
workflow-type: tm+mt
source-wordcount: 1921
ht-degree: 5%

---


# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer oferece continuamente novos recursos, melhorias nos recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

## Notas de pré-lançamento de 26 de junho {#june-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas podem ser lançadas posteriormente — consulte a Data de disponibilidade listada para cada entrada para obter detalhes.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 16 a 17 de junho de 2026

### Jornadas {#june-26-journeys}

Os seguintes recursos e melhorias estão chegando às jornadas nesta versão.

* **Limite de jornadas ao vivo aumentado e novas medidas de proteção** - Agora você pode ter até **200 jornadas ativas**, maior que o limite anterior de 100.

* **Datas de início e término no cabeçalho da jornada** - Quando as datas de início e/ou término são configuradas em uma jornada em tempo real, elas agora são exibidas no **cabeçalho da jornada** ao lado da notificação de status em tempo real. O rótulo exibido se adapta com base no fato de cada data ser futura ou já ter passado.

* **Parar ou fechar uma jornada pausada diretamente** - Agora você pode **parar uma jornada ou fechá-la em novas entradas** diretamente do estado **Pausado**. Anteriormente, uma jornada pausada tinha que ser retomada para Ativa antes de ser interrompida ou fechada.

### Campanhas orquestradas {#june-26-oc}

Os seguintes recursos e melhorias estão chegando às campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>Segmentação baseada em arquivo em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As campanhas orquestradas agora permitem carregar um <strong>arquivo CSV ou TXT</strong> diretamente na tela da campanha como público alvo, sem primeiro assimilar o arquivo na Adobe Experience Platform. Os dados do arquivo são consumidos no tempo de execução e não são mantidos como um conjunto de dados do Adobe Experience Platform. Durante a configuração do arquivo, você pode definir mapeamentos de coluna, tipos de dados, tratamento NULL e políticas de erro por coluna. As linhas que falharem na validação são rejeitadas e registradas antes da execução da campanha, mantendo o público-alvo limpo sem pré-processamento manual. Isso é particularmente adequado para envios ad hoc ou campanhas de lista de parceiros em que a criação de um pipeline de assimilação completo não é prática.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
</td>
</tr>
</tbody>
</table>

* **Personalização baseada em loop para dados relacionais em campanhas orquestradas** - O editor de personalização agora oferece suporte a um **Bloco de loop** que repete coleções relacionais, como pedidos, contas ou reservas, e renderiza um bloco de conteúdo por registro em um único email ou SMS. As coleções são configuradas por meio do seletor de dados usando tokens de personalização, sem a necessidade de gravação de expressão. Você pode visualizar como os blocos em loop são renderizados em relação aos dados de amostra antes da campanha entrar em funcionamento, incluindo o tratamento de coleções vazias.

* **Personalizar detalhes do remetente de email por destinatário e campanha** - As campanhas orquestradas agora oferecem suporte à personalização de **campos de cabeçalho de email**, incluindo Do nome, Do endereço e Responder para, usando atributos de perfil ou dados relacionais. Isso permite que os detalhes do remetente reflitam o supervisor, o local ou a ramificação relevante para cada destinatário, em vez de rotear todos os envios por meio de um único endereço corporativo. Os valores do cabeçalho podem ser definidos no nível do canal e substituídos por campanha usando dados contextuais para obter um controle mais preciso.

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

### Tomada de decisão {#june-26-decisioning}

O recurso a seguir está chegando à Decisão nesta versão.

<table>
<thead>
<tr>
<th><strong>Aproveitar o fragmento de conteúdo do Adobe Experience Manager na Decisão</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode mapear <strong>fragmentos de conteúdo do Adobe Experience Manager</strong> para <strong>itens de decisão</strong> na Decisão e aproveitá-los nas políticas de decisão para fornecer o fragmento certo ao cliente certo na hora certa.</p>
<p>Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
</td>
</tr>
</tbody>
</table>

* **Atributos de oferta dinâmicos** - Os atributos de oferta no Decisioning agora podem ser personalizados no momento da entrega usando dados de perfil, contextuais e de público-alvo. Isso elimina a necessidade de manter ofertas duplicadas para variações de conteúdo secundárias, permitindo que os profissionais de marketing gerenciem um número menor de itens de decisão e mais flexíveis.

* **Limite de frequência no nível de posicionamento na Decisão** - As regras de limite de frequência na Decisão agora podem ser segmentadas para posicionamentos individuais, fornecendo controle mais fino sobre a frequência com que uma oferta é exibida em determinada superfície. Dois modos estão disponíveis:

   * Limite específico de posicionamento: defina um limite que se aplique somente quando a oferta for exibida em um posicionamento selecionado.
   * Limite por posicionamento: aplique um limite de maneira independente em cada posicionamento em que a oferta é exibida, para que cada posicionamento mantenha seu próprio contador de limite.

### Email {#june-26-email}

Os seguintes recursos e melhorias estão chegando ao canal de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Verificações de qualidade de conteúdo no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora inclui pontuação de qualidade de conteúdo diretamente no Designer de email, que analisa seu email em três dimensões antes do lançamento: ortografia, gramática e pontuação; legibilidade e tom, incluindo sinalizadores para frases longas, voz passiva e jargão; e eficácia da linha de assunto e do CTA, pontuada para maior clareza, urgência e estrutura. Cada verificação exibe sugestões acionáveis, permitindo que as equipes capturem e resolvam problemas sem sair da interface de criação.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Habilitar redução de tamanho de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora inclui uma opção para reduzir o tamanho do HTML do seu email removendo espaços em branco, comentários e códigos redundantes desnecessários — sem afetar a forma como o email é renderizado. Isso pode melhorar a capacidade de delivery, evitando limites de tamanho que alguns provedores de email usam para sinalizar ou rejeitar mensagens e pode reduzir o tempo de carregamento dos recipients.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rich text em campos editáveis para fragmentos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar rich text a fragmentos personalizáveis usados no conteúdo de emails. Por exemplo, ao usar o componente de Texto como um campo editável no Designer de email, você pode formatar o conteúdo diretamente (por exemplo, negrito e itálico) e inserir hiperlinks.</p>
</td>
</tr>
</tbody>
</table>

* **Conversor de Imagem para HTML aprimorado** - Uma nova versão do recurso de conversão de Imagem para HTML está disponível, trazendo mais precisão para a geração de HTML. Essa atualização aproveita modelos LLM de camada mais alta para fornecer saída de HTML mais precisa e confiável a partir de entradas de imagem.

+++ Em breve — **As informações abaixo estão sujeitas a alterações**

<table>
<thead>
<tr>
<th><strong>Módulos no Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Designer de email agora inclui uma biblioteca de módulos de layout prontos para uso — como cabeçalhos, cartões de produto, blocos de informações e rodapés — que você pode arrastar e soltar diretamente na tela do email.</p>
<p>Cada módulo vem pré-configurado com propriedades editáveis (imagem, título, texto, botão, links) e pode ser totalmente personalizado por meio da interface do WYSIWYG, acelerando a criação de emails sem exigir a criação de estruturas do zero.</p>
<p>Data de disponibilidade: 22 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

+++

### Mensagens por dispositivo móvel (SMS, MMS, RCS e LINE) {#june-26-mobile}

As seguintes melhorias estão chegando para o sistema de mensagens móveis nesta versão.

* **Cliques únicos para relatórios de SMS** - Um novo módulo **Cliques únicos** foi introduzido nos relatórios de SMS, trazendo o mesmo nível de rastreamento de desempenho granular para o SMS que está disponível atualmente para relatórios de Email.

* **Canal LINE - Alterações de criação** - A interface do canal LINE foi atualizada com recursos avançados de criação de mensagens. Esta versão apresenta suporte para **vários formatos de mensagem**, incluindo Texto, Imagem, Imagemap, Carrossel e Flex (Editor JSON), além de visualizações de dispositivos em tempo real. Os usuários agora podem gerenciar mensagens agrupadas de até cinco mensagens ordenadas (com controles para adicionar, remover e reordenar) e aproveitar o editor de personalização integrado para mensagens dinâmicas validadas.

* **SMS - Exibir Métricas de Uso** - Para clientes que compram SMS diretamente pelo Adobe Journey Optimizer, foi introduzido um novo **painel de uso de SMS**. Agora é possível visualizar e rastrear os últimos 90 dias de métricas de envio de mensagens, categorizadas por mensagens Originadas por dispositivos móveis (MO) e Terminadas por dispositivos móveis (MT). Esses dados também estão disponíveis para download via CSV, fornecendo maior visibilidade e controle sobre o gasto com SMS.

### Conteúdo e integrações {#june-26-content}

Os seguintes recursos e melhorias estão chegando ao gerenciamento de conteúdo e integrações nesta versão.

<table>
<thead>
<tr>
<th><strong>Melhorias nos fragmentos de conteúdo do Adobe Experience Manager no Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta versão traz várias melhorias para tornar os <strong>Fragmentos de conteúdo do Adobe Experience Manager</strong> mais utilizáveis, controláveis e prontos para produção nos fluxos de trabalho de criação do Journey Optimizer:</p>
<ul>
<li>O Journey Optimizer agora é compatível com a busca de fragmentos de conteúdo de várias configurações do Adobe Experience Manager, incluindo níveis de criação, publicação e publicação autenticada.</li>
<li>Depois que um fragmento é selecionado, seu contexto é preservado em toda a mensagem, permitindo que os autores reutilizem campos de fragmento nos blocos de conteúdo sem fazer nova seleção.</li>
<li>Uma nova página dedicada de listagem de fragmentos de conteúdo foi introduzida no Journey Optimizer para melhorar o gerenciamento do ciclo de vida; os usuários podem identificar fragmentos fora de sincronia e acionar sincronizações manuais para se manterem atualizados.</li>
<li>O suporte a local e variação agora permite que os profissionais de marketing trabalhem com versões alternativas do mesmo Fragmento de conteúdo mais deliberadamente.</li>
<li>Agora você tem flexibilidade em como o Adobe Journey Optimizer acessa o conteúdo do Adobe Experience Manager. Esta versão apresenta a capacidade de <strong>alternar o repositório de origem</strong> para fragmentos de conteúdo usados em suas jornadas e campanhas.</li>
<li>Agora compatível com o <b>Managed Services</b>, você pode visualizar, acessar e usar os Fragmentos de conteúdo do Adobe Experience Manager diretamente no Journey Optimizer para personalização. Basta adicionar o URL do repositório do Adobe Experience Manager Managed Services nas definições de configuração do como uma configuração única.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do assistente de IA com o Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Assistente de IA agora busca automaticamente <b>imagens aprovadas pela marca</b> diretamente da sua Adobe Experience Manager Assets ao gerar emails, páginas da Web e notificações por push. Isso elimina a necessidade de pesquisar manualmente o Assets ou confiar em fallbacks de IA genéricos, garantindo que cada visual seja perfeitamente preciso e compatível com a marca.</p>
</td>
</tr>
</tbody>
</table>

### Campanhas {#june-26-campaigns}

O aprimoramento a seguir está chegando às campanhas nesta versão.

* **Substituir o campo de execução padrão em campanhas** - Anteriormente disponível no nível de jornada, agora você pode substituir o **campo de execução** padrão definido globalmente para suas entregas de email, SMS e WhatsApp nos parâmetros da campanha.

### Relatório {#june-26-reporting}

Os seguintes aprimoramentos estão chegando aos relatórios nesta versão.

* **Cliques estimados para relatórios de email e SMS** — Uma nova métrica **Cliques estimados** agora está disponível em Jornadas, Campanhas e Relatórios de canal para email e SMS. Essa métrica exclui o tráfego identificado de bot e de interação não humana (NHI) para fornecer uma visão mais clara do envolvimento genuíno do cliente. A métrica Clicks existente permanece disponível e continua a relatar o total de cliques.

+++ Em breve — **As informações abaixo estão sujeitas a alterações**

* **Novas métricas de clique estimadas para relatórios de email e SMS** - Para fornecer uma visão mais precisa do engajamento real do cliente, novas métricas estimadas agora estão disponíveis nos relatórios de Jornadas, Campanhas e Canais. Essas métricas ajudam a filtrar interações não humanas (NHI) e cliques de bot a partir de dados de relatórios:

   * Estimated CTR: Cliques estimados em relação ao total de deliveries.
   * CTOR estimado somente para email: Estimativa de cliques relativos a Aberturas estimadas.

  Data de disponibilidade: final de junho de 2026

+++

### Configuração {#june-26-configuration}

As seguintes melhorias estão chegando à configuração e administração nesta versão.

* **Conjunto de dados passando do modo de streaming para o modo de lote** - O Conjunto de Dados de Evento de Feedback de Mensagens do AJO está passando do modo de streaming para o **modo de assimilação em lote**. Essa alteração garante que a assimilação de dados não exceda os limites de assimilação de streaming. Se você usar esse conjunto de dados nos relatórios do Customer Journey Analytics ou executar consultas nele, espere um aumento na latência de dados de até 2 horas no futuro.

+++ Em breve — **As informações abaixo estão sujeitas a alterações**

* **Lista de permissões de IP do WAF (Firewall do Aplicativo Web)** - O Adobe Journey Optimizer agora oferece suporte à lista de permissões de IP do WAF (Firewall do Aplicativo Web) para páginas de aterrissagem, permitindo que as organizações garantam que todas as solicitações recebidas sejam roteadas exclusivamente por meio de sua infraestrutura configurada do WAF. Com esse aprimoramento, os clientes podem configurar o Journey Optimizer para rejeitar qualquer solicitação direta que ignore a camada do WAF, garantindo que as políticas de segurança definidas em ferramentas como o Imperva sejam aplicadas de forma consistente. Esse recurso fortalece a postura de segurança para empresas com requisitos rigorosos de acesso à rede, dando a elas controle total sobre o fluxo de tráfego para as páginas de aterrissagem hospedadas pela AJO.

  Data de disponibilidade: final de junho de 2026

+++

### Melhorias de usabilidade {#june-26-usability}

A seguinte melhoria de usabilidade está chegando nesta versão.

* **Pastas para Jornadas e Campanhas** - Agora você pode organizar suas jornadas e campanhas em **pastas** para melhorar a navegação e o gerenciamento na interface.
