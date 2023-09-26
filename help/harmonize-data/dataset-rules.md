---
title: Regras do conjunto de dados
description: Saiba como definir regras de conjunto de dados para usar como parte da harmonização de seus dados no Adobe Mix Modeler.
feature: Harmonized Data, Dataset Rules
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# Regras do conjunto de dados

As regras do conjunto de dados ajudam a mapear os campos harmonizados com campos dos dados assimilados no Adobe Mix Modeler.

* Para dados agregados assimilados no Adobe Experience Platform, mapeie um ou mais campos do conjunto de dados disponíveis para os campos harmonizados apropriados.
* Para dados do evento, você pode mapear individualmente um ou mais campos harmonizados para campos do conjunto de dados, diretamente ou usando condições.


## Gerenciar regras e mapeamentos do conjunto de dados

Para ver uma tabela dos mapeamentos de conjunto de dados disponíveis, na interface do Adobe Mix Modeler:

1. Selecionar ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** do painel esquerdo.

1. Selecionar **[!UICONTROL Dataset rules]** na barra superior. Você verá uma tabela dos mapeamentos do conjunto de dados.

As colunas da tabela especificam detalhes sobre os mapeamentos do conjunto de dados:

| Nome da coluna | Detalhes |
| ---------------------- | ----------|
| Conjunto de dados | O nome do conjunto de dados. |
| Fonte | A origem do conjunto de dados, que pode ser Adobe Analytics, Eventos de experiência, Resumo (agregado) ou Eventos de experiência do consumidor. |
| Esquema | O esquema com o qual o conjunto de dados está em conformidade. Você pode selecionar rapidamente o nome do esquema para abri-lo em uma nova guia no editor de esquemas em Adobe Mix Modeler - Esquemas. |
| Granularidade | A granularidade dos dados no conjunto de dados. Os valores possíveis são Diário, Semanal, Mensal ou Anual. |
| Início da semana | Especifica qual dia da semana é considerado o início de uma nova semana para o conjunto de dados específico. |
| Última modificação | Data e hora da última modificação do mapeamento do conjunto de dados. |

{style="table-layout:auto"}

### Criar um mapeamento de conjunto de dados

Para criar um mapeamento de conjunto de dados, na ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Adobe Mix Modeler, selecione **[!UICONTROL Create Dataset Mapping]**.

No **[!UICONTROL Create]** tela,

1. Entrada **[!UICONTROL Dataset Details]**, selecione um conjunto de dados em **[!UICONTROL Select dataset]** para iniciar a configuração.

1. Selecione um dia para a **[!UICONTROL Start of the week]**.

1. Selecionar **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** para **[!UICONTROL Granularity]**.

