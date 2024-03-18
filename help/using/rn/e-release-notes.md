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
source-git-commit: 2dfcbd1631c7fefccaf02782a3218c9a1c1dc7aa
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 29%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no final de cada mês no [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de março de 2024 {#e-2024}

**Data de lançamento**: 19 a 20 de março de 2024

### Novo recurso {#e-features}

Essa versão traz o novo recurso detalhado abaixo.

<table>
<thead>
<tr>
<th><strong>Experiências baseadas em código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o novo canal de experiência baseado em código, o Adobe Journey Optimizer permite fazer personalização e testes avançados para qualquer uma de suas propriedades de entrada, permitindo a entrega contínua de experiências personalizadas em pontos de contato diversos, como aplicativos Web, aplicativos móveis, aplicativos para desktop, consoles de vídeo, dispositivos conectados a TV, TVs inteligentes, quiosques, ATMs, dispositivos IoT e muito mais.</p>
<P>Os principais recursos incluem:</p>
<ul><li> Personalização universal: estenda experiências personalizadas em todos os pontos de contato, garantindo uma jornada de usuário coesa e personalizada</li>
<li>Precisão de edição granular: edite conteúdo específico em locais individuais em seus aplicativos ou páginas da Web</li>
<li>Implementação versátil: suporte para métodos de implementação no lado do servidor, baseados em API ou baseados em SDK para integração contínua com seu ambiente de desenvolvimento.</li></ul></p>
<p>Para obter mais informações, consulte a <a href="../code-based/get-started-code-based.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Modelos de conteúdo**

* **Miniaturas** - A **Exibição em grade** O modo agora está disponível para modelos de conteúdo, exibindo miniaturas para melhorar o acesso visual. Atualmente, somente os modelos de HTML de email são compatíveis. [Saiba mais](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno conjunto de clientes.

**Jornadas**

Novos status intermediários foram adicionados ao ciclo de vida de criação do jornada:

* **Publicação** status entre a variável **Rascunho** status e o **Ao vivo** status
* **Parando** status entre a variável **Ao vivo** status e o **Parado** status
* **Ativando o modo de teste** ou **Desativando modo de teste** status entre a variável **Rascunho** status e o **Rascunho (teste)** status

Quando uma jornada está em um estado intermediário, ela é somente leitura.