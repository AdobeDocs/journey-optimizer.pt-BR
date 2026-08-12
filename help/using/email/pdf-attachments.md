---
solution: Journey Optimizer
product: journey optimizer
title: Anexar um arquivo PDF a um email
description: Saiba como anexar arquivos estáticos ou personalizados do PDF a um email
feature: Email Design
topic: Content Management
role: User
level: Beginner
keywords: email, mensagem, anexo, pdf, editor, personalizado, acionado por API
exl-id: 71e218d0-5b3b-4db5-8b7b-d08df8f088c4
TQID: https://experienceleague.adobe.com/9IgYERskcUrIAhTb3xlNgWTRyY-04O58ZB8I0lYFh4g
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: c1270581f5184ca1f5375a2838dfb2906805a259
workflow-type: tm+mt
source-wordcount: 916
ht-degree: 7%

---

# Anexar um arquivo PDF a um email {#pdf-attachments}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como anexar arquivos PDF estáticos ou personalizados a emails, incluindo os tipos de campanha compatíveis e os limites aplicáveis de contagem, tamanho e volume.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_pdf_attachments"
>title="Adicionar um anexo do PDF"
>abstract="Navegue para selecionar um arquivo PDF para anexar ao seu email.</br>Você pode enviar até 6 mensagens com um anexo do PDF por perfil por ano. O tamanho máximo permitido para cada anexo é de 5 MB.</br>Para qualquer tamanho ou volume adicional, você pode comprar o complemento Anexos do PDF. Para obter mais informações, entre em contato com um representante da Adobe."

