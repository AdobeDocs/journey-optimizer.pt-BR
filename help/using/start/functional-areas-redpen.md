---
solution: Journey Optimizer
product: journey optimizer
title: Áreas Funcionais
description: Áreas funcionais no AJO
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: c9b02ae2-e07b-41f4-90cc-b2c0966f1ed1
hide: true
source-git-commit: 72ff06a7d87d6d9e5bfc0c6462ea4d60a98fc940
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Conceitos principais

O Adobe Journey Optimizer (AJO) inclui várias áreas funcionais principais que funcionam em conjunto de maneira contínua. Este guia explica cada área e descreve como essas áreas se combinam para criar experiências de cliente impactantes. Compreender essas áreas funcionais garante que você possa aproveitar o AJO para fornecer experiências personalizadas e omnicanais com eficiência.

## Visão Geral das Áreas Funcionais

| Área funcional | Benefício principal | Analogia |
|-------------------------|--------------------------------------------------|------------------------|
| Gerenciamento de dados | Organize os dados certos do cliente | A Fundação |
| Gerenciamento de clientes | Entenda quem são seus clientes | Conhecer seu público-alvo |
| Gerenciamento de conteúdo | Criar e gerenciar mensagens consistentes e personalizadas | Elabore sua mensagem |
| Gestão de decisões | Selecionar a melhor mensagem/oferta em tempo real | O Cérebro |
| Gerenciamento de jornada | Projete e automatize experiências perfeitas do cliente | Orquestra Condutora |
| Conexões | Conectar fontes de dados e entregar via canais do cliente | As tubulações |
| Administração e privacidade | Controlar a configuração, acessar e garantir a conformidade dos dados | O manual |

## Áreas funcionais detalhadas

### Gerenciamento de dados: a base

**Propósito**: assimilar, estruturar e gerenciar os dados que possibilitam a personalização. Esse processo inclui a definição de estruturas de dados (esquemas), a criação de containers de armazenamento (conjuntos de dados) e a importação de dados de vários sistemas.

Trate o gerenciamento de dados como a base para todo o envolvimento do cliente. Uma base de dados bem estruturada garante que cada decisão, mensagem e jornada use informações precisas e organizadas.

**Componentes-chave**:
- **Criação e gerenciamento de esquema**: defina a estrutura dos dados do cliente.
   - Exemplo: crie um esquema descrevendo campos como &quot;Nome,&quot; &quot;Endereço de email&quot; e &quot;Histórico de compras&quot;.
- **Configuração do conjunto de dados**: organize os dados em contêineres lógicos.
   - Exemplo: agrupe os dados da transação em um conjunto de dados de &quot;Transações de vendas&quot; para facilitar a análise.
- **Fluxos de trabalho de assimilação de dados**: importe dados para a plataforma com eficiência.
   - Exemplo: use Conectores pré-criados do Source para importar dados do cliente de um sistema de CRM (relacionamento com o cliente).
- **Ferramentas de qualidade de dados**: mantenha a precisão e a integridade dos dados.

**Benefício**: garante que os dados do cliente sejam confiáveis, organizados e acessíveis, formando a base para todas as atividades do AJO. Os conectores pré-criados da Source otimizam a assimilação de dados de plataformas comuns.



### Gerenciamento de clientes: conheça seu público-alvo

**Propósito**: criar e manter uma compreensão profunda de cada cliente. Isso envolve o uso do Perfil do cliente em tempo real da Adobe Experience Platform (AEP) para mesclar dados de todos os pontos de contato em uma visualização unificada. Ele também gerencia identidades em dispositivos e canais, permitindo o agrupamento de indivíduos em públicos direcionáveis com base em atributos ou comportamentos compartilhados.

As ferramentas de gerenciamento de clientes conectam pontos de dados distintos para fornecer uma imagem coesa de cada cliente. Essa compreensão garante que você possa fornecer experiências relevantes e personalizadas.

**Componentes-chave**:
- **Perfil de cliente em tempo real**: visualização unificada de cada cliente.
   - Exemplo: combine o histórico de navegação na Web, as interações do aplicativo e as compras offline em um único perfil.
- **Resolução de identidade**: vincular dados do cliente entre dispositivos e canais.
   - Exemplo: corresponda o endereço de email de um cliente com os dados de uso do aplicativo usando o Gráfico de identidade.
- **Criação e gerenciamento de público-alvo**: defina grupos com base em atributos e comportamentos.
   - Exemplo: crie um público-alvo para &quot;Clientes fiéis&quot; que fizeram mais de cinco compras no ano passado.
