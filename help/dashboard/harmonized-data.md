---
title: Painel de visão geral de dados harmonizado
description: Saiba como usar o painel de visão geral de dados harmonizados no Mix Modeler.
feature: Dashboard, Harmonized Data
exl-id: fbb01613-d648-4db1-a782-a7720b7a03ad
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Visão geral dos dados harmonizados

A guia Dados harmonizados na Visão geral do Mix Modeler fornece insights sobre os dados harmonizados configurados para serem usados como parte dos dados assimilados e da configuração de dados harmonizados.

A visão geral mostra quatro widgets de cartão de status de KPI (linha superior) e seis outros widgets configuráveis.

Para alterar o período de datas dos dados a serem exibidos nos widgets, insira uma data de início e uma data de término manualmente ou selecione um período usando ![Calendário](../assets/icons/Calendar.svg).

## Filtros de dados

Você pode filtrar os dados exibidos para todos os widgets usando o ![Filtro](../assets/icons/Filter.svg) **[!UICONTROL Category Filters]** painel.

Selecione um ou mais filtros para cada categoria (**[!UICONTROL Brands]**, **[!UICONTROL Campaigns]**, **[!UICONTROL Cannels Type]**, **[!UICONTROL Conversion types]**, **[!UICONTROL Datasets]**, **[!UICONTROL Media types]**, **[!UICONTROL Source types]**, e **[!UICONTROL Traffic Source]**).

Os filtros selecionados são exibidos na parte superior dos widgets em **[!UICONTROL FILTERING BY:]**.

1. Para remover um filtro individual, selecione ![Fechar](../assets/icons/Close.svg) no filtro, listado em **[!UICONTROL FILTERING BY:]**.

1. É possível limpar rapidamente todos os filtros usando **[!UICONTROL Clear All]**.

![Visão geral dos dados harmonizados](../assets/harmonized-data-overview.png)


## Configurar um widget

Você pode configurar cada widget.

* No widget de cartão de status KPI:

   1. Selecionar ![Editar](../assets/icons/Edit.svg) e ![Editar](../assets/icons/Edit.svg) **[!UICONTROL Edit data]** no menu de contexto.

   1. No **[!UICONTROL KPI status card]** diálogo:

      1. Selecione um **[!UICONTROL KPI]** da lista.

      1. Selecionar **[!UICONTROL Apply]** para aplicar a alteração ao cartão. Selecionar **[!UICONTROL Cancel]** para cancelar a alteração.

* Nos outros widgets configuráveis:

   1. Selecionar ![Editar](../assets/icons/Edit.svg) e ![Editar](../assets/icons/Edit.svg) **[!UICONTROL Edit data]** no menu de contexto.

   1. No **[!UICONTROL Edit Data]** diálogo:

      1. Selecione uma métrica em **[!UICONTROL Select a metric]**, por exemplo **[!UICONTROL Impressions]**.
      1. Selecionar uma categoria de **[!UICONTROL Select category]**, por exemplo **[!UICONTROL Media types]**.
      1. (opcional) selecione uma segunda categoria em **[!UICONTROL Select second category (optional)]**, por exemplo **[!UICONTROL Traffic sources]**.
      1. Selecionar ![Relógio](../assets/icons/Clock.svg) **[!UICONTROL Time]** ou ![Calculadora](../assets/icons/Calculator.svg) **[!UICONTROL Total]** como o tipo de análise em **[!UICONTROL Select analysis type]**.

         Se você selecionar ![Relógio](../assets/icons/Clock.svg) **[!UICONTROL Time]**, você pode especificar a frequência de tempo. Selecionar **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Quarterly]** de **[!UICONTROL Select time frequency]**.

         Você verá uma visualização atualizada da seleção atual na [!UICONTROL Preview Area] e o widget abaixo dele [!UICONTROL Current].

         ![Editar widget de dados harmonizado](../assets/edit-harmonized-data-widget.png)

         Se não for possível renderizar a visualização porque os dados não estão disponíveis, você verá ![Erro de dados](../assets/icons/DataUnavailable.svg) [!UICONTROL Insights Not Available] - [!UICONTROL Harmonized fields are not available].

      1. Selecionar **[!UICONTROL Apply]** para aplicar as alterações ao widget. Selecionar **[!UICONTROL Cancel]** para cancelar quaisquer alterações feitas no widget atual.
