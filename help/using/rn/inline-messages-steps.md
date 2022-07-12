---
title: Etapas para migrar para a criação em linha do jornada
description: Etapas para migrar para a criação em linha do jornada
source-git-commit: 3f9844dec9caf520ab59c5f2b433a5c2e86ef44f
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 1%

---


# Etapas de migração da criação em linha{#migration-steps}

O novo processo de criação de mensagens no Adobe Journey Optimizer está descrito nesta [página](../rn/inline-messages.md). Uma conversão automática de jornadas será executada para você. Dito isto, necessitaremos da sua ajuda com alguns passos.

>[!VIDEO](https://video.tv.adobe.com/v/344699)

Estas são as principais fases e etapas:

**[Antes da migração](../rn/inline-messages-steps.md#migration-step-1)**

1. Em sandboxes que não sejam de produção, pare todas as jornadas ativas e fechadas. [Leia mais](../rn/inline-messages-steps.md#migration-step-1-1)
1. Na sandbox de produção, pare todas as jornadas ad-hoc ativas sem perfil ainda no . [Leia mais](../rn/inline-messages-steps.md#migration-step-1-2)

**[Após a primeira iteração](../rn/inline-messages-steps.md#migration-step-2)**

1. Verifique se há erros nas jornadas ativas migradas. [Leia mais](../rn/inline-messages-steps.md#migration-step-2-1)
1. Lista todas as novas versões criadas pela migração. [Leia mais](../rn/inline-messages-steps.md#migration-step-2-2)
1. Teste e publique-os um por um. [Leia mais](../rn/inline-messages-steps.md#migration-step-2-3)
1. Liste todas as versões ativas. [Leia mais](../rn/inline-messages-steps.md#migration-step-2-4)
1. Examine erros na migração da versão de rascunho. [Leia mais](../rn/inline-messages-steps.md#migration-step-2-5)

**[Após a segunda iteração](../rn/inline-messages-steps.md#migration-step-3)**

1. Verifique as duas fases de migração. [Leia mais](../rn/inline-messages-steps.md#migration-step-3-1)
1. Pare as versões anteriores. [Leia mais](../rn/inline-messages-steps.md#migration-step-3-2)

**[Antes da terceira e última iteração](../rn/inline-messages-steps.md#migration-step-4)**

Valide se tudo foi migrado antes da descontinuação.

<br> 

## Antes da migração (25 de julho){#migration-step-1}

### 1. Pare todas as jornadas ao vivo e fechadas{#migration-step-1-1}

Ligado **sandboxes de não produção**, pare todas as jornadas ao vivo e fechadas. Isso permitirá que o processo de migração automatizada migre todas as jornadas dessas sandboxes sem nenhuma ação da sua parte. Após a migração, você poderá duplicar as versões de jornada interrompidas e usá-las.

### 2. Pare todas as jornadas ad-hoc ativas sem o perfil ainda em{#migration-step-1-2}

No **sandbox de produção**, pare todas as jornadas ad-hoc ativas que não contêm mais perfis.

+++Como encontrar essas jornadas?

Para encontrar essas jornadas, navegue até a guia **Jornada** e filtre a lista em &quot;Status = Live&quot; e &quot;Type = Read segment&quot;. Você também pode solicitar cronologicamente da primeira para a última data &quot;Publicada&quot;.

![](assets/inline-migration-steps1.png)

Abra-os de cima para baixo.

* Verifique se a jornada tem uma mensagem.
* Verifique se elas não são jornadas recorrentes. Elas não são ad-hoc. Você provavelmente quer mantê-los vivos. Por exemplo, esta é uma jornada recorrente (não ad-hoc):

   ![](assets/inline-migration-steps2.png)

* Se você tiver usado ouvintes de espera ou evento nessas jornadas, os perfis ainda poderão estar dentro. Examine a data de execução da jornada e adicione quaisquer horas/dias que você tenha definido em suas esperas ou ouvintes de eventos para deduzir a data real em que nenhum perfil é deixado dentro. Se essa data estiver no passado, você pode parar a jornada. Caso contrário, essa jornada será movida automaticamente para o status &quot;Finished&quot; 30 dias após a data de execução da jornada.

+++

**Observações importantes**

* Evite fechar jornadas antes da data da migração (25 de julho). Saber que o script de migração não migrará jornadas ativas ou fechadas, limitar o número de jornadas fechadas na sandbox de produção limitará o número de ações manuais necessárias após a migração.

* Se você tiver jornadas ativas que não sejam a versão mais recente, o que significa que criou outra versão do jornada no rascunho, publique-a ou exclua-a.

* Se você tiver mensagens que não são usadas no jornada e que deseja manter, salve-as como modelos. Observe que você ainda poderá acessá-los até a descontinuação.

## Após a primeira iteração da migração (25 de julho){#migration-step-2}

A migração é sequenciada em duas fases: a fase automatizada (à noite, entre 25 de julho e 26 de julho) e a fase manual (a partir de 26 de julho), que requer itens de ação.

Para a fase automatizada, consulte esta seção [página](../rn/inline-messages.md#process).

Para a fase manual, aqui estão as ações a serem executadas no **sandbox de produção**:

<!--
_On non-production sandboxes:_

**1. Check the migration status report for any error**

Click the **Check status** button in the top banner and check that there has been no error during the automatic migration and that there is nothing left to migrate. 

![](assets/inline-migration-steps3.png)

Look for the "ERROR" status. 

![](assets/inline-migration-steps4.png)

* If there is no error, you are good to go.
* If there are errors, look for the error by searching "errorMessage". The following error is expected as migration of multi-channel messages is not supported: "Migration of multi-channel messages is not supported". You will have to rebuild this journey.

    ![](assets/inline-migration-steps5.png)

_On the production sandbox:_

-->

### 1. Verifique se há erros nas Jornadas ativas migradas{#migration-step-2-1}

Verifique se há erros nas jornadas ativas migradas automaticamente no relatório de status.

Procure por &quot;ERROR_NEW_VERSION_CREATION&quot;:

![](assets/inline-migration-steps6.png)

* Se não houver erro, significa que todas as versões de jornada ativa que exigem migração foram processadas e uma nova versão de rascunho migrada foi criada automaticamente.

* Se vir um erro, você pode procurar por &quot;errorMessage&quot; e verificar a mensagem de erro nos logs. Mensagens de vários canais não são migradas. Você terá que criar outra jornada.

* Para outros erros, entre em contato com seu CSM ou qualquer representante de Adobe para obter orientação.

### 2. Listar todas as novas versões criadas pela migração{#migration-step-2-2}

Eles são marcados como [MIGRADO] no rótulo da jornada e na data de criação é atualizada.

![](assets/inline-migration-steps7.png)

### 3. Teste e publique-os um por um{#migration-step-2-3}

Verifique se a jornada ainda precisa ser executada na produção. Se a variável [preparação antes da migração](../rn/inline-messages-steps.md#migration-step-1) não foi executado corretamente, é possível criar uma nova versão para uma jornada de uma só vez que não é mais necessária.

Teste sua versão de rascunho da jornada que agora contém ações de canal em linha.

Publique sua nova versão do jornada. Sua versão ao vivo anterior mudará para o status &quot;Fechado&quot;.

### 4. Listar todas as versões ativas{#migration-step-2-4}

Todos devem ser marcados como o mais tardar. caso contrário, procure a versão mais recente, teste-a e publique-a.

![](assets/inline-migration-steps8.png)

### 5. Verifique os erros na migração da versão de rascunho{#migration-step-2-5}

Clique no botão **Verificar status** no banner superior e verifique se não houve erro durante a migração automática e se não há mais nada para migrar. Esteja ciente de que qualquer jornada com erro (com mensagens) será descontinuada após 5 de setembro (em todas as sandboxes).

![](assets/inline-migration-steps11.png)

Procure o status &quot;ERROR&quot;.

![](assets/inline-migration-steps9.png)

* Se não houver erro, você pode ir.

* Se houver erros, procure o erro pesquisando &quot;errorMessage&quot;. O seguinte erro é esperado, pois a migração de mensagens de vários canais não é suportada: &quot;Não há suporte para a migração de mensagens de vários canais&quot;. Você terá que reconstruir essa jornada.

![](assets/inline-migration-steps6.png)

## Após a segunda iteração (1 de agosto){#migration-step-3}

A segunda iteração acontecerá à noite entre 1º de agosto e 2 de agosto.

<!--
_On non-production sandboxes:_

**1. Check at the status report**

Click the **Check status** button in the top banner and check that all journeys have been migrated and there's nothing left to migrate. If there is an error or something left to migrate, please reach out to your CSM or Adobe representative for guidance.

-->

Se todas as etapas anteriores foram executadas a tempo, todas as jornadas foram migradas, exceto as fechadas e as com erros. Estas são as etapas a serem seguidas na seção **sandbox de produção**:

### 1. Verifique as duas fases de migração{#migration-step-3-1}

Se não houver erros, você não deverá ter jornadas em &quot;eligibilidadeStatus&quot;, em &quot;toMigrate&quot; e &quot;createNewVersion&quot;. No exemplo a seguir, há um &quot;ERROR&quot; e um &quot;ERROR_NEW_VERSION_CREATION&quot;.

![](assets/inline-migration-steps10.png)

### 2. Parar as versões anteriores{#migration-step-3-2}

Caso não tenha publicado versões mais recentes do jornada (consulte esta seção [seção](../rn/inline-messages-steps.md#migration-step-2-3)) em tempo que significa antes da iteração 2 (1º de agosto), em seguida, publique a versão mais recente e **interrompa a versão anterior ou você a perderá** e seus relatórios associados.

## Antes da terceira e última iteração (5 de setembro){#migration-step-4}

Entre 1º de agosto e 5 de setembro, você precisará validar se tudo foi migrado e se não há jornadas ainda usando mensagens, caso contrário, elas serão substituídas no dia 5 de setembro.

