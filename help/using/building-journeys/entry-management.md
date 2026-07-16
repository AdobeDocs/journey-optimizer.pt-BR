---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de entrada de perfil
description: Saiba como gerenciar a entrada de perfil
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: reentrada, jornada, perfil, recorrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/li1WSyhVKq58N-FiTEL51gX-u911JVyZXcnBZtwNhDE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 48d26b4669ef3fad87fd05d61ec187b7445d00a8
workflow-type: tm+mt
source-wordcount: 2175
ht-degree: 1%

---

# Gerenciamento de entrada de perfis {#entry-management}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como a entrada e a reentrada de perfis funcionam para cada tipo de jornada para que você possa controlar quando e com que frequência os perfis entram em suas jornadas.

>[!ENDSHADEBOX]

O gerenciamento de entrada de perfis depende do tipo de jornada.

>[!TIP]
>
>Procurando orientação prática com exemplos do mundo real? Consulte nosso [guia abrangente para os critérios de entrada e saída do jornada](entry-exit-criteria-guide.md), que inclui casos de uso como campanhas de boas-vindas, recuperação de carrinho abandonado e programas de fidelidade com exemplos completos de configuração de entrada e saída.

## Tipos de jornadas {#types-of-journeys}

Com o [!DNL Adobe Journey Optimizer], você pode criar os seguintes tipos de jornadas:

