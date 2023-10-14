---
title: fluxo de trabalho do Mix Modeler
description: Entenda o fluxo de trabalho típico do Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 512cc28a9fab81438d54e30bb6e20f05da5265d1
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# fluxo de trabalho do Mix Modeler

Assista a este vídeo para obter uma introdução ao fluxo de trabalho do usuário no Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


De um ponto de vista funcional, um fluxo de trabalho típico no Mix Modeler consiste nas seguintes atividades:

![Texto alternativo](../assets/ApplicationWorkflow.svg)

|  | Atividade | Descrição |
|---|---|---|
| ![Dados](../assets/icons/Data.svg){width="100"} | [**Assimilar dados**](../ingest-data/overview.md) | Assimilar dados do evento do Experience Platform (por exemplo, Adobe Analytics, SDK da Web, outras fontes), dados agregados de canais de marketing (por exemplo, TV, jardins murados, email, atividades próprias e operadas), dados de fatores externos de clientes (por exemplo, alterações de preço no serviço de assinatura) e dados de fatores internos (por exemplo, planos de feriados). |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**Harmonizar dados**](../harmonize-data/overview.md) | Configure regras de mapeamento e regras de resolução de conflitos para mesclar os vários conjuntos de dados de marketing necessários para medir e planejar o desempenho da campanha no Mix Modeler. |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**Configurar modelos**](../models/create.md) | Configure instâncias de modelo com pontos de contato de marketing (por exemplo, canais) e definições de conversão. |
| ![ArquivoDados](../assets/icons/FileData.svg){width="100"} | [**Modelos de treinamento e pontuação**](../models/overview.md) | Crie pontuações agregadas e em nível de evento usando treinamento e pontuação de aprendizado de máquina do. |
| ![GráficoDeArquivos](../assets/icons/FileChart.svg){width="100"} | [**Criar planos**](../plans/overview.md) | Determine a melhor alocação de fundos de marketing para atingir um objetivo comercial usando a saída de modelos de Mix Modeler. |
| ![Painel](../assets/icons/Dashboard.svg){width="100"} | [**Painel de visão geral**](../dashboard/overview.md) | Obtenha insights sobre dados, modelos e planos harmonizados usando vários widgets configuráveis. |

{style="table-layout:auto"}