1. Quando tiver selecionado um **[!UICONTROL Summary]** tipo de conjunto de dados:

   1. Mapear cada um dos **[!UICONTROL Available dataset fields]** para o correspondente **[!UICONTROL Standard harmonized fields]**. Se não quiser mapear um campo de conjunto de dados para um campo harmonizado, selecione explicitamente **[!UICONTROL -- None --]**.

   1. Se precisar de um novo campo harmonizado, não disponível na lista, selecione **[!UICONTROL Create New]** para criar um novo campo harmonizado. Você verá a caixa de diálogo conforme descrito em [Adicionar um novo campo harmonizado](fields.md#add-a-harmonized-field) para permitir adicionar um novo campo harmonizado rapidamente.

   1. Quando o mapeamento for concluído para todos os campos, selecione **[!UICONTROL Save]**. Selecionar **[!UICONTROL Cancel]** para cancelar o mapeamento.

      ![Criar regras de conjunto de dados](../assets/dataset-create-summary.png)

1. Ao selecionar um tipo de evento de conjunto de dados, na caixa sombreada abaixo **[!UICONTROL Map to harmonized fields]**:

   1. Selecione um campo harmonizado em **[!UICONTROL Standard harmonized field]**.

   1. Quando o campo harmonizado selecionado for do tipo métrica:

      1. Selecionar **[!UICONTROL Count]** ou **[!UICONTROL Sum]** de **[!UICONTROL Mapping type]**.

      1. Selecione um **[!UICONTROL *Campo do conjunto de dados da AEP *]**para o qual você deseja mapear o campo harmonizado por padrão.

   1. Quando o campo selecionado é do tipo dimensão:

      1. Selecionar **[!UICONTROL Map Into]** ou **[!UICONTROL Case]** de **[!UICONTROL Mapping type]**.

      1. Quando tiver selecionado **[!UICONTROL Map Into]**, selecione **[!UICONTROL Field]** e **[!UICONTROL *Campo do conjunto de dados da AEP *]**ou **[!UICONTROL Value]**e um valor padrão para mapear o campo harmonizado por padrão para o campo do conjunto de dados ou valor inserido.

      1. Quando tiver selecionado **[!UICONTROL Case]**, selecione **[!UICONTROL Field]** e **[!UICONTROL *Campo do conjunto de dados da AEP *]**ou **[!UICONTROL Value]**e um valor padrão para mapear o campo harmonizado por padrão para o campo do conjunto de dados ou valor inserido.

         1. Além disso, você define um ou mais casos, que consistem em uma ou mais condições para definir explicitamente valores. Cada condição pode verificar se há **[!UICONTROL *Campo do conjunto de dados da AEP *]**se **[!UICONTROL Exists]**ou **[!UICONTROL Not Exists]**ou se **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**ou **[!UICONTROL Ends With]**um valor inserido em**[!UICONTROL * Inserir valor de entrada *]**.

         1. Para adicionar outro caso, selecione ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add case]**, para adicionar outra condição, selecione ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Para excluir um caso ou uma condição, selecione ![Fechar](../assets/icons/Close.svg) no recipiente correspondente.

         1. Para selecionar se alguma ou todas as condições devem se aplicar a um caso, selecione **[!UICONTROL Any of]** ou **[!UICONTROL All of]**.

         1. Para definir o valor de resultado de um caso, insira o valor em **[!UICONTROL Then]**.

      O exemplo abaixo

      * usa um **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** para mapear o **[!UICONTROL Channel Type At Source]** campo harmonizado para o **[!UICONTROL channel_type]** do campo **[!DNL Luma Transactions]** conjunto de dados.

      * usa um **[!UICONTROL Case]** **[!UICONTROL Mapping]** digite para mapear condicionalmente o valor do **[!UICONTROL marketing.campaignName]** no campo **[!DNL Luma Transactions]** conjunto de dados **[!UICONTROL Campaign]** harmonizado. O campo Campaign harmonizado está definido como:

         * `Black Friday` quando a variável **[!UICONTROL marketing.campaignName]** é `_black_friday` ou `BlackFriday`.
         * ao valor de **[!UICONTROL marketing.campaignName]** em todos os outros casos.

        ![Evento de regra do conjunto de dados](../assets/dataset-create-event.png)

1. Selecionar ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]** para definir campos adicionais.

Quando terminar, selecione **[!UICONTROL Save]** para salvar o mapeamento ou selecione **[!UICONTROL Cancel]** para cancelar o mapeamento.


### Editar um mapeamento de conjunto de dados

Para editar um mapeamento de conjunto de dados, na ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Adobe Mix Modeler:

1. Selecionar ![Mais](../assets/icons/More.svg) no **[!UICONTROL Dataset]** coluna para o mapeamento do conjunto de dados que você deseja editar.
1. No menu de contexto, selecione ![Editar](../assets/icons/Edit.svg) **[!UICONTROL Edit]** para começar a editar o mapeamento do conjunto de dados. Consulte [Criar um mapeamento de conjunto de dados](#create-a-dataset-mapping) para obter mais detalhes.


### Excluir um mapeamento de conjunto de dados

Para excluir um mapeamento de conjunto de dados, na variável ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Adobe Mix Modeler:

1. Selecionar ![Mais](../assets/icons/More.svg) no **[!UICONTROL Dataset]** coluna para o mapeamento de conjunto de dados que você deseja excluir.
1. No menu de contexto, selecione ![Excluir](../assets/icons/Delete.svg) **[!UICONTROL Delete]** para excluir o mapeamento do conjunto de dados.


## Sincronizar dados

Para sincronizar dados entre seus dados harmonizados e os conjuntos de dados de resumo e/ou evento, siga toda a lógica nas regras do conjunto de dados:

1. Selecione **[!UICONTROL Sync data]**.

1. No **[!UICONTROL Sync data for dataset rules]** , selecione **[!UICONTROL Refresh harmonized data for summary datasets]**, **[!UICONTROL Refresh harmonized data for event datasets]** ou **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Selecionar **[!UICONTROL Sync]** para iniciar a sincronização com base nas regras definidas do conjunto de dados entre os dados harmonizados e os dados em conjuntos de dados. Para cancelar a sincronização, selecione **[!UICONTROL Cancel]**.

   ![Sincronizar dados](../assets/sync-data.png)

