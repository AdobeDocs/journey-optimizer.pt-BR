---
title: Identificador complementar em jornadas acionadas por eventos
description: Saiba como usar o identificador complementar em jornadas acionadas por eventos.
badge: label="Disponibilidade limitada" type="Informative"
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
source-git-commit: 14a0054c605edd8ff0b63e71fb5c30104ff513ed
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 8%

---

# Identificador complementar em jornadas acionadas por eventos {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="Usar identificador complementar"
>abstract="O identificador complementar é um identificador secundário que fornece contexto adicional para a execução de uma jornada. Para defini-lo, selecione o campo a ser usado como o identificador complementar e escolha um namespace para associar a ele."

>[!AVAILABILITY]
>
>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.

Por padrão, as jornadas acionadas por eventos são executadas no contexto de uma **ID de perfil**. Isso significa que, desde que o perfil esteja ativo em uma determinada jornada, ele não poderá inserir outra jornada novamente. Para evitar isso, o Journey Optimizer permite capturar um **identificador complementar** em seus eventos, como uma ID de pedido, ID de assinatura, ID de receita, além da ID de perfil.
Neste exemplo, adicionamos uma ID de reserva como identificador complementar.

![](assets/event-supplemental-id.png){width=40% zoomable}

Ao fazer isso, as jornadas acionadas pelo evento são executadas no contexto da ID de perfil associada ao identificador complementar (aqui, a ID de reserva). Uma instância da jornada é executada para cada iteração do identificador complementar. Isso permite várias entradas da mesma ID de perfil no jornada, caso tenham feito reservas diferentes.

Além disso, o Journey Optimizer permite aproveitar os atributos do identificador complementar (por exemplo, número de reserva, data de renovação da prescrição, tipo de produto) para personalização de mensagens, garantindo comunicações altamente relevantes. <!--Example: A healthcare provider can send renewal reminders for each prescription in a patient's profile.-->

