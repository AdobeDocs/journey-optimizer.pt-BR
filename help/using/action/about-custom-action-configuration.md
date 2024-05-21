---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma ação personalizada
description: Saiba como configurar uma ação personalizada
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, third-party, custom, jornada, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 12423d9fe07e5c757154ae4f732ff20ec6dc2427
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 17%

---

# Configurar uma ação personalizada {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Ações personalizadas"
>abstract="Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que as jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com sua jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase etc."

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que as jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com sua jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas aos profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da jornada, no **[!UICONTROL Ação]** categoria. Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitações{#custom-actions-limitations}

As ações personalizadas vêm com algumas limitações listadas na [esta página](../start/guardrails.md).

Em parâmetros de ação personalizados, você pode passar uma coleção simples, bem como uma coleção de objetos. Saiba mais sobre as limitações de coleção no [esta página](../building-journeys/collections.md#limitations).

Observe também que os parâmetros de ações personalizadas têm um formato esperado (por exemplo: sequência, decimal etc.). Você deve ter cuidado para respeitar esses formatos esperados. Saiba mais nesta página [caso de uso](../building-journeys/collections.md).

As ações personalizadas oferecem suporte ao formato JSON somente ao usar [solicitação](../action/about-custom-action-configuration.md#define-the-message-parameters) ou [cargas de resposta](../action/action-response.md).

## Práticas recomendadas{#custom-action-enhancements-best-practices}

Ao escolher um ponto de acesso para destino usando uma ação personalizada, verifique se:

* Esse ponto de acesso pode suportar a taxa de transferência da jornada, usando configurações da [API de limitação](../configuration/throttling.md) ou da [API de limite](../configuration/capping.md) para limitá-la. Tenha cuidado, pois uma configuração de limitação não pode ficar abaixo de 200 TPS. Qualquer ponto de acesso como destino precisará oferecer suporte a pelo menos 200 TPS.
* Esse ponto de acesso precisa ter um tempo de resposta o mais baixo possível. Dependendo da taxa de transferência esperada, ter um tempo de resposta alto pode afetar a taxa de transferência real.

Um limite máximo de 300.000 chamadas em um minuto é definido para todas as ações personalizadas. Além disso, o limite padrão é executado por host e por sandbox. Por exemplo, em uma sandbox, se você tiver dois pontos de acesso com o mesmo host (por exemplo: `https://www.adobe.com/endpoint1` e `https://www.adobe.com/endpoint2`), o limite será aplicado a todos os pontos de acesso no host adobe.com. &quot;endpoint1&quot; e &quot;endpoint2&quot; compartilharão a mesma configuração de limitação e fazer com que um endpoint atinja o limite terá impacto no outro endpoint.

Esse limite foi definido com base no uso pelos clientes, para proteger pontos de acesso externos direcionados por ações personalizadas. É necessário considerar isso em jornadas baseadas em público-alvo, definindo uma taxa de leitura apropriada (5.000 perfis por segundo ao utilizar ações personalizadas). Se necessário, é possível substituir essa configuração aumentando o limite máximo por meio das APIs de limite e limitação. Consulte [esta página](../configuration/external-systems.md).

Você não deve direcionar endpoints públicos com ações personalizadas por vários motivos:

* Sem limitação ou limitação adequada, há o risco de enviar muitas chamadas para um endpoint público que pode não suportar esse volume.
* Os dados do perfil podem ser enviados por meio de ações personalizadas, portanto, o direcionamento a um endpoint público pode levar ao compartilhamento externo inadvertido de informações pessoais.
* Você não tem controle sobre os dados que estão sendo retornados por pontos de extremidade públicos. Se um endpoint alterar sua API ou começar a enviar informações incorretas, elas serão disponibilizadas nas comunicações enviadas, com possíveis impactos negativos.

## Consentimento e governança de dados {#privacy}

No Journey Optimizer, você pode aplicar políticas de consentimento e governança de dados às ações personalizadas para impedir que campos específicos sejam exportados para sistemas de terceiros ou excluir clientes que não consentiram em receber comunicações por email, push ou SMS. Para obter mais informações, consulte as seguintes páginas:

* [Governança de dados](../action/action-privacy.md).
* [Consentimento](../action/action-privacy.md).


## Etapas de configuração {#configuration-steps}

Estas são as principais etapas necessárias para configurar uma ação personalizada:

1. Na seção de menu ADMINISTRAÇÃO, selecione **[!UICONTROL Configurações]**. No  **[!UICONTROL Ações]** clique em **[!UICONTROL Gerenciar]**. Clique em **[!UICONTROL Criar ação]** para criar uma nova ação. O painel de configuração de ação é aberto no lado direito da tela.

   ![](assets/custom2.png)

1. Digite um nome para a ação.

   >[!NOTE]
   >
   >Somente caracteres alfanuméricos e sublinhados são permitidos. O comprimento máximo é de 30 caracteres.

1. Adicione uma descrição à ação. Esta etapa é opcional.
1. O número de jornadas que usam esta ação é exibido no **[!UICONTROL Usado em]** campo. Você pode clicar no link **[!UICONTROL Exibir jornadas]** botão para exibir a lista de jornadas usando esta ação.
1. Definir o diferente **[!UICONTROL Configuração de URL]** parâmetros. Consulte [esta página](../action/about-custom-action-configuration.md#url-configuration).
1. Configure o **[!UICONTROL Autenticação]** seção. Essa configuração é a mesma das fontes de dados.  Consulte [esta seção](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina o **[!UICONTROL Parâmetros de ação]**. Consulte [esta página](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Clique em **[!UICONTROL Salvar]**.

   A ação personalizada agora está configurada e pronta para ser usada em suas jornadas. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando uma ação personalizada é usada em uma jornada, a maioria dos parâmetros é somente leitura. Você só pode modificar a variável **[!UICONTROL Nome]**, **[!UICONTROL Descrição]**, **[!UICONTROL URL]** e os **[!UICONTROL Autenticação]** seção.

## Configuração do endpoint {#url-configuration}

Ao configurar uma ação personalizada, você precisa definir o seguinte **[!UICONTROL Configuração do endpoint]** parâmetros:

![](assets/action-response1bis.png){width="70%" align="left"}

1. No **[!UICONTROL URL]** especifique o URL do serviço externo:

   * Se o URL for estático, insira o URL neste campo.

   * Se o URL incluir um caminho dinâmico, insira apenas a parte estática do URL, ou seja, o esquema, o host, a porta e, opcionalmente, uma parte estática do caminho.

     Exemplo: `https://xxx.yyy.com/somethingstatic/`

     Você especificará o caminho dinâmico do URL ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Por motivos de segurança, recomendamos que você use o esquema HTTPS para o URL. Não permitimos o uso de endereços Adobe que não sejam públicos e o uso de endereços IP.
   >
   >Somente as portas padrão são permitidas ao definir uma ação personalizada: 80 para http e 443 para https.

1. Selecionar a chamada **[!UICONTROL Método]**: pode ser **[!UICONTROL POST]**, **[!UICONTROL GET]** ou **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > A variável **DELETE** não há suporte para o método. Se precisar atualizar um recurso existente, selecione o **PUT** método.

1. Defina os cabeçalhos e parâmetros de consulta:

   * No **[!UICONTROL Cabeçalhos]** clique em **[!UICONTROL Adicionar um campo de cabeçalho]** para definir os cabeçalhos HTTP da mensagem de solicitação a ser enviada ao serviço externo. A variável **[!UICONTROL Tipo de conteúdo]** e **[!UICONTROL Conjunto de caracteres]** os campos de cabeçalho são definidos por padrão. Não é possível excluir esses campos. Somente o **[!UICONTROL Tipo de conteúdo]** cabeçalho pode ser modificado. Seu valor deve respeitar o formato JSON. Este é o valor padrão:

   ![](assets/content-type-header.png)

   * No **[!UICONTROL Parâmetros de consulta]** clique em **[!UICONTROL Adicionar um campo de parâmetro de Query]** para definir os parâmetros que deseja adicionar ao URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Insira o rótulo ou o nome do campo.

1. Selecione o tipo: **[!UICONTROL Constante]** ou **[!UICONTROL Variável]**. Se você selecionou **[!UICONTROL Constante]**, em seguida, insira o valor constante na variável **[!UICONTROL Valor]** campo. Se você selecionou **[!UICONTROL Variável]**, em seguida, você especificará essa variável ao adicionar a ação personalizada a uma jornada. [Saiba mais](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Depois de ter adicionado a ação personalizada a uma jornada, ainda será possível adicionar campos de parâmetros de cabeçalho ou consulta a ela se a jornada estiver em status de rascunho. Se não quiser que a jornada seja afetada pelas alterações de configuração, duplique a ação personalizada e adicione os campos à nova ação personalizada.
   >
   >Os cabeçalhos são validados de acordo com as regras de análise de campo. Saiba mais em [esta documentação](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Definir os parâmetros de carga {#define-the-message-parameters}

1. No **[!UICONTROL Solicitação]** cole um exemplo da carga JSON para enviar ao serviço externo. Esse campo é opcional e só está disponível para métodos de chamada POST e PUT.

1. No **[!UICONTROL Resposta]** cole um exemplo da carga útil retornada pela chamada. Este campo é opcional e está disponível para todos os métodos de chamada. Para obter informações detalhadas sobre como aproveitar as respostas de chamada da API em ações personalizadas, consulte [esta página](../action/action-response.md).

>[!NOTE]
>
>O recurso de resposta está disponível atualmente na versão beta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>O exemplo de carga útil não pode conter valores nulos. Os nomes de campos na carga não podem conter &quot;.&quot; “?”. Eles não podem começar com um caractere &quot;$&quot;.

Você poderá definir o tipo de parâmetro (por exemplo: sequência, número inteiro etc.).

Você também terá uma escolha entre especificar se um parâmetro é uma constante ou uma variável:

* **Constante** significa que o valor do parâmetro é definido no painel de configuração de ação por uma pessoa técnica. O valor será sempre o mesmo nas jornadas. Ela não variará e o profissional de marketing não a verá ao usar a ação personalizada na jornada. Pode ser, por exemplo, uma ID que o sistema de terceiros espera. Nesse caso, o campo à direita da constante/variável de alternância é o valor transmitido.
* **Variável** significa que o valor do parâmetro varia. Os profissionais de marketing que usam essa ação personalizada em uma jornada poderão passar o valor desejado ou especificar onde recuperar o valor desse parâmetro (por exemplo, do evento, do Adobe Experience Platform etc.). Nesse caso, o campo à direita da constante/variável de alternância é o rótulo que os comerciantes verão na jornada para nomear esse parâmetro.

![](assets/customactionpayloadmessage2.png)

## Suporte ao protocolo mTLS {#mtls-protocol-support}

Agora você pode usar o Mutual Transport Layer Security (mTLS) para garantir segurança aprimorada em conexões de saída para destinos da API HTTP e ações personalizadas do Adobe Journey Optimizer. O mTLS é um método de segurança completo para autenticação mútua que garante que ambas as partes que compartilham informações sejam quem afirmam ser antes que os dados sejam compartilhados. O mTLS inclui uma etapa adicional em comparação ao TLS, na qual o servidor também solicita o certificado do cliente e o verifica ao final.

No Adobe Journey Optimizer, o mTLS é usado em conjunto com ações personalizadas. Nenhuma configuração adicional para ações personalizadas do Adobe Journey Optimizer é necessária da sua parte para habilitar o mTLS. Quando o ponto de extremidade de uma ação personalizada é habilitado para mTLS, o sistema busca o certificado do armazenamento de chaves da Adobe Experience Platform e o fornece automaticamente ao ponto de extremidade (como é necessário para conexões mTLS).

Se você quiser usar mTLS com esses workflows de destino da API HTTP do Adobe Journey Optimizer e do Experience Platform, o endereço do servidor inserido na interface da ação do cliente do Adobe Journey Optimizer ou na interface dos Destinos deve ter os protocolos TLS desativados e somente o mTLS ativado. Se o protocolo TLS 1.2 ainda estiver habilitado nesse endpoint, nenhum certificado será enviado para a autenticação de cliente. Isso significa que para usar mTLS com esses workflows, o terminal de servidor de &quot;recebimento&quot; deve ser um mTLS **somente** ponto de extremidade de conexão habilitado.

>[!IMPORTANT]
>
>Nenhuma configuração adicional é necessária em sua ação personalizada ou jornada do Adobe Journey Optimizer para ativar o mTLS; esse processo ocorre automaticamente quando um terminal habilitado para mTLS é detectado. O Common Name (CN) e o Subject Alternative Names (SAN) de cada certificado estão disponíveis na documentação como parte do certificado e podem ser usados como uma camada adicional de validação de propriedade, se desejar.
>
>O RFC 2818, publicado em maio de 2000, substitui o uso do campo Nome comum (CN) em certificados HTTPS para verificação do nome da entidade. Em vez disso, ele recomenda o uso da extensão &quot;Nome alternativo da entidade&quot; (SAN) do tipo &quot;nome dns&quot;.

Se você quiser verificar a CN ou a SAN para fazer a validação adicional de terceiros, é possível baixar os certificados relevantes aqui:

```
Prod:
{
    "serviceName": "AJO Journeys",
    "publicCertificate": "-----BEGIN CERTIFICATE-----
MIIG9TCCBd2gAwIBAgIQBX+pDP5hB0gqDzFKyq5wLjANBgkqhkiG9w0BAQsFADBZ
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMTMwMQYDVQQDEypE
aWdpQ2VydCBHbG9iYWwgRzIgVExTIFJTQSBTSEEyNTYgMjAyMCBDQTEwHhcNMjQw
NTA5MDAwMDAwWhcNMjUwNjA5MjM1OTU5WjB0MQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTERMA8GA1UEBxMIU2FuIEpvc2UxEzARBgNVBAoTCkFkb2Jl
IEluYy4xKDAmBgNVBAMTH2Fqby1qb3VybmV5cy5hZXAtbXRscy5hZG9iZS5jb20w
ggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDaI8HZHzbmPEgTy9O7cYmq
ZVX5283Gw7j7v4/O810jZXItBDmsSiWotvTgAT0s2oZMZZ6tGPbQB7hL+xJJ+yu2
HxFl1WzB4UGHJ+UbrL94hI930xQs0FVgSOGgIarj5HucF2ZxwHIkVHY5whrOq9t4
UxFBG0siUPQrTzV9GfA0wREElugpTbwaM8CTWwOQ9ekroOD2C5zAcLTycXFtSMiU
B4L4u38S9hGoBByzzKv9GnUMQudvt/s5zsGykZgEEYeN6IitfVO6BOD9jT94Aytx
/O3XH5w8v4KNTn+An99bXFmyg3JRUFSYZFxha8s1f6uu0XbdToQ+ao0WkE06nMmV
AgMBAAGjggOcMIIDmDAfBgNVHSMEGDAWgBR0hYDAZsffN97PvSk3qgMdvu3NFzAd
BgNVHQ4EFgQUn8OqtzccNdrsb+fbRnTHmtTZxLMwKgYDVR0RBCMwIYIfYWpvLWpv
dXJuZXlzLmFlcC1tdGxzLmFkb2JlLmNvbTA+BgNVHSAENzA1MDMGBmeBDAECAjAp
MCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0LmNvbS9DUFMwDgYDVR0P
AQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjCBnwYDVR0f
BIGXMIGUMEigRqBEhkJodHRwOi8vY3JsMy5kaWdpY2VydC5jb20vRGlnaUNlcnRH
bG9iYWxHMlRMU1JTQVNIQTI1NjIwMjBDQTEtMS5jcmwwSKBGoESGQmh0dHA6Ly9j
cmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAy
MENBMS0xLmNybDCBhwYIKwYBBQUHAQEEezB5MCQGCCsGAQUFBzABhhhodHRwOi8v
b2NzcC5kaWdpY2VydC5jb20wUQYIKwYBBQUHMAKGRWh0dHA6Ly9jYWNlcnRzLmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAyMENBMS0x
LmNydDAMBgNVHRMBAf8EAjAAMIIBfwYKKwYBBAHWeQIEAgSCAW8EggFrAWkAdwBO
daMnXJoQwzhbbNTfP1LrHfDgjhuNacCx+mSxYpo53wAAAY9ecsWsAAAEAwBIMEYC
IQDQclgq89ZVlwdYBJFEIs8q4WIcZ9Siw+jb9OgCrz+wjwIhALQLnC1WyT+dHjvY
FvZjc99WkjnEwhIevj/Rz7r0EzhmAHUAfVkeEuF4KnscYWd8Xv340IdcFKBOlZ65
Ay/ZDowuebgAAAGPXnLF5AAABAMARjBEAiBy9cNT3CnmSMOdJe+JbG8f7ha1UGgN
TdDlaR9x9fKmKQIgNmGjz5AzP1evB2G1TTvVLkHfWQw0864c4F23WSV+6TsAdwDP
EVbu1S58r/OHW9lpLpvpGnFnSrAX7KwB0lt3zsw7CAAAAY9ecsYnAAAEAwBIMEYC
IQCTcB7s1xDP8Olif3jj4X8jHgVxv5C3bTvG6wDYBByfcQIhAOt8PhR6tWSLtF1V
HB8r7dns7Oth1+QT7WMonQZsP/3WMA0GCSqGSIb3DQEBCwUAA4IBAQAjTy45fbQV
aVTZ71wcIyHnkJfq/8SSc/UNT5//6AMiV6kb3YsFW1+EaQ1wPHZS0Qfjs7aIsXi5
f2TCGps8onELNpOfFfptrOCMfcYGMvV1wPCBy+kuoGY/YRZlsdNUTTzQAGztfRev
79w+XIDzioCrY+sfyUkkw+N/F7/RIjzMKjP6onSfuD+5WjqVKq9kFE0fCyJixedV
BPoPM4Cktgvc9SsK17JmLWkg+V2yH1eDzmjF3sR0/dcmoAM0qgV/CDuhIIqX2o7m
3/aQSNsPUpgBVbkz+SjEtchmw8DXW/Kro8QVulsXdbkiLTOj4JopxdOzrbKgWMwr
pIw7KKJoktDk
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIEyDCCA7CgAwIBAgIQDPW9BitWAvR6uFAsI8zwZjANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0yMTAzMzAwMDAwMDBaFw0zMTAzMjkyMzU5NTlaMFkxCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxMzAxBgNVBAMTKkRpZ2lDZXJ0IEdsb2Jh
bCBHMiBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBAMz3EGJPprtjb+2QUlbFbSd7ehJWivH0+dbn4Y+9lavyYEEV
cNsSAPonCrVXOFt9slGTcZUOakGUWzUb+nv6u8W+JDD+Vu/E832X4xT1FE3LpxDy
FuqrIvAxIhFhaZAmunjZlx/jfWardUSVc8is/+9dCopZQ+GssjoP80j812s3wWPc
3kbW20X+fSP9kOhRBx5Ro1/tSUZUfyyIxfQTnJcVPAPooTncaQwywa8WV0yUR0J8
osicfebUTVSvQpmowQTCd5zWSOTOEeAqgJnwQ3DPP3Zr0UxJqyRewg2C/Uaoq2yT
zGJSQnWS+Jr6Xl6ysGHlHx+5fwmY6D36g39HaaECAwEAAaOCAYIwggF+MBIGA1Ud
EwEB/wQIMAYBAf8CAQAwHQYDVR0OBBYEFHSFgMBmx9833s+9KTeqAx2+7c0XMB8G
A1UdIwQYMBaAFE4iVCAYlebjbuYP+vq5Eu0GF485MA4GA1UdDwEB/wQEAwIBhjAd
BgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwdgYIKwYBBQUHAQEEajBoMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wQAYIKwYBBQUHMAKG
NGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RH
Mi5jcnQwQgYDVR0fBDswOTA3oDWgM4YxaHR0cDovL2NybDMuZGlnaWNlcnQuY29t
L0RpZ2lDZXJ0R2xvYmFsUm9vdEcyLmNybDA9BgNVHSAENjA0MAsGCWCGSAGG/WwC
ATAHBgVngQwBATAIBgZngQwBAgEwCAYGZ4EMAQICMAgGBmeBDAECAzANBgkqhkiG
9w0BAQsFAAOCAQEAkPFwyyiXaZd8dP3A+iZ7U6utzWX9upwGnIrXWkOH7U1MVl+t
wcW1BSAuWdH/SvWgKtiwla3JLko716f2b4gp/DA/JIS7w7d7kwcsr4drdjPtAFVS
slme5LnQ89/nD/7d+MS5EHKBCQRfz5eeLjJ1js+aWNJXMX43AYGyZm0pGrFmCW3R
bpD0ufovARTFXFZkAdl9h6g4U5+LXUZtXMYnhIHUfoyMo5tS58aI7Dd8KvvwVVo4
chDYABPPTHPbqjc1qCmBaZx2vN4Ye5DUys/vZwP9BFohFrH/6j/f3IL16/RZkiMN
JCqVJUzKoZHm1Lesh3Sz8W2jmdv51b2EQJ8HmA==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65TANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0xMzA4MDExMjAwMDBaFw0zODAxMTUxMjAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IEcyMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAuzfNNNx7a8myaJCtSnX/RrohCgiN9RlUyfuI
2/Ou8jqJkTx65qsGGmvPrC3oXgkkRLpimn7Wo6h+4FR1IAWsULecYxpsMNzaHxmx
1x7e/dfgy5SDN67sH0NO3Xss0r0upS/kqbitOtSZpLYl6ZtrAGCSYP9PIUkY92eQ
q2EGnI/yuum06ZIya7XzV+hdG82MHauVBJVJ8zUtluNJbd134/tJS7SsVQepj5Wz
tCO7TG1F8PapspUwtP1MVYwnSlcUfIKdzXOS0xZKBgyMUNGPHgm+F6HmIcr9g+UQ
vIOlCsRnKPZzFBQ9RnbDhxSJITRNrw9FDKZJobq7nMWxM4MphQIDAQABo0IwQDAP
BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwIBhjAdBgNVHQ4EFgQUTiJUIBiV
5uNu5g/6+rkS7QYXjzkwDQYJKoZIhvcNAQELBQADggEBAGBnKJRvDkhj6zHd6mcY
1Yl9PMWLSn/pvtsrF9+wX3N3KjITOYFnQoQj8kVnNeyIv/iPsGEMNKSuIEyExtv4
NeF22d+mQrvHRAiGfzZ0JFrabA0UWTW98kndth/Jsw1HKj2ZL7tcu7XUIOGZX1NG
Fdtom/DzMNU+MeKNhJ7jitralj41E6Vf8PlwUHBHQRFXGU7Aj64GxJUTFy8bJZ91
8rGOmaFvE7FBcf6IKshPECBV1/MUReXgRPTqh5Uykw7+U0b6LJ3/iyK5S9kJRaTe
pLiaWN0bfVKfjllDiIGknibVb63dDcY3fe0Dkhvld1927jyNxF1WW6LZZm6zNTfl
MrY=
-----END CERTIFICATE-----",
    "expiryDate": "2025-06-09T23:59:59Z"
}
```

