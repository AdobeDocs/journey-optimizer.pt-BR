---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Carregar arquivo
description: Saiba como usar a atividade Load file em uma campanha orquestrada
hide: true
hidefromtoc: true
exl-id: ae0dc980-2361-4c3b-a68e-ae0bb5dc0a26
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 38%

---

# Carregar arquivo {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile"
>title="Atividade Carregar arquivo"
>abstract="A atividade **Carregar arquivo** é uma atividade de **gerenciamento de dados**. Use esta atividade para trabalhar com dados armazenados em um arquivo externo. Perfis e dados não são adicionados ao banco de dados, mas todos os campos no arquivo de entrada estão disponíveis para personalização ou para atualizar perfis ou qualquer outra tabela. "

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition"
>title="Transição de saída do gerenciamento de rejeições"
>abstract="Transição de saída do gerenciamento de rejeições"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition_reject"
>title="Transição de saída do gerenciamento de rejeições para recusas"
>abstract="Transição de saída do gerenciamento de rejeições para recusas"


A atividade **Carregar arquivo** é uma atividade de **gerenciamento de dados**. Use esta atividade para trabalhar com perfis e dados armazenados em um arquivo externo. Perfis e dados não são adicionados ao banco de dados, mas todos os campos no arquivo de entrada estão disponíveis para personalização ou para atualizar perfis ou qualquer outra tabela.

>[!NOTE]
>Os formatos de arquivo compatíveis são: texto (TXT) e valor separado por vírgula (CSV). É possível carregar arquivos com um tamanho máximo de 50 MB.

Esta atividade pode ser usada com uma atividade [Reconciliation](reconciliation.md) para vincular dados não identificados aos recursos existentes. Por exemplo, a atividade **Carregar arquivo** pode ser colocada antes de uma atividade **Reconciliação** se você importar dados não padrão para o banco de dados.

## Configurar a atividade de carregamento de arquivo {#load-configuration}

A configuração da atividade **Carregar arquivo** envolve duas etapas. Primeiro, é necessário definir a estrutura de arquivo esperada fazendo upload de um arquivo de amostra. Depois disso, você poderá especificar a origem do arquivo cujos dados serão importados. Siga as etapas abaixo para configurar a atividade.

![](../assets/workflow-load-file.png)

### Configurar o arquivo de amostra {#sample}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_samplefile"
>title="Arquivo de amostra"
>abstract="Selecione a estrutura de arquivo esperada fazendo upload de um arquivo de amostra."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_formatting"
>title="Formatação da atividade Carregar arquivo"
>abstract="Na seção **Formatação**, especifique como o arquivo está formatado para garantir que os dados sejam importados corretamente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_valueremapping"
>title="Remapeamento de valor da atividade Carregar arquivo"
>abstract="Use essa opção para mapear valores específicos dos arquivos carregados com novos valores. Por exemplo, se a coluna contiver valores “Verdadeiro”/“Falso”, você poderá adicionar um mapeamento para substituir automaticamente esses valores por caracteres “0”/“1”."

Siga estas etapas para configurar o arquivo de amostra usado para definir a estrutura de arquivo esperada:

1. Adicione uma atividade **Load file** à campanha orquestrada.

1. Selecione o arquivo de amostra a ser usado para definir a estrutura de arquivo esperada. Para fazer isso, clique no botão **Selecionar arquivo** na seção **[!UICONTROL Arquivo de exemplo]** e selecione o arquivo local a ser usado.

1. Uma pré-visualização do arquivo de amostra é mostrada, exibindo no máximo 30 linhas.

1. Na lista suspensa **[!UICONTROL Tipo de arquivo]**, especifique se o arquivo está usando colunas delimitadas ou colunas de largura fixa.

   ![](../assets/workflow-load-file-sample.png)

1. Para tipos de arquivo de colunas delimitadas, use a seção **Colunas** para configurar as propriedades de cada coluna.

   +++Opções disponíveis para colunas de arquivo

   * **[!UICONTROL Rótulo]**: rótulo a ser exibido para a coluna.
   * **[!UICONTROL Tipo de dados]**: tipo de dados contidos na coluna.
   * **[!UICONTROL Largura]** (tipo de dados da cadeia de caracteres): número máximo de caracteres a serem exibidos na coluna.
   * **[!UICONTROL Transformação de Dados]** (tipo de dados de cadeia de caracteres): aplique a transformação aos valores contidos na coluna.
   * **[!UICONTROL Gerenciamento de espaço em branco]** (tipo de dados da cadeia de caracteres): especifique como gerenciar os espaços contidos na coluna.
   * **[!UICONTROL Separadores]** (tipos de dados data, hora, número inteiro e número)*: especifique os caracteres a serem usados como separadores.
   * **[!UICONTROL Permitir NULLs]**: especifique como gerenciar valores vazios na coluna.
   * **[!UICONTROL Processamento de erros]** (tipo de dados de cadeia de caracteres): especifique o comportamento em caso de erros em uma das linhas.
   * **[!UICONTROL Remapeamento de valores]**: essa opção permite mapear valores específicos com novos valores. Por exemplo, se a coluna contiver valores “Verdadeiro”/“Falso”, você poderá adicionar um mapeamento para substituir automaticamente esses valores por caracteres “0”/“1”.

