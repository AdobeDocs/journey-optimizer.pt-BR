---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '609'
ht-degree: 100%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de fevereiro de 2024 {#e-2024}

**Data de lançamento**: 21 e 22 de fevereiro de 2024

### Novos recursos{#e-features}

Essa versão traz os novos recursos listados abaixo.


<table>
<thead>
<tr>
<th><strong>Mensagens Web no aplicativo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar o novo recurso de mensagens Web no aplicativo para exibir conteúdo personalizado diretamente em sites, por meio de mensagens de sobreposição modal. Esse recurso permite que você interaja efetivamente com visitantes da Web, melhorando a interação de usuários, a retenção e as taxas de conversão.<br/><br/></p>
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
<p>Agora você pode criar regras de frequência para canais de SMS e correspondência direta. As regras de frequência excluem automaticamente perfis excessivamente solicitados de mensagens e ações quando o limite de frequência é atingido. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

* **Listas de seeds**: as variantes agora são compatíveis ao usar **listas de seeds**. Assim como cada perfil do público-alvo direcionado, os seed addresses recebem uma cópia de todas as variantes da mesma mensagem (assim como os diferentes tratamentos de um experimento de conteúdo).

Anteriormente disponível como Beta, as seguintes melhorias agora estão disponíveis para todos os usuários:

* Agora é possível direcionar **públicos-alvo criados por meio da composição de público-alvo** e aproveitar os atributos de enriquecimento em jornadas. [Saiba mais](../building-journeys/read-audience.md)

* Agora é possível direcionar **públicos-alvo enviados a partir de um arquivo CSV** para jornadas e campanhas. [Saiba mais](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* O públicos-alvo e os atributos da composição de público-alvo e do upload personalizado (arquivo CSV) estão atualmente indisponíveis para uso com o Healthcare Shield ou o Privacy and Security Shield.
  >* Observe que o upload de público-alvo a partir de uma melhoria de arquivo CSV será implementado gradualmente ao longo de vários dias após o lançamento inicial. Embora algumas pessoas tenham acesso imediato, outras podem enfrentar um atraso antes que o recurso seja disponibilizado em suas contas.

**Jornadas**

* **Filtre suas jornadas**: agora você pode usar o inventário **datas personalizadas para filtrar as jornadas**, além dos filtros de data predefinidos já existentes. Isso permite refinar a lista ao exibir jornadas criadas ou publicadas em uma data específica, em um mês específico, durante um ano inteiro ou em intervalos de tempo especificados.
* **Ações personalizadas**: agora você pode atualizar o cabeçalho **tipo de conteúdo**. Este novo **tipo de conteúdo** deve fazer referência ao conteúdo JSON.
* **Configuração**: o atributo identityMap em stepEvents agora é pré-preenchido. A identidade principal é definida como “primary = true”.
* **Interface**: a barra superior, nas telas da jornada, foi reorganizada para obter uma experiência aprimorada. Entre as diferentes atualizações, observe que o ícone de “lápis” que permite acessar as propriedades da jornada agora é exibido à esquerda da barra superior, ao lado do nome da jornada.

**Canal SMS**

* **Palavras-chave de aceitação/recusa**: ao configurar seu canal de SMS, agora é possível personalizar as **Palavras-chave de aceitação e recusa** de acordo com suas preferências. O Journey Optimizer aciona a resposta com base nessas palavras-chave especificadas.

**Campanhas**

* **Campanhas acionadas por API**: o código cURL gerado após a ativação de uma campanha acionada por API foi aprimorado. Agora, todas as variáveis de personalização (perfil e contexto) usadas na mensagem estão presentes.

**Gestão de decisões**

* **Regras de limite**: agora você pode adicionar **várias regras de limite** para uma oferta. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas.

**Modelos de conteúdo**

* **Miniatura**: uma **exibição em miniatura** agora está disponível para modelos e fragmentos de conteúdo para acesso visual aprimorado.

  >[!AVAILABILITY]
  >
  >Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno conjunto de clientes.

* **Modelos multicanais**: os modelos de conteúdo agora estão disponíveis para **todos os canais**, exceto Web. Para email, agora é possível selecionar o tipo (HTML ou Conteúdo).
