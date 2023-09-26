---
title: Fluxo de trabalho do Adobe Mix Modeler
description: Entenda o fluxo de trabalho típico do Adobe Mix Modeler.
feature: Datasets, Event Datasets, Plans, Harmonized Data, Models
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Fluxo de trabalho do Adobe Mix Modeler

Um fluxo de trabalho típico no Adobe Mix Modeler é semelhante a:

![Texto alternativo](../assets/ApplicationWorkflow.svg)

|  | Atividade | Descrição |
|---|---|---|
| ![Dados](../assets/icons/Data.svg){width="100"} | [**Assimilar dados**](../ingest-data/overview.md) | Assimilar dados de eventos do Adobe Experience Platform (por exemplo, Adobe Analytics, SDK da Web, outras fontes), dados agregados de canais de marketing (por exemplo, TV, jardins murados, email, atividades próprias e operadas) e dados de fatores externos de clientes (por exemplo, alterações de preço no serviço de assinatura). |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**Harmonizar dados**](../harmonize-data/overview.md) | Configure regras de mapeamento e regras de resolução de conflitos para mesclar os vários conjuntos de dados de marketing necessários para medir e planejar o desempenho da campanha no Adobe Mix Modeler. |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**Configurar modelos**](../models/create.md) | Configure instâncias de modelo com pontos de contato de marketing (por exemplo, canais) e definições de conversão. |
| ![ArquivoDados](../assets/icons/FileData.svg){width="100"} | [**Modelos de treinamento e pontuação**](../models/overview.md) | Crie pontuações agregadas e em nível de evento usando treinamento e pontuação de aprendizado de máquina do. |
| ![GráficoDeArquivos](../assets/icons/FileChart.svg){width="100"} | [**Criar planos**](../plans/overview.md) | Determine a melhor alocação de fundos de marketing para atingir um objetivo comercial usando a saída dos modelos do Adobe Mix Modeler. |
| ![Painel](../assets/icons/Dashboard.svg){width="100"} | [**Painel de visão geral**](../dashboard/overview.md) | Obtenha insights sobre dados, modelos e planos harmonizados usando vários widgets configuráveis. |

{style="table-layout:auto"}

