---
title: Harmonizar dados
description: Saiba como harmonizar dados no Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 7%

---

# Harmonizar dados

Os dados em Mix Modeler são de natureza diferente dependendo da fonte de dados. Os dados podem ser:

* dados agregados ou resumidos, por exemplo, coletados de fontes de dados muradas ou dados de publicidade offline coletados (como gastos) da execução de uma campanha em outdoor, um evento ou uma campanha de publicidade física,
* dados do evento, por exemplo, de fontes de dados primárias. Esses dados de evento podem ser coletados por meio do conector de origem do Adobe Analytics da Adobe Analytics, ou por meio do SDK da Web ou móvel do Experience Platform ou da API Edge Network, ou por dados assimilados usando conectores de origem.

O serviço de harmonização do Mix Modeler assimila os dados agregados e do evento em uma visualização de dados consistente. Essa visualização de dados, combinada com dados de fatores internos e externos, é a fonte dos modelos no Mix Modeler. O serviço usa a maior granularidade entre os diferentes conjuntos de dados. Por exemplo, se um conjunto de dados tiver uma granularidade de dados mensais e os conjuntos de dados restantes tiverem granularidade semanal e diária, o serviço de harmonização criará uma visualização de dados usando granularidade mensal.

## Um exemplo de dados harmonizados

Imagine que você tenha os seguintes conjuntos de dados disponíveis para o Mix Modeler.

**Conjunto de dados 1**

Contém o conjunto de dados de esforço de marketing da YouTube, com uma granularidade do conjunto de dados agregado para diariamente.

| Data | Tipo de data | Canal | Campaign | Marca | Geo | Cliques | Gastos |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | dia | YouTube | Y_Fall_02 | BrandX | EUA | 10000 | 100 |
| 01-01-2022 | dia | YouTube | Y_Fall_02 | BrandX | EUA | 1000 | 10 |
| 03-01-2022 | dia | YouTube | Y_Fall_01 | MarcaY | CA | 10000 | 100 |
| 04-01-2022 | dia | YouTube | Y_Summer_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**Conjunto de dados 2**

Contém o conjunto de dados de esforço de marketing da Facebook, com uma granularidade do conjunto de dados agregado para semanal.

| Data | Tipo de data | Canal | Campaign | Geo | Cliques | Gastos |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | semana | Facebook | FB_Fall_01 | EUA | 8000 | 100 |
| 08-01-2022 | semana | Facebook | FB_Fall_02 | EUA | 1000 | 10 |
| 08-01-2022 | semana | Facebook | FB_Fall_01 | EUA | 7000 | 100 |
| 16-01-2022 | semana | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Conjunto de dados 3**

Um conjunto de dados de conversão, com uma granularidade do conjunto de dados agregado para diariamente.

| Data | Tipo de data | Geo | Meta | Receita |
|--- |:---: |---|---|---:|
| 01-01-2022 | dia | EUA | Moda | 200 |
| 08-01-2022 | dia | EUA | Moda | 10 |
| 08-01-2022 | dia | EUA | Joias | 1100 |
| 16-01-2022 | dia | CA | Joias | 80 |

{style="table-layout:auto"}


**Conjunto de dados 4**

Um exemplo de conjunto de dados de evento de experiência (eventos do SDK da Web) do cliente.

| Carimbo de data e hora | Namespace de identidade | Identificação de identidade | Canal | Cliques |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 08-01-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 08-01-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Você deseja criar um conjunto de dados harmonizado, com uma granularidade definida como semanal. Os dados do evento são agregados à granularidade da semana e adicionados ao conjunto de dados harmonizado. O resultado é:

**Conjunto de dados harmonizado**

