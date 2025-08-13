---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 667f1a2bd03c958d7d1a95c4f9fb3378417276c0
workflow-type: tm+mt
source-wordcount: '1460'
ht-degree: 96%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.


## Orquestração de campanha  

**Data de disponibilidade**: 4 de agosto de 2025

O Journey Optimizer agora inclui a **Orquestração de campanha**, um novo recurso criado especificamente para campanhas em lotes iniciadas pela marca. Esta versão apresenta uma tela de orquestração de campanhas e uma modelagem de dados aprimorada, que funcionam em conjunto para permitir que os profissionais de marketing planejem, direcionem e entreguem campanhas personalizadas entre canais.

>[!IMPORTANT]
>
>Para acessar o Campaign Orchestration, sua licença deve incluir o pacote **Journey Optimizer - Campanhas e Jornadas** ou **Journey Optimizer - Campanhas**. Entre em contato com o representante da Adobe para confirmar sua licença e atualizar, se necessário.

![GIF da orquestração de campanhas](assets/do-not-localize/release.gif)

Inclui [Esquemas e conjuntos de dados relacionais](#oc-relational) e [Tela da campanha](#oc-canvas). Juntas, essas duas inovações proporcionam um novo padrão para orquestrar campanhas em lotes no Journey Optimizer. Os principais recursos estão listados abaixo.

### Principais recursos {#oc-capabilities}

* **Fluxos de trabalho em várias etapas**

  Crie campanhas sofisticadas em lotes em vários canais com a nova tela de orquestração de campanhas.

* **Públicos-alvo sob demanda**

  Segmente públicos-alvo sob demanda para ativação imediata.

* **Segmentação de várias entidades**

  Crie públicos-alvo com base no contexto comercial (dimensões que não sejam de pessoas), como produtos, lojas, renovações, reservas e muito mais.

* **Visibilidade pré-envio**

  Revise, refine e otimize públicos-alvo e campanhas antes do lançamento e enquanto as campanhas estão em execução

### Tela da campanha {#oc-canvas}

Uma interface de orquestração visual totalmente nova, criada especificamente para campanhas em lotes. Essa tela permite:

* Planejamento visual de fluxos de campanha em várias etapas e vários canais

* Compatibilidade com públicos-alvo sob demanda criados a partir de consultas relacionais

* Divisão avançada de públicos-alvo, esperas e lógica condicional

* Contagens precisas pré-envio após a aplicação de regras de negócios e filtros

### Esquemas e conjuntos de dados relacionais {#oc-relational}

O Adobe Journey Optimizer agora é compatível com entidades relacionais (por exemplo, produtos, lojas, reservas, contratos) vinculadas a perfis com base em pessoas. Isso permite a segmentação e a personalização em estruturas de dados multidimensionais, permitindo casos de uso como:

* Uma mensagem por reserva, assinatura ou contrato

* Segmentação baseada em atributos da entidade relacionada (por exemplo, categoria do produto ou localização da loja)

* Capacidade de endereçamento aprimorada (por exemplo, enviar a todos os contatos conhecidos vinculados a uma entidade)

### Por que isso importa

Esta versão concede aos profissionais de marketing controle total sobre o marketing em lotes com base em públicos-alvo e iniciado pela marca, combinando uma modelagem de dados flexível com uma experiência de orquestração. Ela foi projetada especificamente para orquestração de campanhas em lotes para jornadas em tempo real, oferecendo personalização e capacidade de redimensionado avançadas.

### Saiba mais

Saiba mais na [documentação da orquestração de campanhas](../orchestrated/gs-orchestrated-campaigns.md).

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->

## Atualizações de agosto de 2025 {#25.8-rn}

<table>
<thead>
<tr>
<th><strong>Otimização em campanhas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora fornece as ferramentas necessárias para oferecer conteúdo personalizado e otimizado para o público-alvo das suas campanhas, permitindo que você execute experimentos de conteúdo, crie direcionamentos com base em regras e use combinações avançadas de ambos para maximizar a eficiência das suas campanhas.</p>
<p>Com a otimização, você pode:</p>
<ul>
<li>Testar múltiplas variações de conteúdo para identificar as mensagens mais eficazes.</li>
<li>Fornecer conteúdo personalizado com base nos atributos dos usuários e dados contextuais.</li>
<li>Combinar direcionamento e experimentação para estratégias de campanha avançadas.</li>
<li>Filtrar usuários que não correspondem aos critérios da variante.</li>
<li>Garantir mecanismos de fallback para manter o engajamento dos usuários.</li>
</ul>
<P>Quando a campanha estiver ativa, os perfis serão avaliados em relação aos critérios definidos e, com base nos critérios de correspondência, serão entregues com a experiência ou o conteúdo apropriado da campanha.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Data de lançamento: 8 de agosto de 2025</p>
<p>Para mais informações, consulte a <a href="../campaigns/campaigns-message-optimization.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>



## Notas de versão de julho de 2025 {#25-7-rn}

**Data de lançamento**: 29 de julho de 2025

### Novos recursos {#features-25-7}

Os novos recursos incluídos nesta versão são detalhados abaixo.

#### Recursos

<table>
<thead>
<tr>
<th><strong>Marcas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, você pode criar e personalizar as suas próprias marcas para definir claramente a sua identidade visual e verbal nas comunicações. Com a pontuação de alinhamento à marca, você pode receber feedback em tempo real sobre o desempenho do seu conteúdo em termos de refletir o tom, o estilo e as diretrizes da sua marca, ajudando a manter a consistência da marca a cada mensagem enviada.</p>
<p>Anteriormente lançado na versão beta, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../content-management/brands.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar tomada de decisão no canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, você pode adicionar políticas de decisão a campanhas e jornadas por email. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
Para mais informações, consulte a <a href="../experience-decisioning/create-decision.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal LINE </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer expandiu seus recursos entre canais para incluir suporte para o canal LINE. Esse aprimoramento permite criar, editar e visualizar experiências LINE, garantindo interações mais personalizadas e envolventes. Com o LINE, você pode se conectar com mais clientes, enviar conteúdo relevante e melhorar seu engajamento.</p>
<p>Anteriormente disponível somente mediante solicitação, o canal LINE já está disponível para todos os usuários (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../../rp_landing_pages/line-landing-page.md">documentação detalhada</a>.</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Execução de teste da jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A execução de prática de jornada é um modo especial de publicação no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais sem entrar em contato com clientes do mundo real ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganharem confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para mais informações, consulte a <a href="../building-journeys/journey-dry-run.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>ID complementar para jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar jornadas usando uma ID de perfil juntamente com outro identificador, como uma ID de pedido, ID de assinatura ou ID de prescrição, permitindo que o mesmo perfil esteja na mesma jornada várias vezes ao mesmo tempo. Isso possibilita cenários como o gerenciamento de vários pedidos ou assinaturas em paralelo, com cada instância seguindo seu próprio caminho pela jornada.</p>
<p>Anteriormente lançado com disponibilidade limitada, o uso de IDs complementares em jornadas já está disponível para todos os ambientes. Nesta versão com disponibilidade geral, o recurso agora permite jornadas de público-alvo de leitura.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Para mais informações, consulte a <a href="../building-journeys/supplemental-identifier.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

### Alertas no produto

Agora, você pode inscrever-se para receber **alertas por email e no produto** sobre lançamentos do produto Journey Optimizer.

Para inscrever-se:

* Acesse as **Preferências da Adobe Experience Cloud**
* Em **Notificações**, procure **Novas versões do Journey Optimizer**
* Habilitar notificações no aplicativo e por email

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Alteração nas condições da jornada {#ee-change@}

A partir de 8 de julho, em novas organizações de clientes, a criação de expressões usando eventos de experiência não será mais aceita no editor de expressão usado em condições de jornada. Como resultado, os eventos de experiência na [fonte de dados da Experience Platform](../datasource/adobe-experience-platform-data-source.md) não poderão ser usados para criar expressões. Abordagens alternativas e práticas recomendadas para criar expressões/lógica com eventos de experiência são apresentadas [aqui](../building-journeys/exp-event-lookup.md).

Não há alteração em como os dados do evento de contexto de jornada são acessados em jornadas unitárias. Nos editores de expressão e personalização, os usuários podem continuar a acessar os dados transmitidos com o evento de jornada inicial.

Saiba mais [nesta seção de Perguntas frequentes](../building-journeys/exp-event-lookup.md#faq-ee).

### Aprimoramentos {#25-7-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

* **Campanhas**

   * **Várias ações de entrada em campanhas**: para simplificar a orquestração de campanhas, agora é possível definir várias ações de entrada em uma mesma campanha. Esse recurso permite que você forneça várias experiências baseadas em código, mensagens no aplicativo, cartões de conteúdo ou ações da web para locais diferentes ao mesmo tempo, cada ação com um conteúdo específico.
     [Leia mais](../campaigns/campaign-action.md#multi-action)

   * **Reorganização do inventário de campanhas**: campanhas programadas e acionadas por API agora são divididas em guias separadas no inventário de campanhas para facilitar a navegação e o gerenciamento.

[Saiba mais](../campaigns/modify-stop-campaign.md)

* **Gerenciamento de dados**
   * **Atualização de conjuntos de dados do sistema de gestão de decisões**: as ofertas personalizadas e substitutas excluídas agora são marcadas como arquivadas nos conjuntos de dados “decision_object_repository_personalized_offers” e “decision_object_repository_fallback_offers”. Os registros existentes no conjunto de dados não são alterados.

[Saiba mais](../offers/export-catalog/access-dataset.md)

* **Jornadas**
   * **Aprimoramentos das ferramentas de sandbox da jornada**: ao copiar jornadas em várias sandboxes com os recursos de exportação e importação de pacotes, os seguintes recursos também estão disponíveis:
      * Selecionar um evento existente no destino
      * Copiar um evento independentemente de uma jornada
      * Detectar relações de grupos de campos/fontes de dados, vinculando-os no destino, se existirem, ou criando-os, se não existirem.

[Saiba mais](../configuration/copy-objects-to-sandbox.md)

* **Canal: no aplicativo**
   * **Pares de chave/valor no aplicativo**: com mensagens no aplicativo, é possível definir pares de chave e valor para incluir variáveis personalizadas no conteúdo da mensagem. Esses pares de valor e chave permitem transmitir dados adicionais com base na sua configuração e no caso de uso específicos. [Leia mais](../in-app/design-in-app.md)

* **Canal: cartão de conteúdo**

   * **Desqualificação de campanhas com base em regras**: ao editar regras de entrega adicionais, a opção “Regras de entrega” anterior foi substituída por três tipos de regra distintos para controlar melhor o cronograma e a visibilidade das mensagens:
      * Mostrar mensagem se: condições que determinam quando o cartão de conteúdo é mostrado.
      * Ignorar mensagem se: condições que ocultam temporariamente o cartão de conteúdo. Ele pode reaparecer se as condições de exibição forem satisfeitas novamente.
      * Desqualificar mensagem se: condições que impedem permanentemente que o cartão de conteúdo seja mostrado novamente.

[Saiba mais](../content-card/design-content-card.md)

* **Decisão**
   * **APIs das ferramentas de migração**: a equipe do Journey Optimizer está desenvolvendo APIs das ferramentas de migração para migrar entidades da gestão de decisões para a tomada de decisão. Essas ferramentas permitem uma migração fluida entre sandboxes com recursos de resolução de dependência e reversão. Se tiver interesse, entre em contato com o seu representante da Adobe.

* **Personalização**
   * Uma nova função de ajuda, “SHA256”, foi adicionada ao editor de personalização. Essa função é usada para calcular e retornar o hash sha256 de uma string.

[Saiba mais](../personalization/functions/string.md#sha256)
