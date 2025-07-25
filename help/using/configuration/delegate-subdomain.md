---
solution: Journey Optimizer
product: journey optimizer
title: Delegar um subdomínio
description: Saiba como delegar subdomínios.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, delegação, domínio, DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 7854de133ebcd3b29ca59b747aa89fae242f2ea5
workflow-type: tm+mt
source-wordcount: '1897'
ht-degree: 16%

---

# Delegar um subdomínio {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Delegação de subdomínios"
>abstract="O Journey Optimizer permite delegar os subdomínios à Adobe. Você pode delegar totalmente um subdomínio à Adobe, que é o método recomendado. </br>Você também pode criar um subdomínio usando CNAMEs para apontar para registros específicos do Adobe, mas essa abordagem exige que você mantenha e gerencie registros DNS por conta própria."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation#subdomain-delegation-methods" text="Métodos de configuração de subdomínio"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Delegação de subdomínios"
>abstract="Para começar a enviar emails, você deve delegar seu subdomínio à Adobe. Após a delegação, serão configurados registros DNS, caixas de entrada, remetente e endereços de resposta e rejeição para você."

A delegação de nome de domínio é um método que permite ao proprietário de um nome de domínio (tecnicamente: uma zona DNS) delegar uma subdivisão dele (tecnicamente: uma zona DNS sob ele, que pode ser chamada de subzona) para outra entidade. Basicamente, como cliente, se estiver lidando com a zona &quot;example.com&quot;, você pode delegar a subzona &quot;marketing.example.com&quot; ao Adobe. Saiba mais sobre [delegação de subdomínio](about-subdomain-delegation.md)

Por padrão, o [!DNL Journey Optimizer] permite delegar **até 10 subdomínios**. No entanto, dependendo do contrato de licença, talvez você possa delegar até 100 subdomínios. Fale com seu contato na Adobe para saber mais sobre o número de subdomínios aos quais você tem direito.

É possível:

