---
title: fluxo de trabalho do Mix Modeler
description: Entenda o fluxo de trabalho típico do Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# fluxo de trabalho do Mix Modeler

Assista a este vídeo para obter uma introdução ao fluxo de trabalho do usuário no Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Um fluxo de trabalho típico no Mix Modeler consiste nas seguintes atividades:

![Texto alternativo](/help/assets/ApplicationWorkflow.svg)

|  | Atividade | Descrição |
|---|---|---|
| ![Dados](/help/assets/icons/Data.svg){width="100"} | [**Assimilar dados**](../ingest-data/overview.md) | Assimilar dados do evento do Experience Platform (por exemplo, Adobe Analytics, SDK da Web, outras fontes), dados agregados de canais de marketing (por exemplo, TV, jardins murados, email, atividades próprias e operadas), dados de fatores externos de clientes (por exemplo, alterações de preço no serviço de assinatura) e dados de fatores internos (por exemplo, planos de feriados). |
| ![VerificaçãoDeDados](/help/assets/icons/DataCheck.svg){width="100"} | [**Harmonizar dados**](../harmonize-data/overview.md) | Configure regras de mapeamento e regras de resolução de conflitos para mesclar os vários conjuntos de dados de marketing necessários para medir e planejar o desempenho da campanha no Mix Modeler. |
| ![ConfigArquivo](/help/assets/icons/FileGear.svg){width="100"} | [**Configurar modelos**](../models/create.md) | Configure instâncias de modelo com pontos de contato de marketing (por exemplo, canais), definições de conversão e fatores internos e externos. |
| ![DadosDoArquivo](/help/assets/icons/FileData.svg){width="100"} | [**Treinar e pontuar modelos**](../models/overview.md) | Crie pontuações agregadas e em nível de evento usando treinamento e pontuação de aprendizado de máquina do. |
| ![GráficoDeArquivos](/help/assets/icons/FileChart.svg){width="100"} | [**Criar planos**](../plans/overview.md) | Determine a melhor alocação de fundos de marketing para atingir um objetivo comercial usando a saída de modelos de Mix Modeler. |
| ![Painel](/help/assets/icons/Dashboard.svg){width="100"} | [**Painel de visão geral**](../dashboard/overview.md) | Obtenha insights sobre dados, modelos e planos harmonizados usando várias visualizações configuráveis. |

{style="table-layout:auto"}

O fluxograma detalhado orientado por dados abaixo ilustra como:

* dados harmonizados baseia-se:

   * dados do evento de experiência (originários do conector de origem do Analytics, coletados por meio de SDKs e APIs do Experience Platform, assimilados por meio de conectores de origem ou usando a assimilação de streaming),
   * agregar dados de resumo de jardins murados (como Facebook, YouTube), fontes de tráfego ou dados de publicidade offline e
   * definições de campos harmonizados e regras de conjuntos de dados.

* um modelo se baseia em:

   * as definições dos pontos de contato de conversão e de comercialização resultantes dos dados e
   * dados agregados ou resumidos de não comercialização que contenham fatores internos ou externos.

* as pontuações de evento de atribuição multitoque podem potencialmente ser realimentadas no data lake do Experience Platform para uso em configurações, treinamentos e pontuações de modelo subsequentes.

![Fluxo de trabalho abrangente](/help/assets/comprehensive-workflow.svg)
