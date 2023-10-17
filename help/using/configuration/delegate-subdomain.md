---
solution: Journey Optimizer
product: journey optimizer
title: Delegar um subdomínio
description: Saiba como delegar subdomínios.
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, delegação, domínio, DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: c4b8a74541a3fb9fea054bd1145592d75c62b165
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 23%

---

# Delegar um subdomínio {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Delegação de subdomínios"
>abstract="O Journey Optimizer permite delegar os subdomínios à Adobe. Você pode delegar totalmente um subdomínio à Adobe, que é o método recomendado. Você também pode criar um subdomínio usando CNAMEs para apontar para registros específicos da Adobe, mas esse método exige que você mantenha e gerencie registros DNS por conta própria."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation.html#subdomain-delegation-methods" text="Métodos de configuração de subdomínio"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Delegação de subdomínios"
>abstract="Para começar a enviar emails, você deve delegar seu subdomínio à Adobe. Após a delegação, serão configurados registros DNS, caixas de entrada, remetente e endereços de resposta e rejeição para você."

A delegação de nome de domínio é um método que permite ao proprietário de um nome de domínio (tecnicamente: uma zona DNS) delegar uma subdivisão dele (tecnicamente: uma zona DNS sob ele, que pode ser chamada de subzona) para outra entidade. Basicamente, como cliente, se estiver lidando com a zona &quot;example.com&quot;, você pode delegar a subzona &quot;marketing.example.com&quot; ao Adobe. Saiba mais sobre [delegação de subdomínio](about-subdomain-delegation.md)

>[!NOTE]
>
>Por padrão, [!DNL Journey Optimizer] o contrato de licença permite delegar até 10 subdomínios. Entre em contato com o Adobe se desejar aumentar essa limitação.

Você pode delegar totalmente um subdomínio ou criar um subdomínio usando CNAMEs para apontar para registros específicos de Adobe.

>[!CAUTION]
>
>A delegação completa de subdomínio é o método recomendado. Saiba mais sobre as diferenças entre os dois [métodos de configuração de subdomínio](about-subdomain-delegation.md#subdomain-delegation-methods).
>
>A configuração de subdomínio é comum a todos os ambientes. Portanto, qualquer modificação em um subdomínio também afetará as sandboxes de produção.

## Delegação total de subdomínio {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Gerar os registros DNS correspondentes"
>abstract="Para delegar totalmente um novo subdomínio à Adobe, é necessário copiar e colar as informações do servidor de nomes da Adobe exibidas na interface do Journey Optimizer na solução de hospedagem de domínio para gerar os registros DNS correspondentes. Para delegar um subdomínio usando CNAMEs, também é necessário copiar e colar o registro de validação SSL do URL do CDN. Depois que as verificações forem bem-sucedidas, o subdomínio estará pronto para ser usado para entregar mensagens."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain.html#cname-subdomain-delegation" text="Delegação de subdomínio CNAME"

[!DNL Journey Optimizer] O permite delegar totalmente os subdomínios ao Adobe diretamente da interface do produto. Ao fazer isso, o Adobe poderá enviar mensagens como um serviço gerenciado, controlando e mantendo todos os aspectos do DNS necessários para fornecer, renderizar e rastrear campanhas de email.

Você pode confiar no Adobe para manter a infraestrutura de DNS necessária para atender aos requisitos de capacidade de entrega padrão do setor para seus domínios de envio de marketing por email, enquanto continua mantendo e controlando o DNS para seus domínios de email internos.

Para delegar totalmente um novo subdomínio ao Adobe, siga as etapas abaixo:

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Subdomínios]** e clique em **[!UICONTROL Configurar subdomínio]**.

   ![](assets/subdomain-delegate.png)

1. Selecionar **[!UICONTROL Totalmente delegado]** do **[!UICONTROL Configurar método]** seção.

   ![](assets/subdomain-method-full.png)

1. Especifique o nome do subdomínio que será delegado.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Não é permitido delegar um subdomínio inválido a Adobe. Insira um subdomínio válido de propriedade de sua organização, como marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. A lista de registros que serão colocados em seus servidores DNS é exibida. Copie esses registros, um por um ou baixando um arquivo CSV, e navegue até a solução de hospedagem de domínio para gerar os registros DNS correspondentes.

1. Verifique se todos os registros DNS foram gerados em sua solução de hospedagem de domínio. Se tudo estiver configurado corretamente, marque a caixa &quot;Confirmo...&quot; e clique em **[!UICONTROL Enviar]**.

   ![](assets/subdomain-submit.png)

   >[!NOTE]
   >
   >É possível criar os registros e enviar a configuração de subdomínio posteriormente usando o **[!UICONTROL Salvar como rascunho]** botão. Você poderá retomar a delegação de subdomínio abrindo-a na lista de subdomínios.