Você pode anexar um arquivo PDF estático às mensagens de email enviadas com [!DNL Journey Optimizer]. Se você usa [campanhas acionadas por API](../campaigns/api-triggered-campaigns.md), também será possível anexar um [arquivo PDF personalizado para cada destinatário](#personalized-attachments).

Observe que os anexos personalizados do PDF exigem recuperação e processamento adicionais de arquivos. As campanhas que as usam podem ter latência de processamento mais alta e taxa de transferência mais baixa do que as campanhas sem anexos, especialmente ao usar vários arquivos PDF ou arquivos maiores.

>[!IMPORTANT]
>
>* Você pode enviar até 6 mensagens com um anexo do PDF por perfil por ano, seja o anexo estático ou personalizado.
>
>* O tamanho máximo para cada anexo é 5 MB. Para emails com [anexos personalizados](#personalized-attachments), todos os anexos estáticos e personalizados do PDF no email compartilham um limite combinado de 5 MB por padrão.
>
> Para qualquer tamanho ou volume adicional, você pode comprar o complemento Anexos da PDF, o que aumenta o limite combinado de anexos personalizados para 10 MB. Para obter mais informações, entre em contato com um representante da Adobe.

Para anexar um arquivo do PDF a uma mensagem de email, siga as etapas abaixo.

1. Crie um email em uma jornada ou campanha. [Saiba mais](create-email.md)

1. Na guia jornada ou campanha **[!UICONTROL Conteúdo]**, selecione **[!UICONTROL Adicionar ativo]** na seção **[!UICONTROL Anexo]**.

   ![](assets/email-select-pdf.png)

1. O repositório do Assets Essentials é exibido.

   >[!NOTE]
   >
   >Ao criar mensagens, você acessa o repositório do Assets Essentials diretamente de dentro da interface da Journey Optimizer. Para saber mais sobre a interface do usuário incorporada [!DNL Assets Essentials], consulte a [documentação do Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. Use o filtro **[!UICONTROL PDF]** na seção **[!UICONTROL Tipo MIME]** para restringir a seleção ao formato de arquivo correto.

   ![](assets/email-assets-pdf.png)

   >[!NOTE]
   >
   >Somente o formato PDF é permitido para anexos.

1. Selecione o arquivo de sua escolha.

   * Você só pode selecionar um arquivo por vez.
   * O tamanho máximo para cada anexo é 5 MB.

1. Depois de concluído, o nome e o tamanho do arquivo selecionado são exibidos na seção **[!UICONTROL Anexo]**.

   Você pode remover o arquivo selecionado usando o ícone Mais ações ao lado do nome do arquivo.

   ![](assets/email-remove-attachment.png)

>[!NOTE]
>
>Ao salvar sua mensagem como [modelo de conteúdo](../content-management/create-content-templates.md), o anexo do PDF não é retido com o modelo. Se você criar um novo email a partir do modelo de conteúdo salvo, será necessário reanexar o arquivo.

## Anexar arquivos personalizados do PDF para campanhas acionadas por API {#personalized-attachments}

Você também pode anexar arquivos PDF específicos do recipient a um único email enviado por meio de uma [campanha acionada por API](../campaigns/api-triggered-campaigns.md). Diferentemente de um anexo estático, cada destinatário pode receber um arquivo diferente, como uma fatura, um cartão de embarque, um contrato ou uma etiqueta de envio.

O tamanho combinado de todos os anexos estáticos e personalizados do PDF em um email é limitado a 5 MB por padrão. As organizações com o complemento PDF Attachments aplicável podem usar um limite combinado de até 10 MB.

>[!IMPORTANT]
>
>* Os anexos personalizados do PDF são compatíveis somente com campanhas de email transacionais acionadas por API.
>
>* É possível incluir até cinco anexos do PDF em um email. Esse limite inclui anexos estáticos e personalizados. Por exemplo, um email contendo um PDF estático pode incluir até quatro PDFs personalizados. Se precisar enviar mais, divida-os em várias comunicações.
>
>* Anexos personalizados e estáticos do PDF são contados na mesma cota. [Saiba mais](#pdf-attachments)

Os anexos personalizados do PDF devem ser carregados no contêiner [Data Landing Zone](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"} específico do anexo e depois referenciados na carga da API. Atualmente, a Data Landing Zone é o único local de armazenamento compatível com anexos personalizados da PDF.

1. Recupere as credenciais da Zona de Aterrissagem de Dados para sua sandbox usando `type=ajoemailattachments` para a mesma organização IMS e sandbox da solicitação de execução, conforme descrito na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}. Dependendo do provedor de nuvem, use o container do Azure ou o bucket e a pasta do AWS retornados pela API.

1. Gere os arquivos PDF com a ferramenta de sua escolha e faça upload deles para o contêiner da Data Landing Zone.

   Observe que a Data Landing Zone exclui automaticamente os arquivos após sete dias. Verifique se os arquivos do PDF permanecem disponíveis no contêiner até que a entrega da mensagem e todas as tentativas sejam concluídas.

1. Na carga da API, para cada destinatário, adicione uma matriz `attachments` contendo o nome do arquivo, o tipo de conteúdo e o caminho da Zona de aterrissagem de dados da PDF a ser enviada. [Saiba como personalizar o conteúdo da campanha acionada por API](../campaigns/api-triggered-campaign-content.md#contextual)

   ```json
   "attachments": [
     {
       "name": "invoice-12345.pdf",
       "contentType": "application/pdf",
       "source": {
         "type": "dlzPath",
         "path": "attachments/invoice-12345.pdf"
       }
     }
   ]
   ```

   Observe que `source.path` é o caminho do objeto relativo ao contêiner da Zona de Aterrissagem de Dados específico do anexo recuperado com `type=ajoemailattachments`. Não inclua o nome do container do Azure, o bucket ou a pasta do AWS, credenciais ou um URL de armazenamento completo.

No momento do envio, [!DNL Journey Optimizer] busca o arquivo no local especificado e o anexa à mensagem para esse destinatário. Os anexos personalizados do PDF são suportados para campanhas de [Alta Taxa de Transferência](../campaigns/api-triggered-high-throughput.md) na região primária. Eles não são compatíveis durante o failover regional.

Para obter a referência da carga total da API, consulte a [Documentação da API de execução de mensagem interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution){target="_blank"}.
