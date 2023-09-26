---
title: Assimilar dados
description: Saiba como assimilar dados no Adobe Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
source-git-commit: ae1c74ed2edf1e69e7ab77d16aba797921c14ad9
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 14%

---


# Assimilar dados

O Adobe Mix Modeler funciona com dados de nível de evento e dados agregados do esforço de marketing de vários jardins murados. Os clientes podem usar todos os tipos de dados assimilados na Adobe Experience Platform como conjuntos de dados e baseados em esquemas XDM baseados em eventos de experiência.

Por exemplo:

* dados coletados usando o conector de origem do Adobe Analytics e transformados em conjuntos de dados em conformidade com a versão padrão ou personalizada do esquema do Adobe Analytics ou, como alternativa,
* dados coletados usando o SDK da Web da Adobe Experience Platform, o SDK móvel ou a API do servidor da rede de borda para coletar interações do cliente na Web, em dispositivos móveis ou em qualquer outro tipo de dispositivo,
* dados de resumo de diferentes fontes de tráfego/jardim murado, com base em um esquema que inclui a classe Métricas de resumo XDM com o grupo de campos Resumo de tráfego e conversão,
* dados não relacionados com a comercialização (indicadores macroeconômicos, por exemplo) que sejam úteis para a construção de modelos,

Você pode usar qualquer tipo de mecanismo compatível com o Adobe Experience Platform para assimilar seu nível de evento de experiência e agregar dados de esforço de marketing. Como os SDKs do Adobe Experience Platform, APIs, conectores de origem, assimilação em lote e por transmissão.


## Diretrizes

Para assimilar dados no Adobe Experience Platform para uso com o Adobe Mix Modeler, siga estas diretrizes:

* Não deve haver qualquer sobreposição nos dados incrementais adicionados aos conjuntos de dados.
* Todos os dados de uma única fonte devem ter a mesma granularidade.
* Data e granularidade são campos obrigatórios no esquema subjacente para todos os dados agregados assimilados como conjuntos de dados
* Canal é um campo obrigatório no esquema subjacente para todos os esforços de marketing/dados de gastos assimilados como conjuntos de dados.


## Exemplos

Encontre abaixo alguns exemplos de dados normalmente usados no Adobe Mix Modeler, além de dados de evento de experiência mais padrão.

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

Para trabalhar com dados no Adobe Mix Modeler, é necessário que os dados sejam coletados em conjuntos de dados e modelados de acordo com os esquemas no Adobe Experience Platform. A interface do Modelador de mix de Adobe fornece acesso fácil à interface do usuário de Esquemas e Conjuntos de dados.

>[!MORELIKETHIS]
>
>Consulte para obter mais detalhes sobre como gerenciar esquemas e conjuntos de dados:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de dados](datasets.md)
