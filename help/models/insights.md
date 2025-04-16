---
title: Insights do modelo
description: Saiba como obter detalhes sobre seu modelo, como visão geral histórica, insights do modelo e qualidade do modelo no Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: bc48dc564042890856072a07c3a9715ba9dcdb87
workflow-type: tm+mt
source-wordcount: '1914'
ht-degree: 0%

---

# Insights do modelo

Cada visualização em insights de modelo foi projetada para ajudar você a:

* Visualize e quantifique o impacto das atividades de marketing de sua organização.
* Identifique quais canais têm alto desempenho.
* Identifique quais canais podem precisar de otimização.

Esses insights ajudam a oferecer suporte à priorização e alocação de recursos.

Para exibir insights do modelo, na interface ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** do Mix Modeler:

1. Na tabela **[!UICONTROL Models]**, selecione o nome de um modelo que tenha um **[!UICONTROL Last run status]** de <span style="color:green"> ●</span> **[!UICONTROL Success]**.

1. No menu de contexto, selecione **[!UICONTROL Model Insights]**.

![Barra de guias de insights do modelo](/help/assets/model-insights-tabbar.png)

Você vê quando o modelo especificado foi atualizado pela última vez e as visualizações são exibidas usando quatro guias: [Insights do modelo](#model-insights), [Atribuição](#attribution), [Fatores](#factors), [Diagnósticos](#diagnostics) e [Visão geral histórica](#historical-overview).

É possível alterar o período de data no qual as visualizações em cada uma das guias se baseiam. Insira um período de data ou selecione ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um período de data.

## [!UICONTROL Model insights]

A guia Informações do modelo mostra visualizações para [Contribuição por data e mídia base](#contribution-by-date-and-base-media), [Contribuição por canal](#contribution-by-channel), [Resumo do desempenho de marketing](#marketing-performance-summary) e [Curvas de resposta marginal](#marginal-response-curves). A guia também fornece uma tabela [Detalhamento do ponto de contato](#touchppint-breakdown).

![Modelo - Insights do modelo](/help/assets/model-insights-insights.png)

* Você pode passar o mouse sobre elementos de gráficos individuais em cada visualização para exibir um popover com mais detalhes.

* Para baixar um arquivo CSV contendo os dados da visualização, selecione ![Baixar](/help/assets/icons/Download.svg).

* Para baixar dados completos de insights do modelo no formato do Microsoft® Excel, selecione ![Baixar](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Contribuição por data e mídia base.

Essa visualização de gráfico empilhado é ordenada da seguinte maneira:

* Base na parte inferior.
* Canais não gastos no meio.
* Passe canais por cima.

Essa visualização representa a proporção de contribuição obtida pela base, por canais de gastos e por canais não gastos em um intervalo de datas. Esta visualização é útil para mostrar a incrementalidade. A base representa o que teria acontecido sem qualquer marketing, e o atributo de canais não gastos mais canais gastos (sobre a base) do impacto do seu marketing. Em resumo, não gastar mais gastar equivale ao impacto incremental de seus esforços de marketing e a visualização fornece um insight fácil no valor gerado pelo marketing.

### Contribuição por canal

Uma visualização de rosca que mostra uma distribuição da contribuição por vários canais. Esta visualização mostra a incrementalidade através da lente dos três principais canais de desempenho (excluindo as categorias base e *Todos os outros*). A visualização ajuda a oferecer suporte à priorização e à alocação de orçamento.

### Resumo de desempenho de marketing.

Uma visualização de gráfico de barras horizontal que mostra o desempenho do ROI ou CPA de cada canal. Esta visualização destaca o ROI/CPA de seus investimentos em marketing. Os canais são classificados em ordem decrescente com base no ROI/CPA. A visualização ajuda a identificar quais canais são mais eficazes e quais podem precisar de otimização.

### Curvas de resposta marginal.

O gráfico de linhas visualiza e compara os retornos marginais gerados pelo investimento em seus canais de marketing.  E identifica o ponto de equilíbrio no qual o retorno incremental é menor do que o gasto incremental. Como resultado, essa visualização ajuda você a entender quando seu investimento em marketing começa a ter menos impacto.

A curva, o ponto de equilíbrio e os valores correspondentes são calculados com base no intervalo de dados selecionado e no canal selecionado.

Para alterar o canal:

* Selecione um canal no menu suspenso **[!UICONTROL Channel]** para atualizar a visualização de um canal específico.


### Detalhamento do ponto de contato

A tabela de detalhamento de ponto de contato mostra os detalhamentos de ponto de contato semanais para todos os canais ou para os canais selecionados em uma base semanal, exibindo as métricas principais associadas a cada um. A tabela permite uma fácil comparação, identificação de tendências e rastreamento de desempenho em um nível de canal mais granular. Esta tabela complementa explicitamente a visualização [Contribuição por data e mídia base](#contribution-by-date-and-base-media) e a visualização [Contribuição por canal](#contribution-by-channel).

![Detalhamento do ponto de contato](../assets/touchpoint-breakdown.png)

As seguintes colunas estão disponíveis:

| Coluna | Descrição |
|---|---|
| **[!UICONTROL Date range]** | A semana para relatar. |
| **[!UICONTROL Touchpoint]** | O canal de ponto de contato específico. |
| **[!UICONTROL ROI]** | A porcentagem de (**[!UICONTROL Revenue]** - **[!UICONTROL Spend]**) / **[!UICONTROL Spend]**. |
| **[!UICONTROL Revenue]** | A receita do intervalo de datas. |
| **[!UICONTROL CPA]** | **[!UICONTROL Spend]** / **[!UICONTROL Conversions]**. |
| **[!UICONTROL Conversions]** | As conversões do intervalo de datas. |
| **[!UICONTROL Spend]** | O gasto para o intervalo de dados. |

Para selecionar um canal específico ou todos os canais, selecione no menu suspenso **[!UICONTROL View]**.

Para baixar o conteúdo da tabela de detalhamento Touchpoint, selecione ![Baixar](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**.

## **[!UICONTROL Factors]** [!BADGE beta]

A guia Fatores [!BADGE beta] mostra insights relacionados ao fator externo.

![Fatores](/help/assets/factors.png)

Essa visualização ajuda você a entender o efeito incremental que vários fatores internos e externos têm na linha de base das conversões. Por exemplo, condições econômicas ou atividades promocionais.

Use o menu suspenso **[!UICONTROL Factors]** para selecionar quais fatores você deseja exibir.

<!-- need to update the image when we do have a proper example -->

Para baixar um arquivo CSV contendo os dados da tabela, selecione ![Baixar](/help/assets/icons/Download.svg).

Se nenhum dado estiver disponível, você verá a mensagem ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Attribution]

>[!NOTE]
>
>A guia Atribuição só está disponível para modelos habilitados para MTA.


Usando a guia [!UICONTROL Attribution], você pode entender a eficácia dos pontos de contato e campanhas de marketing que têm dados de nível de evento.  Consulte [Modelo de compilação](build.md).

Os seguintes modelos de atribuição são compatíveis:

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

Selecione um ou mais modelos de atribuição no menu suspenso **[!UICONTROL Attribution Model]**. Os modelos de atribuição selecionados se aplicam a todas as visualizações na guia Atribuição.

![Atribuição](/help/assets/model-insights-attribution.png)

As pontuações granulares do evento de atribuição multitoque do Mix Modeler são alinhadas às pontuações gerais e aos ROIs do Mix Modeler. Essas pontuações também são disponibilizadas como conjuntos de dados no Experience Platform.

A guia Atribuição consiste nas seguintes visualizações:

### [!UICONTROL Overview]

A visualização [!UICONTROL Overview] mostra, para os modelos de atribuição selecionados, os totais e as porcentagens de conversões. Selecionar mais modelos adiciona círculos adicionais à visualização, cada um com sua própria cor correspondente à legenda.

Para ver um pop-up com detalhes de um modelo de atribuição, passe o mouse sobre qualquer um dos círculos na visualização.

### [!UICONTROL Trends]

A visualização [!UICONTROL Daily trends], [!UICONTROL Weekly trends] ou [!UICONTROL Monthly trends] mostra, para os modelos de atribuição selecionados, as tendências de conversão diárias, semanais ou mensais.

Para escolher o período, selecione **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** ou **[!UICONTROL Monthly trends]** de ![Mais](/help/assets/icons/More.svg).

Para ver os detalhes, passe o mouse sobre a linha de dados de um modelo de atribuição específico para exibir um popover que mostra o número total de conversões desses dados.

### [!UICONTROL Breakdown]

A visualização [!UICONTROL Breakdown] é um detalhamento por canal ou ponto de contato das conversões para cada um dos modelos de atribuição selecionados. Essa visualização pode ser útil para tomar decisões sobre a eficácia de cada canal ou ponto de contato.

Para escolher o tipo de detalhamento, selecione **[!UICONTROL Breakdown by channel]** ou **[!UICONTROL Breakdown by touchpoint]** de ![Mais](/help/assets/icons/More.svg).

Para ver detalhes, passe o mouse sobre qualquer um dos elementos do gráfico.

### [!UICONTROL Top campaigns]

A visualização Campanhas principais mostra uma tabela das campanhas principais com colunas para Nome da campanha, Canal, Tipo de mídia e Conversões incrementais. Essa visualização pode ajudar a informar sua equipe sobre a eficácia de uma campanha específica para um determinado canal e fornecer insights sobre em quais campanhas você deve investir ainda mais.

Para classificar a tabela em ordem crescente ↑ ou decrescente ↓ para Canal, Tipo de mídia ou Conversões incrementais, selecione o cabeçalho da coluna e alterne a classificação.

Para expandir a tabela em uma caixa de diálogo separada, selecione **[!UICONTROL Expand]** de ![Mais](/help/assets/icons/More.svg).

A caixa de diálogo Campanhas principais expandida mostra a mesma tabela com colunas de adição para

* Conversões incrementais
* Conversões influenciadas
* Conversões de primeiro contato
* Conversões de último contato

  Você pode selecionar cada um dos cabeçalhos de coluna adicionais para classificar a tabela em ordem crescente ou decrescente.

Para fechar a caixa de diálogo Campanhas principais expandida, selecione **[!UICONTROL Close]**.


### [!UICONTROL Breakdown by touchpoint position]

A visualização [!UICONTROL Breakdown by touchpoint position] é um detalhamento das conversões atribuídas por posição do ponto de contato e do ponto de contato em todos os caminhos de conversão. Este gráfico ajuda a comparar se um ponto de contato contribui melhor em uma posição do que as posições restantes e outros pontos de contato em qualquer posição.

>[!NOTE]
>
>A soma da contribuição percentual para um modelo de atribuição em todos os pontos de contato e posições deve ser igual a 100.


As posições [!UICONTROL Starter], [!UICONTROL Player] e [!UICONTROL Closer] são definidas da seguinte maneira:

| Position | Descrição |
|---|---|
| [!UICONTROL Starter] | Essa posição indica se o ponto de contato é o primeiro contato em um caminho de conversão. |
| [!UICONTROL Player] | Essa posição indica se o ponto de contato não é o primeiro ou o último contato que leva à conversão. |
| [!UICONTROL Closer] | Essa posição indica se o ponto de contato é o último contato antes da conversão. |


### [!UICONTROL Top conversion paths]

A visualização [!UICONTROL Top conversion paths] mostra os 5 principais caminhos de conversão com base nos modelos de atribuição selecionados.

Para cada caminho de conversão, você verá:

* o número de canais que têm impacto,
* o total de caminhos atribuídos,
* a porcentagem de caminhos atribuídos para esse caminho de conversão em relação ao total de caminhos atribuídos,
* para cada canal, a porcentagem de contribuição do modelo de atribuição e
* a soma dessas porcentagens de contribuição do modelo de atribuição de canal.


## [!UICONTROL Diagnostics]

A guia Diagnóstico mostra visualizações para:

* Visualização [!UICONTROL Model Assessment], que pode ser analisada em conversões reais vs. previstas ou residuais.

  Para detalhar a visualização, selecione **[!UICONTROL Actual vs. Predicted]** ou **[!UICONTROL Residuals]** na lista **[!UICONTROL Breakdown]**.

* Tabela [!UICONTROL Model fitting metrics], mostrando as seguintes colunas para cada métrica de conversão:

   * Conversão Efetiva

   * Conversão modelada

   * Conversão Residual (diferença entre a conversão real e a conversão modelada)

   * Valores de pontuação de qualidade do modelo:

      * R2 (R-quadrado), que informa como os dados se encaixam no modelo de regressão (a adequação do ajuste).

      * MAPE (Mean Absolute Percentage Error), que é um dos KPIs mais usados para medir a precisão da previsão e expressa o erro de previsão como uma porcentagem do valor real.

      * RMSE (Root Mean Square Error): que mostra o erro médio, ponderado de acordo com o quadrado do erro.

  Para baixar um arquivo CSV contendo os dados da tabela, selecione ![Baixar](/help/assets/icons/Download.svg).

* Tabela [!UICONTROL Touchpoint effectiveness], que representa o resultado do modelo algorítmico da IA de atribuição. Os dados desta tabela são gerados apenas para períodos específicos. Selecione **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) para obter mais detalhes.

  A visualização mostra, em ordem decrescente de [!UICONTROL Efficiency measure] ![Ordem decrescente](/help/assets/icons/SortOrderDown.svg), para cada ponto de contato:

   * [!UICONTROL Paths touched]: visualiza a porcentagem de caminhos que atingem a conversão e a porcentagem de caminhos que não atingem a conversão. Para um ponto de contato, você verá mais conversões atribuídas quando a taxa de conversão de atribuição estiver alta. Essa proporção compara a porcentagem de caminhos que levam à conversão com a porcentagem de caminhos que *não* levam à conversão.
   * [!UICONTROL Efficiency measure]: gerada pelo modelo de atribuição algorítmica, a medida de eficiência indica a importância relativa de um ponto de contato em direção à conversão, independentemente do volume do ponto de contato. A eficiência é medida em uma escala de 1 a 5. Observe que um maior volume de pontos de contato não garante uma medida de eficiência mais alta.
   * [!UICONTROL Total volume]: O número agregado de vezes que um usuário toca um ponto de contato. O número inclui os pontos de contato que aparecem em um caminho que alcança a conversão, assim como os caminhos *não* que resultam na conversão.

![Diagnósticos](/help/assets/model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

A guia Visão geral histórica mostra visualizações para:

![Modelo - Visão geral histórica](/help/assets/model-insights-historical-overview.png)


### Conversão e gasto por trimestre fiscal e produto

Esta visualização representa a conversão e a distribuição de gastos em vários trimestres dentro do intervalo de datas especificado. A visualização ajuda a identificar trimestres de alto desempenho nos quais o gasto está gerando conversões.


### Gastos por canal

Esta visualização representa a distribuição de gastos em vários canais dentro do intervalo de datas especificado. A visualização permite a identificação rápida de quais canais recebem mais gastos.


### Gastos com Touchpoint

Esta visualização representa a distribuição de gastos em pontos de contato pagos para cada trimestre dentro do intervalo de datas especificado. A visualização permite compreender quais pontos de contato são priorizados em canais e trimestres específicos. A visualização ajuda a identificar padrões e tendências de gasto do canal, especialmente canais com gasto baixo e pouco frequente ao longo do tempo.

Para selecionar um canal alternativo com base em gastos a ser exibido para essa visualização:

* Selecione um canal de **[!UICONTROL Channels]**.


### Volume do ponto de contato

Essa visualização representa a distribuição do volume em todos os pontos de contato para cada trimestre dentro do intervalo de datas especificado.

Para selecionar um canal alternativo baseado em volume a ser exibido para essa visualização:

* Selecione um canal de **[!UICONTROL Channels]**.


## **[!UICONTROL Edit]**

É possível editar o nome, a descrição e a programação do treinamento e a pontuação do modelo.

1. Selecionar ![Editar](/help/assets/icons/Edit.svg) Editar

1. No diálogo **[!UICONTROL Edit model]**:

   * Insira um(a) novo(a) **[!UICONTROL Name]** e **[!UICONTROL Description]**.

   * Para habilitar o agendamento, habilite **[!UICONTROL Status]**. Você só pode habilitar a programação para modelos treinados e pontuados.

      1. Selecione um **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: Insira uma hora válida (por exemplo `05:22 pm`) ou use ![Clock](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: Selecione um dia da semana e insira um horário válido (por exemplo `05:22 pm`) ou use ![Relógio](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: Selecione um dia do mês no menu suspenso Executar em cada e insira um horário válido (por exemplo `05:22 pm`) ou use ![Relógio](/help/assets/icons/Clock.svg).

      1. Selecione um **[!UICONTROL Training frequency]** no menu suspenso: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

     ![Editar um modelo](../assets/model-edit.png)

1. Selecione **[!UICONTROL Save]**.