* **jornadas de evento unitário**: essas jornadas começam com um evento unitário. Quando o evento é recebido, o perfil associado entra na jornada. [Leia mais](#entry-unitary)

* **jornadas de eventos comerciais**: essas jornadas começam com um evento comercial seguido imediatamente por uma atividade **Ler público**. Quando o evento for recebido, os perfis pertencentes ao público-alvo direcionado entram na jornada. Uma instância dessa jornada é criada para cada perfil. [Leia mais](#entry-business)

* jornadas de **Leitura de público-alvo**: essas jornadas começam com uma atividade **Leitura de público-alvo**. Quando a jornada for executada, os perfis que pertencem ao público-alvo de destino entram na jornada. Uma instância dessa jornada é criada para cada perfil. Essas jornadas podem ser recorrentes ou &quot;únicas&quot;. [Leia mais](#entry-read-audience)

* **jornadas de qualificação de público-alvo**: essas jornadas começam com um evento de qualificação de público-alvo. Essas jornadas escutam as entradas e saídas dos perfis nos públicos-alvo. Quando isso acontece, o perfil associado entra na jornada. [Leia mais](#entry-unitary)

[Comparar todos os tipos de jornada com casos de uso →](journey.md#journey-types)

Em todos os tipos de jornada, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo, para todas as [versões ativas da jornada](publish-journey.md#journey-versions). Para verificar se uma pessoa está em uma jornada, a identidade do perfil é usada como uma chave. O sistema não permite que a mesma chave, por exemplo, a chave `CRMID=3224`, esteja em locais diferentes na mesma jornada.

## Taxa de processamento de jornada {#journey-processing-rate}

A taxa de processamento da jornada é afetada por vários fatores que determinam como os perfis fluem em uma jornada:

### Taxa de entrada do perfil {#profile-entrance-rate}

A forma como os perfis inserem jornadas e a taxa esperada depende da primeira atividade usada:

* **Ler público-alvo** jornadas (cenário de lote, em que você direciona um público-alvo de perfis e aciona uma jornada para esse público-alvo completo): o máximo é 20.000 TPS (transações por segundo). Esta é a cota disponível em um **nível de sandbox**. Se várias jornadas forem executadas ao mesmo tempo nessa sandbox, talvez não seja possível atingir 20.000 TPS. Considere esse máximo como um cenário otimizado.

* **jornadas de qualificação de público-alvo** (cenário unitário, em que você deseja acionar uma jornada quando um perfil é qualificado ou desqualificado para um público-alvo de transmissão): o máximo é de 5.000 TPS. Observe que esse é um limite compartilhado com jornadas que começam com eventos e também é compartilhado entre jornadas em um **nível de organização**.

* **jornadas de evento unitário** (cenário unitário, em que você deseja acionar uma jornada quando um evento é emitido de um perfil): o mesmo acima, ambos compartilhando o mesmo limite de 5.000 TPS. Mais informações sobre a taxa de transferência do evento de jornada estão disponíveis em [esta seção](../event/about-events.md#event-thoughput).

* **jornadas de evento comercial** (um cenário unitário em lote porque um evento comercial é sempre seguido por um público-alvo de Leitura): a contagem de eventos comerciais é de 5.000 TPS. A atividade Read audience a seguir tem o mesmo limite que as jornadas que começam com um público-alvo de Leitura (20.000 TPS).

### Eventos e qualificações de público dentro do jornada {#events-inside-journeys}

Após a entrada, você pode usar as atividades de **Evento unitário** ou **Qualificação de público-alvo** dentro da jornada. Um perfil pode entrar em qualquer um dos quatro tipos de jornadas descritos acima e esperar que um evento seja emitido ou esperar que esse perfil se qualifique para um público-alvo. Esses eventos unitários e qualificações de Público-alvo contarão na cota descrita acima. Por exemplo: se você iniciar uma jornada com um público-alvo de Leitura (com um máximo de 20.000 TPS) e tiver um evento logo após, esse evento terá no máximo 5.000 TPS.

### Impacto das atividades de espera {#wait-activities-impact}

As atividades de **Aguardar** no jornada também podem afetar quantos perfis estão fluindo por uma jornada em um momento específico. Normalmente, uma atividade Wait é baseada em um tempo relativo (por exemplo: sai 2 horas após inserir a espera, portanto, todos os perfis não sairão ao mesmo tempo). No entanto, se um tempo fixo for definido nessa atividade de espera, vários perfis poderão sair dessa jornada exatamente ao mesmo tempo. Esta não é uma prática recomendada. Volumes maciços podem então ser vistos e a TPS a partir deste ponto pode exceder 20.000 TPS.

### Atividades de ação {#action-activities-impact}

Finalmente, as atividades de **ação** podem ser afetadas pelo carregamento do perfil proveniente do jornada e também podem afetar a taxa de processamento. Isso inclui canais nativos, como Email, SMS e Push, além de ações personalizadas, saltos para outras jornadas e atividades de atualização de perfil. Por exemplo, uma ação personalizada direcionada a um endpoint externo com um tempo de resposta alto reduzirá a taxa de processamento da jornada.

Para ações personalizadas, o limite padrão é de 300.000 chamadas por minuto, que podem ser alteradas com uma política de limite personalizada. Saiba mais sobre o limite de ação personalizada em [esta seção](../configuration/external-systems.md#capping).

## Jornadas unitárias de qualificação de evento e público-alvo{#entry-unitary}

Nas jornadas **Evento unitário** e **Qualificação de público-alvo**, você pode habilitar ou desabilitar a reentrada:

* Se a reentrada estiver ativada, um perfil poderá inserir uma jornada várias vezes, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada.

* Se a reentrada estiver desativada, um perfil não poderá entrar várias vezes na mesma jornada dentro do tempo limite global da jornada. Consulte esta [seção](../building-journeys/journey-properties.md#global_timeout).

Por padrão, as jornadas permitem a reentrada. Quando a opção **Permitir reentrada** está ativada, o campo **Período de espera de reentrada** é exibido. Isso permite definir o tempo de espera antes de permitir que um perfil entre na jornada novamente. Isso impede que uma mesma jornada seja incorretamente acionada várias vezes no mesmo evento. Por padrão, o campo é definido como 5 minutos. A duração máxima é de 90 dias ([tempo limite global](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![Alternância das configurações de reentrada nas propriedades da jornada](assets/journey-re-entrance.png)

Após o período de reentrada, os perfis podem entrar na jornada novamente. Para evitar isso e desativar totalmente a reentrada desses perfis, você pode adicionar uma condição para testar se o perfil entrou já ou não, usando dados de perfil ou público-alvo.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. 
-->

### Reentrada nas versões do jornada {#reentrance-versions}

Um perfil não pode estar ativo na mesma jornada mais de uma vez ao mesmo tempo, incluindo em versões ativas dessa jornada.

As configurações de reentrada estão definidas na versão atual do jornada, mas o [!DNL Journey Optimizer] também verifica se o perfil já está ativo em outra versão ativa da mesma jornada. Se o perfil ainda estiver avançando por uma versão anterior, uma nova entrada será bloqueada até que a instância ativa termine ou o perfil seja removido.

A publicação de uma nova versão do jornada não move perfis em andamento para a nova versão. Os perfis que já inseriram uma versão anterior permanecem nessa versão até que saiam da jornada. Se se tornarem qualificados novamente mais tarde, eles inserirão a versão mais recente disponível.

**Exemplo**

Para entender como o bloqueio entre versões funciona, considere a seguinte sequência:

1. A versão 1 de uma jornada está ativa e um perfil a insere.
1. Você publica a versão 2 da mesma jornada.
1. Se o perfil ainda estiver ativo na Versão 1, ele não poderá iniciar uma nova instância ativa na Versão 2 ao mesmo tempo.
1. Depois que o perfil sair da instância anterior, ele poderá inserir a versão mais recente novamente, sujeita à configuração de reentrada da jornada.

>[!WARNING]
>
>**Por que vejo `exportedsegment_existinginstance`?**
>
>Se você vir o erro `exportedsegment_existinginstance`, isso geralmente significa que o perfil já tem uma instância ativa na mesma jornada. Isso geralmente ocorre quando uma entrada recorrente ou repetida tenta iniciar enquanto o perfil ainda está ativo em outra instância dessa jornada, incluindo uma versão ativa anterior.
>
>Ao solucionar esse erro, verifique o seguinte:
>
>* Se o perfil ainda está em andamento em outra versão ativa da jornada.
>* Se uma execução recorrente anterior ainda está ativa.
>* Se o design da jornada inclui esperas longas ou outras atividades que mantêm os perfis ativos por um período estendido.

## Jornadas comerciais {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

Em **jornadas comerciais**, para permitir várias execuções de eventos comerciais, ative a opção correspondente na seção **[!UICONTROL Execução]** das propriedades de jornada.

![Opções de gerenciamento de entrada de evento comercial na configuração do jornada](assets/business-entry.png)

No caso de eventos comerciais, para determinada jornada, os dados do público-alvo recuperados na primeira execução são reutilizados durante uma janela de tempo de 1 hora.

Um perfil pode estar presente várias vezes na mesma jornada, ao mesmo tempo, mas no contexto de diferentes eventos comerciais.

Para obter mais informações, consulte esta [seção](../event/about-creating-business.md)

## Ler jornadas de público {#entry-read-audience}

**Ler público-alvo** As jornadas podem ser recorrentes ou não recorrentes:

* Para jornadas não recorrentes: o perfil insere uma e apenas uma vez na jornada.

* Para jornadas recorrentes: por padrão, todos os perfis pertencentes ao público-alvo inserem a jornada em cada recorrência. Eles devem concluir a jornada antes de entrar novamente em outra ocorrência.

Várias opções estão disponíveis para jornadas recorrentes de Leitura de público. Para obter mais informações, consulte a seção [Usar um público em uma jornada](../building-journeys/read-audience.md).

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->

## Tópicos relacionados

* [Guia dos critérios de entrada e saída do Jornada](entry-exit-criteria-guide.md) - Guia completo com exemplos reais e práticas recomendadas
* [Configurar critérios de saída](journey-properties.md#exit-criteria) - Defina quando os perfis devem sair da sua jornada
* [Encerrar uma jornada](end-journey.md) - Entenda como as jornadas são fechadas e concluídas
* [Casos de uso do Jornada](jo-use-cases.md) - Consulte exemplos completos com configurações de entrada e saída

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página explica como o gerenciamento de entradas de perfil funciona nos quatro tipos de jornada no Adobe Journey Optimizer, incluindo limites de taxa de transferência, configurações de reentrada e o comportamento de atividades de espera e ação na taxa de processamento.

**Intenções:**

* Entenda o comportamento de entrada e os limites de taxa de transferência para cada tipo de jornada (Evento unitário, Evento comercial, Público de leitura, Qualificação de público)
* Ative ou desative a reentrada de perfis e configure o período de espera de reentrada
* Permitir várias execuções de eventos comerciais para uma jornada comercial
* Identificar como as atividades de espera e as atividades de ação afetam a taxa de processamento da jornada
* Verifique se um perfil não está presente na mesma jornada ao mesmo tempo

**Glossário:**

* **Reentrada**: a capacidade de um perfil entrar na mesma jornada novamente depois de sair anteriormente; configurável com um período de espera *(específico do produto)*
* **Período de espera de reentrada**: o tempo mínimo que deve decorrer antes que um perfil possa inserir novamente uma jornada; o padrão é 5 minutos, o máximo é 90 dias nas propriedades de jornada *(específico do produto)*
* **TPS (Transações por Segundo)**: a taxa de transferência na qual perfis podem ser inseridos ou processados em uma jornada *(específico do produto)*
* **jornada de eventos unitária**: uma jornada acionada por um único evento associado a um perfil *(específico do produto)*
* **Ler jornada de público-alvo**: uma jornada que processa um lote de perfis que pertencem a um público-alvo definido, uma vez ou em um agendamento recorrente *(específico do produto)*
* **jornada de eventos comerciais**: uma jornada acionada por um evento comercial que direciona a um público-alvo, criando uma instância de jornada por perfil *(específico do produto)*
* **jornada de qualificação de público-alvo**: uma jornada disparada quando um perfil entra ou sai de um público-alvo de streaming em tempo real *(específico do produto)*

**Medidas de Proteção:**

* Um perfil não pode estar presente várias vezes na mesma jornada ao mesmo tempo em todas as versões ativas.
* Ler jornadas de público-alvo: máximo de 20.000 TPS (cota no nível da sandbox; compartilhada em todas as jornadas simultâneas Ler público-alvo na mesma sandbox)
* Jornadas de qualificação de público-alvo e evento unitário: máximo de 5.000 TPS (cota no nível da organização; compartilhadas entre si em todas as sandboxes da organização)
* Os eventos comerciais contam para a cota de nível de organização de 5.000 TPS; a atividade subsequente Ler público compartilha a cota de nível de sandbox de 20.000 TPS
* O período de espera de reentrada padrão é de 5 minutos; o valor máximo configurável é de 90 dias nas propriedades do jornada
* As atividades de espera em tempo fixo podem causar sobretensões de perfil superiores a 20.000 TPS e não são recomendadas.
* O limite padrão de ação personalizada é de 300.000 chamadas por minuto.
* Para o Business jornada, os dados do público-alvo da primeira execução são reutilizados por 1 hora.

**Terminologia:**

* Nome canônico: Gerenciamento de entrada de perfil — Acrônimo: n/a — variantes: gerenciamento de entrada de perfil, entrada de jornada
* Sinônimos: &quot;reentrada&quot; = &quot;reentrada&quot;
* Não confunda: &quot;jornada de evento unitária&quot; ≠ &quot;jornada de qualificação de público-alvo&quot; — ambos são cenários unitários, mas acionados de forma diferente (emissão do evento vs. alteração de associação de público-alvo)

**Perguntas frequentes:**

* **P: Um perfil pode inserir a mesma jornada duas vezes simultaneamente?** — Não, o sistema usa a identidade do perfil como uma chave e impede que o mesmo perfil esteja em lugares diferentes na mesma jornada ao mesmo tempo.
* **P: Qual é o período de espera de reentrada padrão?** — 5 minutos, configuráveis até um máximo de 90 dias nas propriedades do jornada.
* **P: Quantos perfis por segundo um processo de jornada de Leitura de público-alvo pode ser executado?** — até 20.000 TPS no nível da sandbox, embora esse máximo possa não ser atingível se várias jornadas forem executadas simultaneamente na mesma sandbox.
* **P: O que acontece com a taxa de transferência após uma atividade de espera com um tempo fixo?** — Vários perfis podem sair da espera simultaneamente, excedendo potencialmente 20.000 TPS; para evitar isso, recomenda-se o uso de atividades de espera em tempo relativo.
* **P: Um perfil pode aparecer em uma jornada Comercial várias vezes ao mesmo tempo?** — Sim, mas somente no contexto de eventos comerciais diferentes.

+++
