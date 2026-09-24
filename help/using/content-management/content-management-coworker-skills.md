---
solution: Journey Optimizer
product: journey optimizer
title: Colaborador para gerenciamento de conteúdo
description: Descubra as ferramentas de gerenciamento de conteúdo do CX Enterprise Coworker disponíveis para descobrir, criar e gerenciar ativos de conteúdo do Journey Optimizer, com orientação detalhada e prompts de amostra.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 9f23a6f5-7221-4f87-95cd-047955ca33d5
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: 6077cdb74f93fb258c60fa127397251141638c79
workflow-type: tm+mt
source-wordcount: '1842'
ht-degree: 1%
---

# Colaborador para gerenciamento de conteúdo {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**Nesta página:** descubra as ferramentas de gerenciamento de conteúdo do CX Coworker disponíveis no Adobe Journey Optimizer — para navegar, criar, atualizar, clonar e publicar modelos de conteúdo, fragmentos, páginas de aterrissagem e conteúdo integrado de jornada/campanha; para planejar a estratégia da campanha e gerar cópias e imagens da marca entre canais, localidades, públicos-alvo e variantes; e para criar, revisar e distribuir HTML de email acessível — com orientações detalhadas, exemplos de prompts e práticas recomendadas.

Saiba mais:

* [Habilidades de colega de trabalho para o Journey Optimizer](../start/ai-features.md#cx-coworker-skills) — visão geral das habilidades de colega em Jornadas, Fidelidade e Gerenciamento de Conteúdo no Journey Optimizer.
* [Documentação do colaborador](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} — visão geral dos recursos de Campanhas, Chat e Projetos do colaborador.
* [Guia da interface de Chat do Colaborador](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} — como acessar e navegar pelo Chat do Colaborador.

>[!ENDSHADEBOX]

## Ferramentas de gerenciamento de conteúdo {#content-management}

>[!AVAILABILITY]
>
>O Gerenciamento de conteúdo está disponível para todos os clientes que têm acesso ao Colaborador.

Os usuários do Journey Optimizer podem descobrir e gerenciar ativos de conteúdo — modelos de conteúdo, fragmentos, páginas de aterrissagem e conteúdo de mensagem em linha de jornada/campanha — diretamente do Colaborador usando prompts de linguagem natural. Ela permite ir de &quot;me falar sobre meu conteúdo&quot; a &quot;criar, atualizar e publicar&quot;, sem sair da conversa. Esse recurso é alimentado por 15 ferramentas de MCP com capacidade de leitura e gravação para conteúdo do Journey Optimizer.

### Principais casos de uso

1. **Procurar e inspecionar conteúdo**

   * Liste os modelos de conteúdo, fragmentos ou páginas de aterrissagem disponíveis e recupere sua estrutura, metadados e status.
   * Recupere o conteúdo da mensagem em linha configurado em um nó de ação de campanha ou do jornada.

   Exemplos de prompts:
   * &quot;Listar meus modelos de conteúdo de email.&quot;
   * &quot;Mostre-me os fragmentos disponíveis para minha campanha de verão.&quot;
   * &quot;Obtenha os detalhes da landing page-123.&quot;
   * &quot;Qual conteúdo está configurado para a variante de email do nó de ação no campaign camp-789?&quot;

1. **Criar modelos de conteúdo**

   * Crie um novo modelo de conteúdo para qualquer canal.

   Exemplos de prompts:
   * &quot;Crie um modelo de email chamado Vendas de verão com este conteúdo do HTML.&quot;
   * &quot;Crie um novo modelo de SMS chamado Alerta Flash.&quot;

1. **Atualizar modelos de conteúdo**

   * Substituir totalmente o conteúdo de um template existente.

   Exemplos de prompts:
   * &quot;Atualize o template abc-123 com este novo corpo do HTML.&quot;

1. **Criar, atualizar, clonar e publicar fragmentos**

   * Crie um novo fragmento de HTML ou expressão.
   * Atualize o conteúdo ou os metadados de um fragmento existente.
   * Clonar um fragmento existente com um novo nome.
   * Enviar um fragmento de rascunho para publicação.

   Exemplos de prompts:
   * &quot;Crie um fragmento do HTML chamado Banner promocional com esta marcação.&quot;
   * &quot;Atualize o fragmento frag-456 para alterar seu nome para Banner promocional V2.&quot;
   * &quot;Clonar fragmento abc-123 como Banner promocional - Verão (Variante B).&quot;
   * &quot;Publicar fragmento frag-456.&quot;

1. **Atualizar conteúdo da mensagem integrada**

   * Substituir uma variante de canal em uma mensagem em linha do nó de ação de campanha ou jornada.
   * Liste as variantes de canal definidas em um nó de ação de jornada ou campanha.

   Exemplos de prompts:
   * &quot;Atualize a variante de email do nó de ação no campaign camp-789 com este novo conteúdo.&quot;
   * &quot;Quais variantes de canal são definidas neste nó de ação?&quot;

### No escopo

Os seguintes recursos são compatíveis com o gerenciamento de conteúdo:

* **Listar e obter modelos de conteúdo**: procure modelos de conteúdo e recupere sua estrutura e metadados.
* **Listar e obter fragmentos**: procure fragmentos de conteúdo e expressão e recupere seus detalhes.
* **Listar e obter páginas de aterrissagem**: procure páginas de aterrissagem e recupere seus metadados e conteúdo da página.
* **Obter conteúdo embutido de campanha/jornada**: recupere o conteúdo da mensagem embutida configurado em um nó de ação de campanha ou jornada, incluindo variantes multilíngues.
* **Criar modelos de conteúdo**: crie um novo modelo para qualquer canal.
* **Atualizar modelos de conteúdo**: substituir totalmente o conteúdo de um modelo existente.
* **Criar, atualizar, clonar e publicar fragmentos**: crie novos fragmentos, atualize os existentes, clone um fragmento com um novo nome e envie um fragmento de rascunho para publicação.
* **Atualizar conteúdo da mensagem embutida**: substitua uma variante de canal em uma mensagem embutida de nó de ação de campanha/jornada, incluindo variantes multilíngues, e liste as variantes de canal definidas em um nó de ação.

### Fora do escopo

As seguintes funcionalidades não são compatíveis no momento:

* **Pesquisa de texto completo entre modelos ou fragmentos**
* **Validação de modelo ou fragmento** (referências órfãs, links corrompidos, componentes obsoletos)
* **Criando ou publicando páginas de aterrissagem**
* **Excluindo modelos de conteúdo, fragmentos ou páginas de aterrissagem**

### Solicitação de práticas recomendadas

1. **IDs de referência quando conhecidas**: forneça o modelo, fragmento, página de aterrissagem ou ID de campanha/jornada ao solicitar a obtenção, atualização, clonagem ou publicação de um ativo específico.
1. **Seja explícito sobre o canal**: ao criar um modelo ou fragmento, especifique o canal ou o tipo de conteúdo (email, fragmento de HTML, fragmento de expressão).
1. **Confirmar antes de publicar**: revise o conteúdo de um fragmento depois de criá-lo ou atualizá-lo antes de solicitar que o Co-worker o publique.
1. **Forneça o conteúdo de substituição completo**: as operações de atualização substituem o conteúdo na íntegra, portanto, inclua o conteúdo completo do corpo ou da variante do HTML no prompt.

## Conteúdo do canal {#ce-channel-content}

>[!AVAILABILITY]
>
>O Conteúdo do canal está disponível para todos os clientes com acesso ao CX Coworker. Gerar imagens com um modelo personalizado e treinado pela marca requer acesso de produção ao Firefly Services.

O Conteúdo do canal pega uma breve, jornada, campanha ou prompt e a transforma em uma cópia planejada da marca e imagens em canais, localidades, públicos-alvo e variantes, incluindo HTML de email final, acessível e montado. O conteúdo pode ser explorado e estrategicamente criado, avaliado quanto à prontidão, revisado e salvo novamente na solução ativa (Adobe Journey Optimizer ou outra solução de ativação compatível).

### Competências disponíveis

As seguintes habilidades estão disponíveis no plug-in **Conteúdo do canal**:

* **Orquestrar Criação de Conteúdo** (`orchestrate-content-authoring`)

  Executa o ciclo de vida completo da criação a partir de um resumo, jornada, campanha ou prompt, idealizando, gerando, revisando e salvando conteúdo, inclusive cópia, imagens e as verificações de conformidade, acessibilidade e fidelidade em todos os canais compatíveis.

  >[!BEGINSHADEBOX &quot;Exemplos de prompt&quot;]

  &quot;Execute a criação completa de conteúdo para nossa campanha de email de vendas de outono a partir deste resumo e, em seguida, revise e salve a HTML final.&quot;

  >[!ENDSHADEBOX]

* **Explorar a Estratégia de Conteúdo** (`explore-content-strategy`)

  Descreve o que uma campanha ou mensagem deve dizer antes que a cópia seja escrita, comparando mapas de mensagens e o sequenciamento de pontos de contato no nível da campanha e decidindo a ordem da seção, a ênfase e o CTA no nível da mensagem.

  >[!BEGINSHADEBOX &quot;Exemplos de prompt&quot;]

  * &quot;Compare um único email de winback com um programa de email e SMS com três toques.&quot;
  * &quot;Dê-me três direções de campanha para este lançamento antes de escolhermos um.&quot;
  * &quot;Ajude a decidir o que este email deve dizer e em que ordem antes de escrevermos a cópia.&quot;

  >[!ENDSHADEBOX]

* **Resumo do conteúdo** (`content-brief`)

  Transforma uma direção de campanha aprovada em requisitos de escrita concretos, incluindo tom, mensagens principais, oferta, pontos obrigatórios, canal, localidade e variantes, além de um plano para produzir o conteúdo.

  >[!BEGINSHADEBOX]

  * &quot;Transforme este resumo em requisitos de escrita para um email de winback quente para assinantes dos EUA expirados: 20% de desconto até o domingo, com o CTR como KPI.&quot;
  * &quot;Queremos promover nossa venda de primavera por e-mail e SMS para novos assinantes e membros fiéis. Estruturar os requisitos e criar um resumo de cópia completa separado para cada canal e público-alvo.&quot;
  * &quot;Capture este resumo de email de boas-vindas para os públicos-alvo de inglês e espanhol, incluindo os requisitos localizados do rodapé legal, e prepare-o para a redação da cópia, não para o design do HTML.&quot;

  >[!ENDSHADEBOX]

* **Gerar conteúdo** (`generate-content`)

  Rascunha uma única mensagem de marketing ou variante de cópia nova para um canal, com base em um público, oferta, tom, CTA e comprimento declarados. Somente criação de primeiro rascunho.

  >[!BEGINSHADEBOX]

  * &quot;Escreva três opções de linha de assunto e visualize o texto para nosso email de promoção do primeiro trimestre.&quot;
  * &quot;Gere uma cópia de SMS quente e concisa para clientes antigos com uma oferta de 20%.&quot;
  * &quot;Crie uma cópia de lançamento na marca para e-mail, push e SMS a partir da direção da campanha aprovada.&quot;

  >[!ENDSHADEBOX]

* **Verificar Preparação do Conteúdo** (`check-content-readiness`)

  Avalia o conteúdo existente, incluindo um email montado, para voz da marca, qualidade editorial, acessibilidade e conformidade e, em seguida, exibe bloqueadores explicáveis e as próximas etapas.

  >[!BEGINSHADEBOX]

  * &quot;Esta cópia do email está pronta para ser enviada? Verifique a voz da marca, a clareza, a acessibilidade e a conformidade.&quot;
  * &quot;Revise este SMS quanto a qualidade editorial, engajamento e quaisquer bloqueadores antes da aprovação.&quot;
  * &quot;Verifique se há problemas de rodapé legal, acessibilidade e disponibilidade de envio no email montado.&quot;

  >[!ENDSHADEBOX]

* **Revisar e Regenerar Conteúdo** (`revise-regenerate-content`)

  Aplica uma alteração específica e confirmada ao conteúdo existente, como corrigir uma conclusão de revisão, ajustar o tom, traduzir ou trocar uma linha de assunto ou CTA, preservando o artefato.

  >[!BEGINSHADEBOX]

  * &quot;Aplicar as correções de maior severidade deste relatório de avaliação ao SMS.&quot;
  * &quot;Deixe o tom mais quente, preservando a oferta aprovada e o CTA.&quot;
  * &quot;Altere o título principal para &#39;Horas finais a salvar&#39; e mostre-me o conteúdo revisado.&quot;

  >[!ENDSHADEBOX]

* **Gerar Imagem** (`generate-image`)

  Produz e manipula visuais para uma inserção aprovada, incluindo imagens herói, recortes, sobreposições, variações ou ativos assinados, confirmando o plano antes de aplicá-lo.

  >[!BEGINSHADEBOX]

  * &quot;Gere uma imagem principal premium para este email de venda de primavera usando a direção da marca aprovada.&quot;
  * &quot;Crie um recorte móvel amigável desta imagem do produto para o herói de email.&quot;
  * &quot;Faça duas variações visuais desta imagem de campanha.&quot;
  * &quot;Gera uma imagem semelhante à imagem fornecida.&quot;

  >[!ENDSHADEBOX]

* **Avaliar Design de Conteúdo** (`assess-content-design`)

  Avalia como o conteúdo é realmente renderizado, incluindo hierarquia, espaçamento, imagens, posicionamento do CTA e capacidade de resposta, e recomenda alterações de cópia ou imagem para fechar as lacunas.

  >[!BEGINSHADEBOX]

  * &quot;Como esse email se parece visualmente? Verifique a hierarquia, o espaçamento, a densidade, as imagens e a CTA.&quot;
  * &quot;O herói ocupa muito espaço nesta página de aterrissagem do HTML?&quot;
  * &quot;Compare esse email criado com o design aprovado e chame a atenção para as maiores incompatibilidades visuais.&quot;

  >[!ENDSHADEBOX]

* **Salvar Conteúdo Do Canal** (`save-channel-content`)

  Salva o conteúdo da campanha aprovada como um ativo de rascunho ou o preenche em seu modelo de origem no Adobe Journey Optimizer ou em outra solução compatível.

  >[!BEGINSHADEBOX]

  * &quot;Salvar esta cópia do email aprovado como rascunho da solução.&quot;
  * &quot;Preencha o conteúdo aprovado no modelo de origem e prepare-o para revisão.&quot;
  * &quot;O email é aprovado; salve o conteúdo do canal e prepare a entrega.&quot;

  >[!ENDSHADEBOX]

* **Criar email a partir do Figma** (`build-email-from-figma`)

  Cria HTML de email final diretamente de um quadro Figma ao vivo quando sua cópia, layout e imagens são o que deve ser enviado sem alterações, sem nenhum plano de layout separado envolvido.

  >[!BEGINSHADEBOX]

  * &quot;Crie o HTML de email final a partir deste quadro Figma; a cópia no design é o que deve ser enviado.&quot;
  * &quot;Transforme este desktop aprovado e o design móvel do Figma em um email responsivo.&quot;
  * &quot;Crie esse email a partir do quadro Figma e preserve exatamente os recortes de imagem, o CTA e o texto do design.&quot;

  >[!ENDSHADEBOX]

  +++Como usar esta habilidade

  1. Entre no Colaborador e vá para **[!UICONTROL Configurações]** > **[!UICONTROL Segredos]**.

     ![](assets/coworker-1.png)

  1. Em **[!UICONTROL Seus segredos]**, clique em **[!UICONTROL Adicionar]**.

  1. Em **[!UICONTROL Name]**, digite `FIGMA_ACCESS_TOKEN`.

  1. Gere um PAT (Figma Personal Access Token) com pelo menos o escopo **File content: Read-only**. [Saiba como gerar um token de acesso pessoal do Figma](https://help.figma.com/hc/en-us/articles/8085703771159-Manage-personal-access-tokens#h_01JHJXYMB9CREBR8PB5VJ1Q5ME).

  1. Cole o PAT no **[!UICONTROL Valor]** e clique em **[!UICONTROL Salvar]**.

  +++

* **Pesquisa de Marca** (`brand-lookup`)

  Localiza, soluciona e aplica as diretrizes da marca aprovada, incluindo voz, imagens e assuntos legais, antes de qualquer fluxo de trabalho que gere ou avalie conteúdo na marca.

  >[!BEGINSHADEBOX]

  * &quot;Quais kits de marca publicados estão disponíveis para esta campanha?&quot;
  * &quot;Obtenha os textos e as diretrizes visuais para nossa marca Acme.&quot;

  >[!ENDSHADEBOX]

### Solicitação de práticas recomendadas

1. **Comece com o resumo**: forneça o objetivo da campanha, o público-alvo e os canais antecipadamente para que o plano de conteúdo reflita seu escopo pretendido.
1. **Especificar dimensões do plano**: chame os canais, pontos de contato, localidades, públicos-alvo e variantes que você deseja representar no plano de conteúdo.
1. **Incluir contexto de marca**: faça referência ao kit de marca ou às diretrizes de voz para que as cópias e imagens geradas permaneçam na marca.
1. **Limites de caracteres de estado**: forneça limites de caracteres de canal explicitamente e revise a cópia gerada para confirmar se ela se encaixa antes de publicar.
1. **Solicitar todas as análises relevantes**: antes de tratar o conteúdo como pronto para envio, solicite uma análise de marca, conformidade, design e acessibilidade.
1. **Revisar antes de salvar**: avalie e edite o conteúdo gerado antes de pedir ao Colaborador para salvá-lo novamente no Adobe Journey Optimizer ou em outra solução de ativação com suporte.

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
