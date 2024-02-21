---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: a0a4d39519f7f02265c52934db401e036ea12df6
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 16%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de fevereiro de 2024 {#e-2024}

**Data de lançamento**: 21 a 22 de fevereiro de 2024

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
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Regras de frequência para SMS e correspondência direta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar regras de Frequência para canais de SMS e Mala direta. As regras de frequência excluem automaticamente perfis excessivamente solicitados de mensagens e ações quando o limite de frequência é atingido. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

* **Seed lists** - As variantes agora são compatíveis ao usar **seed lists**. Como cada perfil do público-alvo direcionado, os seed addresses recebem uma cópia de todas as variantes da mesma mensagem (como os diferentes tratamentos de um experimento de conteúdo).

Anteriormente disponível como Beta, as seguintes melhorias agora estão disponíveis para todos os usuários:

* Agora você pode direcionar **públicos-alvo criados por meio da composição do público-alvo** e aproveitar atributos de enriquecimento no Jornada. [Saiba mais](../building-journeys/read-audience.md)

* Agora você pode direcionar **públicos carregados de um arquivo CSV** em jornadas e campanhas. [Saiba mais](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* O uso de públicos-alvo e atributos da composição de público-alvo e do upload personalizado (arquivo CSV) está atualmente indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield.
  >* Observe que o upload do público-alvo a partir de uma melhoria de arquivo CSV será lançado gradualmente ao longo de vários dias após o lançamento inicial. Embora alguns usuários tenham acesso imediato, outros podem enfrentar um atraso antes que ele seja disponibilizado em suas contas.

**Jornadas**

* **Filtrar suas jornadas** - Agora você pode usar **datas personalizadas para filtrar as jornadas** inventário, além dos filtros de data predefinidos existentes. Isso permite refinar a lista ao exibir jornadas criadas ou publicadas em uma data específica, em um mês específico, durante um ano inteiro ou dentro de intervalos de tempo especificados.
* **Ações personalizadas** - Agora você pode atualizar o **tipo de conteúdo** cabeçalho. Este novo **tipo de conteúdo** O deve fazer referência ao conteúdo JSON.
* **Configuração** - O atributo identityMap em stepEvents agora é pré-preenchido. A identidade principal é definida como &quot;primary = true&quot;.
* **Interface do usuário** - A barra superior, nas telas do jornada, foi reorganizada para obter uma experiência aprimorada. Entre as diferentes atualizações, observe que o ícone de &quot;lápis&quot; que permite acessar as propriedades da jornada agora é exibido à esquerda da barra superior, ao lado do nome da jornada.

**Canal SMS**

* **Palavras-chave de aceitação/recusa** - Ao configurar seu canal SMS, agora é possível personalizar o **Palavras-chave de aceitação e recusa** de acordo com suas preferências. O Journey Optimizer aciona a resposta com base nessas palavras-chave especificadas.

**Campanhas**

* **Campanhas acionadas por API** - O código cURL gerado após a ativação de uma campanha acionada por API foi aprimorado. Agora, ela inclui todas as variáveis de personalização (perfil e contexto) usadas na mensagem.

**Gestão de decisões**

* **Regras de limite** - Agora você pode adicionar **várias regras de limite** para uma oferta. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas.

**Modelos de conteúdo**

* **Miniatura** - A **exibição em miniatura** O agora está disponível para modelos e fragmentos de conteúdo para acesso visual aprimorado.

  >[!AVAILABILITY]
  >
  >Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno conjunto de clientes.

* **Modelos multicanais** - Os modelos de conteúdo agora estão disponíveis para **todos os canais**, exceto Web. Para Email, agora é possível selecionar o tipo (HTML ou Conteúdo).
