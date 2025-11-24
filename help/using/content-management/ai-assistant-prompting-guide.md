---
solution: Journey Optimizer
product: journey optimizer
title: Guia de prompt de conteúdo do Assistente de IA
description: Saiba como criar prompts eficazes para a geração de conteúdo habilitado por IA usando a estrutura CO-STAR para criar conteúdo de marketing alinhado à marca e de alta conversão.
role: User
level: Intermediate
source-git-commit: bacfe2e04898e8417308e3f1c889214547e3ea02
workflow-type: tm+mt
source-wordcount: '2088'
ht-degree: 0%

---


# Práticas recomendadas do prompt do Assistente do AI {#ai-assistant-prompting-guide}

Este guia ajuda a estruturar suas solicitações, comunicar a intenção com clareza e garantir que a IA produza mensagens que se alinhem às diretrizes da sua marca, às necessidades do público-alvo e às metas da campanha.
Saiba como escrever prompts eficazes que permitem que o AI Assistant gere conteúdo de marketing de alta qualidade e sob marca, adaptado aos seus objetivos.

## Usar a estrutura CO-STAR {#costar-framework}

Para obter melhores resultados com o Assistente de IA, organize seus prompts usando a estrutura CO-STAR. Essa abordagem estruturada garante que a IA entenda exatamente o que você precisa.

| Componente | O que significa | Por que isso importa |
|-|-|-|
| **C - Contexto** | Histórico de sua campanha, produto ou situação | Ajuda a IA a entender o cenário geral |
| **O - Objetivo** | Sua meta de marketing específica | Orienta o que o conteúdo deve alcançar |
| **S - Estilo** | Como você deseja se comunicar | Define a abordagem |
| **T - Tom** | Estilo emocional e voz | Forma como a mensagem é exibida |
| **A - Público** | Público-alvo que você está direcionando | Garante que a mensagem repercuta com as pessoas certas |
| **R - Requisitos** | Restrições específicas ou must-haves | Define limites e elementos críticos |

## Fundamentos dos prompts de IA {#key-takeaways}


### Fazer e não fazer


<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Fazer</th>
<th>Não</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>Usar a estrutura CO-STAR para a estrutura</p>
<p>Seja explícito sobre conteúdo novo ou existente</p>
<p>Focaliza o uso do documento com uma orientação específica de extração</p>
<p>Use seleções suspensas para tom, estratégia e localidade</p>
<p>Combinar objetivos de marketing com recursos de tipo de conteúdo</p>
<p>Gerar várias variantes para teste A/B</p>
</td>
<td>
<p>Solicitar alterações estruturais, estilo ou edição de imagem em prompts</p>
<p>Mencionar tom/estratégia em prompts, se disponível em menus suspensos</p>
<p>Use objetivos vagos como "promover nosso produto"</p>
<p>Solicitar seleções de elementos condicionais</p>
<p>Esperar modificações de layout por meio de prompts</p>
</td>
</tr>
</tbody>
</table>

### Conteúdo não suportado em prompts

>[!TIP]
>
>Use o **editor de email** ou o **Adobe Express** para modificações visuais/de imagem.

