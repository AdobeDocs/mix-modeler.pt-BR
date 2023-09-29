---
title: Esquemas
description: Saiba como gerenciar os esquemas necessários para assimilar dados no Adobe Mix Modeler.
feature: Schemas
source-git-commit: 4a6cbda1ff0a779ebf8a38a4de3f797ed9e54b00
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Esquemas

Para gerenciar esquemas, com suporte aos dados que você deseja assimilar no Adobe Experience Platform e usar no Adobe Mix Modeler:

1. Vá para a interface do Adobe Mix Modeler.

1. Selecionar ![Esquemas](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, abaixo **[!UICONTROL DATA MANAGEMENT]**.

Consulte a [Visão geral da interface de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) para obter mais informações.

## Dados agregados ou resumidos

É altamente recomendável usar a classe Métricas de resumo XDM como a base do esquema subjacente a qualquer dado agregado ou de resumo que você deseja assimilar no Experience Platform e usar no Modelador de combinação de Adobe.

Veja abaixo um exemplo de **[!DNL LumaPaidMarketingSchema]** usar as Métricas de resumo XDM como classe base e grupos de campos dedicados (anotados com cores) para métrica (**[!DNL AMMMetrics]**), dimensões (**[!DNL AMMDimensions]**) e outras informações específicas do cliente (**[!DNL CustomerSpecific]**).

![Esquema de resumo](../assets/summary-schema.png)

Para definir um conjunto de propriedades de auditoria, é altamente recomendável usar o grupo de campos Detalhes de auditoria do sistema de origem externa, como parte de um esquema usado para coletar dados agregados ou resumidos de fontes externas.
