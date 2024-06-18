---
solution: Journey Optimizer
product: journey optimizer
title: Usar JavaScript personalizado em uma página de destino
description: Saiba como criar o conteúdo de uma landing page no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: Developer
level: Experienced
keywords: landing page, landing page, javascript, código
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 2%

---

# Usar JavaScript personalizado em uma página de destino {#lp-custom-js}

Você pode definir o conteúdo da página de aterrissagem usando o JavaScript personalizado. Por exemplo, se você precisar executar estilos avançados ou adicionar comportamentos personalizados às páginas de aterrissagem, será possível criar seus próprios controles e executá-los no [!DNL Journey Optimizer].

## Inserir código JavaScript em uma página inicial

Para inserir JavaScript personalizado no conteúdo da página de aterrissagem, faça o seguinte:

* Importe o conteúdo de HTML existente ao começar a criar o conteúdo e selecione o arquivo que inclui o código JavaScript personalizado. Saiba como importar conteúdo [nesta seção](../email/existing-content.md).

* Projete a landing page do zero ou com base em um template salvo. Arraste e solte a **[!UICONTROL HTML]** componente de conteúdo na tela e mostrar o código-fonte para adicionar seu JavaSCript no componente. Saiba como usar o componente de HTML no [nesta seção](../email/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

  ![](assets/lp_designer-html-component.png)

* Insira ou cole o código JavaScript diretamente no designer de conteúdo. Saiba como codificar seu próprio conteúdo [nesta seção](../email/code-content.md).

>[!NOTE]
>
>Atualmente, não é possível exibir JavaScript em ação quando [visualização da landing page](create-lp.md#test-landing-page).

Para que a landing page seja exibida corretamente, use a seguinte sintaxe conforme descrito nas seções abaixo.

## Inicialização de código

Para inicializar o código JavaScript, você deve usar o `lpRuntimeReady` evento. Esse evento será acionado após a inicialização bem-sucedida da biblioteca. O retorno de chamada será executado com o `lpRuntime` objeto para expor o método de biblioteca e os ganchos.

`LpRuntime` significa &quot;Tempo de execução da landing page&quot;. Esse objeto é o identificador principal da biblioteca. Ele vai expor ganchos, métodos de envio de formulário e outros métodos de utilitário que podem ser usados no JavaScript personalizado.

**Exemplo:**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## Ganchos

Usando ganchos, você pode anexar um método durante o ciclo de vida do envio do formulário. Por exemplo, você pode usar ganchos para executar alguma validação de formulário antes que o formulário seja realmente enviado.

Estes são os ganchos que você pode usar:

| Nome | Descrição |
|--- |--- |
| addBeforeSubmitHook | O gancho personalizado a ser chamado antes do envio do formulário. Retorna verdadeiro para continuar o envio, caso contrário, retorna falso para bloquear o envio. |
| addOnFailureHook | O gancho personalizado a ser chamado no envio de formulário com falha. |
| addOnSuccessHook | Gancho personalizado a ser chamado no envio bem-sucedido do formulário. |

**Exemplo:**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## Envio de formulário personalizado

Os métodos listados abaixo são usados para executar envios de formulários personalizados.

>[!NOTE]
>
>Como o envio do formulário é manipulado pelo JavaScript personalizado, o envio padrão precisa ser desativado explicitamente ao configurar uma variável global `disableDefaultFormSubmission` para `true`.

| Nome | Descrição |
|--- |--- |
| submitForm | Este método enviará o formulário e lidará com o fluxo de envio posterior. |
| submitFormPartial | Esse método também enviará o formulário, mas ignorará o fluxo de envio posterior. Por exemplo, se você tiver configurado o redirecionamento para página bem-sucedida após o envio bem-sucedido, esse redirecionamento não ocorrerá no caso de envio parcial de formulário. |

**Exemplos:**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## Função de utilitário

| Nome | Descrição |
|--- |--- |
| getFormData | Este método pode ser usado para obter o `formData` no formato de um objeto JSON. Este objeto pode ser passado para `submitForm` para envio de formulário. |

**Exemplo:**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## Casos de uso

### Caso de uso 1: Adição de validação antes do envio do formulário

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### Caso de uso 2: envio parcial do formulário

Por exemplo, você tem um formulário com várias caixas de seleção na página. Ao marcar qualquer caixa de seleção, você deseja que esses dados sejam salvos no backend sem esperar que o usuário clique no botão Enviar.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### Caso de uso 3: tags personalizadas do Analytics

Usando o JavaScript, é possível adicionar ouvintes de campos de entrada e anexar um acionador de chamada de análise personalizado.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### Caso de uso 4: Formulário dinâmico

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