1. Depois que a delegação completa de subdomínio for enviada, o subdomínio será exibido na lista com o **[!UICONTROL Processando]** status. Para obter mais informações sobre os status dos subdomínios, consulte [nesta seção](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que o Adobe execute as verificações necessárias, que podem levar até 3 horas. Saiba mais [nesta seção](#subdomain-validation).

   >[!NOTE]
   >
   >Todos os registros ausentes, ou seja, os registros ainda não criados em sua solução de hospedagem, serão listados.

1. Depois que as verificações forem bem-sucedidas, o subdomínio obterá o **[!UICONTROL Sucesso]** status. Ele está pronto para ser usado para enviar mensagens.

   >[!NOTE]
   >
   >O subdomínio será marcado como **[!UICONTROL Failed]** se você não criar o registro de validação na solução de hospedagem.

Depois que um subdomínio é delegado ao Adobe em [!DNL Journey Optimizer], um registro PTR é criado e associado automaticamente a esse subdomínio. [Saiba mais](ptr-records.md)

>[!CAUTION]
>
>No momento, a execução paralela de subdomínios não é compatível com o [!DNL Journey Optimizer]. Se você tentar enviar um subdomínio para delegação quando outro tiver o **[!UICONTROL Processando]** , você receberá uma mensagem de erro.

## Delegação de subdomínio CNAME {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Gerar o DNS correspondente e os registros de validação"
>abstract="Para delegar um subdomínio usando CNAMEs, é necessário copiar e colar as informações do servidor de nomes da Adobe e o registro de validação do URL CDN do SSL exibido na interface do Journey Optimizer em sua plataforma de hospedagem. Depois que as verificações forem bem-sucedidas, o subdomínio estará pronto para ser usado para entregar mensagens."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="Copiar o registro de validação"
>abstract="A Adobe gera um registro de validação. Você precisa criar o registro correspondente em sua plataforma de hospedagem para validação de URL de CDN."

Se você tiver políticas de restrição específicas de domínio e quiser que o Adobe tenha somente controle parcial sobre o DNS, poderá optar por realizar todas as atividades relacionadas ao DNS da sua parte.

A delegação de subdomínio CNAME permite criar um subdomínio e usar CNAMEs para apontar para registros específicos da Adobe. Com essa configuração, você e a Adobe compartilham a responsabilidade pela manutenção do DNS para configurar o ambiente para enviar, renderizar e rastrear emails.

>[!CAUTION]
>
>O método CNAME é recomendado se as políticas de sua organização restringirem o método completo de delegação de subdomínio. Essa abordagem exige que você mantenha e gerencie registros DNS por conta própria. O Adobe não poderá ajudar na alteração, manutenção ou gerenciamento de DNS em um subdomínio configurado por meio do método CNAME.

➡️ [Saiba como criar um subdomínio usando CNAME para apontar para registros específicos de Adobe neste vídeo](#video)

Para delegar um subdomínio usando CNAMEs, siga as etapas abaixo:

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Subdomínios]** e clique em **[!UICONTROL Configurar subdomínio]**.

1. Selecione o **[!UICONTROL Configuração de CNAME]** método.

   ![](assets/subdomain-method-cname.png)

1. Especifique o nome do subdomínio que será delegado.

   >[!CAUTION]
   >
   >Não é permitido delegar um subdomínio inválido a Adobe. Insira um subdomínio válido de propriedade de sua organização, como marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. A lista de registros que serão colocados em seus servidores DNS é exibida. Copie esses registros, um por um ou baixando um arquivo CSV, e navegue até a solução de hospedagem de domínio para gerar os registros DNS correspondentes.

1. Verifique se todos os registros DNS foram gerados em sua solução de hospedagem de domínio. Se tudo estiver configurado corretamente, marque a caixa &quot;Confirmo...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

   >[!NOTE]
   >
   >É possível criar os registros posteriormente usando a variável **[!UICONTROL Salvar como rascunho]** botão. É possível retomar a delegação de subdomínio nesse estágio, abrindo-a na lista de subdomínios.

1. Aguarde até que o Adobe verifique se esses registros são gerados sem erros na solução de hospedagem. Esse processo pode levar até 2 minutos.

   >[!NOTE]
   >
   >Todos os registros ausentes, ou seja, os registros ainda não criados em sua solução de hospedagem, serão listados.

1. O Adobe gera um registro de validação de URL CDN SSL. Copie este registro de validação na plataforma de hospedagem. Se você criou corretamente esse registro na solução de hospedagem, marque a caixa &quot;Confirmo...&quot; e clique em **[!UICONTROL Enviar]**.

   <!--![](assets/subdomain-cdn-url-validation.png)-->

   >[!NOTE]
   >
   >Também é possível criar o registro de validação e enviar a configuração de subdomínio posteriormente usando o **[!UICONTROL Salvar como rascunho]** botão. Você poderá retomar a delegação de subdomínio abrindo-a na lista de subdomínios.

1. Depois que a delegação de subdomínio CNAME for enviada, o subdomínio será exibido na lista com o **[!UICONTROL Processando]** status. Para obter mais informações sobre os status dos subdomínios, consulte [nesta seção](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que o Adobe execute as verificações necessárias, que normalmente levam de 2 a 3 horas. Saiba mais [nesta seção](#subdomain-validation).

1. Quando as verificações forem bem-sucedidas<!--i.e Adobe validates the record you created and installs it-->, o subdomínio obtém o **[!UICONTROL Sucesso]** status. Ele está pronto para ser usado para enviar mensagens.

   >[!NOTE]
   >
   >O subdomínio será marcado como **[!UICONTROL Failed]** se você não criar o registro de validação na solução de hospedagem.

Após validar o registro e instalar o certificado, o Adobe cria automaticamente o registro PTR para o subdomínio CNAME. [Saiba mais](ptr-records.md)

>[!CAUTION]
>
>No momento, a execução paralela de subdomínios não é compatível com o [!DNL Journey Optimizer]. Se você tentar enviar um subdomínio para delegação quando outro tiver o **[!UICONTROL Processando]** , você receberá uma mensagem de erro.

## Validação de subdomínio {#subdomain-validation}

As verificações e ações abaixo serão executadas até que o subdomínio seja verificado e possa ser usado para enviar mensagens.

>[!NOTE]
>
>Essas etapas são executadas por Adobe e podem levar até 3 horas.

1. **Pré-validar**: o Adobe verifica se o subdomínio foi delegado ao Adobe DNS (registro NS, registro SOA, configuração de zona, registro de propriedade). Se a etapa de pré-validação falhar, um erro será retornado junto com o motivo correspondente; caso contrário, o Adobe continuará para a próxima etapa.

1. **Configurar DNS para o domínio**:

   * **Registro MX**: registro Mail eXchange - Registro do servidor de email que processa emails de entrada enviados para o subdomínio.
   * **Registro SPF**: registro da Estrutura de Política do Remetente - Lista os IPs dos servidores de email que podem enviar emails do subdomínio.
   * **Registro DKIM**: registro padrão DomainKeys Identified Mail - usa criptografia de chave pública-privada para autenticar a mensagem e evitar falsificação.
   * **A**: Mapeamento de IP padrão.
   * **CNAME**: um registro CNAME ou Nome canônico é um tipo de registro DNS que mapeia um nome de alias para um nome de domínio verdadeiro ou canônico.

1. **Criar URLs de rastreamento e espelho**: se o domínio for email.example.com, o domínio de rastreamento/espelho será data.email.example.com. É protegido por meio da instalação do certificado SSL.

1. **Provisionar CDN CloudFront**: se o CDN ainda não estiver configurado, o Adobe o provisionará para a ID da organização.

1. **Criar domínio CDN**: se o domínio for email.example.com, o domínio CDN será cdn.email.example.com.

1. **Criar e anexar certificado SSL CDN**: o Adobe cria o certificado CDN para o domínio CDN e anexa o certificado ao domínio CDN.

1. **Criar DNS direto**: se este for o primeiro subdomínio que você está delegando, o Adobe criará o DNS de encaminhamento necessário para criar registros PTR - um para cada um de seus IPs.

1. **Criar registro PTR**: o registro PTR, também conhecido como registro DNS reverso, é exigido pelos ISPs para que eles não marquem os emails como spam. O Gmail também recomenda ter registros PTR para cada IP. O Adobe cria registros PTR somente quando você delega um subdomínio pela primeira vez, um para cada IP, todos os IPs que apontam esse subdomínio. Por exemplo, se o IP for *192.1.2.1* e o subdomínio for *email.example.com*, o registro PTR será: *192.1.2.1 PTR r1.email.example.com*. Você pode atualizar o registro PTR posteriormente para apontar para o novo domínio delegado. [Saiba mais sobre registros PTR](ptr-records.md)

## Vídeo explicativo{#video}

Saiba como criar um subdomínio usando CNAME para apontar para registros específicos do Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
