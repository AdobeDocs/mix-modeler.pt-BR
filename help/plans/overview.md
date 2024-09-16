---
title: Planos
description: Saiba como exibir, selecionar e executar ações nos planos no Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

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

1. Selecione ![](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** no painel esquerdo.

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
   | Status | O status de um plano: <p><span style="color:red"> ●</span> Falhou, <p><span style="color:blue"> ●</span> Processando, ou <p><span style="color:green"> ●</span> Concluído. |

   {style="table-layout:auto"}

1. Use a ![Pesquisa](/help/assets/icons/Search.svg) para pesquisar e filtrar a tabela para um ou mais planos específicos.

## Criar um plano

Para criar um plano, use o assistente de criação de plano Mix Modeler. Consulte [Criar um plano](create.md) para obter mais detalhes.


## Editar um plano

Para editar um plano, selecione o nome do plano na tabela. Consulte [Editar um plano](edit.md) para obter mais informações.


## Selecionar e executar ações nos planos

Você pode selecionar um ou mais planos, o que revela a barra de ação Planos. A barra de ações permite excluir, comparar ou duplicar planos.

Para remover todas as seleções na tabela Planos, selecione ![Fechar](/help/assets/icons/Close.svg) na barra de ações

![Barra de ação de planos](/help/assets/plans-action-bar.png)

### Duplicação de um plano

Para duplicar um plano:

1. Selecione um único plano na tabela.
1. Selecione ![Copiar](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]** na barra de ações. Um novo plano, com um nome composto pelo nome do plano original anexado com **[!UICONTROL (Copy)]**, é adicionado à parte superior da tabela.

Alternativamente:

1. Selecione ![Mais](/help/assets/icons/More.svg) para um plano na tabela.
1. Selecione **[!UICONTROL Duplicate]** no menu de contexto. Um novo plano, com um nome composto pelo nome do plano original anexado com **[!UICONTROL (Copy)]**, é adicionado à parte superior da tabela.

### Comparar planos

Para comparar planos:

1. Selecione dois planos na tabela.
1. Selecione ![Comparar](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]** na barra de ações. Você vê a interface do usuário **[!UICONTROL Compare plans]**.


### Excluir planos

Para deletar planos:

1. Selecione um ou mais planos na tabela.
1. Selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** da barra de ações.

Alternativamente:

1. Selecione ![Mais](/help/assets/icons/More.svg) para um plano na tabela.
1. Selecione **[!UICONTROL Delete]** no menu de contexto. Um novo plano, com um nome composto pelo nome do plano original anexado com **[!UICONTROL (Copy)]**, é adicionado à parte superior da tabela.

   >[!WARNING]
   >
   >   Os planos selecionados são excluídos imediatamente!
