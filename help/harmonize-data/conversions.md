---
title: Conversões
description: Saiba como criar conversões para usar como parte da harmonização de seus dados no Mix Modeler.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---

# Conversões

Eventos de conversão são objetivos de negócios que identificam o impacto das atividades de marketing. Exemplos: pedidos de comércio eletrônico, compras na loja, visitas a sites e assim por diante.

Você define conversões de marketing para análise de atribuição.

## Gerenciar conversões

Para ver uma tabela das conversões disponíveis, na interface do Mix Modeler:

1. Selecionar ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** do painel esquerdo.

1. Selecionar **[!UICONTROL Conversions]** na barra superior. Você verá uma tabela das conversões.

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

Para adicionar uma conversão, no campo ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** interface no Mix Modeler:

1. Selecionar ![Adicionar](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. No **[!UICONTROL Create conversion]** diálogo:

   1. Digite um nome para **[!UICONTROL Conversion]**, por exemplo `Store Conversions`.

   1. Defina o **[!UICONTROL Conversion category]**.

      1. Selecione um valor de **[!UICONTROL *Selecionar harmonizar...*]**, por exemplo `Conversion types`.

      1. Selecione um valor para o operador ![Divisa](/help/assets//icons/ChevronDown.svg), por exemplo **[!UICONTROL is]**.

      1. Selecione um valor de **[!UICONTROL *Selecionar valor *]**ou insira um valor, por exemplo **[!UICONTROL Store]**.

   1. Selecione um campo harmonizado em **[!UICONTROL Conversion metric for analysis]**, por exemplo **[!UICONTROL Orders]**.

   1. Selecione um campo harmonizado em **[!UICONTROL Revenue field]**, por exemplo **[!UICONTROL Gross Demand]**.

   1. Para criar a conversão, selecione **[!UICONTROL Create]**. Para cancelar a criação de uma conversão, selecione **[!UICONTROL Cancel]**.

      ![Texto alternativo](/help/assets//create-conversion.png)

1. Quando criada, a conversão é adicionada à tabela de conversões.


## Exibir uma conversão

Para exibir uma conversão:

1. Selecionar ![Mais](/help/assets//icons/More.svg) ao passar o mouse sobre um nome de conversão na tabela.

1. Selecionar ![Exibir](/help/assets//icons/ViewDetail.svg) **Exibir**. Uma caixa de diálogo mostra detalhes da conversão. Consulte [Adicionar uma conversão](#add-a-conversion) para obter mais informações. Selecionar **[!UICONTROL Cancel]** para fechar o diálogo.


## Excluir uma conversão

Para excluir uma conversão:

1. Selecionar ![Excluir](/help/assets//icons/Delete.svg) **Excluir** ao passar o mouse sobre um nome de conversão na tabela.
1. No **[!UICONTROL Delete conversion]** caixa de diálogo de confirmação caixa de diálogo selecionar **[!UICONTROL Delete]** para excluir permanentemente a conversão.
