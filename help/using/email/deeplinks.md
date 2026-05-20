---
solution: Journey Optimizer
product: journey optimizer
title: Usar e configurar deeplinks em mensagens de email e SMS
description: Saiba como adicionar deeplinks a conteúdo de email e SMS e como implementar o manuseio de deeplinks em aplicativos iOS e Android.
feature: Email, SMS
topic: Content Management
role: User, Developer
level: Intermediate
keywords: deeplink, deep link, links universais, links de aplicativos, email, sms
source-git-commit: accdbd5bd5023ed8352ca6fba58a26e797ac1d68
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 1%

---


# Usar e configurar deeplinks em emails e SMS {#deeplinks}

Os Deeplinks ajudam a levar recipients de um email ou mensagem SMS para uma tela específica ou conteúdo no aplicativo móvel. Isso ajuda a trazer as pessoas diretamente para a experiência no aplicativo desejada, sem encaminhá-las por um navegador da Web ou uma loja de aplicativos, para que a jornada permaneça relevante e sob a marca.

Quando os destinatários clicam no link profundo, eles são levados diretamente ao conteúdo pretendido no aplicativo - **contanto que você tenha concluído**:

* as [etapas de configuração](#configuration) no Journey Optimizer;

* as etapas da [implementação do aplicativo móvel](#mobile-implementation) para iOS e Android em seu aplicativo móvel.

>[!NOTE]
>
>O [!DNL Adobe Journey Optimizer] oferece suporte ao deeplinking para o iOS e o Android usando URLs rastreadas (`/ee/v1/mclick/*`) para garantir compatibilidade e rastreamento de cliques.

## Criação de deeplinks {#authoring}

### Email {#authoring-email}

Para mensagens de email, você tem duas opções para inserir um deep link:

* **Designer de email**: verifique se o [rastreamento de links está habilitado](message-tracking.md#enable-tracking). Selecione o elemento que deseja vincular (texto, botão ou imagem), clique em **[!UICONTROL Inserir link]** na barra de ferramentas contextual e escolha **[!UICONTROL Deeplink]** para inserir sua URL de deeplink. [Saiba mais sobre como inserir links](message-tracking.md#insert-links)

* **Editor do Personalization (código)**: insira o deep link diretamente na HTML usando o seguinte trecho:

  ```html
  <a class="arc-link" data-nl-type="DEEPLINK" href="<<deeplink_url>>" id="acr-link-7821368" style="text-decoration:underline;" target="_blank" data-tracking-type="DEEPLINK">Click Here</a>
  ```

  Substitua `<<deeplink_url>>` pela URL de deep link real e use um `id` exclusivo para cada bloco para evitar conflitos.

### SMS {#authoring-sms}

Para SMS, os deeplinks são criados usando a função auxiliar **Url** no editor de personalização. Saiba mais sobre como adicionar links ao conteúdo de SMS [nesta seção](../mobile/create-mobile-message.md#sms-content).

Para inserir deeplinks no conteúdo de SMS, use a seguinte sintaxe:

```
{{url originalUrl='<<url>>' type='DEEPLINK' action='CLICK'}}
```

Substitua `<<url>>` pela URL de deeplink real.

## Configuração no Journey Optimizer {#configuration}

Para usar deeplinks em emails e SMS em seus aplicativos móveis, conclua as etapas de configuração abaixo.

>[!NOTE]
>
>Esta seção se aplica quando você usa **links universais (iOS)** e **links de aplicativos (Android)** (deeplinks baseados em HTTPS).

1. No Journey Optimizer, delegue o subdomínio em que o deeplinking está ativado. [Saiba mais](../configuration/delegate-subdomain.md)

1. Hospede o arquivo AASA para o iOS e o arquivo assetLinks.json para o Android no subdomínio. Entre em contato com o [Atendimento ao cliente da Adobe](https://helpx.adobe.com/br/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} ou com o representante da Adobe com os detalhes abaixo:

   * **Para o iOS (AASA)**:
      * Subdomínio delegado
      * ID do pacote do aplicativo
   * **Para o Android (assetLinks.json)**:
      * Subdomínio delegado
      * ID do pacote do aplicativo
      * Impressão digital do certificado SHA-256

>[!IMPORTANT]
>
>O deeplinking por meio da infraestrutura do Adobe se aplica quando o rastreamento de link está habilitado para a sua mensagem — nas[configurações de rastreamento de email](message-tracking.md#enable-tracking) ou na seção **[!UICONTROL Rastreamento de ações]** para campanhas de SMS. Os cliques de deep link rastreados usam URLs em `/ee/v1/mclick/*`, que a Adobe hospeda e resolve.
>
>Para links **não rastreados**, a URL não é regravada pelos sistemas Adobe. Você deve configurar links universais ou links de aplicativos em seus próprios domínios e hosts para que esses links abram seu aplicativo conforme planejado.

## Implementação do aplicativo móvel {#mobile-implementation}

Esta seção explica como implementar deeplinks móveis com [!DNL Adobe Journey Optimizer] para que, em uma configuração típica de **HTTPS** (links universais e links de aplicativos), uma única URL possa:

* Abra uma tela específica dentro do aplicativo móvel quando o aplicativo estiver instalado ou
* Abra o site como um fallback quando o aplicativo não estiver instalado.

Quando o rastreamento de links é habilitado para sua mensagem, o [!DNL Journey Optimizer] continua a rastrear esses cliques, os inclui nos relatórios e pode usá-los em [experimentos de conteúdo](../content-management/content-experiment.md) se você executá-los na mensagem.

Esta seção fornece padrões comuns de implementação para deeplinks. A configuração exata depende da arquitetura do aplicativo e da estrutura de roteamento.

### iOS (Links universais) {#ios-implementation}

1. No Xcode, selecione seu destino por meio de **[!UICONTROL Assinatura e Recursos]** > **[!UICONTROL + Recurso]** > **[!UICONTROL Domínios Associados]**.
1. Adicione entradas para subdomínios delegados, por exemplo:

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. Gerencie Links universais no aplicativo e obtenha o link original do cabeçalho de resposta.

   +++ Exemplo: iOS 13+ com cenas

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>O aplicativo deve executar uma **GET** na URL `mclick` e ler o cabeçalho **`Location`** e, em seguida, rotear com base na URL **final**.
>
>Não abra simplesmente o URL `mclick` no Safari; que anula a finalidade do deeplinking.

### Android (Links de aplicativo) {#android-implementation}

1. Adicione o filtro de intenção Link do aplicativo no aplicativo Android.

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. Implemente o manipulador de deep link.

   +++ Em Kotlin:

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>Assim como o iOS, o aplicativo deve chamar a URL `mclick` e usar o cabeçalho **`Location`** para determinar o destino final.
>
>Use o `followRedirects(false)` para controlar o tratamento do redirecionamento e registrar a análise com precisão, se necessário.
>
>A lógica de roteamento é específica do aplicativo; defina um mapeamento claro de URLs para telas.

## Práticas recomendadas {#deeplink-best-practices}

* **Usar caminhos estáveis**: prefira rotas resilientes às alterações na interface do usuário do aplicativo (por exemplo `/account/orders` em vez de `/tab/3/view/2`).
* **Conta para caminhos rastreados**: quando o rastreamento de link está habilitado, o link clicado pode usar padrões de caminho rastreado (por exemplo, `/ee/v1/mclick/`). Verifique se o roteador pode analisar o URL final após resolver o link rastreado.
* **Manter parâmetros previsíveis**: defina um esquema de parâmetros consistente (por exemplo, `?orderId=12345`).
* **Evite dados confidenciais nas URLs**: não coloque segredos ou dados pessoais diretamente na URL de deep link.
* **Testar seu deeplink**: envie uma prova e clique no deeplink de um dispositivo onde o aplicativo esteja instalado.
* **Validar em dispositivos reais**: links universais e comportamentos de resolução de links rastreados são mais confiáveis para validação em dispositivos físicos do que em simuladores.
* **Validar o roteamento do lado do aplicativo**: se o link direto não abrir a tela esperada, valide o roteamento do lado do aplicativo e o formato da URL (host/caminho/consulta e codificação de URL).
* **Lembre-se da inicialização do aplicativo**: o comportamento Links de Aplicativo/Links Universais é mais confiável depois que o aplicativo é instalado e aberto pelo menos uma vez.

## Solução de problemas e perguntas frequentes {#troubleshooting-faq}

+++ O aplicativo não abre quando eu toco no link profundo.

* Verifique se a URL corresponde ao host e aos padrões de caminho com os quais seu aplicativo está registrado para lidar, incluindo caminhos de cliques rastreados quando o rastreamento de link está habilitado (por exemplo, caminhos em `/ee/v1/mclick/`).
* Para links universais do iOS e links de aplicativos do Android, confirme se a associação de domínio (AASA / `assetlinks.json`) está configurada e acessível corretamente.
* Testar em um dispositivo real (simuladores/emuladores podem se comportar de forma diferente para associação de link).

+++

+++ O aplicativo abre, mas não navega até a tela esperada.

* Confirme se o roteador do lado do aplicativo analisa corretamente o caminho/consulta do URL.
* Verificar codificação do URL: os caracteres reservados devem ser codificados por URL.
* Valide os nomes e os valores dos parâmetros de acordo com o que o roteador espera.

+++

+++ O que acontece se o aplicativo não estiver instalado?

* Se o mesmo URL HTTPS puder ser fornecido pelo seu site, o link poderá abrir uma página da Web como um fallback quando o aplicativo não estiver instalado (configure o destino e o roteamento da Web de acordo).

+++

+++ Como faço para incluir caracteres especiais em parâmetros de segurança?

Valores de parâmetro de consulta codificados por URL. Isso reduz os problemas de entrega e renderização e ajuda a evitar erros de análise no aplicativo.

+++

+++ Como devemos testar de ponta a ponta?

* Crie uma prova com um deeplink, clique nele em dispositivos iOS e Android (cenários instalados e não instalados).
* Validar:
   * O valor final do email ou link de SMS (host/caminho/query)
   * A associação no nível do sistema operacional (se estiver usando links universais/links de aplicativos)
   * O resultado do roteamento no aplicativo

+++

+++ Tenho um aplicativo, mas subdomínios diferentes para a organização. Devo solicitar que o AASA e o assetLinks.json sejam criados para cada subdomínio?

Sim. Se quiser fazer o deeplinking em cada subdomínio delegado, solicite a configuração AASA e `assetlinks.json` para cada subdomínio que deve dar suporte ao recurso.

+++

+++ A URL que eu configuro deve usar um formato de deeplinking (por exemplo `appname://path`)?

Você pode usar um esquema de URL personalizado (por exemplo, `appname://path`), mas a abordagem recomendada é um link universal ou link de aplicativo (`https://`), que corresponde à configuração baseada em HTTPS nas seções de configuração e implementação desta página.

+++

+++ Os parâmetros UTM no URL estarão disponíveis no aplicativo móvel para análise?

Sim. Os parâmetros UTM configurados no [!DNL Journey Optimizer] são incluídos na URL final retornada no cabeçalho do `Location` quando o aplicativo executa um GET na URL do `mclick`, para que você possa usá-los para análises no aplicativo.

+++

+++ Qual é a experiência do usuário para `/ee/v1/click/` URLs?

O link é aberto no navegador da Web padrão do dispositivo (comportamento de rastreamento de cliques padrão), em vez de ser tratado como um deep link de aplicativo por meio do fluxo do `mclick` descrito nesta página.

+++
