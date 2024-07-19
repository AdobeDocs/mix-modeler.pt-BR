---
title: Dados de pontuação
description: Saiba como os dados de pontuação de um modelo no Mix Modeler são mantidos.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 5%

---

# Dados de pontuação

Como parte da pontuação de um modelo, os dados de pontuação são mantidos em um conjunto de dados no Experience Platform. Esse conjunto de dados está em conformidade com um esquema criado para cada modelo na instância do Mix Modeler.

O esquema para pontuação de dados é nomeado como `AMM AI Schema - <name of model> <id>`. Por exemplo: `AMM AI Schema - Model for Online Conversion 10120`.

O conjunto de dados, que persiste nos dados de pontuação de um modelo, é nomeado como `AMM AI Aggregrate Scores - <id>`, por exemplo `AMM AI Aggregrate Scores - 10120`.


## Esquema

O esquema inclui um grupo de campos com um objeto que contém detalhes sobre as pontuações. O objeto consiste nos seguintes campos.

| Nome do campo | Tipo | Definição |
|---|---|---|
| **campaignGroup** | String | Nome do grupo de campanhas. |
| **nomedacampanha** | String | Nome da campanha. |
| **contribuição** | Duplo | Contribuição atribuída a essa conversão para o ponto de contato especificado. |
| **conversionEndDate** | Data | Data final da janela de conversão. |
| **conversionName** | String | Nome da conversão criada durante a etapa de configuração da definição de conversão. |
| **conversionStartDate** | Data | Data inicial da janela de conversão. |
| **geo** | String | A localização geográfica onde ocorreu a conversão. |
| **mediaChannel** | String | Nome do canal usado durante a etapa de configuração do ponto de contato. |
| **mediaSubChannel** | String | Nome do subcanal. |
| **receita** | Duplo | Receita atribuída a esta conversão para o ponto de contato especificado. |
| **scoreCreatedTime** | DateTime | Hora em que este registro de pontuação é criado. |
| **DataFinalDoPontoDeContato** | Data | Data final da janela do ponto de contato. |
| **nomeDoPontoDeContato** | String | Nome do ponto de contato criado durante a etapa de configuração de definição do ponto de contato. Atualmente, o ponto de contato é definido no canal de mídia. |
| **DatadeIníciodoPontoDeContato** | Data | Data de início da janela do ponto de contato. |

Consulte [Esquemas](../ingest-data/schemas.md) para obter mais informações.
