---
title: Conversões
description: Saiba como criar conversões para usar como parte da harmonização de dados no Adobe Mix Modeler.
feature: Harmonized Data, Conversions
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 3%

---


# Conversões

Eventos de conversão são objetivos de negócios que identificam o impacto das atividades de marketing. Exemplos: pedidos de comércio eletrônico, compras na loja, visitas a sites e assim por diante.

Você define conversões de marketing para análise de atribuição.

## Gerenciar conversões

Para ver uma tabela das conversões disponíveis, na interface do Adobe Mix Modeler:

1. Selecionar ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** do painel esquerdo.

1. Selecionar **[!UICONTROL Conversions]** na barra superior. Você verá uma tabela das conversões.

As colunas da tabela especificam detalhes sobre a conversão:

| Nome da coluna | Detalhes |
| --- | ---|
| Nome | O nome da conversão. |
| Receita | A métrica de dados harmonizada a ser usada para calcular a receita de uma conversão. |
| Métrica de conversão | A métrica de dados harmonizada a ser usada como a métrica de conversão para análise. |
| Criado | Data e hora de criação da conversão. |
| Última modificação | Data e hora da última modificação da conversão. |

{style="table-layout:auto"}

## Adicionar uma conversão

Para adicionar uma conversão, no campo ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** no Adobe Mix Modeler:

1. Selecionar ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. No **[!UICONTROL Create Conversion]** diálogo:

   1. Digite um nome para **[!UICONTROL Conversion]**, por exemplo `Store Conversions`.

   1. Defina o **[!UICONTROL Conversion category]**.

      1. Selecione um valor de **[!UICONTROL *Selecionar harmonizar...*]**, por exemplo `Conversion Type`.

      1. Selecione um valor para o operador ![Divisa](../assets/icons/ChevronDown.svg), por exemplo **[!UICONTROL is]**.

      1. Selecione um valor de **[!UICONTROL *Selecionar valor *]**ou insira um valor, por exemplo **[!UICONTROL Store]**.

   1. Selecione um campo harmonizado em **[!UICONTROL Conversion metric for analysis]**, por exemplo **[!UICONTROL Orders]**.

   1. Selecione um campo harmonizado em **[!UICONTROL Revenue field]**, por exemplo **[!UICONTROL Gross Demand]**.

   1. Para criar a conversão, selecione **[!UICONTROL Create]**. Para cancelar a criação de uma conversão, selecione **[!UICONTROL Cancel]**.

      ![Texto alternativo](../assets/create-conversion.png)

1. Quando criada, a conversão é adicionada à tabela de conversões.
