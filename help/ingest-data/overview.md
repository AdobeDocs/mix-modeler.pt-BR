---
title: Assimilar dados
description: Saiba como assimilar dados no Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 1dbdee00f518d98241fc042e2aabc0e40d5a9153
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 14%

---

# Assimilar dados

O Mix Modeler funciona com dados de nível de evento, agrega um resumo dos dados de esforço de marketing de vários jardins murados e agrega ou resume dados de qualquer outra fonte, como publicidade offline, fatores internos ou fatores externos.

Os clientes podem usar qualquer tipo de dados assimilados no Experience Platform como conjuntos de dados e que se baseiam em esquemas que usam o XDM ExperienceEvent ou as Métricas de resumo XDM como a classe base.

Por exemplo:

* dados coletados usando o conector de origem do Adobe Analytics e transformados em conjuntos de dados em conformidade com a versão padrão ou personalizada do esquema do Adobe Analytics ou, como alternativa,
* dados coletados usando o SDK da Web do Experience Platform, o SDK móvel ou a API do servidor da rede de borda para coletar interações do cliente na Web, em dispositivos móveis ou em qualquer outro tipo de dispositivo,
* dados agregados ou resumidos de jardins murados (como Facebook, YouTube), fontes de tráfego ou dados de publicidade offline,
* dados agregados ou resumidos não relacionados à comercialização que contêm fatores internos ou externos úteis para a construção de modelos.

Você pode usar qualquer tipo de mecanismo, compatível com o Experience Platform, para assimilar o nível do evento da experiência, agregar dados de esforço de marketing e dados de outras fontes. Como os SDKs do Experience Platform, APIs, conectores de origem e assimilação em lote e por transmissão.


## Diretrizes

Para assimilar dados no Experience Platform para uso com o Mix Modeler, siga estas diretrizes:

* Não deve haver qualquer sobreposição nos dados incrementais adicionados aos conjuntos de dados.
* Todos os dados de uma única fonte devem ter a mesma granularidade.
* Data e granularidade são campos obrigatórios no esquema subjacente para todos os dados agregados assimilados como conjuntos de dados
* Canal é um campo obrigatório no esquema subjacente para todos os esforços de marketing/dados de gastos assimilados como conjuntos de dados.


## Exemplos

Encontre abaixo alguns exemplos de dados normalmente usados no Mix Modeler, além dos dados de evento de experiência mais padrão.

+++ Dados agregados do esforço de marketing

| Geo | Data | Tipo de data | Canal | Campaign | Clique em | Ganho | Envolvimento | impressão | Abrir | Próprio | Enviado |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|
| AMER | 2021-10-31 | dia | EMAIL | | 12752 | | | | | | 1132945 |
| AMER | 2021-10-31 | dia | FB | | 148844 | | | | | | |
| AMER | 2021-10-31 | dia | YT | | | | 2314452 | | | | |
| JPN | 2021-10-21 | dia | EMAIL | | 21089 | | | | | | 3283626 |
| JPN | 2021-10-21 | dia | SOCIAL | | | | 621 | | | | |

{style="table-layout:auto"}

+++

+++ Dados de conversão agregados

| Geo | Data | Tipo de data | Produto | Unidades Vendidas | Receita |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | dia | Economia do criador | 603 | 36537.68 |
| EMEA | 2021-09-13 | dia | Metaverso | 55 | 21704.37 |
| JPN | 2022-05-30 | dia | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | dia | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Dados de fatores externos

| Dados | Tipo de data | Fator | Valor |
|---|:---:|:---:|:---|
| 2020-08-02 | semana | SPX | 3325.866 |
| 2020-08-09 | semana | SPX | 3364.158 |
| 2020-08-16 | semana | SPX | 3385.858 |
| 2020-08-23 | semana | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Para trabalhar com dados no Mix Modeler, você precisa de dados coletados em conjuntos de dados e modelados após esquemas no Experience Platform. A interface do Mix Modeler fornece acesso fácil à interface do usuário de Esquemas e Conjuntos de dados.


>[!MORELIKETHIS]
>
>Consulte para obter mais detalhes sobre como gerenciar esquemas e conjuntos de dados:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de dados](datasets.md)
