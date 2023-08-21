---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de entrada de perfil
description: Saiba como gerenciar a entrada de perfil
feature: Journeys
role: User
level: Intermediate
keywords: reentrada, jornada, perfil, recorrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: c4b40d66db042e7dce1326e64b9d706f33cb01c2
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 14%

---


# Gerenciamento de entrada de perfil {#entry-management}

Há dois tipos principais de jornadas:

* jornadas baseadas em eventos: a partir de um evento, essas jornadas são unitárias e estão associadas a um indivíduo. Quando o evento é recebido, o indivíduo entra na jornada. [Leia mais](#entry-unitary)
* ler jornadas de público-alvo: a partir de um público-alvo de leitura, essas são jornadas em lote. Todos os indivíduos pertencentes ao público entram na mesma jornada. Essas jornadas podem ser recorrentes ou únicas. [Leia mais](#entry-read-segment)

Em ambos os tipos de jornada, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo.

## Jornadas unitárias{#entry-unitary}

Em jornadas unitárias, você pode ativar ou desativar a reentrada:

* Se a reentrada estiver ativada, um perfil poderá inserir uma jornada várias vezes, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada.

* Se a reentrada estiver desativada, um perfil não poderá entrar várias vezes na mesma jornada.

Por padrão, novas jornadas permitem a reentrada. Você pode desmarcar a opção para jornadas &quot;one shot&quot;, por exemplo, se quiser oferecer um presente único quando uma pessoa visitar uma loja. Nesse caso, o cliente não poderá inserir novamente a jornada e receber a oferta novamente. Quando uma jornada termina, seu status é **[!UICONTROL Fechado]**. Novos indivíduos não podem mais entrar na jornada. As pessoas que já estão na jornada terminam a jornada normalmente. [Saiba mais](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

Após o tempo limite global padrão de 30 dias, a jornada muda para a tag **Concluído** status. Os perfis que já estão na jornada concluem a jornada normalmente. Novos perfis não podem mais entrar na jornada. Para alinhar-se à conformidade com a privacidade, esse comportamento é definido somente para 30 dias. Após esse período, os perfis poderão inserir novamente a jornada. Para evitar isso, adicione uma condição para testar se o perfil já entrou ou não. Saiba mais sobre o tempo limite da jornada em [nesta seção](journey-gs.md#global_timeout).

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. -->

As jornadas unitárias (começando com um evento ou uma qualificação de público-alvo) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12h01 para um perfil específico e outra chegar às 12h03 (se for o mesmo evento ou outro acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.

A chave também é usada para verificar se uma pessoa está em uma jornada. De fato, uma pessoa não pode estar em dois lugares diferentes na mesma jornada. Como resultado, o sistema não permite que a mesma chave, por exemplo, a chave CRMID=3224, esteja em locais diferentes na mesma jornada.

## Ler jornadas de público{#entry-read-segment}

Em uma jornada de público-alvo de leitura:

* Para jornadas não recorrentes: o perfil insere uma vez e somente uma vez na jornada.

* Para jornadas recorrentes: por padrão, todos os perfis pertencentes ao público-alvo entram na jornada em cada recorrência. Eles devem concluir a jornada antes de entrar novamente em outra ocorrência.

>[!NOTE]
>
>Duas opções estão disponíveis para jornadas de leitura de público-alvo recorrentes. A variável **Forçar reentrada na recorrência** faz com que todos os perfis ainda presentes na jornada saiam automaticamente na próxima execução. A variável **Leitura incremental** Esta opção segmenta somente os indivíduos que entraram no público-alvo desde a última execução da jornada. Consulte esta [seção](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

Em jornadas de eventos comerciais que começam com um **Ler público** Atividade: sabendo que essa jornada se baseia na recepção de um evento comercial, se o perfil for qualificado no público-alvo esperado, eles inserirão a jornada para cada evento comercial recebido, o que significa que esse perfil pode ser várias vezes na mesma jornada, ao mesmo tempo, mas no contexto de diferentes eventos comerciais.