---
title: Visualizar as notas de versão atuais do Mix Modeler
description: Notas de versão mais recentes do Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 9b400aeac26a3b02a8dfaf1faad435e0d3ac6cd8
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 3%

---

# Notas de versão atuais do Mix Modeler

**Última atualização**: fevereiro de 2025.

Essas notas de versão abordam a versão mais recente do Mix Modeler. As versões do Mix Modeler operam em um modelo de entrega contínua, que permite uma cadência de lançamento mensal aproximada. Devido a isso, essas notas de versão são atualizadas, portanto, verifique-as regularmente.

## Março - abril de 2025

| Recurso | Descrição | [Início da implantação](#release-strategy) | [Disponibilidade geral](#release-strategy) |
|---|---|---|---|
| **Detecção de desvio de modelo** | Ao abrir um modelo, você é [solicitado a treinar novamente o modelo quando o desvio do modelo for detectado](/help/models/insights.md#model-drift). | 3 de abril de 2025 | 7 de maio de 2025 |
| **Retorno de canal marginal em insights de plano** | Uma visualização de [retorno de canal marginal](/help/plans/insights.md#marginal-channel-return) foi adicionada aos insights do plano, que mostra o ponto de equilíbrio marginal e o retorno de plano para todos os canais ou para os canais selecionados. | 3 de abril de 2025 | 24 de abril de 2025 |


## Janeiro - fevereiro de 2025

| Recurso | Descrição | [Início da implantação](#release-strategy) | [Disponibilidade geral](#release-strategy) |
|---|---|---|---|
| **Condições aninhadas** | Você pode criar condições aninhadas usando AND e OR ao definir uma população de dados qualificada como parte da [configuração de um modelo](/help/models/build.md#configure). | 15 de janeiro de 2025 | 18 de fevereiro de 2025 |
| **Exibir relatórios** | Você pode exibir um relatório em uma [conversão](/help/harmonize-data/conversions.md#view-report) ou em um [ponto de contato de marketing](/help/harmonize-data/marketing-touchpoints.md#view-report) definido como parte da harmonização de dados. | 15 de janeiro de 2025 | 18 de fevereiro de 2025 |
| **Excluir confirmações** | Você será solicitado a confirmar a exclusão de um [plano](/help/plans/overview.md#delete-plans) ou um [modelo](/help/models/overview.md#delete-models). | 15 de janeiro de 2025 | 18 de fevereiro de 2025 |
| **Aperfeiçoamento da interface do usuário de fatores** | Você pode selecionar quais [fatores](/help/models/insights.md#factors-beta) deseja exibir nos insights do modelo. | 15 de janeiro de 2025 | 18 de fevereiro de 2025 |
| **Tratamento de erros** | Mensagens de erro de fácil utilização e experiência do utilizador melhorada para cenários de erro na harmonização e nos planos de dados. | 18 de fevereiro de 2025 | 18 de fevereiro de 2025 |
| **Status do modelo** | Redefinição de [status de modelo](/help/models/overview.md#manage-models) no ciclo de vida do modelo. | 18 de fevereiro de 2025 | 18 de fevereiro de 2025 |


## Estratégia de lançamento

O [!UICONTROL Mixx Modeler] usa sinalizadores de recursos (também conhecidos como &quot;alternadores&quot;) para controlar a visibilidade de novos recursos, permitindo testes de escala controlados antes do lançamento completo. Essa estratégia de lançamento inclui as seguintes fases:

* **Teste limitado**: uma versão em fases começa com testes feitos por usuários internos da Adobe. Ele é então disponibilizado para um pequeno grupo de contas de clientes para garantir que o recurso atenda às necessidades e expectativas do cliente.

* **Início da implantação**: a implantação de uma versão em fases começa com a fase de Teste limitado. A versão é redimensionada de 0% a 100% de disponibilidade para os clientes ao longo de alguns meses. A implantação em fases acontece no nível da Organização da Experience Cloud, de modo que todos os usuários autorizados em uma organização recebem a mesma experiência.
