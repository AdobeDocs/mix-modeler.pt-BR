---
title: Esquemas
description: Saiba como gerenciar os esquemas necessários para assimilar dados na Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 7524c2ffc0408b04e6bef5bd5deedc1feea0b682
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 4%

---

# Esquemas

Para gerenciar esquemas, com suporte aos dados que você deseja assimilar no Experience Platform e usar no Mix Modeler:

1. Acesse a interface do Mix Modeler.

1. Selecione ![Esquemas](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, abaixo de **[!UICONTROL SETUP]**.

Consulte a [Visão geral da interface do usuário de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=pt-BR) para obter mais informações.

## Dados agregados ou resumidos

É altamente recomendável usar a classe Métricas de resumo XDM como a base do esquema subjacente a qualquer dado agregado ou resumido que você deseja assimilar no Experience Platform e usar no Mix Modeler.

Use a classe Métricas de resumo XDM para:

- dados de jardim murado, por exemplo, dados do Facebook ou YouTube.

- dados de fatores externos, como dados de SPX (índices de preços de ações S&amp;P 500), dados meteorológicos,

- dados de fatores internos, por exemplo, alterações de preço, um calendário de feriados.

>[!IMPORTANT]
>
>A definição do esquema deve conter pelo menos um campo numérico (usando Integer, Double, Boolean ou outro tipo numérico) para oferecer suporte às métricas necessárias para os dados assimilados.

Um esquema usando a classe base **[!DNL XDM Summary Metrics]** pode ser simples, como mostrado no **[!DNL ExternalFactorSummarySchema]** abaixo.

![Esquema de Fatores Externos](/help/assets/external-factors-schema.png)

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

![Esquema de resumo](/help/assets/summary-schema.png)

Dada a natureza assíncrona da assimilação de perfis, ao coletar dados agregados ou resumidos de fontes externas, é recomendável usar o grupo de campos Detalhes de auditoria do sistema Source externo como parte de um esquema. Esse grupo de campos define um conjunto de propriedades de auditoria para fontes externas.

## Grupo de campos Campos Padrão de Fator

Para maior comodidade, o Experience Platform oferece suporte a um grupo de campos Campos padrão de fator dedicado para dados de fatores internos e externos que geralmente fazem parte do resumo, do fator interno ou dos dados de fatores externos. Esse grupo de campos define os seguintes campos:

| Nome de exibição do campo | Nome do campo | Tipo de campo | Tipo de dados | Obrigatório | Descrição |
|---|---|---|---|:-:|---|
| Nome do fator | fatorNome | Dimensão | String | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | O nome do fator |
| Valor do fator | fatorValor | Métrica | Duplo | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | O valor do fator |
| Tipo de fator | fatorTipo | Dimensão | String (Enum) | | O tipo do fator.<br/>Os valores possíveis são: <ul><li>Interno (Fator Interno)</li><li>Externo (Fator Externo)</li></ul> |
| Tipo de valor | valueType | Dimensão | String (Enum) | | Os valores possíveis são:<ul><li>Real (Valor Real)</li><li>Previsto (Valor Previsto)</li></ul>Quando nenhum valor, Real é o valor padrão. |
| Granularidade | granularidade | Dimensão | String (Enum) | | Os valores possíveis são:<ul><li>Diariamente</li><li>Semanalmente</li><li>Mensal</li></ul> |

Um resumo, fator interno ou conjunto de dados de fator externo pode ser baseado em:

- Um esquema que **usa** o grupo Campos Padrão de Fator. Esse conjunto de dados é mostrado como um conjunto de dados **[!UICONTROL Factors]** quando você configura regras de conjunto de dados. E os campos harmonizados que você define, como parte das regras do conjunto de dados para o conjunto de dados, estão disponíveis como fatores ao criar um modelo.
- Um esquema que **não usa** o grupo Campos Padrão de Fator. Esse conjunto de dados é mostrado como um conjunto de dados **[!UICONTROL Summary]** quando você configura regras de conjunto de dados. O conjunto de dados é configurado como dados de resumo e não influencia os dados harmonizados.

## Tipos de dados compatíveis

Atualmente, o Mix Modeler oferece suporte a um subconjunto de tipos de dados do Experience Platform. Os seguintes tipos de dados básicos (campos), mencionados em [Noções básicas da composição de esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR#data-type), são suportados:

- String
- Integer
- Duplo
- Booleano
- Longo
- Short
- Byte
- Data
- Data e hora


>[!MORELIKETHIS]
>
>- [Esquemas](schemas.md)
