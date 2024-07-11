---
title: Informações do modelo
description: Saiba como obter detalhes sobre seu modelo, como visão geral histórica, insights do modelo e qualidade do modelo no Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# Informações do modelo

Para exibir insights do modelo, na variável ![Modelos](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** interface no Mix Modeler:

1. No **[!UICONTROL Models]** , selecione o nome de um modelo que tenha uma **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]**.

1. No menu de contexto, selecione **[!UICONTROL Model Insights]**.

![Barra de guias de insights do modelo](/help/assets//model-insights-tabbar.png)

Você verá quando o modelo especificado foi atualizado pela última vez e os widgets são exibidos usando quatro guias: [Insights do modelo](#model-insights), [Atribuição](#attribution), [Diagnóstico](#diagnostics), e [Visão geral histórica](#historical-overview).

Você pode alterar o período de data no qual os widgets em cada uma das guias se baseiam. Insira um período de data ou selecione ![Calendário](/help/assets//icons/Calendar.svg) para selecionar um período de data.

## [!UICONTROL Model insights]

A guia Informações do modelo mostra widgets para:

* Contribuição por data e mídia base. O gráfico empilhado é ordenado: Base na parte inferior, Canais de não gasto no meio e Canais de gasto na parte superior.

* Contribuição por canal.

* Resumo de desempenho de marketing.

* Curvas de resposta marginal.
  <br/>Selecione um canal na **[!UICONTROL Channel]** lista suspensa para atualizar o widget de um canal específico.

![Modelo - Informações do modelo](/help/assets//model-insights-insights.png)

Você pode passar o mouse sobre elementos de gráficos individuais em cada widget para exibir um popover com mais detalhes.

Para baixar um arquivo CSV contendo os dados do widget, selecione ![Baixar](/help/assets//icons/Download.svg).

Para baixar dados de insights do modelo completo no formato do Microsoft® Excel, selecione ![Baixar](/help/assets//icons/Download.svg) **[!UICONTROL Download data]**.

## [!UICONTROL Attribution]

Usar o [!UICONTROL Attribution] você pode entender a eficácia dos pontos de contato e das campanhas de marketing que têm dados de nível de evento. Os seguintes modelos de atribuição são compatíveis:

* Com base no modelo selecionado no Mix Modeler:
   * Algorítmico - Influenciado
   * Algorítmico - Incremental
* Baseado em regra:
   * Unidades de decaimento
   * Primeiro contato
   * Último contato
   * Linear
   * Ushape

Consulte [Atribuição multitoque](../get-started/about.md#multi-touch-attribution) para obter uma introdução sobre o recurso de atribuição multitoque no Mix Modeler.

Selecione um ou mais modelos de atribuição na **[!UICONTROL Attribution Model]** lista suspensa. Os modelos de atribuição selecionados se aplicam a todos os widgets na guia Atribuição.

![Atribuição](/help/assets//model-insights-attribution.png)

As pontuações do evento granular de atribuição multitoque do Mix Modeler são alinhadas às pontuações gerais do Mix Modeler e aos ROIs. Essas pontuações também são disponibilizadas como conjuntos de dados no Experience Platform.

A guia Atribuição consiste nos seguintes widgets:

### [!UICONTROL Overview]

A variável [!UICONTROL Overview] O widget mostra, para os modelos de atribuição selecionados, os totais e as porcentagens de conversões. Selecionar mais modelos adiciona círculos adicionais à visualização, cada um com sua própria cor correspondente à legenda.

Para ver um pop-up com detalhes de um modelo de atribuição, passe o mouse sobre qualquer um dos círculos na visualização.

### [!UICONTROL Trends]

A variável [!UICONTROL Daily trends], [!UICONTROL Weekly trends]ou [!UICONTROL Monthly trends] O widget mostra, para os modelos de atribuição selecionados, as tendências de conversão diárias, semanais ou mensais.

Para escolher o período, selecione **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** ou **[!UICONTROL Monthly trends]** de ![Mais](/help/assets//icons/More.svg).

Para ver os detalhes, passe o mouse sobre a linha de dados de um modelo de atribuição específico para exibir um popover que mostra o número total de conversões desses dados.

### [!UICONTROL Breakdown]

A variável [!UICONTROL Breakdown] o widget é um detalhamento por canal ou ponto de contato das conversões para cada um dos modelos de atribuição selecionados. Este widget pode ser útil para tomar decisões sobre a eficácia de cada canal ou ponto de contato.

Para escolher o tipo de detalhamento, selecione **[!UICONTROL Breakdown by channel]** ou **[!UICONTROL Breakdown by touchpoint]** de ![Mais](/help/assets//icons/More.svg).

Para ver detalhes, passe o mouse sobre qualquer um dos elementos do gráfico.

### [!UICONTROL Top campaigns]

O widget Campanhas principais mostra uma tabela das campanhas principais com colunas para Nome da campanha, Canal, Tipo de mídia e Conversões incrementais. Este widget pode ajudar a informar sua equipe sobre a eficácia de uma campanha específica para um determinado canal e fornecer insights sobre em quais campanhas você deve investir ainda mais.

Para classificar a tabela em ordem crescente ↑ ou decrescente ↓ para Canal, Tipo de mídia ou Conversões incrementais, selecione o cabeçalho da coluna e alterne a classificação.

Para expandir a tabela em uma caixa de diálogo separada, selecione **[!UICONTROL Expand]** de ![Mais](/help/assets//icons/More.svg).

A caixa de diálogo Campanhas principais expandida mostra a mesma tabela com colunas de adição para

* Conversões incrementais
* Conversões influenciadas
* Conversões de primeiro contato
* Conversões de último contato

  Você pode selecionar cada um dos cabeçalhos de coluna adicionais para classificar a tabela em ordem crescente ou decrescente.

Para fechar a caixa de diálogo Campanhas principais expandida, selecione **[!UICONTROL Close]**.


### [!UICONTROL Breakdown by touchpoint position]

A variável [!UICONTROL Breakdown by touchpoint position] a visualização é um detalhamento das conversões atribuídas por posição do ponto de contato e do ponto de contato em todos os caminhos de conversão. Este gráfico ajuda a comparar se um ponto de contato contribui melhor em uma posição do que as posições restantes e outros pontos de contato em qualquer posição.

>[!NOTE]
>
>A soma da contribuição percentual para um modelo de atribuição em todos os pontos de contato e posições deve ser igual a 100.


As posições [!UICONTROL Starter], [!UICONTROL Player] e [!UICONTROL Closer] são definidos da seguinte forma:

| Position | Descrição |
|---|---|
| [!UICONTROL Starter] | Essa posição indica se o ponto de contato é o primeiro contato em um caminho de conversão. |
| [!UICONTROL Player] | Essa posição indica se o ponto de contato não é o primeiro ou o último contato que leva à conversão. |
| [!UICONTROL Closer] | Essa posição indica se o ponto de contato é o último contato antes da conversão. |


### [!UICONTROL Top conversion paths]

A variável [!UICONTROL Top conversion paths] a visualização mostra os 5 principais caminhos de conversão com base nos modelos de atribuição selecionados.

Para cada caminho de conversão, você verá:

* o número de canais que têm impacto,
* o total de caminhos atribuídos,
* a porcentagem de caminhos atribuídos para esse caminho de conversão em relação ao total de caminhos atribuídos,
* para cada canal, a porcentagem de contribuição do modelo de atribuição e
* a soma dessas porcentagens de contribuição do modelo de atribuição de canal.


## [!UICONTROL Diagnostics]

A guia Diagnóstico mostra widgets para:

* [!UICONTROL Model Assessment] visualização, que pode ser analisada em conversões reais versus previstas ou residuais.

  Para detalhar a visualização, selecione **[!UICONTROL Actual vs. Predicted]** ou **[!UICONTROL Residuals]** do **[!UICONTROL Breakdown]** lista.

* [!UICONTROL Model fitting metrics] , mostrando as seguintes colunas para cada métrica de conversão:

   * Conversão Efetiva

   * Conversão modelada

   * Conversão Residual (diferença entre a conversão real e a conversão modelada)

   * Valores de pontuação de qualidade do modelo:

      * R2 (R-quadrado), que informa como os dados se encaixam no modelo de regressão (a adequação do ajuste).

      * MAPE (Mean Absolute Percentage Error), que é um dos KPIs mais usados para medir a precisão da previsão e expressa o erro de previsão como uma porcentagem do valor real.

      * RMSE (Root Mean Square Error): que mostra o erro médio, ponderado de acordo com o quadrado do erro.

  Para baixar um arquivo CSV contendo os dados da tabela, selecione ![Baixar](/help/assets//icons/Download.svg).

* [!UICONTROL Touchpoint effectiveness] tabela, representando o resultado do modelo Attribution AI. Os dados desta tabela são gerados apenas para períodos específicos. Selecionar **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Informações](/help/assets//icons/InfoOutline.svg) para obter mais detalhes.

  A visualização mostra, em ordem decrescente de [!UICONTROL Efficiency measure] ![Ordem decrescente](/help/assets//icons/SortOrderDown.svg), para cada ponto de contato:

   * [!UICONTROL Paths touched]: visualiza a porcentagem de caminhos que atingem a conversão e a porcentagem de caminhos que não atingem a conversão. Para um ponto de contato, você verá mais conversões atribuídas quando a taxa de conversão de atribuição estiver alta. Essa proporção compara a porcentagem de caminhos que levam à conversão com a porcentagem de caminhos que levam *não* levar à conversão.
   * [!UICONTROL Efficiency measure]: gerada pelo modelo de atribuição algorítmica, a medida de eficiência indica a importância relativa de um ponto de contato em direção à conversão, independentemente do volume do ponto de contato. A eficiência é medida em uma escala de 1 a 5. Observe que um maior volume de pontos de contato não garante uma medida de eficiência mais alta.
   * [!UICONTROL Total volume]: o número agregado de vezes que um usuário toca um ponto de contato. O número inclui os pontos de contato que aparecem em um caminho que alcança a conversão, bem como caminhos *não* resultando em conversão.

![Diagnóstico](/help/assets//model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

A guia Visão geral histórica mostra widgets para:

* Conversão e gasto por trimestre fiscal e produto.

* Gastos por canal.

* Gastos com Touchpoint.

  Você pode selecionar um canal alternativo com base em gastos para exibir para este widget. Selecionar um canal em **[!UICONTROL Channels]**.

* Volume do ponto de contato.

  Você pode selecionar um canal alternativo baseado em volume para exibir para este widget. Selecionar um canal em **[!UICONTROL Channels]**.

![Modelo - Visão geral histórica](/help/assets//model-insights-historical-overview.png)
