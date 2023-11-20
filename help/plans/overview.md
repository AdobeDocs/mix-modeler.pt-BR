---
title: Planos
description: Saiba como exibir, selecionar e executar ações nos planos no Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 73534d1aecb6d1513f6f3b5f1801b497ad73278f
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 1%

---

# Planos

Os planos no Mix Modeler permitem alocar orçamentos por unidade de negócios e canal. A funcionalidade de planejamento está integrada aos resultados dos modelos treinados com base em seus dados harmonizados.

Um plano descreve os investimentos discricionários (por exemplo, orçamentos) que uma empresa pretende gastar em projetos relacionados a marketing durante um determinado período em serviço de KPI comum (por exemplo, pedidos, receita). Os planos podem incluir despesas de canais como publicidade paga, conteúdo da Web patrocinado, eventos.

Um plano exige:

- um modelo,
- um intervalo de dados,
- um orçamento.

Um plano pode incluir, opcionalmente:

- uma janela de reconhecimento configurada,
- várias datas de voo com cada uma tendo um orçamento de target,
- restrições de orçamento mínimo e máximo por canal e data de voo.


## Gerenciar planos

Para exibir uma tabela de seus planos atuais, na interface do Mix Modeler:

1. Selecionar ![](../assets/icons/FileChart.svg) **[!UICONTROL Plans]** do painel esquerdo.

1. Você verá uma tabela dos planos atuais e seus status.

   As colunas da tabela especificam detalhes sobre os planos.

   | Nome da coluna | Detalhes |
   |---|---|
   | Nome | Nome do plano |
   | Modelo | O modelo usado como base para o plano. |
   | Intervalo de data | O intervalo de datas completo de um plano. |
   | Orçamento | O orçamento total de um plano. |
   | Retorno previsto | O retorno previsto de um plano |
   | ROI previsto | O ROI previsto para um plano. |
   | Status | O status de um plano. |

   {style="table-layout:auto"}

1. Uso ![Pesquisar](../assets/icons/Search.svg) para pesquisar e filtrar a tabela para um ou mais planos específicos.

## Criar um plano

Para criar um plano, use o assistente de criação de plano Mix Modeler. Consulte [Criar um plano](create.md) para obter mais detalhes.


## Editar um plano

Para editar um plano, selecione o nome do plano na tabela. Consulte [Editar um plano](edit.md) para obter mais informações.


## Selecionar e executar ações nos planos

Você pode selecionar um ou mais planos, o que revela a barra de ação Planos. A barra de ações permite excluir, comparar ou duplicar planos.

Para remover todas as seleções na tabela Planos, selecione ![Fechar](../assets/icons/Close.svg) na barra de ações

![Barra de ação Planos](../assets/plans-action-bar.png)

### Duplicação de um plano

Para duplicar um plano:

1. Selecione um único plano na tabela.
1. Selecionar ![Copiar](../assets/icons/Copy.svg) **[!UICONTROL Duplicate]** na barra de ações. Um novo plano, com um nome composto pelo nome do plano original anexado com **[!UICONTROL (Copy)]**, é adicionado à parte superior da tabela.

### Comparar planos

Para comparar planos:

1. Selecione dois planos na tabela.
1. Selecionar ![Comparar](../assets/icons/Compare.svg) **[!UICONTROL Compare]** na barra de ações. Você vê a **[!UICONTROL Compare plans]** IU.


### Excluir planos

Para deletar planos:

1. Selecione um ou mais planos na tabela.
1. Selecionar ![Excluir](../assets/icons/Delete.svg) **[!UICONTROL Delete]** na barra de ações.

   >[!WARNING]
   >
   >   Os planos selecionados são excluídos imediatamente!