Essas solicitações não são compatíveis e devem ser tratadas por meio de outras ferramentas:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>* Modificações na estrutura do email</th>
<th>* Alterações no estilo visual</th>
<th>Operações de edição de imagens</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Selecionar seções específicas para alterar</li>
<li>Exclusão ou clonagem de elementos</li>
<li>Seleções condicionais</li>
<li>Adição ou remoção de seções de layout</li>
</ul>
</td>
<td>
<ul>
<li>Formatação de texto (negrito, itálico, tamanho da fonte)</li>
<li>Modificações de cores</li>
<li>Estilo de layout (bordas, preenchimento, margens)</li>
<li>Efeitos visuais (sombras)</li>
</ul>
</td>
<td>
<ul>
<li>Alterações de fundo</li>
<li>Adicionar sobreposições de texto ou logotipos</li>
<li>Recorte ou redimensionamento de imagens</li>
<li>Ajustes de cor</li>
<li>Substituição de imagem</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Lista de verificação de qualidade {#quality-checklist}

Antes de gerar o conteúdo, verifique o seguinte:

&check; **Limpar objetivo**: indica claramente a ação, o produto/serviço, o valor e o contexto.

&check; **Público-alvo definido**: especifica a demografia, função ou segmento.

&check; **Alinhamento do tipo de conteúdo**: o objetivo corresponde ao canal ou formato selecionado.

&check; **Seleções suspensas configuradas**: tom, estratégia e localidade são escolhidos, não os inclua no prompt.

&check; **Foco do documento especificado**: destaca o conteúdo ou as seções a serem referenciadas.

&check; **Marca aplicada**: as diretrizes de marca adequadas estão selecionadas.

&check; **Escopo realista**: evitar solicitações de alterações de layout, estilo ou edições estruturais.

## Escreva objetivos de marketing eficazes {#marketing-objectives}

### Ser específico e orientado para ações

Ao criar objetivos de marketing, verifique se eles são claros, acionáveis e mensuráveis. Evite declarações vagas ou genéricas.

**Exemplos de bons objetivos:**

&check; &quot;Impulsionar inscrições para nossa avaliação gratuita de 30 dias do novo painel de análise alimentado por IA&quot;

&check; &quot;Gerar clientes em potencial para nosso webinário B2B sobre &quot;Redução de custos na nuvem em 40%&quot; acontecendo em 15 de março&quot;

&check; &quot;Promover nosso desconto de feriado limitado de 25% em assinaturas premium, terminando em 25 de dezembro&quot;

**Exemplos a serem evitados:**

✕ &quot;Promova nosso produto&quot; (muito vago)

✕ &quot;Fazer as pessoas comprarem coisas&quot; (valor não definido)

✕ &quot;Email sobre novos recursos&quot; (sem finalidade)

### Estruturar o objetivo

Sempre forneça contexto e a proposta de valor para que a IA possa gerar conteúdo relevante.
Use esta fórmula para ajudá-lo a escrever objetivos efetivos: **Ação + Produto/Serviço + Valor/Benefício + Urgência/Contexto**

**Exemplos de bons objetivos:**

&check; &quot;Incentive os downloads do nosso novo aplicativo móvel que ajudam os usuários a rastrear hábitos de vida sustentáveis com recomendações personalizadas e ecológicas&quot;

&check; &quot;Promover registro para nosso workshop exclusivo sobre técnicas avançadas de visualização de dados para profissionais de marketing&quot;

&check; &quot;Impulsionar a participação no nosso evento de lançamento de produto apresentando o revolucionário assistente de escrita de IA que economiza mais de 5 horas por semana&quot;

**Exemplos a serem evitados:**

✕ &quot;Anunciar novo aplicativo&quot; (proposta de valor e contexto ausentes)

✕ &quot;Fazer com que as pessoas se inscrevam no workshop&quot; (não há especificidade sobre público-alvo e benefícios)

✕ &quot;Promover evento&quot; (sem ação, valor ou urgência claros)

## Criar novo conteúdo vs. modificar conteúdo existente {#new-vs-modify}

Indique claramente se a sua solicitação envolve a geração de novo conteúdo ou a atualização de material existente. Esta distinção é importante porque orienta a IA na seleção da abordagem adequada e garante um resultado mais preciso e útil.

### Criação de novo conteúdo

Aplique esta estratégia quando estiver lançando campanhas de marketing, revelando novos produtos ou iniciando qualquer tipo de comunicação atualizada ou atualizada. Ela garante que sua mensagem comece forte e se alinhe às suas metas.

**Como avisar** ➤ Ao criar um novo conteúdo, concentre-se no seu objetivo de marketing sem fazer referência ao conteúdo existente.

>[!BEGINSHADEBOX]

**Exemplos:**

* **Avaliação do SaaS**: &quot;Inicie nosso novo software CRM para proprietários de pequenas empresas, destacando 50% de economia de tempo, qualificação de cliente potencial 90% mais rápida e oferecendo uma avaliação gratuita de 30 dias com integração personalizada&quot;
* **Anúncio de recursos**: &quot;Anuncie novos recursos de integração de API que reduzem o tempo de desenvolvimento em 60% para clientes corporativos, direcionando tomadores de decisão técnicos&quot;
* **Promoção de eventos**: &quot;Impulsione inscrições para o nosso webinário sobre &quot;Tendências de marketing digital 2024&quot;, com especialistas da Google, Meta e Adobe, enfatizando insights acionáveis e vagas limitadas (500 no máximo)&quot;

>[!ENDSHADEBOX]

### Modificação de conteúdo existente

>[!TIP]
>
>Para modificações padrão como elaborar, resumir ou simplificar, use o recurso **Refinar** em vez de escrever prompts personalizados. [Saiba mais](generative-uc.md##refine)

Aplique isso quando precisar atualizar ou adaptar suas campanhas de marketing atuais. Esse método oferece suporte a melhorias incrementais, garantindo que suas mensagens permaneçam relevantes sem iniciar do zero.

**Como avisar** ➤ Ao modificar conteúdo existente, especifique claramente o que deseja alterar e como alterá-lo.

>[!BEGINSHADEBOX]

**Exemplos:**

* **Atualização da campanha**: &quot;Modifique o email de lançamento do produto para se concentrar nos recursos de segurança da empresa em vez dos benefícios gerais de produtividade, direcionando os tomadores de decisão de TI com certificações de conformidade&quot;
* **Tabela dinâmica de público-alvo**: &quot;Adapte nosso convite de demonstração de software para direcionar especificamente a área de saúde, substituindo exemplos genéricos por casos de uso da área de saúde e benefícios de conformidade com a HIPAA&quot;
* **Atualização sazonal**: &quot;Atualize nossa campanha promocional do 3º trimestre para compras de fim de ano do 4º trimestre, mudando o foco das ofertas escolares para as ofertas de fim de ano, com ênfase no envio rápido&quot;

>[!ENDSHADEBOX]

## Aprimorar seu prompt com configurações avançadas {#personalize-prompt}

### Tipos de estratégia de comunicação

>[!TIP]
>
>Use a lista suspensa Estratégia de comunicação do menu Configurações de texto em vez de mencioná-la no prompt para processamento especializado.

A estratégia de comunicação determina como você apresenta a mensagem para maximizar o impacto. Estratégias diferentes funcionam melhor para metas diferentes, seja para criar urgência, estabelecer confiança ou promover ação imediata. Escolha a estratégia que melhor se alinha aos objetivos da campanha e à mentalidade do público-alvo.

| **Estratégia** | **Melhor Para** | **Estilo de Mensagens** | **Exemplos** |
|--------------|--------------|------------------------|--------------|
| **Urgente** | Ofertas sensíveis ao tempo, prazos e ação imediata | Cria pressão imediata com linguagem baseada no tempo | &quot;Atue agora: a oferta expira à meia-noite&quot; <br> &quot;Inscreva-se hoje mesmo antes do preenchimento de vagas&quot; <br> &quot;A venda rápida de 48 horas começa agora&quot; |
| **FOMO (Medo de ficar de fora)** | Ofertas limitadas, eventos, acesso exclusivo | Usa dicas de urgência, escassez e pressão de tempo | &quot;Só faltam 24 horas! Ação limitada com 40% de desconto&quot; <br> &quot;Última chance: o preço antecipado dos pássaros termina amanhã&quot; <br> &quot;Restam apenas 100 pontos beta&quot; |
| **Prova social** | Construção de confiança, testemunhos, produtos populares | Aproveita as experiências e a validação de outras pessoas | &quot;Junte-se a mais de 50.000 clientes satisfeitos&quot; <br> &quot;Classificados em 4,9/5 estrelas por profissionais do setor&quot; <br> &quot;Confiados por empresas da Fortune 500&quot; |
| **Escassez** | Inventário limitado, versões exclusivas, itens de alta demanda | Enfatiza disponibilidade limitada e exclusividade | &quot;Apenas 5 disponíveis no estoque&quot; <br> &quot;Edição limitada: 100 unidades disponíveis&quot; <br> &quot;Lançamento exclusivo: primeiro a chegar, primeiro a ser servido&quot; |
| **Incentivo** | Promoções, programas de recompensas, ofertas especiais | Destaca benefícios e recompensas tangíveis | &quot;Obtenha 20% de desconto em seu primeiro pedido&quot; <br> &quot;Ganhe pontos duplos neste fim de semana&quot; <br> &quot;Envio gratuito em pedidos acima de US$ 50&quot; |
| **Exclusividade** | Produtos Premium, experiências VIP, ofertas somente para membros | Usa posicionamento premium e linguagem de acesso especial | &quot;Convite exclusivo para nossa visualização privada&quot; <br> &quot;A associação Elite desbloqueia análises avançadas&quot; <br> &quot;Ingresse em algumas empresas da Fortune 500 que já nos usam&quot; |
| **Gamification** | Campanhas de engajamento, programas de fidelidade, conteúdo interativo | Usa mecânica de jogos e linguagem de realização | &quot;Desbloqueie seu próximo nível de recompensa&quot; <br> &quot;Desafios completos para ganhar medalhas&quot; <br> &quot;Suba na tabela de classificação para prêmios exclusivos&quot; |
| **Informativo** | Educação, pesquisa, produtos complexos, liderança de pensamento | Usa fatos, dados, insights e explicações | &quot;5 insights da análise de mais de 10.000 interações&quot; <br> &quot;Nova pesquisa revela 3 abordagens inovadoras&quot; <br> &quot;Guia completo para a implementação de IA em marketing&quot; |
| **Educação e Insights** | Conteúdo de aprendizado, tendências do setor, práticas recomendadas | Fornece conhecimentos valiosos e argumentos acionáveis | &quot;Domine as técnicas avançadas com nosso guia especializado&quot; <br> &quot;Descubra as 7 estratégias que os principais profissionais de marketing usam&quot; <br> &quot;Saiba como otimizar seu fluxo de trabalho em 5 etapas&quot; |

### Definir o tom correto {#tone}

>[!TIP]
>
>Use a lista suspensa Tom do menu Configurações de texto, em vez de especificá-lo no prompt.

O tom molda como o público-alvo percebe e responde à mensagem. Sempre selecione um tom que se alinhe à voz da sua marca e ao estágio da jornada do perfil.

Use a tabela abaixo para explorar cada tom em detalhes, incluindo quando funciona melhor e exemplos de conteúdo que se encaixam em cada estilo.

| Tonalidade | Melhor para | Exemplo de conteúdo |
|-|-|-|
| Profissional | Comunicações B2B, anúncios formais | &quot;Temos o prazer de anunciar nossa parceria estratégica...&quot; |
| Empático | Suporte ao cliente, tópicos confidenciais | &quot;Entendemos o quanto isso deve ser frustrante para você...&quot; |
| Humorístico | Campanhas envolventes, conteúdo alegre | &quot;Aviso: pode causar sérios ganhos de produtividade!&quot; |
| Emocionante | Lançamentos de produtos, promoções de eventos | &quot;Este é o momento pelo qual você estava esperando!&quot; |
| Inspirador | Campanhas motivacionais, finalidade da marca | &quot;Juntos, podemos fazer a diferença no mundo...&quot; |
| Persuasivo | Campanhas de vendas, conversões | &quot;Não perca essa oportunidade de tempo limitado para...&quot; |
| Amigável | Engajamento do cliente, mensagens de boas-vindas | &quot;Estamos tão felizes por você estar aqui conosco!&quot; |
| Formal | Comunicações legais, avisos oficiais | &quot;Por meio deste, notificamos você sobre as seguintes alterações...&quot; |
| Pedidos de desculpas | Recuperação de serviço, resolução de problemas | &quot;Lamentamos sinceramente qualquer inconveniente causado...&quot; |
| Assertivo | Conteúdo de liderança, mensagens autoritativas | &quot;Aqui está o que você precisa fazer agora...&quot; |
| Contar histórias | Narrativas de marca, conexões emocionais | &quot;Tudo começou com uma pergunta simples...&quot; |
| Conversação | Campanhas de incentivo, construção de relacionamentos | &quot;Vamos falar sobre como isso pode ajudá-lo...&quot; |

### Otimize os ativos da sua marca {#brand-assets}

>[!TIP]
>
>Se você já tiver carregado um ativo de marca por meio do menu **Brand Assets**, não será necessário referenciá-lo no prompt. O sistema usa automaticamente todos os documentos selecionados.

Os recursos da marca fornecem informações fatuais que enriquecem o conteúdo gerado, com detalhes específicos e precisos.
Ao fazer upload de documentos abrangentes, como folhetos de produtos, adicione ao seu prompt em quais partes focar:

* **Em vez de** _&quot;Usar o folheto de produto&quot;_ **usar** _&quot;Concentrar-se nos recursos avançados de segurança e certificações de conformidade, especificamente conformidade SOC 2 e criptografia de dados&quot;_

* **Em vez de** _&quot;Consultar os estudos de caso&quot;_ **usar** _&quot;Destacar resultados de ROI de clientes da área de saúde, especificamente a redução de 40% no Centro Médico Regional&quot;_

* **Em vez de** _&quot;Incluir detalhes técnicos&quot;_ **você deve usar** _&quot;Enfatizar os recursos de integração de API e os benefícios do desenvolvedor, concentrando-se nos pontos de extremidade da API REST e no SLA com 99,9% de tempo de atividade&quot;_

### Refinamento de conteúdo

>[!TIP]
>
>Use o recurso Refinar, em vez de solicitar, quando quiser elaborar, resumir, simplificar, alterar o tom ou traduzir o conteúdo existente. [Saiba mais](generative-uc.md#refine)

Depois que o conteúdo for gerado, use o recurso **Refinar** para iterar e aprimorar com as seguintes opções:

| **Ação** | **Caso de uso** | **Exemplo de Solicitação** |
|-|-|-|
| **Elaborar** | Adicionar profundidade e detalhes ao conteúdo resumido | &quot;Elabore os benefícios técnicos de nossos recursos de segurança&quot; |
| **Resumir** | Condensar conteúdo longo para formatos diferentes | &quot;Resuma esta visão geral do produto para uma publicação em redes sociais&quot; |
| **Simplificar** | Tornar o conteúdo complexo mais acessível | &quot;Simplifique esta explicação técnica para um público em geral&quot; |
| **Alterar Tom** | Adaptar conteúdo para públicos diferentes | &quot;Mude o tom para mais casual para o público mais jovem&quot; |
| **Transcriar** | Adaptação cultural além da tradução | &quot;Transcriar esta campanha para o mercado japonês&quot; |

## Exemplos de Prompt Baseados em Cenário

### Com base no tipo de conteúdo {#content-type-practices}

<table style="table-layout: fixed; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canal</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Email</strong></td>
<td>"Impulsionar prospetos empresariais, apresentando três histórias de sucesso de clientes com métricas detalhadas de ROI (IBM: 45% de redução de custos, Accenture: 200% de aumento de lead, Microsoft: 60% de economia de tempo), direcionando diretores de TI a empresas com mais de 1.000 funcionários"</td>
</tr>
<tr>
<td><strong>SMS</strong></td>
<td>"Alerte os clientes do VIP sobre a venda rápida de 4 horas em produtos eletrônicos premium com 40% de desconto, limitada aos primeiros 100 clientes"</td>
</tr>
<tr>
<td><strong>Notificações por push</strong></td>
<td>"Reenvolva os usuários que não abrem o aplicativo há 7 dias com recomendações de conteúdo personalizadas com base em seu histórico de leitura"</td>
</tr>
<tr>
<td><strong>Páginas de aterrissagem</strong></td>
<td>"Converta visitantes B2B em clientes potenciais qualificados demonstrando como nossa solução de segurança corporativa impede 99,9% dos ataques cibernéticos, com declarações da Fortune 500 e auditoria de segurança gratuita"</td>
</tr>
</tbody>
</table>

### Com base em abordagens específicas do setor {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Setor</th>
<th>Exemplo de prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Tecnologia B2B</strong></td>
<td>"Demonstre o ROI e as especificações técnicas enquanto lida com as preocupações de segurança para os tomadores de decisão de TI que avaliam nossa solução de infraestrutura em nuvem, enfatizando 99,9% de tempo de atividade SLA, conformidade SOC 2 e 40% de economia de custos."</td>
</tr>
<tr>
<td><strong>Varejo de comércio eletrônico</strong></td>
<td>"Crie a urgência em torno de itens de feriado de estoque limitado, destacando o frete gratuito e retornos fáceis para os compradores de última hora, enfatizando quantidades limitadas (menos de 50 restantes) e corte de frete de 24 horas."</td>
</tr>
<tr>
<td><strong>Serviços financeiros</strong></td>
<td>"Educar os clientes sobre as estratégias de diversificação do portfólio de investimentos, mantendo a conformidade normativa, com informações de consultores financeiros certificados e isenções de responsabilidade sobre riscos."</td>
</tr>
<tr>
<td><strong>Saúde e bem-estar</strong></td>
<td>"Promova os benefícios de cuidados preventivos e as triagens de saúde anuais, mantendo a precisão médica, com recomendações médicas certificadas pelo conselho e garantias de privacidade do paciente."</td>
</tr>
<tr>
<td><strong>Educação e treinamento</strong></td>
<td>"Enfatize os resultados de progressão na carreira e as certificações do setor, ao mesmo tempo em que exibe a experiência de instrutor, destacando a taxa de 92% de colocação em cargos e o currículo baseado em projetos."</td>
</tr>
<tr>
<td><strong>Plataformas SaaS</strong></td>
<td>"Destaque os benefícios de economia de tempo e automação com métricas específicas enquanto lida com preocupações de integração, apresentando economia de tempo semanal em média de 25 horas e integração com mais de 200 ferramentas populares."</td>
</tr>
</tbody>
</table>
