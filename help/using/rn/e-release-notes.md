---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 00a1b3cab9f5d7060ab8db9e27a31a6afaede79e
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 18%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de fevereiro de 2024 {#e-2024}

**Data de lançamento**: 20 a 21 de fevereiro de 2024

### Novos recursos{#e-features}

Essa versão traz os novos recursos listados abaixo.


<table>
<thead>
<tr>
<th><strong>Mensagens no aplicativo da Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar o novo recurso de mensagens na Web no aplicativo para exibir conteúdo personalizado diretamente nos sites, por meio de mensagens de sobreposição modal. Esse recurso permite que você interaja efetivamente com visitantes da Web, melhorando a interação do usuário, a retenção e as taxas de conversão.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Regras comerciais (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar regras de Limite de frequência que se aplicam aos canais de SMS e de Correspondência direta. Além disso, você pode definir regras de limite de frequência por tipo de comunicação.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>



### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

* **Seed lists** - As variantes agora são compatíveis ao usar **seed lists**. Como cada perfil do público-alvo direcionado, os seed addresses recebem uma cópia de todas as variantes da mesma mensagem (como os diferentes tratamentos de um experimento de conteúdo).

Anteriormente disponível como Beta, as seguintes melhorias agora estão disponíveis para todos os usuários:

* Agora você pode direcionar **públicos carregados de um arquivo CSV** em jornadas e campanhas. [Saiba mais](../audience/about-audiences.md#segments-in-journey-optimizer)
* Agora você pode direcionar **públicos-alvo criados por meio da composição do público-alvo** e aproveitar atributos de enriquecimento no Jornada. [Saiba mais](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>O uso de públicos-alvo e atributos da composição de público-alvo e do upload personalizado (arquivo CSV) está atualmente indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

**Jornadas**

* **Filtrar suas jornadas** - Agora você pode usar **datas personalizadas para filtrar as jornadas** inventário, além dos filtros de data predefinidos existentes. Isso permite refinar a lista ao exibir jornadas publicadas em uma data específica, em um mês específico, durante um ano inteiro ou dentro de intervalos de tempo especificados.
* **Ações personalizadas** - Agora você pode atualizar no cabeçalho &quot;content-type&quot; no **ações personalizadas**.
* **Configuração** - O atributo identityMap em stepEvents agora é pré-preenchido. A identidade principal é definida como &quot;primary = true&quot;.
* **Interface do usuário** - A barra superior, nas telas do jornada, foi reorganizada para obter uma experiência aprimorada. Entre as diferentes atualizações, observe que o ícone de &quot;lápis&quot; que permite acessar as propriedades da jornada agora é exibido à esquerda da barra superior, ao lado do nome da jornada.

**Canal SMS**

* **Palavras-chave de aceitação/recusa** - Ao configurar seu canal SMS, agora é possível personalizar o **Palavras-chave de aceitação e recusa** de acordo com suas preferências. O Journey Optimizer aciona a resposta com base nessas palavras-chave especificadas.

**Campanhas**

* **Campanhas acionadas por API** - Foram adicionadas informações no **solicitação cURL** seção de **Campanhas acionadas por API** que estão em **Rascunho** para especificar que a solicitação cURL de amostra estará visível somente depois que a campanha for publicada e executada.

**Gestão de decisões**

* **Regras de limite** - Agora você pode adicionar **várias regras de limite** para uma oferta. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas.

**Modelos de conteúdo**

* **Miniatura** - A **exibição em miniatura** O agora está disponível para modelos e fragmentos de conteúdo para acesso visual aprimorado.
* **Modelos multicanais** - Os modelos de conteúdo agora estão disponíveis para **todos os canais**, exceto Web.