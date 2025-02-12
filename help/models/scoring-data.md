---
title: Usar dados de pontuação
description: Saiba como os dados de pontuação de um modelo no Mix Modeler são mantidos.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: 5f6c35816a8850bf170cb73d9710e65809e5f372
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 6%

---

# Usar dados de pontuação

Como parte da pontuação de um modelo, os dados de pontuação são mantidos em um conjunto de dados na Experience Platform. Quando você tiver ativado a atribuição multitoque durante a criação do modelo, dados adicionais de pontuação do evento serão mantidos em um conjunto de dados na Experience Platform.

Cada um desses conjuntos de dados está em conformidade com um esquema. Este artigo documenta esses esquemas.


## Esquema de dados de pontuação agregada

O esquema para pontuação de dados é nomeado como `AMM AI Schema - <name of model> <id>`. Por exemplo: `AMM AI Schema - Model for Online Conversion 10120`.

O conjunto de dados, que persiste nos dados de pontuação de um modelo, é nomeado como `AMM AI Aggregrate Scores - <id>`, por exemplo `AMM AI Aggregrate Scores - 10120`.

O esquema inclui um grupo de campos com um objeto que contém detalhes sobre as pontuações. O objeto consiste nos seguintes campos.

| Nome do campo | Tipo | Definição |
|---|---|---|
| `campaignGroup` | String | Nome do grupo de campanhas. |
| `campaignName` | String | Nome da campanha. |
| `contribution` | Duplo | Contribuição atribuída a essa conversão para o ponto de contato especificado. |
| `conversionEndDate` | Data | Data final da janela de conversão. |
| `conversionName` | String | Nome da conversão criada durante a etapa de configuração da definição de conversão. |
| `conversionStartDate` | Data | Data inicial da janela de conversão. |
| `geo` | String | A localização geográfica onde ocorreu a conversão. |
| `mediaChannel` | String | Nome do canal usado durante a etapa de configuração do ponto de contato. |
| `mediaSubChannel` | String | Nome do subcanal. |
| `revenue` | Duplo | Receita atribuída a esta conversão para o ponto de contato especificado. |
| `scoreCreatedTime` | DateTime | Carimbo de data e hora quando esse registro de pontuação é criado. |
| `touchpointEndDate` | Data | Data final da janela do ponto de contato. |
| `touchpointName` | String | Nome do ponto de contato criado durante a etapa de configuração de definição do ponto de contato. Atualmente, o ponto de contato é definido no canal de mídia. |
| `touchpointStartDate` | Data | Data de início da janela do ponto de contato. |


## Esquema de dados de pontuação de evento

