---
title: Modelos de treinamento e pontuação
description: Saiba como treinar e pontuar modelos.
feature: Models
source-git-commit: 6855d19347b7f6f1477a6265310df5950b8463c9
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Modelos de treinamento e pontuação

Depois de [criar](/help/models/build.md) um modelo, ele é automaticamente treinado e classificado. Você pode treinar novamente ou pontuar um modelo manualmente.

## Treinamento

Considere treinar novamente um modelo quando quiser incluir novos dados de marketing incremental e de fatores. Por exemplo, durante o último trimestre, a dinâmica do mercado mudou ou sua distribuição de dados de marketing mudou significativamente.

Para treinar novamente um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Train]**. Como alternativa, selecione ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** na barra de ação azul.

   Na caixa de diálogo **[!UICONTROL Train model]**, selecione a opção para:

   * **[!UICONTROL Train model with last 2 years of marketing data]** ou
   * **[!UICONTROL Train model using specific date range of data]**.
Especifique o intervalo de datas. Você pode usar o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de datas. Você deve selecionar um intervalo de dados com no mínimo um ano.

   ![Retreinar um modelo](../assets/retrain-model.png)

1. Selecione **[!UICONTROL Train]** para treinar novamente o modelo.


Você só poderá treinar novamente um modelo quando ele for treinado com êxito.


## Pontuação


Você pode pontuar incrementalmente um modelo com base em novos dados de marketing ou repontuar um modelo para um intervalo de datas específico.

Considere pontuar um modelo quando quiser:

* Corrija dados de marketing incorretos. Por exemplo, os dados de pesquisa paga recentes incluídos no treinamento e na pontuação do modelo perderam uma semana de dados.
* Use os novos dados de marketing incrementais que se tornaram disponíveis por meio de atualizações nos conjuntos de dados configurados como parte de seus dados harmonizados.

Para pontuar ou repontuar um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Score]**. Como alternativa, selecione ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** na barra de ação azul.

   Na caixa de diálogo **[!UICONTROL Score marketing data]**, selecione a opção para:

   * **[!UICONTROL Score new marketing data from *mm/dd/aaaa *]**, para pontuar seu modelo de forma incremental usando novos dados de marketing, ou
   * **[!UICONTROL Score specific date range of marketing data]** para pontuar para um intervalo de datas específico.
Especifique o intervalo de datas. Você pode usar o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de datas.

   ![Pontuar novamente um modelo](../assets/rescore-model.png)

1. Selecione **[!UICONTROL Score]**. Ao pontuar novamente um modelo usando um intervalo de dados específico, você verá uma caixa de diálogo **[!UICONTROL Existing model is replaced]**, solicitando a confirmação para substituir o modelo por novas pontuações para o intervalo de datas selecionado. Selecione **[!UICONTROL Replace model]** para confirmar.

>[!IMPORTANT]
>
>A pontuação de um modelo não altera nenhum plano já criado com base no modelo rescored. Para usar o novo modelo ressaltado em um plano, é necessário criar um novo plano.

