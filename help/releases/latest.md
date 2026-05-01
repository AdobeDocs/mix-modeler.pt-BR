---
title: Visualizar as notas de versão atuais do Mix Modeler
description: Notas de versão mais recentes do Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
TQID: https://experienceleague.adobe.com/8o2hpkneIUMbBNEZfw9TsQLaGuPOxqF-XA2TV9cJnqc
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: ca6bcd6f-f5ca-4e5f-a5ae-7dce7177bde9
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-05-01T09:06:55.437Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 435
ht-degree: 5%

---

# Notas de versão atuais do Mix Modeler

**Última atualização**: 26 de fevereiro de 2026.

Essas notas de versão abordam a versão mais recente do Mix Modeler. As versões do Mix Modeler operam em um modelo de entrega contínua, que permite uma cadência de lançamento mensal aproximada. Devido a isso, essas notas de versão são atualizadas, portanto, verifique-as regularmente.

## Março de 2026

| Recurso | Descrição | [Início da implantação](#release-strategy) | [Disponibilidade geral](#release-strategy) |
|---|---|---|---|
| **Estoque de canal** | Você pode incorporar conhecimento de domínio, resultados de experimentação ou análises de canal anteriores diretamente na configuração avançada do modelo por meio do [Channel adstock](/help/models/build.md#channel-adstock). E mostre [insights do canal adstock](/help/models/insights.md#channel-adstock) na análise de canal de um modelo. | 30 de março de 2026 | 30 de março de 2026 |

## Fevereiro de 2026

| Recurso | Descrição | [Início da implantação](#release-strategy) | [Disponibilidade geral](#release-strategy) |
|---|---|---|---|
| **Fluxo de trabalho de fatores harmonizados** | Os fatores agora são gerenciados como parte de um [fluxo de trabalho de fatores harmonizados](/help/harmonize-data/overview.md#factors). Isso simplifica como [definir dados de fator](/help/ingest-data/schemas.md#factor-standard-fields-field-group), [gerenciar fatores internos e externos como parte de suas regras de conjunto de dados](/help/harmonize-data/dataset-rules.md#factor-datasets) e usar dados de fator em [modelos](/help/models/build.md#configure). | 25 de fevereiro de 2026 | 25 de fevereiro de 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Defina campos harmonizados para que você possa detalhar os relatórios do seu modelo usando [campos de relatórios de insights granulares](/help/models/build.md#granular-insights-reporting-fields), em vez de precisar criar modelos separados. | 18 de fevereiro de 2026 | 18 de fevereiro de 2026 |

## Janeiro de 2026

| Recurso | Descrição | [Início da implantação](#release-strategy) | [Disponibilidade geral](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Atualização da tabela de regras do conjunto de dados](/help/harmonize-data/dataset-rules.md). É possível pesquisar uma ou mais regras de conjunto de dados e exibir, editar ou excluir uma regra de conjunto de dados diretamente da tabela. | 13 de janeiro de 2026 | 13 de janeiro de 2026 |
| **[!UICONTROL Current spend]** | Adicione um ponto de gasto atual na [visualização da curva de resposta marginal](/help/models/insights.md#marginal-response-curves) nos insights do modelo. | 13 de janeiro de 2026 | 13 de janeiro de 2026 |
| **[!UICONTROL Sort and resize columns]** | Adição de classificação e redimensionamento de colunas na tabela [Modelos](/help/models/overview.md) e [Planos](/help/plans/overview.md). | 13 de janeiro de 2026 | 13 de janeiro de 2026 |
| **Correções** | Correções para os seguintes tíquetes: <ul><li>AMM-3328: Entrada de campo desativada para novos operadores para Fatores</li><li>AMM-3359: Seletor de datas e bloqueio da caixa de combinação.</li><li>AMM-3441: A duplicação de um plano não preenche automaticamente o intervalo de datas e o orçamento.</li></ul> | 13 de janeiro de 2026 | 13 de janeiro de 2026 |


## Estratégia de lançamento

O [!UICONTROL Mix Modeler] usa sinalizadores de recursos (também conhecidos como &quot;alternadores&quot;) para controlar a visibilidade de novos recursos, permitindo testes de escala controlados antes do lançamento completo. Essa estratégia de lançamento inclui as seguintes fases:

* **Teste limitado**: uma versão em fases começa com testes feitos por usuários internos da Adobe. Ele é então disponibilizado para um pequeno grupo de contas de clientes para garantir que o recurso atenda às necessidades e expectativas do cliente.

* **Início da implantação**: a implantação de uma versão em fases começa com a fase de Teste limitado. A versão é redimensionada de 0% a 100% de disponibilidade para os clientes ao longo de alguns meses. A implantação em fases acontece no nível da Organização da Experience Cloud, de modo que todos os usuários autorizados em uma organização recebem a mesma experiência.

