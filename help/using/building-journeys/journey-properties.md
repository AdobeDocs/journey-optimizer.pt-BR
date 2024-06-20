---
solution: Journey Optimizer
product: journey optimizer
title: Definir as propriedades da jornada
description: Saiba como definir as propriedades da sua jornada com o Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: jornada, configuração, propriedades
source-git-commit: 67032a4bcbfd56552d783f3ef78593375bfcc378
workflow-type: tm+mt
source-wordcount: '1568'
ht-degree: 8%

---

# Definir as propriedades da jornada {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propriedades da jornada"
>abstract="Essa seção mostra as propriedades da jornada. Por padrão, os parâmetros somente leitura ficam ocultos. As configurações disponíveis dependem do status da jornada, das permissões e da configuração do produto."

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Critérios de saída da jornada"
>abstract="Esta seção mostra as opções de critérios de saída. É possível criar uma ou várias regras de critérios de saída para a sua jornada."

As propriedades da jornada são centralizadas no painel direito da jornada. Esta seção é exibida por padrão ao criar uma nova jornada. Para jornadas existentes, clique no ícone de lápis, ao lado do nome da jornada para acessar suas propriedades.


Use esta seção para definir o nome da jornada, adicionar uma descrição e:

* gerenciar [entrada e reentrada](#entrance),
* escolher início e término [datas](#dates),
* gerenciar [acesso aos dados](#manage-access),
* definir um [duração do tempo limite](#timeout) em atividades de jornada (somente para usuários administradores),
* selecionar a jornada e o perfil [fusos horários](#timezone)
* atribua Tags unificadas do Adobe Experience Platform à sua jornada para classificá-las facilmente e melhorar a pesquisa na lista de campanhas. [Saiba como trabalhar com tags](../start/search-filter-categorize.md#tags)

![](assets/journey32.png)

>[!NOTE]
>
>Para jornadas ao vivo, essa tela exibe somente a data da publicação e o nome do usuário que publicou a jornada.

A variável **Copiar detalhes técnicos** O permite copiar informações técnicas sobre a jornada que a equipe de suporte pode usar para a solução de problemas. As seguintes informações são copiadas: `JourneyVersion UID`, `OrgID`, `orgName`, `sandboxName`, `lastDeployedBy`, `lastDeployedAt`.


## Entrada e reentrada {#entrance}

Por padrão, novas jornadas permitem a reentrada. Você pode desmarcar a opção **Permitir reentrada** opção para jornadas &quot;one shot&quot;, por exemplo, se você quiser oferecer um presente único quando uma pessoa entrar em uma loja.

Quando a variável **Permitir reentrada** estiver ativada, a variável **Período de espera de reentrada** é exibido. Este campo possibilita definir o tempo de espera antes de permitir que um perfil entre novamente em jornadas unitárias (que começam com um evento ou uma qualificação de público-alvo). Isso impede que uma mesma jornada seja incorretamente acionada várias vezes no mesmo evento. Por padrão, o campo é definido como 5 minutos. A duração máxima é de 29 dias.

Saiba mais sobre o gerenciamento de entrada e reentrada de perfis, em [nesta seção](entry-management.md).

## Gerenciar acesso {#manage-access}

Para atribuir rótulos de uso de dados personalizados ou principais à jornada, clique no botão **[!UICONTROL Gerenciar acesso]** botão. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

## Fusos horários de Jornada e perfil {#timezone}

O fuso horário é definido no nível da jornada. Você pode inserir um fuso horário fixo ou usar perfis do Adobe Experience Platform para definir o fuso horário de jornada. Se um fuso horário for definido no perfil do Adobe Experience Platform, ele poderá ser recuperado na jornada.

Para obter mais informações sobre o gerenciamento de fuso horário, consulte [esta página](../building-journeys/timezone-management.md).

## Datas de início e término {#dates}

Você pode definir um **Data inicial**. Se não tiver especificado um, ele será definido automaticamente no momento da publicação.

Você também pode adicionar um **Data final**. Isso permite que os perfis saiam automaticamente quando a data for atingida. Se nenhuma data final for especificada, os perfis poderão permanecer até que o [tempo limite de jornada global](#global_timeout) (que geralmente dura 91 dias e é reduzido para 7 dias com a oferta complementar do Healthcare Shield). A única exceção são as jornadas recorrentes de leitura de público com **Forçar reentrada na recorrência** ativadas, que terminam na data de início da próxima ocorrência.

## Tempo esgotado {#timeout}

### Tempo limite ou erro em atividades de jornada {#timeout_and_error}

Ao editar uma atividade de ação ou condição, é possível definir um caminho alternativo em caso de erro ou tempo limite. Se o processamento da atividade que interroga um sistema de terceiros exceder a duração do tempo limite definida em **[!UICONTROL Tempo limite ou erro]** das propriedades da jornada, o segundo caminho será escolhido para executar uma possível ação de fallback.

Os valores autorizados estão entre 1 e 30 segundos.

Recomendamos que você defina um período muito curto **[!UICONTROL Tempo limite ou erro]** valor se a jornada for sensível ao tempo (por exemplo: reagir ao local em tempo real de uma pessoa) porque você não pode atrasar a ação por mais de alguns segundos. Se a jornada for menos sensível ao tempo, você poderá usar um valor mais longo para dar mais tempo ao sistema chamado para enviar uma resposta válida.

O Jornada também usa um tempo limite global, conforme detalhado abaixo.

### Tempo limite de jornada global {#global_timeout}

Além do [timeout](#timeout_and_error) usada em atividades de jornada, um tempo limite de jornada global é aplicado. Ele não é exibido na interface e não pode ser alterado.

Esse tempo limite global interrompe o progresso das pessoas físicas na jornada **91 dias** após entrarem. Este tempo limite é reduzido a **7 dias** com a oferta complementar do Healthcare Shield. Isso significa que a jornada de um indivíduo não pode durar mais de 91 dias (ou 7 dias). Após esse período de tempo limite, os dados do indivíduo são excluídos. Os indivíduos que ainda fluem na jornada no final do período de tempo limite serão interrompidos e não serão considerados nos relatórios. Portanto, você poderia ver mais pessoas entrando na jornada do que saindo.

>[!NOTE]
>
>As jornadas não reagem diretamente a solicitações de recusa de privacidade, acesso ou exclusão. No entanto, o tempo limite global garante que os indivíduos nunca fiquem mais de 91 dias em qualquer jornada.

Devido ao tempo limite de jornada de 91 dias, quando a reentrada da jornada não é permitida, não podemos garantir que o bloqueio de reentrada funcionará por mais de 91 dias. De fato, à medida que removemos todas as informações sobre as pessoas que entraram na jornada 91 dias depois de entrarem, não podemos saber a pessoa que entrou anteriormente, há mais de 91 dias.

Um indivíduo só poderá inserir uma atividade de espera se tiver tempo suficiente na jornada para concluir a duração da espera antes do tempo limite de jornada de 91 dias. Consulte [esta página](../building-journeys/wait-activity.md).


#### Perguntas frequentes sobre TTL (Time-to-Live) e retenção de dados {#timeout-faq}

A partir da versão de junho de 2024 do Adobe Journey Optimizer, o tempo limite global do jornada mudou de 30 para 91 dias. Os impactos estão listados nas Perguntas frequentes abaixo:

**Para Jornadas unitárias**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>O que acontece com o jornada publicado depois que a extensão TTL é implantada?</p>
    </td>
    <td>
      <p>Os perfis que entram na nova jornada terão um TTL de 91 dias automaticamente.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um perfil que entra em uma jornada publicada antes do lançamento da extensão TTL?</p>
    </td>
    <td>
      <p>O perfil terá um TTL de 91 dias (7 dias para a HIPAA), consistente com o horário em que a jornada foi originalmente publicada.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um perfil que já entrou em uma jornada quando a extensão TTL é iniciada?</p>
    </td>
    <td>
      <p>O perfil manterá um TTL de 91 dias (7 dias para a HIPAA), de acordo com o tempo de publicação original da jornada.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um perfil em uma versão anterior do jornada republicada após a inicialização da extensão TTL?</p>
    </td>
    <td>
      <p>O perfil manterá um TTL de 91 dias (7 dias para a HIPAA), alinhado ao tempo de publicação da versão original do jornada.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um novo perfil que entra em uma versão republicada do jornada após a inicialização da extensão TTL?</p>
    </td>
    <td>
      <p>O perfil terá um TTL de 91 dias, que corresponde ao TTL da versão do jornada recém-republicada.</p>
    </td>
  </tr>
</table>

**Para Jornadas de acionador de segmento**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>O que acontece com as novas jornadas únicas publicadas após a extensão TTL?</p>
    </td>
    <td>
      <p>Os perfis que entram na nova jornada terão um TTL de 91 dias automaticamente.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com as novas jornadas recorrentes sem reentrada forçada publicadas após a extensão TTL?</p>
    </td>
    <td>
      <p>Os perfis que entram na nova jornada terão um TTL de 91 dias automaticamente.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com as novas jornadas recorrentes com reentrada forçada publicadas após a extensão TTL?</p>
    </td>
    <td>
      <p>Os perfis que entram na nova jornada terão um TTL igual ao período de recorrência. Por exemplo, se a jornada for executada diariamente, o TTL será 1 dia.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um perfil que entra em uma jornada publicada antes do lançamento da extensão TTL?</p>
    </td>
    <td>
      <p>O perfil terá um TTL de 91 dias (7 dias para a HIPAA), consistente com o tempo de publicação original. Para jornadas recorrentes com reentrada forçada, o TTL corresponderá ao período de recorrência.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um perfil executado em uma jornada quando a extensão TTL é iniciada?</p>
    </td>
    <td>
      <p>O perfil manterá um TTL de 91 dias (7 dias para a HIPAA), de acordo com o tempo de publicação original da jornada. Para jornadas recorrentes com reentrada forçada, o TTL corresponderá ao período de recorrência.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um perfil em execução em uma versão anterior do jornada republicada após a inicialização da extensão TTL?</p>
    </td>
    <td>
      <p>O perfil manterá um TTL de 91 dias (7 dias para o HIPPA), alinhado ao tempo de publicação da versão original do jornada. Para jornadas recorrentes com reentrada forçada, o TTL corresponderá ao período de recorrência.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>O que acontece com um novo perfil que entra em uma versão republicada do jornada após a inicialização da extensão TTL?</p>
    </td>
    <td>
      <p>O perfil terá um TTL de 91 dias, que corresponde ao TTL da versão do jornada recém-republicada. Para jornadas recorrentes com reentrada forçada, o TTL corresponderá ao período de recorrência.</p>
    </td>
  </tr>
</table>

## Políticas de mesclagem {#merge-policies}

O Jornada usa políticas de mesclagem ao recuperar dados de perfil do Adobe Experience Platform. Dependendo do tipo de jornada, são usadas diferentes políticas de mesclagem:

* Em Ler jornadas de qualificação de público ou público-alvo: a política de mesclagem do público-alvo é usada
* Em jornadas de eventos unitários: a política de mesclagem padrão é usada
* Nas jornadas de eventos comerciais: a política de mesclagem do público-alvo na seguinte atividade Ler público é usada

O Jornada seguirá a política de mesclagem usada em toda a jornada. Portanto, se vários públicos-alvo forem usados em uma jornada (por exemplo: em funções &quot;inAudience&quot;), criando inconsistências com a política de mesclagem usada pela jornada, um erro será gerado e a publicação será bloqueada. No entanto, se um público-alvo inconsistente for usado na personalização da mensagem, um alerta não será gerado, apesar da inconsistência. Por isso, é altamente recomendável verificar a política de mesclagem associada ao seu público-alvo quando ele for usado na personalização da mensagem.

Para saber mais sobre políticas de mesclagem, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

