---
title: visão geral do Mix Modeler
description: Obtenha uma visão geral da funcionalidade e dos recursos do Mix Modeler.
short-description: Obtenha uma visão geral da funcionalidade e dos recursos do Mix Modeler.
feature: Plans, Harmonized Data, Models
exl-id: aa1018d5-b073-4dfb-b40c-ca16a8970b2f
source-git-commit: 59869553c4a5856e897aded441520dd8938eb8c1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 3%

---

# visão geral do Mix Modeler

Assista a este vídeo para obter uma visão geral rápida dos recursos do Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424872/?learn=on)

O Mix Modeler, desenvolvido pela Adobe Sensei, permite que os profissionais de marketing avaliem campanhas e otimizem o planejamento de forma holística em todos os canais: pagos, conquistados e próprios. Sua metodologia unificada mede de forma incremental tanto em pontos de contato de marketing quanto em níveis agregados, garantindo resultados totalmente consistentes.

o Mix Modeler oferece o impacto incremental de todas as atividades de marketing nos resultados de negócios e campanhas por meio de um aplicativo de medição holístico (completo) para marketing digital e offline.

O Mix Modeler fornece os seguintes tipos de insights otimizados e acionáveis em nível estratégico e tático, para que você possa entender melhor:

* gastos com marketing e o desempenho resultante em vários canais, e
* níveis de investimento recomendados para atingir os objetivos de negócios futuros.


Para conseguir essa funcionalidade, o Mix Modeler combina:

* dados de baixo para cima (nível de evento) e dados de cima para baixo (nível agregado),
* fatores do mercado externo e fatores internos, e
* metodologias de aprendizagem automática preditiva e de transferência.

O aprendizado de transferência bidirecional de IA/ML unifica os resultados de modelagem de mix de marketing (MMM) e atribuição de multitoque (MTA) para garantir resultados consistentes na medição e no planejamento em um mundo sem cookies.

![Aprendizado de transferência bidirecional](../assets/birdirectional-transfer-learning.png){width="500" align="center"}


## Capacidades

O Mix Modeler oferece os seguintes recursos:

| Recurso | Descrição |
|---|---|
| **Meça o desempenho incremental** | Entenda o ROI incremental e o impacto do marketing em todas as metas comerciais ou metas táticas de campanha. |
| **Unificar resultados no MMM e MTA** | Tome decisões mais confiantes por meio da unificação dos modelos de modelagem de mix de marketing (MMM) e atribuição de multitoque (MTA) por meio do aprendizado de transferência. |
| **Alocar orçamentos de maneira ideal** | Identifique a alocação de orçamento ideal com base nos gastos com marketing e no impacto nas metas. |
| **Criar e comparar cenários de orçamento** | Desenvolva vários planos de orçamento e compare seu impacto para tomar decisões ideais para sua empresa. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>[Entender o fluxo de trabalho do Mix Modeler](workflow.md)


### Modelagem de mix de marketing (MMM)

A modelagem de mix de marketing no Mix Modeler é uma análise de aprendizado de máquina de privacidade usada para medir o impacto incremental de várias táticas de marketing e fatores comerciais nas métricas de conversão. Ele ajuda as empresas e os profissionais de marketing a entender

* a eficácia de suas estratégias de marketing,
* os efeitos de fatores comerciais no comportamento do cliente, e
* o que impulsiona o ROI e as conversões.

Essa análise abrangente permite que as empresas aloquem orçamentos de marketing estrategicamente em várias linhas de negócios, regiões, canais e campanhas, além de fornecer insights preditivos sobre o impacto comercial de eventos futuros.

Os recursos de modelagem de mix de marketing do Mix Modeler são fundamentais para resolver os seguintes casos de uso:

* Relatórios executivos: permita que os executivos entendam o verdadeiro impacto incremental do marketing, tanto como um todo quanto por canal, região, SKU etc.
* Planejamento estratégico: informe estratégias de marketing de longo prazo e defina metas e referências realistas para campanhas futuras
* Medição abrangente: análise integral de como os diferentes fatores de marketing e negócios interagem e contribuem para as vendas e o desempenho gerais
* Análise de cenário: permite que as empresas simulem diferentes cenários e estratégias de marketing e prevejam seus resultados


### Atribuição multitoque (MTA)

A atribuição multitoque no Mix Modeler é uma análise opcional de aprendizado de máquina que você pode aproveitar para atribuir créditos a pontos de contato no nível do evento, resultando em eventos de conversão. Essa atribuição é usada pelos profissionais de marketing para ajudar a quantificar o impacto de marketing de cada ponto de contato de marketing individual nas jornadas do cliente que podem ser rastreadas. Esses pontos de contato da campanha de marketing digital normalmente são cliques de anúncio de exibição, envios por email, aberturas de email e cliques de pesquisa pagos. A atribuição multitoque não pode medir a maioria dos pontos de contato offline, como anúncios impressos, outdoors, comerciais de TV e fatores comerciais. Esses pontos de contato têm apenas dados de nível de resumo que não podem ser compilados nas jornadas do cliente.

A atribuição multitoque do Mix Modeler é compatível com duas categorias de pontuações:

* Pontuações algorítmicas, que incluem pontuações incrementais e influenciadas:
   * A pontuação influenciada é a fração da conversão pela qual cada ponto de contato de marketing é responsável.
   * A pontuação incremental é a quantidade de impacto marginal causado diretamente por um ponto de contato de marketing. Essa pontuação remove a linha de base (a parte da conversão obtida sem nenhuma atividade de marketing) da pontuação influenciada.

* Pontuações baseadas em regras, que incluem Primeiro contato, Último contato, Linear, Forma de U e Declínio de tempo.

Você pode usar o recurso de atribuição multitoque do Mix Modeler nos seguintes casos de uso:

* Alocação de orçamento de campanha: informe as decisões de alocação de orçamento no canal de marketing.
* Otimização de campanha: em cada canal, entenda quais campanhas, criações e palavras-chave estão funcionando melhor para quais SKUs ou Geos. Essa compreensão permite que você veja cada canal para que a equipe de marketing possa otimizar suas táticas.
* Atribuição de nível de evento de funil completo: entenda o impacto do marketing na jornada do cliente inteiro. Por exemplo, assinatura de conta gratuita para conversão paga e muito além.
* Avaliações de parceiros: avalie a eficácia de agências e parceiros com base nos resultados da atribuição.

Consulte [Informações do modelo - Atribuição](../models/insights.md#attribution) sobre como acessar os insights de atribuição multitoque no Mix Modeler.