| Data | Tipo de data | Canal | Campaign | Marca | Geo | Meta | Cliques | Gastos | Receita |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | semana | YouTube | Y_Fall_02 | BrandX | EUA | Null | 11000 | 110 | Null |
| 03-01-2022 | semana | YouTube | Y_Fall_01 | MarcaY | CA | Null | 10000 | 100 | Null |
| 03-01-2022 | semana | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | semana | Facebook | FB_Fall_01 | Null | EUA | Null | 8000 | 100 | Null |
| 08-01-2022 | semana | Facebook | FB_Fall_02 | Null | EUA | Null | 1000 | 10 | Null |
| 08-01-2022 | semana | Facebook | FB_Fall_01 | Null | EUA | Null | 7000 | 100 | Null |
| 16-01-2022 | semana | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | semana | Null | Null | Null | EUA | Moda | Null | Null | 200 |
| 03-01-2022 | semana | Null | Null | Null | EUA | Moda | Null | Null | 10 |
| 03-01-2022 | semana | Null | Null | Null | EUA | Joias | Null | Null | 1100 |
| 10-01-2022 | semana | Null | Null | Null | CA | Joias | Null | Null | 80 |
| 01-01-2022 | semana | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 08-01-2022 | semana | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Configurar dados harmonizados

Para criar um conjunto de dados harmonizado, como no [exemplo](#an-example-of-harmonized-data) simplificado, siga estas etapas:

1. Defina [campos harmonizados](fields.md) adicionais que você deseja usar além dos campos harmonizados globais já disponíveis.
1. Configure [regras do conjunto de dados](dataset-rules.md) para mapear campos de seus conjuntos de dados de evento de agregação ou experiência para campos harmonizados.
1. Defina [pontos de contato de marketing](marketing-touchpoints.md) usando os campos harmonizados padrão e adicionais que você definiu.
1. Defina [conversões](conversions.md) usando os campos harmonizados padrão e adicionais que você definiu.


## Exibir dados harmonizados

Para ver seus dados harmonizados, na interface do Mix Modeler:

1. Selecione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** no painel esquerdo.

1. Selecione **[!UICONTROL Harmonized Data]** na barra superior. Um resumo de seus dados harmonizados é mostrado com base nos campos, nas regras do conjunto de dados, nos pontos de contato de marketing e nas conversões definidos.

   1. Para redefinir o período no qual se baseia a recapitulação de dados harmonizados, insira um intervalo de datas para **[!UICONTROL Date range]** ou use o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de dados.

   1. Para modificar as colunas de campo harmonizado exibidas para a tabela de dados Harmonizada, use ![Configurações](/help/assets/icons/Setting.svg) para abrir a caixa de diálogo **[!UICONTROL Column settings]**.

      1. Selecione ![SelectBox](/help/assets/icons/SelectBox.svg) uma ou mais colunas de **[!UICONTROL AVAILABLE COLUMNS]** e use ![Divisa direita](/help/assets/icons/ChevronRight.svg) para adicionar essas colunas a **[!UICONTROL SELECTED COLUMNS]**.

      1. Selecione ![SelectBox](/help/assets/icons/SelectBox.svg) uma ou mais colunas de **[!UICONTROL SELECTED COLUMNS]** e use ![Divisa à esquerda](/help/assets/icons/ChevronLeft.svg) para remover as colunas selecionadas e retornar essas colunas de volta para **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Selecione uma coluna de **[!UICONTROL DEFAULT SORT]** e alterne entre **[!UICONTROL Ascending]** ou **[!UICONTROL Descending]**.

      1. Para alterar a ordem das colunas exibidas, você pode mover uma coluna em **[!UICONTROL SELECTED COLUMNS]** para cima e para baixo por meio da ação de arrastar e soltar.

   1. Selecione **[!UICONTROL Submit]** para enviar suas alterações de configuração de coluna. Selecione **[!UICONTROL Close]** para cancelar as alterações feitas.

1. Se mais páginas estiverem disponíveis, use a ![Seta para a esquerda](/help/assets/icons/ChevronLeft.svg) ou a ![Seta para a direita](/help/assets/icons/ChevronRight.svg) em **[!UICONTROL Page _x _de_x_]** para se mover entre as páginas.
