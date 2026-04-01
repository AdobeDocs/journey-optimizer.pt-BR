---
title: Auxiliares
description: Auxiliares
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 39a4893357f3b95938c5a3402516aa45277411aa
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 3%

---

# Auxiliares {#gs-helpers}

## Valor de fallback padrão{#default-value}

O auxiliar `Default Fallback Value` será usado para retornar um valor de fallback padrão se um atributo estiver vazio ou nulo. Esse mecanismo funciona para atributos de Perfil e eventos de Jornada.

**Sintaxe**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

Neste exemplo, o valor `there` será exibido se o atributo `firstName` desse perfil estiver vazio ou nulo.

## Condições{#if-function}

O auxiliar `if` é usado para definir um bloco condicional.
Se a expressão evaluation retornar true, o bloco será renderizado, caso contrário, será ignorado.

**Sintaxe**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Após o auxiliar `if`, você pode inserir uma instrução `else` para especificar um bloco de código a ser executado, se a mesma condição for falsa.
A instrução `elseif` especificará uma nova condição para testar se a primeira instrução retorna false.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Exemplos**

1. **Renderizar diferentes links de repositório com base em expressões condicionais**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalog</a>
   {%/if%}
   ```

1. **Determinar extensão de endereço de email**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Adicionar um link condicional**

   A operação a seguir adicionará um link para o site &#39;www.adobe.com/academia&#39; para perfis com endereços de email &#39;.edu&#39; somente, para o site &#39;www.adobe.com/org&#39; para perfis com endereços de email &#39;.org&#39; e o URL padrão &#39;www.adobe.com/users&#39; para todos os outros perfis:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Conteúdo condicional com base na associação ao público-alvo**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Para saber mais sobre públicos-alvo e o serviço de segmentação, consulte [esta seção](../../audience/about-audiences.md).


## A menos que{#unless}

O auxiliar `unless` é usado para definir um bloco condicional. Por oposição ao auxiliar `if`, se a avaliação da expressão retornar falso, o bloco será renderizado.

**Sintaxe**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Exemplo**

Renderize algum conteúdo com base na extensão de endereço de email:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

## Each{#each}

O auxiliar `each` é usado para iterar sobre uma matriz.
A sintaxe do auxiliar é ```{{#each ArrayName}}``` YourContent `{{/each}}`
Podemos fazer referência a itens de matriz individuais usando a palavra-chave **this** dentro do bloco. O índice do elemento da matriz pode ser renderizado usando `{{@index}}`.

**Sintaxe**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Exemplo**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Exemplo**

Renderize uma lista de produtos que este usuário tem em seu carrinho:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

>[!NOTE]
>
>Você também pode usar o auxiliar `each` para iterar sobre matrizes retornadas de respostas de ação personalizadas. Para obter um exemplo de iteração sobre matrizes aninhadas de uma resposta de ação personalizada, consulte [Usando respostas de ação personalizada em canais nativos](../../action/action-response.md#response-in-channels).

## Com{#with}

O auxiliar `with` é usado para alterar o token de avaliação da parte do modelo.

**Sintaxe**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

O auxiliar `with` é útil também para definir uma variável de atalho.

**Exemplo**

Use com para suavizar nomes de variáveis longos para nomes mais curtos:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

A função `let` permite que uma expressão seja armazenada como uma variável a ser usada posteriormente em uma consulta.

**Sintaxe**

```sql
{% let variable = expression %} {{variable}}
```

**Exemplo**

O exemplo a seguir permite calcular a soma total dos preços dos produtos no carrinho com preços entre 100 e 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

## Metadados de execução {#execution-metadata}

O auxiliar `executionMetadata` permite capturar e armazenar dinamicamente pares de valores-chave personalizados no contexto de execução da mensagem.

**Sintaxe**

```
{{executionMetadata key="your_key" value="your_value"}}
```

Nesta sintaxe, `key` refere-se ao nome dos metadados e `value` são os metadados a serem mantidos.

**Caso de uso**

Com essa função, é possível anexar informações contextuais a qualquer ação nativa de suas campanhas ou jornadas. Isso permite exportar dados contextuais de delivery em tempo real para sistemas externos para várias finalidades, como rastreamento, análise, personalização e processamento downstream.

>[!NOTE]
>
>* Não há suporte para a função de Metadados de Execução em [ações personalizadas](../../action/action.md).
>* A função de Metadados de execução não é visível quando o próprio conteúdo é exibido.

Por exemplo, você pode usar o assistente de Metadados de execução para anexar uma ID específica a cada delivery enviado para cada perfil. Essas informações são geradas durante o tempo de execução e os metadados de execução enriquecidos podem ser exportados para reconciliação downstream com uma plataforma de relatórios externa.

**Como funciona**

Selecione qualquer elemento do conteúdo do canal dentro de uma campanha ou jornada e, usando o editor de personalização, adicione o auxiliar do `executionMetadata` a esse elemento.


Durante o tempo de execução, o valor dos metadados é adicionado ao **[!UICONTROL Conjunto de Dados de Eventos de Feedback de Mensagens]** existente com a seguinte adição de esquema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>Saiba mais sobre conjuntos de dados em [esta seção](../../data/get-started-datasets.md).

**Limitações**

Há um limite superior de 2 kb nos pares de valores principais por ação. Se o limite de 2Kb for excedido, a mensagem ainda será entregue, mas qualquer um dos pares de valores principais poderá ser truncado.

Os metadados não são capturados para perfis excluídos da ação. Quando um perfil é excluído do recebimento de uma mensagem, nenhuma entrada de metadados é criada para esse perfil no conjunto de dados.

**Exemplo**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

Neste exemplo, assumindo `profile.person.name.firstName` = &quot;Alex&quot;, a entidade resultante é:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

## Criptografar {#url-parameter-encryption-helper}

>[!AVAILABILITY]
>
>Esse recurso está disponível em Disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.
>
>No momento, esse recurso só está disponível para o canal de email.

A função `Encrypt` permite criptografar qualquer valor de expressão no momento da renderização — geralmente um atributo de perfil, um token ou até mesmo uma estrutura JSON rígida criada na expressão — antes de ser gravado em um parâmetro de consulta em links de rastreamento ou páginas de aterrissagem.

Os valores que apareceriam como texto sem formatação no URL (incluindo PII ou outros dados confidenciais) não são legíveis quando o link é inspecionado ou encaminhado. Somente os valores envolvidos com este auxiliar são criptografados; o restante do URL permanece inalterado.

**Caso de uso**

Este auxiliar permite proteger os dados de perfil confidenciais (PII) antes de incluí-los na saída renderizada.

**Pré-requisitos**

Um administrador deve criar pelo menos uma chave ativa no registro de chaves no nível da sandbox. [Saiba como criar e gerenciar chaves](../url-parameter-encryption.md#create-keys)

>[!NOTE]
>
>O uso de uma chave revogada ou de outra forma não ativa deve causar falha na personalização no momento da renderização, para que uma mensagem não seja enviada com uma chave inválida.

**Sintaxe**

```text
{{encrypt dataPath keyName="keyName" version="version" result="variableName"}}
```

**Uso**

Este auxiliar criptografa dados confidenciais e armazena o resultado em uma variável de modelo. <!--The encryption is performed using the AES-256-GCM algorithm.-->

Você pode aplicar o auxiliar a um parâmetro, vários ou todos os parâmetros em um link, dependendo do design do URL e das restrições de comprimento.

* **Entrada**: `dataPath` (referência de dados que deve ser resolvida para uma cadeia de caracteres), `keyName` (identificador de chave de criptografia), `version` (versão de chave opcional), `result` (nome de variável para saída criptografada)
* **Saída**: torna o valor criptografado disponível na variável `result` especificada.
* **Formato do resultado**: a variável do resultado contém uma cadeia de caracteres separada por pontos: `keyName.version.nonce.authTag.cipherText` (todos os segmentos, exceto `keyName` e `version`, são codificados com base64 segura para URL sem preenchimento).
* **Requisitos de chave estática**: `keyName` e `version` devem ser literais de cadeia de caracteres estática (não há suporte para referências dinâmicas).
* **Versão padrão**: o parâmetro `version` é opcional; se omitido, o serviço de chave de criptografia resolverá a versão padrão

**Exemplos**

| Exemplo de expressão | Resultado |
| --- | --- |
| `{{encrypt profile.person.email keyName="email-key" version="1" result="enc"}}{{enc}}` | `email-key.1.RkFrZU5vbmNlQUJD.T3V0cHV0QXV0aFRhZ0Fh.am9obkBleGFtcGxlLmNvbQ` |
| `{{encrypt profile.person.name.firstName keyName="pii-key" version="2" result="encName"}}{{encName}}` | `pii-key.2.U29tZVJhbmRvbUlW.QXV0aGVudGljYXRpb25UYQ.Sm9obg` |

**Medidas de proteção**

* A descriptografia é tratada fora de [!DNL Journey Optimizer] em suas páginas de aterrissagem, aplicativos ou APIs. Planeje o ciclo de vida e a rotação da chave com sua equipe de segurança para que as cargas históricas ainda possam ser descriptografadas onde necessário.

* As chaves revogadas não devem ser usadas para a nova criptografia. Siga sua política de segurança para rodízio e desativação.

* O processo de criptografia que consome muitos recursos, usando a função `Encrypt`, pode afetar a taxa de transferência no momento da renderização.
