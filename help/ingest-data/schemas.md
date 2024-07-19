---
title: Esquemas
description: Saiba como gerenciar os esquemas necessários para assimilar dados no Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 3%

---

# Esquemas

Para gerenciar esquemas, suportando os dados que você deseja assimilar no Experience Platform e usar no Mix Modeler:

1. Vá para a interface do Mix Modeler.

1. Selecione ![Esquemas](/help/assets//icons/Schemas.svg) **[!UICONTROL Schemas]**, abaixo de **[!UICONTROL SETUP]**.

Consulte a [Visão geral da interface do usuário de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) para obter mais informações.

## Dados agregados ou resumidos

É altamente recomendável usar a classe Métricas resumidas do XDM como a base do esquema subjacente a qualquer dado agregado ou resumido que você deseja assimilar no Experience Platform e usar no Mix Modeler.

Use a classe Métricas de resumo XDM para:

- dados murados, por exemplo, dados do Facebook ou do YouTube.

- dados de fatores externos, como dados de SPX (índices de preços de ações S&amp;P 500), dados meteorológicos,

- dados de fatores internos, por exemplo, alterações de preço, um calendário de feriados.

>[!IMPORTANT]
>
>A definição do esquema deve conter pelo menos um campo numérico (usando Integer, Double, Boolean ou outro tipo numérico) para oferecer suporte às métricas necessárias para os dados assimilados.

Um esquema usando a classe base **[!DNL XDM Summary Metrics]** pode ser simples, como mostrado no **[!DNL ExternalFactorSummarySchema]** abaixo.

![Esquema de Fatores Externos](/help/assets//external-factors-schema.png)

Esse esquema simples pode ser usado para assimilar conjuntos de dados que contenham dados para, por exemplo:

- Dados do índice do concorrente

  | carimbo de data e hora | date_type | fator | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semana | competitor_index | 289,8 |
  | 2020-12-05T00:00:00.000Z | semana | competitor_index | 291,2 |
  | 2020-12-12T00:00:00.000Z | semana | competitor_index | 280,07 |
  | .. | ... | ... | ... |

- Dados de feriados

  | carimbo de data e hora | date_type | fator | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semana | all_Holiday_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | semana | all_Holiday_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | semana | all_Holiday_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | semana | all_Holiday_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | semana | all_Holiday_flag | 1,0 |
  | ... | ... | ... | ... |


Veja abaixo um exemplo mais abrangente de **[!DNL LumaPaidMarketingSchema]** usando **[!DNL XDM Summary Metrics]** como classe base. O esquema usa grupos de campos dedicados (anotados com cores) para métricas (**[!DNL AMMMetrics]**), dimensões (**[!DNL AMMDimensions]**) e outras informações específicas do cliente (**[!DNL CustomerSpecific]**).

![Esquema de resumo](/help/assets//summary-schema.png)

Dada a natureza assíncrona da assimilação de perfis, ao coletar dados agregados ou resumidos de fontes externas, é recomendável usar o grupo de campos Detalhes de auditoria do sistema Source externo como parte de um esquema. Esse grupo de campos define um conjunto de propriedades de auditoria para fontes externas.


## Tipos de dados compatíveis

Atualmente, o Mix Modeler não suporta um subconjunto de tipos de dados Experience Platform. Os seguintes tipos de dados básicos (campos), mencionados em [Noções básicas da composição de esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#data-type), são suportados:

- String
- Integer
- Duplo
- Booleano
- Longo
- Short
- Byte
- Data
- Data e hora
