---
title: Conversões
description: Saiba como criar conversões para usar como parte da harmonização de seus dados no Mix Modeler.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 665b344dfa94275d71e0ecf198d9bb9b73ea584b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---

# Conversões

Eventos de conversão são objetivos de negócios que identificam o impacto das atividades de marketing. Exemplos: pedidos de comércio eletrônico, compras na loja, visitas a sites e assim por diante.

Você define conversões de marketing para análise de atribuição.

## Gerenciar conversões

Para ver uma tabela das conversões disponíveis, na interface do Mix Modeler:

1. Selecione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** no painel esquerdo.

1. Selecione **[!UICONTROL Conversions]** na barra superior. Você verá uma tabela das conversões.

As colunas da tabela especificam detalhes sobre a conversão:

| Nome da coluna | Detalhes |
| --- | ---|
| Nome | O nome da conversão. |
| Receita | A métrica de dados harmonizada a ser usada para calcular a receita de uma conversão. |
| Métrica de conversão | A métrica de dados harmonizada a ser usada como a métrica de conversão para análise. |
| Categoria | A categoria de conversão da conversão. |
| Criado em | Data e hora de criação da conversão. |
| Última modificação | Data e hora da última modificação da conversão. |

{style="table-layout:auto"}

## Adicionar uma conversão

Para adicionar uma conversão, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** em Mix Modeler:

1. Selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. No diálogo **[!UICONTROL Create conversion]**:

   1. Digite um nome para **[!UICONTROL Conversion]**, por exemplo `Store Conversions`.

   1. Defina o **[!UICONTROL Conversion category]**.

      1. Selecione um valor de **[!UICONTROL *Selecionar harmonizar...*]**, por exemplo `Conversion types`.

      1. Selecione um valor para o operador ![Divisa](/help/assets/icons/ChevronDown.svg), por exemplo **[!UICONTROL is]**.

      1. Selecione um valor em **[!UICONTROL *Selecione o valor *]**ou insira um valor, por exemplo **[!UICONTROL Store]**.

   1. Selecione um campo harmonizado de **[!UICONTROL Conversion metric for analysis]**, por exemplo **[!UICONTROL Orders]**.

   1. Selecione um campo harmonizado de **[!UICONTROL Revenue field]**, por exemplo **[!UICONTROL Gross Demand]**.

   1. Para criar a conversão, selecione **[!UICONTROL Create]**. Para cancelar a criação de uma conversão, selecione **[!UICONTROL Cancel]**.

      ![Texto alternativo](/help/assets/create-conversion.png)

1. Quando criada, a conversão é adicionada à tabela de conversões.


## Exibir detalhes

Para exibir detalhes de uma conversão:

1. Selecione ![Mais](/help/assets/icons/More.svg) ao passar o mouse sobre um nome de conversão na tabela.

1. Selecione ![Exibir](/help/assets/icons/ViewDetail.svg) **Exibir detalhes**. Uma caixa de diálogo mostra detalhes da conversão. Consulte [Adicionar uma conversão](#add-a-conversion) para obter mais informações. Selecione **[!UICONTROL Cancel]** para fechar a caixa de diálogo.

## Exibir relatório

Para exibir um relatório de uma conversão:

1. Selecione ![Mais](/help/assets/icons/More.svg) ao passar o mouse sobre um nome de conversão na tabela.

1. Selecione ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Exibir relatório**. Uma caixa de diálogo mostra um relatório da conversão.

   ![Relatório de exibição de conversão](../assets/conversion-view-report.png)

   * Para alterar a granularidade sobre a qual relatar, selecione um valor no menu suspenso **[!UICONTROL Weekly]**.
   * Para alterar o período para o relatório, insira uma data de início e término ou use o ![Calendário](/help/assets/icons/Calendar.svg) para definir um período no pop-up do calendário.

1. Selecione **[!UICONTROL Close]** para fechar a caixa de diálogo.

## Excluir uma conversão

Para excluir uma conversão:

1. Selecione ![Excluir](/help/assets/icons/Delete.svg) **Excluir** ao passar o mouse sobre um nome de conversão na tabela.
1. Na caixa de diálogo de confirmação **[!UICONTROL Delete conversion]**, selecione **[!UICONTROL Delete]** para excluir permanentemente a conversão.
