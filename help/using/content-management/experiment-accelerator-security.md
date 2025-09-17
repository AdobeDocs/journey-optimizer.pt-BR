---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Experimentation Accelerator
description: Uso de dados na IA com o Journey Optimizer Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: conteúdo, experimento, vários, público-alvo, tratamento
hide: true
hidefromtoc: true
source-git-commit: ddeb3512fbe1d1de86456fe2c3ccd2b3805b5684
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Uso de dados na IA com o Journey Optimizer Experimentation Accelerator{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [Introdução à Journey Optimizer Experimentation Accelerator](experiment-accelerator.md)
* [Uso de dados na IA com o Journey Optimizer Experimentation Accelerator](experiment-accelerator-security.md)
* [Práticas recomendadas do Journey Optimizer Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Monitorar experimentos](experiment-accelerator-monitor.md)
* [Métricas de experimentação](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

O **Adobe Journey Optimizer Journey Optimizer Experimentation Accelerator** permite que você descubra insights automaticamente e recomende oportunidades para melhorar seus experimentos e programa de experimentação. A solução usa IA e aprendizado de máquina para fornecer essas recomendações. Esta instrução esclarece como os dados de seus clientes são usados no **Journey Optimizer Experimentation Accelerator**.

## Quais dados a Journey Optimizer Experimentation Accelerator usa?

Atualmente, há três tipos de dados usados pelo **Journey Optimizer Experimentation Accelerator**:

* **Metadados de experimento**: nome do experimento, a definição do público-alvo usado no experimento e os tratamentos no experimento, por exemplo, nome, porcentagens divididas, local ou superfície em que o experimento é tratado.

* **Desempenho dos tratamentos**: número de pessoas, média da métrica de sucesso e desvio padrão para cada tratamento.

* **Conteúdo do tratamento**: o HTML renderizado e a captura de tela do tratamento como ele apareceria para um usuário no seu site.

## O que a Journey Optimizer Experimentation Accelerator faz com esses dados?

O **Journey Optimizer Experimentation Accelerator** pega o conteúdo de cada tratamento e cria uma incorporação, ou seja, uma representação matemática do conteúdo, e então correlaciona essas incorporações com o desempenho dos tratamentos. Esse processo permite a extração dos atributos de conteúdo que tiveram melhor desempenho para uso futuro. Esses atributos são alimentados em um modelo de linguagem grande hospedado pela Adobe, que os converte em instruções legíveis por humanos usadas para gerar insights e sugerir oportunidades.

## Quais restrições o Journey Optimizer Experimentation Accelerator tem sobre os dados usados?

Cada cliente é atribuído a uma organização e sandbox específicas. Um modelo dedicado é treinado para cada sandbox. Quando uma sandbox é excluída, todos os dados, sinais e modelos relacionados são removidos permanentemente.

* Usamos apenas os dados do cliente para treinar ou ajustar o modelo desse cliente.

* Nunca misturamos clientes para treinar ou ajustar um modelo.

## Os modelos do Adobe ou a IA mudarão a experiência do usuário de uma marca automaticamente?

Não. **Journey Optimizer Experimentation Accelerator** faz somente recomendações sobre o que pode ser alterado e como pode ser alterado. Somente os usuários com permissões para alterar a experiência usando o Journey Optimizer ou o Target poderão agir de acordo com essas recomendações. Todas as recomendações podem ser revisadas e editadas antes de serem enviadas.

## Há algum risco para a estabilidade dos dados ou do sistema?

O **Journey Optimizer Experimentation Accelerator** assimila e analisa somente dados, produzindo insights e recomendações para testes futuros. Ele não tem acesso para modificar configurações de teste. Todas as sugestões geradas na ferramenta são enviadas ao Target e à Journey Optimizer para implementação, garantindo que não haja impacto nas atividades atuais de um cliente.