- **Segmentação**: aplique regras para associação de público-alvo dinâmico.
   - Exemplo: configure um segmento para &quot;Compradores de alto valor&quot; que é atualizado automaticamente quando os clientes gastam mais de US$ 500.

**Benefício**: permite o direcionamento e a personalização precisos por meio de uma compreensão dinâmica de preferências individuais, histórico e associações de segmento.



### Gestão de conteúdo: Elabore sua mensagem

**Propósito**: criar, gerenciar, personalizar e reutilizar conteúdo de marketing em vários canais. Isso inclui gerenciar ativos digitais, criar mensagens com editores visuais ou código, aproveitar modelos e fragmentos de conteúdo reutilizáveis, criar páginas de aterrissagem e usar inteligência artificial (AI) para gerar conteúdo.

As ferramentas de gerenciamento de conteúdo garantem que as equipes criem e entreguem mensagens personalizadas com eficiência, mantendo a consistência e a relevância em cada ponto de contato.

**Componentes-chave**:
- **Editores de conteúdo**: criar e formatar mensagens visualmente ou com código.
   - Exemplo: use o editor visual para criar uma campanha de email promovendo vendas de feriados.
- **Gerenciamento de ativos digitais**: organize e use imagens e outras mídias.
   - Exemplo: armazene imagens de produtos em uma biblioteca centralizada para fácil reutilização em campanhas.
- **Modelos e fragmentos**: criar componentes de conteúdo reutilizáveis.
   - Exemplo: criar um modelo de &quot;Mensagem de boas-vindas&quot; que insere dinamicamente nomes de clientes.
- **Ferramentas do Personalization**: personalize conteúdo dinamicamente para indivíduos.
   - Exemplo: mostrar recomendações de produto personalizadas com base no histórico de navegação.
- **Construtor de página de aterrissagem**: crie destinos da Web para campanhas.

**Benefício**: simplifica a criação de conteúdo, garante a consistência da marca e facilita a entrega eficiente de mensagens altamente personalizadas.



### Gestão de decisões: os cérebros do Personalization

**Propósito**: selecione a melhor mensagem ou oferta para cada cliente no momento certo, com base em seu perfil em tempo real, contexto e regras de negócios ou modelos de IA predefinidos. A Gestão de decisões envolve gerenciar uma biblioteca central de ofertas, definir regras de elegibilidade, aplicar restrições (como limite de frequência) e estabelecer lógica de classificação.

O Gerenciamento de decisões garante que a personalização opere em escala, fornecendo valor máximo por meio da automação inteligente.

**Componentes-chave**:
- **Biblioteca de ofertas**: repositório central de ofertas de marketing.
   - Exemplo: armazenar ofertas como &quot;Cupom com 20% de desconto&quot; ou &quot;Envio gratuito&quot; em uma biblioteca compartilhada.
- **Regras de decisão**: lógica para selecionar o conteúdo ideal.
   - Exemplo: mostre um &quot;Desconto de fidelidade&quot; somente para clientes no segmento &quot;Clientes fiéis&quot;.
- **Restrições e qualificação**: controlar quem recebe o que e quando.
   - Exemplo: aplique o limite de frequência para impedir que um cliente receba a mesma oferta duas vezes em uma semana.
- **Estratégias de classificação**: priorize ofertas com base em metas comerciais ou AI.
   - Exemplo: Classifique as ofertas por lucratividade, mostrando primeiro os produtos com altas margens.
- **Ferramentas de simulação**: testar e validar estratégias de decisão.

**Benefício**: automatiza e otimiza a personalização, garantindo que experiências relevantes e de impacto sejam entregues em todos os pontos de contato.



### Gerenciamento de jornadas: O Maestro da Orquestra

**Propósito**: projetar, organizar e automatizar as experiências do cliente em várias etapas e canais. As jornadas reagem aos comportamentos e eventos do cliente em tempo real, guiando os indivíduos por caminhos personalizados. O AJO também oferece suporte a Campanhas para enviar mensagens programadas e únicas a públicos específicos.

O Gerenciamento de jornadas garante que as experiências se sintam adaptáveis e perfeitas, orientando os indivíduos com base em suas preferências e ações.

**Componentes-chave**:
- **Designer de Jornadas**: tela visual para criar caminhos de clientes.
   - Exemplo: crie uma jornada que envia um email de boas-vindas quando um cliente se inscreve.
- **Acionadores de Jornada**: eventos que iniciam ou avançam jornadas.
   - Exemplo: acione um SMS de acompanhamento depois que um cliente abandonar o carrinho.
