---
title: Visão geral dos dados de assimilação
description: Saiba como assimilar dados na Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: bb05cee1d4e2245cf665e5dcea17a30c5c0cf203
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 7%

---

# Visão geral dos dados de assimilação

O Mix Modeler funciona com dados no nível do evento, dados de esforço de marketing agregados ou resumidos de vários jardins murados e dados agregados ou resumidos de qualquer outra fonte, como publicidade offline, fatores internos ou fatores externos.

Os clientes podem usar qualquer tipo de dados assimilados na Experience Platform como conjuntos de dados e que se baseie em esquemas que usam o XDM ExperienceEvent ou as Métricas de resumo XDM como a classe base.

Por exemplo:

* dados coletados usando o conector de origem do Adobe Analytics e transformados em conjuntos de dados em conformidade com a versão padrão ou personalizada do esquema do Adobe Analytics ou, como alternativa,
* dados coletados usando o Experience Platform Web SDK, Mobile SDK ou a API do Edge Network Server para coletar interações do cliente na Web, em dispositivos móveis ou em qualquer outro tipo de dispositivo,
* dados agregados ou resumidos de jardins murados (como Facebook, YouTube), fontes de tráfego ou dados publicitários offline,
* dados agregados ou resumidos não relacionados à comercialização que contêm fatores internos ou externos úteis para a construção de modelos.

Você pode usar qualquer tipo de mecanismo, compatível com o Experience Platform, para assimilar o nível do evento da experiência, agregar dados de esforço de marketing e dados de outras fontes. Os mecanismos de assimilação incluem SDKs da Experience Platform, APIs, conectores de origem, assimilação em lote e por transmissão. Para saber mais sobre como assimilar seus dados no Experience Platform para uso no Adobe Mix Modeler, consulte [Visão geral da assimilação de dados](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home).

## Diretrizes

Para assimilar dados na Experience Platform para uso com o Mix Modeler, siga estas diretrizes:

* Não deve haver qualquer sobreposição nos dados incrementais adicionados aos conjuntos de dados.
* Todos os dados de uma única fonte devem ter a mesma granularidade.
* Data e granularidade são campos obrigatórios no esquema subjacente para todos os dados agregados assimilados como conjuntos de dados
* Canal é um campo obrigatório no esquema subjacente para todos os esforços de marketing/dados de gastos assimilados como conjuntos de dados.


## Exemplos

Encontre abaixo alguns exemplos de dados normalmente usados no Mix Modeler, além dos dados do evento de experiência mais padrão.

+++ Dados agregados do esforço de marketing

| Geo | Data | Tipo de data | Canal | Campaign | Clique em | Ganho | Engajamento | impressão | Abrir | Próprio | Enviado | Gastos |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 2021-10-31 | dia | EMAIL | | 12752 | | | | | | 1132945 | |
| AMER | 2021-10-31 | dia | FB | | 148844 | | | | | | | 42111 |
| AMER | 2021-10-31 | dia | YT | | | | 2314452 | | | | | 10540 |
| JPN | 21-10-2021 | dia | EMAIL | | 21089 | | | | | | 3283626 | |
| JPN | 21-10-2021 | dia | SOCIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Dados de conversão agregados

| Geo | Data | Tipo de data | Produto | Unidades Vendidas | Receita |
|---|:---|:---:|---|--:|--:|
| EMEA | 09-2021-13 | dia | Economia do criador | 603 | 36537,68 |
| EMEA | 09-2021-13 | dia | Metaverso | 55 | 21704,37 |
| JPN | 30/05/2022 | dia | Pro Imaging | 487 | 64469,60 |
| JPN | 30/05/2022 | dia | Document Cloud | 642 | 100509,07 |

{style="table-layout:auto"}

+++

+++ Dados de fatores externos

| Dados | Tipo de data | Fator | Valor |
|---|:---:|:---:|:---|
| 2020-08-02 | semana | SPX | 3325,866 |
| 08-2020-09 | semana | SPX | 3364,158 |
| 2020-08-16 | semana | SPX | 3385,858 |
| 23/08/2020 | semana | SPX | 3497,965 |

{style="table-layout:auto"}

+++

Para trabalhar com dados na Mix Modeler, você precisa dos dados coletados nos conjuntos de dados e modelados de acordo com os esquemas na Experience Platform. A interface do Mix Modeler fornece acesso fácil à interface do usuário de Esquemas e Conjuntos de dados do Experience Platform.


## Validar

Para validar se os dados estão disponíveis corretamente no Mix Modeler, você pode fazer o seguinte:

* Use visualizações em [Visão geral](/help/overview.md).
* Baixe e inspecione dados de [Dados harmonizados](/help/harmonize-data/overview.md) em conjuntos de dados harmonizados.

Para validar se seus dados foram assimilados corretamente no Experience Platform, você pode [gravar e executar consultas SQL usando o Serviço de Consulta do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Consulte para obter mais detalhes sobre como gerenciar esquemas e conjuntos de dados:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de dados](datasets.md)