➡️ [Conheça este recurso no vídeo](#video)

## Medidas de proteção e limitações {#guardrails}

* **Limites de instância simultânea**: os perfis não podem ter mais de 10 instâncias de jornada simultâneas.

<!--* **Array depth**: Supplemental identifier objects can have a maximum depth of 3 levels (2 levels of nesting).

    +++Example

    ```
    [
    (level 1) "Atorvastatin" : {
    "description" : "used to lower cholesterol",
    "renewal_date" : "11/20/25",
    "dosage" : "10mg"
    (level 2) "ingredients" : [
    (level 3) "Atorvastatin calcium",
    "lactose monohydrate",
    "microcrystalline cellulose",
    "other" ]
    }
    ]
    ```

    +++
-->
* **Critério de saída**: os critérios de saída, se acionados, sairiam de todas as instâncias do perfil ativas na jornada nesse momento. Ela não seria contextual à combinação de ID de perfil + identificador complementar.

* **Regras de frequência**: cada instância do jornada criada a partir do uso de identificador complementar conta para o limite de frequência, mesmo que um único evento resulte em várias instâncias do jornada.

* **Tipo de dados e estrutura de esquema**: o identificador complementar deve ser do tipo `string`. Ele pode ser um atributo de string independente ou pode ser um atributo de string dentro de uma matriz de objetos. O atributo de string independente resultará em uma única instância de jornada, enquanto o atributo de string dentro de uma matriz de objetos resultará em uma instância de jornada exclusiva por iteração da matriz de objetos. Não há suporte para matrizes de cadeia de caracteres e mapas.

* **reentrada de Jornada**

  O comportamento de reentrada da jornada com identificadores complementares segue a política de reentrada existente:

   * Se a jornada não for reentrante, a mesma ID de perfil + ID complementar não poderá entrar na jornada novamente.
   * Se a jornada for reentrante com uma janela de tempo, a mesma combinação de ID de perfil + ID complementar poderá entrar novamente após a janela de tempo definida.

## Adicionar um identificador complementar e aproveitá-lo em uma jornada {#add}

Para usar um identificador complementar em uma jornada, siga estas etapas:

1. **Marcar o atributo como um identificador no esquema de evento**

   1. Acesse o esquema de evento e localize o atributo que deseja usar como um identificador complementar (por exemplo, ID de reserva, ID de assinatura) e marque-o como uma ID. [Saiba como trabalhar com esquemas](../data/get-started-schemas.md)

   1. Marcar o identificador como uma **[!UICONTROL Identidade]**.

      ![](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >Certifique-se de não marcar o atributo como **Identidade principal**.

   1. Selecione o namespace a ser associado à ID complementar. Deve ser um namespace de identificador não pessoal.

1. **Adicionar a ID complementar ao evento**

   1. Crie ou edite o evento desejado. [Saiba como configurar um evento unitário](../event/about-creating.md)

   1. Na tela de configuração do evento, marque a opção **[!UICONTROL Usar identificador complementar]**.

      ![](assets/supplemental-ID-event.png)

   1. Use o editor de expressão para selecionar o atributo marcado como a ID complementar.

      >[!NOTE]
      >
      >Verifique se você está usando o editor de expressão no **[!UICONTROL modo Avançado]** para selecionar o atributo.

   1. Depois de selecionar a ID complementar, o namespace associado é exibido na tela de configuração do evento como somente leitura.

1. **Adicionar o evento à jornada**

   Arraste o evento configurado para a tela de jornada. Ela acionará uma entrada de jornada com base na ID do perfil e na ID complementar.

   ![](assets/supplemental-ID-journey.png)

1. **Aproveitar atributos de ID complementares**

   Use o editor de expressão e o editor de personalização para fazer referência a atributos do identificador complementar para personalização ou lógica condicional. Os atributos podem ser acessados pelo menu **[!UICONTROL Atributos contextuais]**.

   ![](assets/supplemental-ID-perso.png)

   >[!NOTE]
   >
   >Se estiver trabalhando com arrays (por exemplo, várias receitas ou políticas), use uma fórmula para extrair elementos específicos.

+++ Ver exemplos

   Em uma matriz de objetos com a ID complementar como `bookingNum` e um atributo no mesmo nível chamado `bookingCountry`, a jornada percorrerá o objeto de matriz com base no bookingNum e criará uma instância de jornada para cada objeto.

   * A seguinte expressão na atividade de condição iterará por meio da matriz de objetos e verificará se o valor de `bookingCountry` é igual a &quot;FR&quot;:

     ```
     @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
     ```

   * A seguinte expressão no editor de personalização de email iterará por meio da matriz de objetos, obterá o `bookingCountry` aplicável à instância atual do jornada e o exibirá no conteúdo:

     ```
     {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
     
     {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
     
     {{/each}}
     ```

   * Exemplo do evento usado para acionar a jornada:

     ```
     "bookingList": [
           {
               "bookingInfo": {
                   "bookingNum": "x1",
                         "bookingCountry": "US"
               }
           },
           {
               "bookingInfo": {
                   "bookingNum": "x2",
                   "bookingCountry": "FR"
               }
           }
       ]
     ```

+++

1. **Publicar a jornada**

   Depois de configurada, publique a jornada para começar a usar várias entradas simultâneas com base em identificadores complementares.

## Exemplo de casos de uso

### **Notificações de Renovação de Política**

* **Cenário**: um provedor de seguro envia lembretes de renovação para cada política ativa mantida por um cliente.
* **Execução**:
   * Perfil: &quot;John&quot;.
   * IDs complementares: `"AutoPolicy123", "HomePolicy456"`.
   * O Jornada é executado separadamente para cada política, com datas de renovação personalizadas, detalhes de cobertura e informações sobre prêmios.

### **Gerenciamento de Assinaturas**

* **Cenário**: um serviço de assinatura envia mensagens personalizadas para cada assinatura quando um evento é acionado para essa assinatura.
* **Execução**:
   * Perfil: &quot;Jane&quot;.
   * IDs complementares: `"Luma Yoga Program ", "Luma Fitness Program"`.
   * Cada evento inclui uma ID de assinatura e detalhes sobre essa assinatura. O Jornada é executado separadamente para cada evento/assinatura, permitindo ofertas de renovação personalizadas por assinatura.

### **Recomendações de produto**

* **Cenário**: uma plataforma de comércio eletrônico envia recomendações com base em produtos específicos comprados por um cliente.
* **Execução**:
   * Perfil: &quot;Alex&quot;.
   * IDs complementares: `"productID1234", "productID5678"`.
   * O Jornada é executado separadamente para cada produto, com oportunidades personalizadas de venda adicional.

## Vídeo tutorial {#video}

Saiba como habilitar e aplicar um identificador complementar no [!DNL Adobe Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3464797?quality=12&captions=por_br)
