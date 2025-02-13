---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão antecipadas
description: 'Notas de versão antecipadas do Journey Optimizer '
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 99f4dc8dc7ba3c6acb886e4a37ba36d9b187c68b
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 25%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão anteriores a 25 de fevereiro {#25-02-rn}

### Novos recursos {#25-02-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Regras de negócios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar regras de negócios usando conjuntos de regras. Os conjuntos de regras são grupos de regras que ajudam a limitar as mensagens enviadas em campanhas e ações de jornada entre canais, além de controlar as entradas de perfis nas jornadas.<p>
<p><ul><li>Crie conjuntos de regras de canal para restringir o número de mensagens enviadas por um ou vários canais. Aplique-as a campanhas ou ações de jornada para aplicar as regras definidas no conjunto de regras. O conjunto de regras de canal permite aplicar regras de limitação com base nos tipos de comunicação. Por exemplo, defina uma regra definida para limitar "mensagens promocionais" e outra para "boletins informativos". Aplique o conjunto de regras apropriado em sua ação de campanha ou jornada, dependendo do tipo de comunicação que você está enviando.</li>
<li> Crie conjuntos de regras de jornada para controlar entradas de perfil nas jornadas. Limite a frequência com que um perfil pode inserir uma jornada em um determinado período ou o número de jornadas nas quais um perfil pode ser inscrito simultaneamente. Aplique-as no nível da jornada para garantir o gerenciamento de entradas adequado.</li></p>
<p>Anteriormente disponível para um conjunto de organizações (DL), as regras de negócios agora estão disponíveis para todos os usuários (DG).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte de várias regiões para SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível gerenciar a entrega de mensagens SMS de endpoints multirregionais substituindo URLs de entrega, feedback, entrada e retorno de chamada. Para oferecer suporte a isso, um novo campo Substituir URL foi adicionado à configuração Credenciais da API. Essa alteração está disponível somente com o provedor Sinch.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modelos do Customer Journey Analytics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há a opção de aprimorar os relatórios do Journey Optimizer utilizando modelos do Customer Journey Analytics. Esse novo recurso permite simplificar o processo de geração de relatórios com modelos projetados previamente e personalizados para suas necessidades de análise.
</p>
<img src="assets/do-not-localize/cja-templates.gif">
<p>Para obter mais informações, consulte a <a href="../reports/report-cja-manage.md#cja-template">documentação detalhada</a>.</p>
<p>Data de disponibilidade: a partir de 15 de janeiro de 2025</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avaliação de público-alvo flexível (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A avaliação flexível do público-alvo permite executar um trabalho de segmentação sob demanda para públicos-alvo selecionados, garantindo que você sempre tenha os dados do público-alvo mais atualizados antes de direcioná-los para jornadas e campanhas do Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obter mais informações, consulte a <a href="../audience/about-audiences.md#flexible">documentação detalhada</a>.</p>
<p> A avaliação flexível do público só está disponível para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.</p>
<p>Data de disponibilidade: 28 de janeiro de 2025</p>
</tr>
</tbody>
</table>


### Melhorias {#25-02-improvements}

As melhorias abaixo vêm com a atualização de fevereiro.

* **Jornada** - Agora é possível testar suas ações personalizadas do jornada enviando chamadas de API da interface do usuário de administração. Esse novo recurso ajuda você a solucionar problemas de ações personalizadas.

* **Tempo de vida (TTL) do conjunto de dados** - A partir deste mês, uma proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema da Journey Optimizer em novas sandboxes e novas organizações, da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada nas sandboxes de clientes existentes em uma fase subsequente.

* **Guias de reprodução** - Agora você pode criar e publicar seus próprios Guias de reprodução de casos de uso no Journey Optimizer.

* **Correspondência direta** - DLZ (Zona de Aterrissagem DAta) agora tem suporte como tipo de servidor para roteamento de arquivo na configuração de Correspondência direta.

**Personalização**

* O editor de personalização foi aprimorado com novos recursos, como opções de Preenchimento automático, Pesquisa e Filtragem. Também é possível mostrar ou ocultar atributos obsoletos.

* Data de disponibilidade: 29 de janeiro de 2025 - Novas funções auxiliares de data/hora estão disponíveis para uso no editor de personalização. [Leia mais](../personalization/functions/dates.md)

**Configuração de email** - Data de disponibilidade: 12 de fevereiro de 2025

* Se você estiver gerenciando o consentimento fora do Adobe, agora é possível definir um endereço de email de cancelamento de inscrição personalizado e um URL de cancelamento de inscrição personalizado com um clique como parte das configurações do canal de email. [Leia mais](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

  >[!AVAILABILITY]
  >
  >Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno conjunto de clientes.

**Decisão** - Data de disponibilidade: 28 de janeiro de 2025

* O Decisioning agora oferece suporte a tipos de dados de Objeto ao editar o esquema do catálogo de itens. [Leia mais](../experience-decisioning/catalogs.md)