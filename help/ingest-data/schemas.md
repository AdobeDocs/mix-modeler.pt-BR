---
title: Esquemas
description: Saiba como gerenciar os esquemas necessários para assimilar dados no Mix Modeler.
feature: Schemas
source-git-commit: c145754ecd6a6d8f5aab333ced739c4053aeaae5
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 6%

---


# Esquemas

Para gerenciar esquemas, com suporte aos dados que você deseja assimilar na Adobe Experience Platform e usar no Mix Modeler:

1. Vá para a interface do Mix Modeler.

1. Selecionar ![Esquemas](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, abaixo **[!UICONTROL DATA MANAGEMENT]**.

Consulte a [Visão geral da interface de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) para obter mais informações.

## Dados agregados ou resumidos

É altamente recomendável usar a classe Métricas resumidas do XDM como a base do esquema subjacente a qualquer dado agregado ou resumido que você deseja assimilar no Experience Platform e usar no Mix Modeler.

Use a classe Métricas de resumo XDM para:

- dados murados, por exemplo, dados do Facebook ou do YouTube.

- dados de fatores externos, como dados de SPX (índices de preços de ações S&amp;P 500), dados meteorológicos,

- dados de fatores internos, por exemplo, alterações de preço, um calendário de feriados.

>[!IMPORTANT]
>
>A definição do esquema deve conter pelo menos um campo numérico (usando Integer, Double, Boolean ou outro tipo numérico) para oferecer suporte às métricas necessárias para os dados assimilados.

Um esquema usando o **[!DNL XDM Summary Metrics]** a classe base pode ser simples, como mostrado na **[!DNL ExternalFactorSummarySchema]** abaixo.

![Esquema de fatores externos](../assets/external-factors-schema.png)

Esse esquema simples pode ser usado para assimilar conjuntos de dados que contenham dados para:

- Dados do índice do concorrente

  | carimbo de data e hora | date_type | fator | Valor de  |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semana | competitor_index | 289.8 |
  | 2020-12-05T00:00:00.000Z | semana | competitor_index | 291.2 |
  | 2020-12-12T00:00:00.000Z | semana | competitor_index | 280.07 |
  | .. | ... | ... | ... |

- Dados de feriados

  | carimbo de data e hora | date_type | fator | Valor de  |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semana | all_Holiday_flag | 0.0 |
  | 2020-12-05T00:00:00.000Z | semana | all_Holiday_flag | 0.0 |
  | 2020-12-12T00:00:00.000Z | semana | all_Holiday_flag | 0.0 |
  | 2020-12-19T00:00:00.000Z | semana | all_Holiday_flag | 0.0 |
  | 2020-12-26T00:00:00.000Z | semana | all_Holiday_flag | 1.0 |
  | ... | ... | ... | ... |


Veja abaixo um exemplo mais abrangente de **[!DNL LumaPaidMarketingSchema]** usando o **[!DNL XDM Summary Metrics]** como a classe base. O esquema usa grupos de campos dedicados (anotados com cores) para métricas (**[!DNL AMMMetrics]**), dimensões (**[!DNL AMMDimensions]**) e outras informações específicas do cliente (**[!DNL CustomerSpecific]**).

![Esquema de resumo](../assets/summary-schema.png)

Dada a natureza assíncrona da assimilação de perfis, ao coletar dados agregados ou resumidos de fontes externas, é recomendável usar o grupo de campos Detalhes de auditoria do sistema de origem externa como parte de um esquema. Esse grupo de campos define um conjunto de propriedades de auditoria para fontes externas.