* Delegar totalmente um subdomínio - [Saiba como](#set-up-subdomain)
* Crie um subdomínio usando CNAMEs para apontar para registros específicos do Adobe - [Saiba como](#set-up-subdomain)

A **delegação de subdomínio completa** é o método recomendado. Saiba mais sobre as diferenças entre os diferentes métodos de configuração de subdomínio em [esta seção](about-subdomain-delegation.md#subdomain-delegation-methods).

>[!CAUTION]
>
>O envio paralelo de subdomínios não tem suporte em [!DNL Journey Optimizer]. Se você tentar enviar um subdomínio para delegação quando outro estiver com o status **[!UICONTROL Processando]**, receberá uma mensagem de erro.

## Acessar subdomínios delegados {#access-delegated-subdomains}

Todos os subdomínios delegados são exibidos no menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Subdomínios]**. Os filtros estão disponíveis para ajudar a refinar a lista (data de delegação, usuário ou status).

<!--![](assets/subdomain-list.png)-->

A coluna **[!UICONTROL Status]** fornece informações sobre o processo de delegação de subdomínio:

* **[!UICONTROL Rascunho]**: a delegação de subdomínio foi salva como rascunho. Clique no nome do subdomínio para retomar o processo de delegação,
* **[!UICONTROL Processando]**: o subdomínio está passando por várias verificações de configuração antes de ser usado,
* **[!UICONTROL Sucesso]**: o subdomínio passou pelas verificações com êxito e pode ser usado para entregar mensagens,
* **[!UICONTROL Falha]**: uma ou várias verificações falharam após o envio da delegação de subdomínio.

Para acessar informações detalhadas sobre um subdomínio com o status **[!UICONTROL Sucesso]**, abra-o na lista.

![](assets/subdomain-delegated.png)

É possível:

* Recupere o nome do subdomínio (somente leitura) configurado durante o processo de delegação, bem como os URLs gerados (recursos, mirror pages, URLs de rastreamento),

* Adicione um registro TXT de verificação de site do Google ao subdomínio para garantir que ele seja verificado (consulte [Adicionar um registro TXT do Google a um subdomínio](google-txt.md)).

>[!CAUTION]
>
>A configuração de subdomínio é comum a todos os ambientes. Portanto, qualquer modificação em um subdomínio também afetará as sandboxes de produção.

## Configurar um subdomínio no Journey Optimizer {#set-up-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Gerar os registros de DNS correspondentes"
>abstract="Para delegar totalmente um novo subdomínio à Adobe, é necessário copiar e colar as informações do servidor de nomes da Adobe exibidas na interface do Journey Optimizer na solução de hospedagem de domínio para gerar os registros DNS correspondentes. Para delegar um subdomínio usando CNAMEs, também é necessário copiar e colar o registro de validação SSL do URL do CDN. Depois que as verificações forem bem-sucedidas, o subdomínio estará pronto para ser usado para entregar mensagens."

Para configurar um novo subdomínio em [!DNL Journey Optimizer], siga as etapas abaixo.

>[!NOTE]
>
>Esta seção descreve como configurar um subdomínio usando a delegação completa ou os métodos CNAME. O método de delegação personalizado está detalhado em [esta seção](#setup-custom-subdomain).


1. Acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** > **[!UICONTROL Subdomínios]** e clique em **[!UICONTROL Configurar subdomínio]**.

   <!--![](assets/subdomain-delegate.png)-->

   >[!CAUTION]
   >
   >A configuração de subdomínio é **comum a todos os ambientes**. Portanto, qualquer modificação em um subdomínio também afeta as sandboxes de produção.

1. Na seção **[!UICONTROL Configurar método]**, selecione:

   * Totalmente delegado - [Saiba mais](about-subdomain-delegation.md#full-subdomain-delegation)
   * Configuração de CNAME - [Saiba mais](about-subdomain-delegation.md#cname-subdomain-setup)

     Saiba como configurar subdomínios com CNAMEs nesta [seção dedicada](#cname-subdomain-setup)

   <!--![](assets/subdomain-method-full.png)-->

1. Especifique o nome do subdomínio que será delegado.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Não é permitido delegar um subdomínio inválido à Adobe. Insira um subdomínio válido de propriedade de sua organização, como marketing.yourcompany.com.
   >
   >Você não pode usar o mesmo domínio de envio para enviar mensagens de [!DNL Adobe Journey Optimizer] e de outro produto, como [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage].

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. Configurar **[!UICONTROL registro do DMARC]** na seção dedicada. Se o subdomínio tiver um [registro DMARC](dmarc-record.md) existente e for buscado por [!DNL Journey Optimizer], você poderá usar os mesmos valores ou alterá-los conforme necessário. Se você não adicionar nenhum valor, os valores padrão serão usados. [Saiba como gerenciar registros do DMARC](dmarc-record.md#set-up-dmarc)

   ![](assets/dmarc-record-found.png)

1. Na seção **[!UICONTROL Registro DNS]**, a lista de registros a serem colocados em seus servidores DNS é exibida. Copie esses registros, um por um ou baixando um arquivo CSV, e navegue até a solução de hospedagem de domínio para gerar os registros DNS correspondentes.

1. Verifique se todos os registros DNS foram gerados em sua solução de hospedagem de domínio. Se tudo estiver configurado corretamente, marque a caixa &quot;Confirmo...&quot;.

   ![](assets/subdomain-submit.png)

1. Se você estiver configurando um subdomínio com **CNAMEs**, vá para [esta seção](#cname-subdomain-setup).

1. Clique em **[!UICONTROL Enviar]** para que o Adobe execute as verificações necessárias. [Saiba mais](#submit-subdomain)

## Configurar um subdomínio com CNAMEs {#cname-subdomain-setup}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Gerar o DNS correspondente e os registros de validação"
>abstract="Para delegar um subdomínio usando CNAMEs, é necessário copiar e colar as informações do servidor de nomes da Adobe e o registro de validação do URL CDN do SSL exibido na interface do Journey Optimizer em sua plataforma de hospedagem. Depois que as verificações forem bem-sucedidas, o subdomínio estará pronto para ser usado para entregar mensagens."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="Copiar o registro de validação"
>abstract="A Adobe gera um registro de validação. Você precisa criar o registro correspondente em sua plataforma de hospedagem para validação de URL de CDN."

Ao configurar um subdomínio, você pode usar CNAMEs para apontar para registros específicos do Adobe. Usando essa configuração, você e a Adobe compartilham a responsabilidade pela manutenção do DNS.

>[!CAUTION]
>
>O método CNAME é recomendado se as políticas de sua organização restringirem o método completo de delegação de subdomínio. Essa abordagem exige que você mantenha e gerencie registros DNS por conta própria.
>
>O Adobe não poderá ajudar na alteração, manutenção ou gerenciamento de DNS em um subdomínio configurado por meio do método CNAME.

Para configurar um subdomínio usando CNAMEs, siga as etapas abaixo.

1. Execute todas as etapas descritas em [esta seção](#set-up-subdomain).

1. Antes de enviar a configuração de subdomínio, você tem mais uma etapa a concluir - clique em **[!UICONTROL Continuar]**. Aguarde até que o Adobe verifique se os registros são gerados sem erros na solução de hospedagem. Esse processo pode levar até 2 minutos.

   >[!NOTE]
   >
   >Verifique se todos os registros foram criados corretamente antes de continuar.

1. O Adobe gera um registro de validação de URL CDN SSL. Copie este registro de validação na plataforma de hospedagem. Se você criou corretamente esse registro na solução de hospedagem, marque a caixa &quot;Confirmo...&quot;.

1. Clique em **[!UICONTROL Enviar]** para que o Adobe execute as verificações necessárias. [Saiba mais](#submit-subdomain)

➡️ [Saiba como criar um subdomínio usando CNAME para apontar para registros específicos do Adobe neste vídeo](#video)

## Enviar a configuração do subdomínio {#submit-subdomain}

Para concluir a delegação de subdomínio, siga as etapas abaixo.

1. Clique em **[!UICONTROL Enviar]**.

   >[!NOTE]
   >
   >Se ocorrer um erro ao tentar enviar um subdomínio personalizado, consulte [esta seção](#check-list).


1. Você pode criar os registros e enviar a configuração de subdomínio posteriormente usando o botão **[!UICONTROL Salvar como rascunho]**.

   >[!NOTE]
   >
   >Você poderá retomar a delegação de subdomínio abrindo-a na lista de subdomínios.

1. O subdomínio é exibido na lista com o status **[!UICONTROL Processando]**. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](#access-delegated-subdomains).

   <!--![](assets/subdomain-processing.png)-->

1. Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que o Adobe execute as verificações necessárias, que podem levar até 3 horas. [Saiba mais](#subdomain-validation).

   >[!NOTE]
   >
   >Verifique se todos os registros foram criados corretamente antes de continuar.

### Validação de subdomínio {#subdomain-validation}

As verificações e ações abaixo são executadas até que o subdomínio seja verificado e possa ser usado para enviar mensagens.

Estas etapas são executadas pela Adobe e podem levar **até 3 horas**.

1. **Pré-validar**: o Adobe verifica se o subdomínio foi delegado ao DNS do Adobe (registro NS, registro SOA, configuração de zona, registro de propriedade). Se a etapa de pré-validação falhar, um erro será retornado junto com o motivo correspondente; caso contrário, o Adobe continuará para a próxima etapa.

1. **Configurar DNS para o domínio**:

   * **Registro MX**: registro Mail eXchange - registro do servidor de email que processa emails de entrada enviados para o subdomínio.
   * **Registro SPF**: registro da Estrutura de Política do Remetente - Lista os IPs dos servidores de email que podem enviar emails do subdomínio.
   * **Registro do DKIM**: registro padrão DomainKeys Identified Mail - Usa criptografia de chave pública-privada para autenticar a mensagem e evitar falsificação.
   * **A**: mapeamento de IP padrão.
   * **CNAME**: um registro CNAME ou Nome Canônico é um tipo de registro DNS que mapeia um nome de alias para um nome de domínio verdadeiro ou canônico.

1. **Criar URLs de rastreamento e espelho**: se o domínio for email.example.com, o domínio de rastreamento/espelho será data.email.example.com. É protegido por meio da instalação do certificado SSL.

1. **Provisionar CDN CloudFront**: se o CDN ainda não estiver configurado, a Adobe o provisionará para a ID da sua organização.

1. **Criar domínio CDN**: se o domínio for email.example.com, o domínio CDN será cdn.email.example.com.

1. **Criar e anexar certificado SSL de CDN**: a Adobe cria o certificado CDN para o domínio CDN e anexa o certificado ao domínio CDN.

1. **Criar DNS de encaminhamento**: se este for o primeiro subdomínio que você está delegando, a Adobe criará o DNS de encaminhamento necessário para criar registros PTR - um para cada um de seus IPs.

1. **Criar registro PTR**: o registro PTR, também conhecido como registro de DNS reverso, é exigido pelos ISPs para que eles não marquem os emails como spam. O Gmail também recomenda ter registros PTR para cada IP. O Adobe cria registros PTR somente quando você delega um subdomínio pela primeira vez, um para cada IP, todos os IPs que apontam esse subdomínio. Por exemplo, se o IP for *192.1.2.1* e o subdomínio for *email.example.com*, o registro PTR será: *192.1.2.1PTR r1.email.example.com*. Você pode atualizar o registro PTR posteriormente para apontar para o novo domínio delegado. [Saiba mais sobre registros PTR](ptr-records.md)

Depois que as verificações forem bem-sucedidas, o subdomínio obterá o status **[!UICONTROL Success]**. Ele está pronto para ser usado para enviar mensagens.

O subdomínio será marcado como **[!UICONTROL Falha]** se você não criar o registro de validação na solução de hospedagem.

Após validar o registro, o Adobe cria automaticamente o registro PTR para o subdomínio. [Saiba mais](ptr-records.md)

## Cancelar delegação de um subdomínio {#undelegate-subdomain}

Se quiser cancelar a delegação de um subdomínio, entre em contato com o representante da Adobe.

No entanto, é necessário executar várias etapas na interface do usuário antes de acessar o Adobe.

>[!NOTE]
>
>Você só pode desdelegar subdomínios com o status **[!UICONTROL Sucesso]**. Subdomínios com os status **[!UICONTROL Rascunho]** e **[!UICONTROL Falha]** podem simplesmente ser excluídos da interface do usuário.

Primeiro, execute as seguintes etapas no [!DNL Journey Optimizer]:

1. Desative todas as configurações de canal associadas ao subdomínio. [Saiba como](../configuration/channel-surfaces.md#deactivate-a-surface)

1. Cancele a delegação de qualquer subdomínio de página de aterrissagem, subdomínio SMS e subdomínio da Web associado a esse subdomínio.

   Você precisa levantar uma solicitação dedicada para cada [página de aterrissagem](../landing-pages/lp-subdomains.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain) ou [subdomínio da Web](../web/web-delegated-subdomains.md#undelegate-subdomain).

1. Interrompa as campanhas ativas associadas aos subdomínios. [Saiba como](../campaigns/modify-stop-campaign.md#stop)

1. Interrompa as jornadas ativas associadas aos subdomínios. [Saiba como](../building-journeys/end-journey.md#stop-journey)

1. Aponte os [registros PTR](ptr-records.md#edit-ptr-record) vinculados ao subdomínio para outro subdomínio.

   Se esse for o único subdomínio delegado, ignore esta etapa.

Depois de concluir, entre em contato com o representante da Adobe com o subdomínio que você deseja cancelar a delegação.

Depois que a solicitação for tratada pela Adobe, o domínio não delegado não será mais exibido na página de inventário do subdomínio.

>[!CAUTION]
>
>Depois que a delegação de um subdomínio é cancelada, o seguinte se aplica:
>
>* Não é possível reativar as configurações de canal que estavam usando esse subdomínio.
>* Não é possível delegar o mesmo subdomínio novamente por meio da interface do usuário. Caso deseje, entre em contato com o representante da Adobe.

## Vídeo tutorial{#video}

Saiba como criar um subdomínio usando CNAME para apontar para registros específicos do Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/342240?quality=12&captions=por_br)
