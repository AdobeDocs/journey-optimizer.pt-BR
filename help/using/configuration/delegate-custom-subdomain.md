---
solution: Journey Optimizer
product: journey optimizer
title: Delegar um subdomínio personalizado
description: Saiba como delegar subdomínios personalizados.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, delegação, domínio, DNS
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 34af1329-f0c8-4fcd-a284-f8f4214611d4
source-git-commit: 722d37dc4bcb9ab7983ea336aa0b12a6a09e01dc
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 22%

---

# Configurar um subdomínio personalizado {#delegate-custom-subdomain}

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

Como alternativa aos métodos [Totalmente delegado](about-subdomain-delegation.md#full-subdomain-delegation) e [CNAME configurado](about-subdomain-delegation.md#cname-subdomain-delegation), o método **Delegação personalizada** permite que você assuma a propriedade de seus subdomínios dentro do Journey Optimizer e tenha controle total sobre os certificados gerados.

Como parte desse processo, a Adobe precisa garantir que seu DNS esteja configurado adequadamente para entregar, renderizar e rastrear mensagens. É por isso que você deverá [carregar o certificado SSL](#upload-ssl-certificate) obtido da Autoridade de Certificação e concluir as [etapas do Loop de Comentários](#feedback-loop-steps) verificando a propriedade do domínio e o endereço de email de relatórios.

Para configurar um subdomínio personalizado, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** > **[!UICONTROL Subdomínios]**.

1. Clique em **[!UICONTROL Configurar subdomínio]**.

1. Na seção **[!UICONTROL Configurar método]**, selecione **[!UICONTROL Delegação personalizada]**.

   ![](assets/subdomain-method-custom.png){width=90%}

1. Especifique o nome do subdomínio que será delegado.

   >[!CAUTION]
   >
   >Você não pode usar o mesmo domínio de envio para enviar mensagens de [!DNL Adobe Journey Optimizer] e de outro produto, como [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage].

## Criar os registros de DNS {#create-dns-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom_dns"
>title="Gerar os registros de DNS correspondentes"
>abstract="Para delegar um subdomínio personalizado à Adobe, é necessário copiar e colar as informações do servidor de nomes exibidas na interface do Journey Optimizer na sua solução de hospedagem de domínio para gerar os registros de DNS correspondentes."

1. A lista de registros que serão colocados em seus servidores DNS é exibida. Copie esses registros, um por um ou baixando um arquivo CSV.

1. Navegue até a solução de hospedagem de domínio para gerar os registros DNS correspondentes.

1. Verifique se todos os registros DNS foram gerados em sua solução de hospedagem de domínio.

1. Se tudo estiver configurado corretamente, marque a caixa &quot;Confirmo...&quot;.

   ![](assets/subdomain-custom-submit.png){width="75%"}

## Fazer upload do certificado SSL {#upload-ssl-certificate}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom-ssl"
>title="Gerar a solicitação de assinatura do certificado"
>abstract="Ao configurar um novo subdomínio personalizado, é necessário gerar a solicitação de assinatura do certificado (CSR, na sigla em inglês), preenchê-la e enviá-la à autoridade de certificação para obter o certificado SSL a ser enviado para o Journey Optimizer."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_key_length"
>title="Selecionar comprimento da chave"
>abstract="O comprimento da chave pode ser somente 2048 ou 4096 bits. Ele não pode ser alterado após o envio do subdomínio."

1. Na seção **[!UICONTROL Certificado SSL]**, clique em **[!UICONTROL Gerar CSR]**.

   ![](assets/subdomain-custom-ssl-certificate.png){width="85%"}

   >[!NOTE]
   >
   >A data de expiração do seu certificado SSL é exibida. Depois que a data for atingida, é necessário carregar um novo certificado.

1. Preencha o formulário que exibe e gera a Solicitação de assinatura de certificado (CSR).

   ![](assets/subdomain-custom-generate-csr.png){width="70%"}

   >[!NOTE]
   >
   >O comprimento da chave pode ser somente 2048 ou 4096 bits. Ele não pode ser alterado após o envio do subdomínio.

1. Clique em **[!UICONTROL Baixar CSR]** e salve o formulário no computador local.

1. Envie-o à Autoridade de certificação (CA) para obter seu certificado SSL. Antes de enviar essa CSR à sua CA para assinatura, há alguns pontos importantes a serem considerados:

   * A CSR baixada da etapa 3 é somente para data.subdomain.com.

   * No entanto, o certificado deve abranger as entradas data.subdomain.com e cdn.subdomain.com como Nomes alternativos da entidade (SAN) em um único certificado. Por exemplo, se você estiver delegando example.adobe.com, data.subdomain.com corresponde a data.example.adobe.com, e cdn.subdomain.com corresponde a cdn.example.adobe.com.

   * Os subdomínios Data (data.example.adobe.com) e CDN (cdn.example.adobe.com) precisam ser adicionados como entradas pares no mesmo certificado.

   * A maioria das CAs permite adicionar outras SANs (como o subdomínio CDN) durante o processo de assinatura

      * Por meio do portal da CA (recomendado, se disponível) ou
      * Solicitando-o manualmente com a equipe de suporte caso a opção de portal não esteja disponível.

   * Depois de assinada, a CA emitirá um único certificado que abrangerá o domínio de dados e o subdomínio CDN.

1. Depois de recuperado, clique em **[!UICONTROL Carregar certificado SSL]** e carregar o certificado para [!DNL Journey Optimizer] no formato .pem com a cadeia completa de certificados. Este é um exemplo de formato de arquivo .pem:

   ```
   -----BEGIN CERTIFICATE-----
   MIIDXTCCAkWgAwIBAgIJALc3... (base64 encoded data)
   -----END CERTIFICATE-----
   ```

<!--
>[!CAUTION]
>
>Both Data and CDN subdomains must be included in the same certificate.
-->

## Concluir as etapas do loop de comentários {#feedback-loop-steps}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_feedback-loop"
>title="Concluir as etapas do loop de comentários"
>abstract="Acesse o Yahoo! Sender Hub e preencha o formulário para confirmar a propriedade do domínio. Insira o endereço de email para a geração de relatórios FBL listado abaixo e use o OTP que será recebido para confirmar a propriedade no Yahoo! Sender Hub."

1. Vá para o [Yahoo! Site do Hub do Remetente ](https://senders.yahooinc.com/) e preencha o formulário necessário para verificar a propriedade do domínio.

1. Para verificar a propriedade do domínio, o Yahoo! O Hub do remetente exigirá que você forneça um endereço de email. Insira o endereço de email de relatório FBL listado em **[!UICONTROL Valor]**. Este é um endereço de email da Adobe.

1. Quando o Yahoo! O Hub do Remetente gera uma OTP (Senha ocasional). Ela será enviada para este endereço Adobe.

1. Entre em contato com a equipe de Entregabilidade da Adobe que fornecerá a você este OTP. <!--Specify how to reach out + any information that customer should share in the request to deliverability team to get access to the right OTP-->

   >[!CAUTION]
   >
   >O OTP é válido apenas por 24 horas, portanto, entre em contato com a Adobe assim que o OTP for gerado. <!--TBC?-->
   >
   >A solicitação OTP só pode ser feita em dias da semana. Não há suporte nos finais de semana. <!--Add times + timezone-->

1. Digite o OTP no Yahoo! Sender Hub.

1. Verifique se você concluiu todas as etapas do Loop de Comentários.

1. Se tudo estiver configurado corretamente, marque a caixa &quot;Concluído...&quot;.

   ![](assets/subdomain-custom-feedback-loop.png){width="85%"}

1. Clique em **[!UICONTROL Continuar]** e aguarde até que o Adobe verifique se os registros foram gerados sem erros na solução de hospedagem. Esse processo pode levar até 2 minutos.

   >[!NOTE]
   >
   >Verifique se todos os registros foram criados corretamente antes de continuar.

1. O Adobe gera um registro de validação de URL CDN SSL. Copie este registro de validação na plataforma de hospedagem. Se você criou corretamente esse registro na solução de hospedagem, marque a caixa &quot;Confirmo...&quot;.

1. Clique em **[!UICONTROL Enviar]** para que o Adobe execute as verificações necessárias. [Saiba mais](delegate-subdomain.md#submit-subdomain)

## Lista de verificação de solução de problemas {#check-list}

Se ocorrerem erros ao tentar enviar o subdomínio personalizado, execute as ações de solução de problemas listadas abaixo.

* Verifique se todos os registros DNS foram propagados corretamente usando as ferramentas de pesquisa de DNS.

* Verifique se o certificado atende a todos os requisitos técnicos antes de fazer o upload.

* Verifique se o upload do certificado foi feito no formato correto.