- **Etapas de condição**: usar ramificação baseada em lógica.
   - Exemplo: enviar uma mensagem diferente dependendo se um cliente abrir um email.
- **Atividades de espera**: controlar a progressão com atrasos de tempo.
   - Exemplo: aguarde três dias antes de enviar um email de lembrete.
- **Gerenciamento de campanha**: ferramentas para mensagens agendadas, únicas.

**Benefício**: cria experiências integradas e conectadas que se adaptam a interações individuais, estimulando relacionamentos e gerando resultados desejados.



### Conexões: Os Pipes

**Propósito**: gerenciar o fluxo de dados na AJO (Fontes) e a entrega de mensagens ou dados da AJO (Canais e Destinos). As fontes trazem dados para a Adobe Experience Platform (AEP). Os canais entregam mensagens (por email, SMS, push, Web etc.). Os destinos permitem que as informações do público-alvo ou conjunto de dados fluam para plataformas externas.

As conexões garantem que os dados entrem no AJO de maneira eficaz e cheguem aos clientes de maneira confiável por meio dos pontos de contato certos.

**Componentes-chave**:
- **Conectores do Source**: importar dados para a plataforma.
   - Exemplo: use um conector para trazer dados de compra de uma plataforma de comércio eletrônico.
- **Configuração de canal**: configurar e gerenciar mecanismos de entrega.
   - Exemplo: configurar o delivery de SMS para mensagens promocionais.
- **Configuração de destino**: conectar a sistemas de ativação externos.
   - Exemplo: compartilhar dados de público-alvo com uma plataforma de publicidade de redes sociais.
- **Gerenciamento do fluxo de dados**: controlar movimentação de informações.

**Benefício**: garante a assimilação eficiente de dados e a entrega confiável de mensagens entre canais, permitindo a ativação em sistemas externos.



### Administração e privacidade: o manual de regras

**Propósito**: definir configurações do sistema, gerenciar permissões e acessos de usuário, configurar canais de comunicação, definir parâmetros de jornada e garantir a conformidade com políticas de governança e privacidade de dados. Isso inclui gerenciar o consentimento, aplicar regras de uso de dados e manipular solicitações de acesso ou exclusão de dados.

As ferramentas de administração e privacidade garantem que a integridade dos dados seja protegida e que todas as políticas legais e organizacionais sejam seguidas.

**Componentes-chave**:
- **Gerenciamento de usuários e de acesso**: controlar acesso e permissões.
   - Exemplo: atribuir permissões específicas a equipes de marketing e TI.
- **Configuração de sandbox**: ambientes separados para desenvolvimento e teste.
   - Exemplo: use uma sandbox para testar novos designs de jornada antes de implantá-los em tempo real.
- **Configuração do canal**: definir configurações técnicas para entrega.
   - Exemplo: configurar detalhes do servidor de email para mensagens de campanha.
- **Ferramentas de privacidade**: gerenciar preferências de consentimento e privacidade.
   - Exemplo: lide com solicitações do GDPR (Regulamento Geral sobre a Proteção de Dados) para excluir dados com eficiência.
- **Controles de governança**: impor políticas de uso de dados.

**Benefício**: garante a operação segura da plataforma, a conformidade com as regulamentações e o alinhamento com as políticas organizacionais.



## Conectando os pontos: como tudo funciona em conjunto

Essas áreas funcionais operam em um ciclo contínuo para fornecer e otimizar experiências personalizadas do cliente:

1. **Assimilação de dados**: os dados fluem para o AEP, estruturados pelo Gerenciamento de dados.
2. **Compreensão do cliente**: os perfis de clientes em tempo real unificam esses dados, enquanto o gerenciamento de clientes refina os insights por meio de perfis e públicos.
3. **Estratégia de conteúdo e oferta**: o gerenciamento de conteúdo cria mensagens e ativos. A Gestão de decisões define as ofertas e a lógica para selecionar a melhor.
4. **Orquestração**: o Gerenciamento de Jornadas mapeia interações entre canais, aproveitando a compreensão, o conteúdo e as decisões do cliente.
5. **Entrega**: as conexões facilitam a entrega de mensagens por meio de canais escolhidos ou o compartilhamento de dados com sistemas externos.
6. **Medição e otimização**: os dados de desempenho e as interações com o cliente alimentam os insights de volta para o sistema para refinar públicos, conteúdo, decisões e jornadas.
7. **Governança**: os controles de administração e privacidade garantem a conformidade e a configuração adequada do sistema.

Esse processo iterativo permite que as organizações aprendam e melhorem continuamente suas estratégias de engajamento com o cliente.
