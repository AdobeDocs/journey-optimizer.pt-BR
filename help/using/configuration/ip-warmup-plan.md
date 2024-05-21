---
solution: Journey Optimizer
product: journey optimizer
title: Criar um plano de aquecimento de IP
description: Saiba como criar um plano de aquecimento de IP no Journey Optimizer
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupo, subdomínios, capacidade de entrega
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: c400104c86e1a9a2de819db7743b3f77153ad90b
workflow-type: tm+mt
source-wordcount: '1674'
ht-degree: 8%

---

# Criar um plano de aquecimento de IP {#ip-warmup}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução aos planos de aquecimento de IP](ip-warmup-gs.md)
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* **[Criar um plano de aquecimento de IP](ip-warmup-plan.md)**
* [Executar o plano de aquecimento de IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Depois de criar um ou mais [Campanhas de aquecimento de IP](ip-warmup-campaign.md) com uma superfície dedicada e a opção correspondente ativada, você pode começar a criar seu plano de aquecimento de IP.

Para acessar, criar, editar e excluir os planos de aquecimento de IP, você deve ter a **[!UICONTROL Consultor de avaliação de entrega]** função ou planos de aquecimento de IP relacionados a permissões.

+++Saiba como atribuir a função de Consultor de capacidade de entrega ou as permissões relacionadas a planos de aquecimento de IP

O controle de acesso no nível do objeto permite proteger dados e conceder acesso específico para visualizar e gerenciar seus planos. Se nenhum rótulo for atribuído ao seu plano de aquecimento de IP, ele será aberto para visualização e edição por todos os usuários.

A concessão da **[!UICONTROL Exibir planos de aquecimento de IP]** restringe o acesso somente à exibição e publicação, enquanto atribui a **[!UICONTROL Gerenciar planos de aquecimento de IP]** permite que os usuários visualizem e editem o plano.

Para atribuir a permissão correspondente a um **[!UICONTROL Função]**:

1. No [!DNL Permissions] produto, navegue até o **[!UICONTROL Funções]** e selecione a função que deseja atualizar com o novo **[!UICONTROL Configurações de Warmup de IP]** permissões.

1. Do seu **[!UICONTROL Função]** painel, clique em **[!UICONTROL Editar]**.

   ![](assets/ip_permissions_1.png)

1. Arraste e solte a **[!UICONTROL Configurações de Warmup de IP]** recurso para atribuir permissão.

1. No **[!UICONTROL Configurações de Warmup de IP]** selecione as permissões de que seu usuário precisa: **[!UICONTROL Exibir planos de aquecimento de IP]**, **[!UICONTROL Gerenciar planos de aquecimento de IP]**, e/ou **[!UICONTROL Exibir relatórios de aquecimento de IP]**. Você pode selecioná-los todos de uma vez, se necessário.

   ![](assets/ip_permissions_2.png)

1. Clique em **[!UICONTROL Salvar]**.

Para atribuir a função correspondente a um **[!UICONTROL Usuário]**:

1. No [!DNL Permissions] produto, navegue até o **[!UICONTROL Funções]** e selecione o **[!UICONTROL Consultor de avaliação de entrega]** função interna.

1. Do seu **[!UICONTROL Função]** painel, acesse o **[!UICONTROL Usuários]** guia.

   ![](assets/ip_permissions_3.png)

1. Clique em **[!UICONTROL Adicionar usuário]** para atribuir o **[!UICONTROL Consultor de avaliação de entrega]** função interna.

   ![](assets/ip_permissions_4.png)

1. Selecione o **[!UICONTROL Usuário]** e clique em **[!UICONTROL Salvar]**.

   ![](assets/ip_permissions_5.png)

+++

## Preparar o arquivo do plano de aquecimento de IP {#prepare-file}

O aquecimento de IP é uma atividade que consiste em aumentar gradualmente o volume de emails que saem de seus IPs e domínios para os principais provedores de serviços de Internet (ISPs), a fim de estabelecer sua reputação como remetente legítimo.

Normalmente, essa atividade é realizada com a ajuda de um especialista em capacidade de entrega que ajuda a preparar um plano bem pensado com base nos domínios do setor, casos de uso, regiões, ISPs e vários outros fatores.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Antes de poder criar um plano de aquecimento de IP no [!DNL Journey Optimizer] é necessário preencher um modelo do Excel com todos os dados que alimentarão seu plano.

* Na interface do usuário, é possível baixar o Excel em branco [Modelo de plano de aquecimento de IP](assets/IPWarmupPlan-Template.xlsx) para preencher.

* Você também pode baixar um [exemplo de plano de aquecimento de IP](assets/IPWarmupPlan-Sample.xlsx) já preenchido com alguns dados que você pode usar como exemplo.

<!--
* From the user interface you can download the blank Excel IP warmup plan template to fill in.

* You can also download a sample IP warmup plan already filled in with some data you can use as an example.
-->

>[!CAUTION]
>
>Trabalhe com seu consultor de entrega para garantir que seu arquivo de plano de aquecimento de IP esteja configurado corretamente.
>
>Use o formato fornecido no modelo.

Veja abaixo um exemplo de um arquivo contendo um plano de aquecimento de IP.

![](assets/ip-warmup-sample-file.png)

### Guia Plano de aquecimento de IP {#ip-warmup-plan-tab}

* Neste exemplo, um plano foi preparado abrangendo mais de 17 dias (chamado de &quot;**execuções**&quot;) para atingir um volume-alvo de mais de um milhão de perfis.

* Este plano é executado até seis **fases**, cada um deles contendo pelo menos uma execução.

* Você pode ter quantas colunas quiser para os domínios que deseja entregar. Neste exemplo, o plano é dividido em seis colunas:

   * Quatro dos quais correspondem a **grupos de domínio prontos para uso** para usar no seu plano (Gmail, Microsoft, Yahoo e Orange).
   * Um corresponde a um grupo de domínio personalizado (que você precisa adicionar usando o [Grupo de domínio personalizado](#custom-domain-group-tab) guia ).
   * A sexta coluna, **Outros**, contém todos os endereços restantes de outros domínios que não estão explicitamente cobertos no plano. Essa coluna é opcional: se omitida, os emails irão somente para os domínios especificados.

A ideia é aumentar progressivamente o número de endereços direcionados em cada execução, enquanto reduz o número de execuções para cada fase.

Os grupos de domínio principais predefinidos que você pode adicionar ao seu plano estão listados abaixo:

<!--
* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Orange
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple
-->

+++ Gmail gmail.com;google.com;googlemail.com;googlemail.co.uk
+++

+++WP;wp.pl;o2.pl
+++

+++Comcast comcast.net
+++

+++Yahoo.aol;fi;games.com;cs.com;yahoo.com.in;y7mail.com;yahoo.co.uk;yahoo.hu;yahoo.co.hu;yahoo.cn;yahoogroups.com.sg;aol.es;yahoogroups.com.au;yahoo.ca;aol.hk;yahoo.com.au;aolpoland.pl;aolnorge.no;yahoo.com.vn;yahoo.fi;aol.co.nz;yahoo.com.br;yahoo.hr;aol.cz;yahoo.ee;aol.be;aolcom.tr;yahoo.si;yahoo.ne.jp;aol.it;ymail.com;yaol.it;netscape.com;yaol;yahoo.com.pe;yaol ahoo.es;yahoo.dk;yahoogroups.ca;yahoo.co.id;citlink.net;aol.kr;yahoo.ie;aol.jp;wmconnect.com;yahoo.lt;yahoo.com.jp;aol.nl;yahoo.com.hk;yahoo.bg;aol.com.br;aol.se;yahoo.co.kr;yahoo.de;yahoo.com.ar;ygm.com;yahoo.nl;yahoo.co.nz;aol.dk;aol.com;aol.cl;goowy.com;yahoo.no;rocketmail.com;yahoo.cz;frontiernet.net;yahoo.cz;aim.com;yahoo hoo.sk;yahoogroups.co.in;yahoogroups.de;yahoo.gr;netscape.net;yahoo.ro;luckymail.com;yahoo.at;yahoo.co.jp;yahoo.com.kr;yahoo.co.za;aol.fr;yahoo.in;aol.in;verizon.net;yahoo.rs;aol.de;aol.com.ve;aol.com.ar;aol.com.co;wild4music.com;yahoo.se;myaol.jp;yahoogroups.com.cn;yahoo.pt;yahoo.com.co;wow.com;yahoogrupper.dk;yahoo.fr;yahoo.com;aol.aol l;yahooxtra.co.nz;yahoo.com.mx;aol.ch;yahoo.it;yahoo.com.ph;sky.com;aolpolcka.pl;aol.com.mx;aol.com.au;yahoogruppi.it;aolchina.com;yahoo.cl;yahoo.com.net;yahoo.com.tw;talk21.com;yahoo.be;compuserve.com;aol.tw;yahoo.com.sg;yahoogroups.com.tw;frontier.com;yahoo.co.in;yahoo.co.il;verizon.net.in;yahoo.com.tr;yahoogroups.com.hk;aol.ru;yahoogroups.co.uk yahoo.com.biz yahoo.com.hr aol.co.uk ybb.ne.jp yahoogroups.co.kr yahoo.com.my rogers.com gte.net yahoogroups.com yahoo.co.th yahoo.com.cn love.com bellatlantic.net yahoo.com.ve yahoo.com.ua;yahoo.lv;aolpolska.pl;aol.at;yahoo.pl
+++

+++Bigpond bigpond.com;bigpond.com.au;bigpond.net;telstra.com;bigpond.net.au
+++

+++Laranja voila.com;francetelecom.com;orange.com;orange.fr;wanadoo.fr;voila.fr
+++

+++Softbank c.vodafone.ne.jp;jp-h.ne.jp;k.vodafone.ne.jp;jp-d.ne.jp;jp-c.ne.jp;t.vodafone.ne.jp;h.vodafone.ne.jp;r.vodafone.ne.jp;q.vodafone.ne.jp;jp-t.ne.jp;jp-q.ne.jp;s.vodafone.ne.jp;jp-s.ne.jp;jp-r.ne.jp;jp-k.ne.jp;n.vodafone.ne.jp;d.vodafone.ne.jp;softbank.ne.jp;jp-n.ne.jp
+++

+++DoCoMo docomo.ne.jp
+++

+++United Internet gmx.de;1and1.com;gmx.fr;mail.com;1und1.de;gmx.com;gmx.net;gmx.at;web.de;gmx.ch
+++

+++Microsoft hotmail.com.tr;live.de;live.ru;live.nl;windowslive.com;live.jp;mts.net;xbox.com;hotmail.fr;hotmail.cl;hotmail.jp;live.cl;live.at;live.com.au;live.hk;hotmail.co.th;hotmail.com.au;hotmail.com;live.com.my;hotmail.co.kr;live.ie;outlook.com.br;hotmail.dk;hotmail.co.il;live.co.kr;outlook.ie;live.cn;live.co.uk;live.com.mx;hotmail.es;live.fr;live.no;live.dk;hotmail.it;hotmail.co.uk;live.se;live.com.sg;msn.com;.be;hotmail.co.jp;live.in;hotmail.se;live.co.za;hotmail.ch;live.com.pt;outlook.com;hotmail.gr;live.it;live.com;hotmail.ca;live.com.ar;hotmail.com.br hotmail.com.ar;live.ca;hotmail.de
+++

+++KDDI au.com;ezweb.ne.jp;uqmobile.jp
+++

+++Italia Online inwind.it;blu.it;virgilio.it;giallo.it;iol.it;libero.it
+++

+++La Poste laposte.net
+++

+++Apple mac.com;icloud.com;apple.com;me.com
+++

### Guia Grupo de domínio personalizado {#custom-domain-group-tab}

Você também pode adicionar mais colunas ao seu plano, incluindo grupos de domínio personalizados.

Use o **[!UICONTROL Grupo de domínio personalizado]** para definir um novo grupo de domínio. Para cada domínio, você pode adicionar todos os subdomínios que ele abrange.<!--TBC-->

Certifique-se de que cada domínio seja exclusivo do seu grupo de domínio e não se sobreponha a outros grupos de domínio. Como os grupos de domínio globais são definidos automaticamente, os usuários devem considerar isso ao criar grupos de domínio personalizados.

Por exemplo, se você adicionar o domínio personalizado Luma, desejará que os seguintes subdomínios sejam incluídos: luma.com, luma.co.uk, luma.it, luma.fr, luma.de, etc.

![](assets/ip-warmup-sample-file-custom.png)

### Exemplo {#example}

Digamos que você queira ter dois grupos de domínio personalizados:

* Um somente para domínios do Hotmail.
* Um para todos os outros domínios do grupo de domínio Microsoft (excluindo todos os domínios do Hotmail).

Observe que todos os outros domínios serão coletados na variável **[!UICONTROL Outros]** coluna.

1. No **[!UICONTROL Grupo de domínio personalizado]** , crie a **Hotmail** grupo de domínio.

1. Adicione todos os domínios do Hotmail na mesma linha.

   Você pode [copiar e colar](#copy-paste) todos os domínios do Hotmail listados na variável [Guia Plano de aquecimento de IP](#ip-warmup-plan-tab) seção.

1. Adicione outra linha.

1. Crie o **Microsoft_X** grupo de domínio.

1. Adicione todos os domínios do Microsoft que não são do Hotmail na mesma linha. Da mesma forma, você pode copiá-los e colá-los da lista acima. [Saiba mais](#copy-paste)

1. Volte para o **[!UICONTROL Plano de aquecimento de IP]** guia.

1. Crie três colunas: uma para **Hotmail**, um para **Microsoft_X** e um para **Outros**.

1. Preencha as colunas de acordo com suas necessidades.

>[!NOTE]
>
>Depois que o plano de aquecimento de IP for carregado em [!DNL Journey Optimizer], não será necessário excluir os grupos de domínio do Microsoft.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Copiar e colar domínios padrão {#copy-paste}

Se quiser criar um grupo de domínios personalizado contendo todos os domínios do Hotmail, por exemplo, você pode copiar e colar os domínios da lista padrão fornecida [acima](#ip-warmup-plan-tab).

Em seguida, use a ferramenta de conversão do Excel para converter texto em colunas:

1. Selecionar **[!UICONTROL Dados]** > **[!UICONTROL Texto para colunas...]**, escolha **[!UICONTROL Delimitado]** e selecione **[!UICONTROL Próxima]**.

1. Selecionar **[!UICONTROL Ponto e vírgula]**, clique em **[!UICONTROL Próxima]** e **[!UICONTROL Concluir]**.

Cada domínio agora é exibido em uma coluna diferente na mesma linha.

## Acessar e gerenciar planos de aquecimento de IP {#manage-ip-warmup-plans}

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Planos de aquecimento de IP]** menu. Todos os planos de aquecimento de IP criados até o momento são exibidos.

   ![](assets/ip-warmup-filter-list.png)

1. Você pode filtrar pelo status. Os diferentes status são:

   * **Não iniciado**: nenhuma execução foi ativada ainda. [Saiba mais](ip-warmup-execution.md#define-runs)
   * **Ao vivo**: o plano muda para esse status assim que a primeira execução na primeira fase é ativada com sucesso. [Saiba mais](ip-warmup-execution.md#define-runs)
   * **Concluído**: o plano foi marcado como concluído. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [Saiba mais](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Para excluir um plano de aquecimento de IP, selecione o **[!UICONTROL Excluir]** ícone ao lado do nome de um plano e confirmar a exclusão.

   >[!NOTE]
   >
   >Somente planos com o **Não iniciado** O status pode ser excluído.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >O plano de aquecimento de IP selecionado será excluído permanentemente.

## Criar um plano de aquecimento de IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Especifique o seu plano de aquecimento de IP"
>abstract="Preencha o modelo do Excel com todos os dados que alimentarão seu plano, como fases de aquecimento de IP e número-alvo de perfis, e faça upload dele aqui."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-plan.html?lang=pt-BR#prepare-file" text="Preparar o arquivo do plano de aquecimento de IP"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Selecione uma superfície de marketing"
>abstract="Você precisa selecionar a mesma superfície que a selecionada na campanha que deseja associar ao plano de aquecimento de IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=pt-BR" text="Configurar superfícies de canais"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=pt-BR" text="Criar campanhas de aquecimento de IP"

Para criar um plano de aquecimento de IP, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Planos de aquecimento de IP]** e clique em **[!UICONTROL Criar plano de aquecimento de IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Preencha os detalhes do plano de aquecimento de IP: dê a ele um nome e uma descrição.

   ![](assets/ip-warmup-plan-details.png)

1. Selecione o [superfície](channel-surfaces.md) que você quer aquecer. Somente as superfícies de marketing estão disponíveis para seleção. [Saiba mais sobre tipo de email](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >As campanhas que você deseja associar ao plano de aquecimento de IP devem usar a mesma superfície. [Saiba como criar uma campanha de aquecimento de IP](ip-warmup-campaign.md)

1. Carregue o arquivo do Excel que contém seu plano de aquecimento de IP. [Saiba mais](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >Caso o upload falhe, verifique se você está usando a formatação e o formato de arquivo corretos (.xls ou .xlsx). Use o [modelo](assets/IPWarmupPlan-Template.xlsx) fornecido a você pelo Adobe.

1. Clique em **[!UICONTROL Criar]**. Todas as fases, execuções, colunas e seu conteúdo definido no arquivo que você carregou são automaticamente exibidas na [!DNL Journey Optimizer] interface.

   ![](assets/ip-warmup-plan-uploaded.png)

   >[!NOTE]
   >
   >A variável **[!UICONTROL Direcionado]** mostra a soma de todos os perfis segmentados para cada execução, ou seja, todos os perfis de cada grupo de domínio que você definiu, incluindo o **Outros** coluna, se houver.

Agora você está pronto para executar seu plano de aquecimento de IP. [Saiba mais](ip-warmup-execution.md)
