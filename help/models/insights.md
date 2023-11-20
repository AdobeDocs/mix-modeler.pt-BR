---
title: Informações do modelo
description: Saiba como obter detalhes sobre seu modelo, como visão geral histórica, insights do modelo e qualidade do modelo no Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 73534d1aecb6d1513f6f3b5f1801b497ad73278f
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Informações do modelo

Para exibir insights do modelo, na variável ![Modelos](../assets/icons/FileData.svg) **[!UICONTROL Models]** interface no Mix Modeler:

1. Selecione o nome de um modelo com um **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** do **[!UICONTROL Models]** tabela.

1. No menu de contexto, selecione **[!UICONTROL Model Insights]**.

Você pode ver quando o modelo especificado foi atualizado pela última vez e os widgets são exibidos usando três guias: Visão geral histórica, Insights do modelo e Qualidade do modelo.

Você pode alterar o período de data no qual os widgets em cada uma das guias se baseiam. Insira um período de data ou selecione ![Calendário](../assets/icons/Calendar.svg) para selecionar um período de data.


## Visão geral histórica

A guia Visão geral histórica mostra widgets para:

* Conversão e gasto por trimestre fiscal e produto.

* Gastos por canal.

* Gastos com Touchpoint.

  Você pode selecionar um canal alternativo com base em gastos para exibir para este widget. Selecionar um canal em **[!UICONTROL Channels]**.

* Volume do ponto de contato.

  Você pode selecionar um canal alternativo baseado em volume para exibir para este widget. Selecionar um canal em **[!UICONTROL Channels]**.

![Modelo - Visão geral histórica](../assets/model-historical-overview.png)

## Insights do modelo

A guia Informações do modelo mostra widgets para:

* Contribuição por data e mídia base. O gráfico empilhado é ordenado: Base na parte inferior, Canais não gastos no meio e Canais gastos na parte superior.

* Contribuição por canal.

* Resumo de desempenho de marketing.

![Modelo - Informações do modelo](../assets/model-model-insights.png)

Você pode passar o mouse sobre elementos de gráficos individuais em cada widget para exibir um popover com mais detalhes.

Para baixar um arquivo CSV contendo os dados do widget, selecione ![Baixar](../assets/icons/Download.svg).




## Qualidade do modelo

A guia Qualidade do modelo mostra widgets para medir:

* R2 (R-quadrado), que informa como os dados se encaixam no modelo de regressão (a adequação do ajuste).

* MAPE (Mean Absolute Percentage Error), que é um dos KPIs mais usados para medir a precisão da previsão e expressa o erro de previsão como uma porcentagem do valor real.

* RMSE (Erro de Raiz Quadrada Média): que mostra a média de &quot;erro&quot;, ponderada de acordo com o quadrado do erro.

![Qualidade do modelo](../assets/model-quality.png)

Para baixar um arquivo CSV contendo os dados do widget, selecione ![Mais](../assets/icons/More.svg) no widget e, no menu de contexto, selecione ![Baixar](../assets/icons/Download.svg) **[!UICONTROL Download as CSV]**.
