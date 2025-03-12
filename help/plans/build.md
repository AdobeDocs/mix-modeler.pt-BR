---
title: Criar planos
description: Saiba como criar planos no Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: d05eccef370598ce64363ca6ae20886b0e5dccd0
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---


# Criar planos

No Mix Modeler, você cria um plano usando a tela do plano. Na tela do plano, é possível configurar os detalhes e os orçamentos do plano e o modelo subjacente a ser usado para o plano. Depois de especificar os detalhes, o orçamento e o modelo, você pode seguir com um plano recomendado por IA ou editar o gasto por canal.

Para criar um plano, na interface ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** do Mix Modeler, selecione **[!UICONTROL Create plan]**.

1. Na tela **[!UICONTROL Plan creation]**:

   1. Na seção **[!UICONTROL Setup]**:

      1. Digite um **[!UICONTROL Plan name]**, por exemplo `Demo plan`. Digite um **[!UICONTROL Description]**, por exemplo `Demo plan for Luma company`.
      1. Selecione um **[!UICONTROL Model]** de **[!UICONTROL _Selecione uma opção._.]**
      1. Você pode selecionar ![LinkOut](/help/assets/icons/LinkOut.svg) **[!UICONTROL Create model]** para criar um modelo diretamente de dentro da criação do plano. Uma nova guia será aberta no navegador e mostrará a interface [Modelos](../models/overview.md).

         ![Configuração do Plano](/help/assets/plan-setup.png)

   1. Na seção **[!UICONTROL Budget]**:

      1. Especifique um intervalo de datas, digitando datas ou selecionando um intervalo de datas usando ![Calendário](/help/assets/icons/Calendar.svg).
      1. Informe um orçamento.

      Para adicionar intervalos de datas adicionais, cada um com seu orçamento, selecione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Para excluir um intervalo de datas e o orçamento associado, selecione ![Fechar](/help/assets/icons/Close.svg).

      Para definir um orçamento máximo especificado:

      1. Ligar **[!UICONTROL Maximize budget]**.
      1. Especificar a quantidade do orçamento máximo. O valor deve ser igual ou superior ao valor total de orçamentos especificado para os intervalos de datas.

         ![Planejar orçamento](/help/assets/plan-budget.png)

   1. Selecione **[!UICONTROL Next]**.

1. No diálogo **[!UICONTROL Done with all required fields]**:

   ![Plano concluído](/help/assets/plan-done-required-fields.png)

   * Selecionar <img src="/help/assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** se você deseja gerar um plano recomendado de IA com ROI previsto.

     Selecione **[!UICONTROL OK]**. Seu plano foi criado.


   * Selecione ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** se desejar editar o orçamento do canal antes de criar um plano com ROI previsto.

     Selecione **[!UICONTROL OK]** para definir os gastos do canal em **[!UICONTROL Spend selection]** na próxima etapa.



1. Na seção **[!UICONTROL Spend selection]**, para cada intervalo de datas do orçamento, use a ![Divisa](/help/assets/icons/ChevronRight.svg) para abrir a exibição de distribuição de canal para esse intervalo de dados.

   1. Para definir orçamentos para cada canal, insira um valor para **[!UICONTROL Min]** e **[!UICONTROL Max]** ou use os controles deslizantes.

   1. Para alternar entre entrada de moeda ou porcentagem, selecione **[!UICONTROL $]** ou **[!UICONTROL %]** para **[!UICONTROL View spend by]**.

      ![Gastar seleção](/help/assets/plan-spend-selection.png)

   1. Quando terminar, selecione **[!UICONTROL Create]**.

   1. Na caixa de diálogo **[!UICONTROL Create plan]**, selecione **[!UICONTROL Create plan]** para criar seu plano. Selecione **[!UICONTROL Cancel]** para cancelar a criação do seu plano. Uma caixa de diálogo **[!UICONTROL No work is saved]** é exibida para confirmar.
