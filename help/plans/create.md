---
title: Criar um plano
description: Saiba como criar um plano no Mix Modeler.
feature: Plans
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Criar um plano

No Mix Modeler, você cria um plano usando a tela de plano. Na tela do plano, é possível configurar os detalhes e os orçamentos do plano e o modelo subjacente a ser usado para o plano. Depois de especificar os detalhes, o orçamento e o modelo, você pode seguir com um plano recomendado por IA ou editar o gasto por canal.

Para criar um plano, no campo ![PLan](../assets/icons/FileChart.svg) **[!UICONTROL Plans]** no Mix Modeler, selecione **[!UICONTROL Open plan canvas]**.

1. Na tela Plan creation:

   1. No **[!UICONTROL Setup]** seção

      1. Insira um **[!UICONTROL Plan name]**, por exemplo `Demo plan`. Insira um **[!UICONTROL Description]**, por exemplo `Demo plan for Luma company`.
      1. Selecione um **[!UICONTROL Model]** de **[!UICONTROL _Selecione uma opção._.]**.
      1. É possível selecionar ![LinkOut](../assets/icons/LinkOut.svg) **[!UICONTROL Create model]** para criar um modelo diretamente da criação do plano.

         ![Configuração do plano](../assets/plan-setup.png)

   1. No **[!UICONTROL Budget]** seção:

      1. Especifique um intervalo de datas, digitando datas ou selecionando um intervalo de datas usando ![Calendário](../assets/icons/Calendar.svg).
      1. Informe um orçamento.

      Para adicionar intervalos de datas adicionais, cada um com seu orçamento, selecione ![CalendárioAdicionar](../assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Para deletar um intervalo de datas e o orçamento associado, selecione ![Fechar](../assets/icons/Close.svg).

      Para definir um orçamento máximo especificado:

      1. Alternar **[!UICONTROL Maximize budget]** em.
      1. Especificar a quantidade do orçamento máximo. O valor deve ser igual ou superior ao valor total de orçamentos especificado para os intervalos de datas.

         ![Planejar orçamento](../assets/plan-budget.png)

   1. Selecione **[!UICONTROL Next]**.

1. No **[!UICONTROL Done with all required fields]** diálogo:

   ![Plano Concluído](../assets/plan-done-required-fields.png)

   * Selecionar <img src="../assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** se você quiser gerar um plano recomendado de IA com ROI previsto.

     Selecione **[!UICONTROL OK]**. Seu plano foi criado.


   * Selecionar ![EditarTabela](../assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** se quiser editar o orçamento do canal antes de criar um plano com ROI previsto.

     Selecionar **[!UICONTROL OK]**, para que você possa definir os gastos do canal no **[!UICONTROL Spend selection]** na próxima etapa.



1. No **[!UICONTROL Spend selection]** para cada intervalo de datas do orçamento, use o ![Divisa](../assets/icons/ChevronRight.svg) início abra a exibição distribuição de canal para esse intervalo de dados.

   1. Para definir orçamentos para cada canal, insira um valor para **[!UICONTROL Min]** e **[!UICONTROL Max]** ou use os controles deslizantes.

   1. Para alternar entre entrada de moeda ou porcentagem, selecione **[!UICONTROL $]** ou **[!UICONTROL %]** para **[!UICONTROL View spend by]**.

      ![Seleção de gastos](../assets/plan-spend-selection.png)

   1. Quando terminar, selecione **[!UICONTROL Create]**.

   1. No **[!UICONTROL Create plan]** , selecione **[!UICONTROL Create plan]** para criar seu plano. Selecionar **[!UICONTROL Cancel]** para cancelar a criação do seu plano.