+++

1. Na seção **Formatação**, especifique como o arquivo está formatado para garantir que os dados sejam importados corretamente.

### Definir o arquivo de destino para upload {#target}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetfile"
>title="Arquivo de destino da atividade Carregar arquivo"
>abstract="Na seção **[!UICONTROL Arquivo de destino]**, especifique como recuperar o arquivo para fazer upload no servidor."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_nameofthefile"
>title="Nome do arquivo"
>abstract="Especifique o nome do campo a ser carregado no servidor. Clique no ícone **[!UICONTROL Abrir caixa de diálogo de personalização]** para usar o editor de expressão, incluindo variáveis de evento, para calcular o nome do arquivo."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetdb"
>title="Banco de dados de públicos-alvo"
>abstract="Se você estiver acessando uma atividade de **[!UICONTROL Carregar arquivo]** que já tenha sido configurada, uma seção adicional de **[!UICONTROL Banco de dados de destino]** estará disponível se você tiver configurado a atividade para carregar o arquivo para um banco de dados externo."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_command"
>title="Comando Carregar arquivo"
>abstract="Permitir comandos arbitrários para pré-processamento é uma vulnerabilidade de segurança. Desabilite a opção de segurança XtkSecurity_Disable_Preproc para forçar o uso de uma lista predefinida de comandos."

>[!CAUTION]
>
>Antes de carregar o arquivo de destino, verifique se ele segue à formatação do arquivo de amostra. Qualquer discrepância no formato de arquivo, estrutura de coluna ou número de colunas pode levar a erros durante a execução orquestrada da campanha.

Para definir o arquivo de destino para upload, siga estas etapas:

1. Na seção **[!UICONTROL Arquivo de destino]**, especifique a ação a ser executada ao recuperar o arquivo a ser carregado no servidor.

   * **[!UICONTROL Carregar arquivo do computador local]**: selecione o arquivo a ser carregado do computador.

   * **[!UICONTROL Especificado na transição]**: carregue o arquivo especificado na transição de entrada futura de uma atividade anterior, como **[!UICONTROL Transferir arquivo]**.

   * **[!UICONTROL Pré-processar o arquivo]**: carregue o arquivo especificado na transição anterior e aplique um comando de pré-processamento a ele, como **[!UICONTROL Descompactação]** ou **[!UICONTROL Descriptografar]**.

   * **[!UICONTROL Calculado]**: carregue o arquivo cujo nome está especificado no campo **[!UICONTROL Nome do arquivo]**. Clique no ícone **[!UICONTROL Abrir caixa de diálogo de personalização]** para usar o editor de expressão, incluindo variáveis de evento, para calcular o nome do arquivo.

   ![](../assets/workflow-load-file-config.png)

   >[!NOTE]
   >
   >Se você estiver acessando uma atividade de **[!UICONTROL Carregar arquivo]** que já foi configurada, uma seção adicional de **[!UICONTROL Banco de dados de destino]** será exibida se você tiver configurado a atividade para carregar o arquivo para um banco de dados externo. Ele permite especificar se você deseja fazer upload do arquivo no servidor do Campaign ou no banco de dados externo.

### Opções adicionais {#options}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_rejectmgt"
>title="Gerenciamento de rejeições da atividade Carregar arquivo"
>abstract="Na seção **Rejeitar gerenciamento**, especifique como a atividade deve se comportar em caso de erros. Você pode definir o número máximo de erros permitidos e ativar a opção **[!UICONTROL Manter rejeições em um arquivo]** para fazer download no servidor de um arquivo contendo os erros que ocorreram durante a importação."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_delete"
>title="Excluir arquivo após importação"
>abstract="Ative a opção **Excluir arquivo após importação** para excluir o arquivo original do servidor após a importação."


1. Na seção **Reject management**, especifique como a atividade deve se comportar em caso de erros:

   * No campo **[!UICONTROL Número de erros permitidos]**, especifique o número máximo de erros autorizados ao processar o arquivo a ser carregado. Por exemplo, se o valor for definido como &quot;20&quot;, a execução da campanha orquestrada falhará se houver mais de 20 erros ao carregar o arquivo.

   * Para manter ativados os erros ocorridos ao carregar o arquivo, alterne a opção **[!UICONTROL Manter rejeições em um arquivo]** e especifique o nome desejado para o arquivo no campo **[!UICONTROL Arquivo de Rejeição]**.

     Após ativar essa opção, uma transição de saída adicional chamada &quot;Complement&quot; é adicionada após a atividade. Qualquer erro que ocorrer durante a importação será armazenado no arquivo especificado no servidor.

1. Para excluir o arquivo carregado do servidor após a execução da campanha orquestrada, alterne a opção **[!UICONTROL Excluir arquivo após importação]**.

   ![](../assets/workflow-load-file-options.png)

1. Clique em **Confirmar** assim que as configurações estiverem corretas.

## Exemplo {#load-example}

Um exemplo de carregamento de arquivo externo usado com a atividade **Reconciliação** está disponível em [esta seção](reconciliation.md#reconciliation-example).