O esquema para pontuação de dados é nomeado como `Attribution AI Scores - <name of model> <id> - Schema`. Por exemplo: `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

O conjunto de dados, que persiste nos dados de pontuação de um modelo, é nomeado como `Attribution AI Scores - <name of model> <id>`, por exemplo `Attribution AI Scores - Model for Online Conversion 10120 `.

O esquema inclui um grupo de campos contendo um objeto com detalhes sobre os núcleos. O objeto tem o nome de `attibution_AI_scores__<name of model> id`.

O grupo de campos contém os seguintes campos.

| Nome do campo | Tipo | Descrição |
|---|---|---|
| `conversion` | Objeto | Colunas de metadados de conversão. |
|     `passThrough` | Objeto |  |
|         `eventType` | String | |
|         `channel_typeAtSource` | String | |
|      `dataSource` | String | Identificação globalmente exclusiva de uma fonte de dados. <br> **Exemplo:** `Adobe Analytics` |
|      `eventSource` | String | A origem quando o evento real ocorreu. <br> **Exemplo:** `Adobe.com` |
|      `eventType` | String | O tipo de evento principal para este registro de série temporal. <br> **Exemplo:** `Order` |
|      `geo` | String | A localização geográfica onde a conversão foi entregue `placeContext.geo.countryCode`. <br> **Exemplo:** `US` |
|      `path` | String | |
|      `priceTotal` | Duplo | Receita obtida por meio da conversão <br> **Exemplo:** `99.9` |
|      `product` | String | O identificador XDM do próprio produto. <br> **Exemplo:** `RX 1080 ti` |
|      `productType` | String | O nome de exibição do produto conforme apresentado ao usuário para esta visualização do produto. <br> **Exemplo:** `Gpus` |
|      `quantity` | Integer | Quantidade comprada durante a conversão. <br> **Exemplo:** `1` |
|      `receivedTimeStamp` | DateTime | Carimbo de data/hora da conversão recebido. <br> **Exemplo:** `2020-06-09T00:01:51.000Z` |
|      `skuId` | String | Unidade de manutenção de estoque (SKU), o identificador exclusivo de um produto definido pelo fornecedor. <br> **Exemplo:** `MJ-03-XS-Black` |
|      `timestamp` | DateTime | Carimbo de data e hora da conversão. <br> **Exemplo:** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Integer |  |
|      `totalTouchpointCount` | Integer | |
| `customerProfile` | Objeto | Detalhes de identidade do usuário usado para criar o modelo. |
|      `identity` | Objeto | |
|           `id` | String | |
|           `namespace` | String | Contém os detalhes do usuário usado para criar o modelo, como `id` e `namespace`. |
| `touchpointsDetail` | Objeto[] | A lista de detalhes do ponto de contato que leva à conversão, ordenada pela ocorrência do ponto de contato ou carimbo de data e hora. |
|      `scores` | Objeto | Contribuição do ponto de contato para essa conversão como pontuação. |
|           `algorithmicInfluenced` | Duplo | A pontuação influenciada é a fração da conversão pela qual cada ponto de contato de marketing é responsável. |
|           `algorithmicSourced` | Duplo | Pontuação incremental é a quantidade de impacto marginal causado diretamente por um ponto de contato de marketing. |
|           `decayUnits` | Duplo | Pontuação de atribuição baseada em regras, em que os pontos de contato mais próximos da conversão recebem mais crédito do que os pontos de contato mais distantes da conversão. |
|           `firstTouch` | Duplo | Pontuação de atribuição baseada em regras que atribui todos os créditos ao ponto de contato inicial em um caminho de conversão. |
|           `lastTouch` | Duplo | Pontuação de atribuição baseada em regras que atribui todo o crédito ao ponto de contato mais próximo da conversão. |
|           `linear` | Duplo | Pontuação de atribuição baseada em regras que atribui crédito igual a cada ponto de contato em um caminho de conversão. |
|           `uShape` | Duplo | Pontuação de atribuição baseada em regras que atribui 40% do crédito ao primeiro ponto de contato e 40% do crédito ao último ponto de contato. Os outros pontos de contato dividem os 20% restantes igualmente. |
|      `touchPoint` | Objeto | Metadados do ponto de contato. |
|           `passThrough` | Objeto | |
|                `eventType` | String | |
|           `campaignGroup` | String |  |
|           `campaignName` | String | |
|           `campaignTag` | String | |
|           `eventId` | String | |
|           `geo` | String | |
|           `mediaAction` | String | |
|           `mediaChannel` | String | |
|           `receivedTimeStamp` | DateTime | |
|           `timestamp` | DateTime | |
|      `isFirstInThePosition` | Integer | |
|      `lag` | Integer | |
|      `position` | String | |
|      `touchpointCountToConversion` | Integer | |
|      `touchpointName` | String | Nome do ponto de contato configurado durante a configuração. <br> **Exemplo:** `PAID_SEARCH_CLICK` |
| `conversionName` | String | Nome da conversão configurada durante a instalação. <br> **Exemplo:** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | DateTime | |
| `segmentation` | String | Segmento de conversão, como segmentação geográfica, em que o modelo é criado. Quando os segmentos estão ausentes, `segmentation` é o mesmo que `conversionName`. <br> **Exemplo:** `ORDER_US` |





Consulte [Esquemas](../ingest-data/schemas.md) para obter mais informações.
