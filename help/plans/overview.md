---
title: Visão geral dos planos
description: Saiba como exibir, selecionar e executar ações em planos no Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 3b6b127bfaf79cee99a869b21ff0c1a911b3ad6c
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 1%

---

# Visão geral dos planos

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

Se um modelo que você usou para seu plano for pontuado em novos dados, será necessário criar um novo plano para considerar os dados repontuados.


## Criar planos

Para criar um plano, use o assistente de criação de plano do Mix Modeler. Consulte [Planos de compilação](build.md) para obter mais detalhes.

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
   | Conversão prevista | A conversão prevista de um plano |
   | CPA previsto | O CPA previsto para um plano |
   | Status | O status de um plano: <p><span style="color:red"> ●</span> Falhou, <p><span style="color:blue"> ●</span> Processando, ou <p><span style="color:green"> ●</span> Concluído. |

   {style="table-layout:auto"}

   Você pode usar ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) para selecionar ![Checkmark](/help/assets/icons/Checkmark.svg) as colunas a serem exibidas na tabela.

1. Use a ![Pesquisa](/help/assets/icons/Search.svg) para pesquisar e filtrar a tabela para um ou mais planos específicos.

### Planejar insights

Para exibir os insights de um plano e editar um plano:

1. Selecione ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** no painel esquerdo.

1. Selecione o nome do plano.

Você foi redirecionado para [Planejar insights](insights.md).


### Duplicação de um plano

Para duplicar um plano:

- Selecione ![Mais](/help/assets/icons/More.svg) para um plano. No menu de contexto, selecione **[!UICONTROL Duplicate]**.
- Como alternativa, selecione um plano na tabela ![SelectBox](/help/assets/icons/SelectBox.svg) e selecione ![Copy](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]** na barra de ação azul.

Um novo plano, com um nome composto pelo nome do plano original anexado com **[!UICONTROL (Copy)]**, é adicionado à parte superior da tabela.

### Comparar planos

Para comparar planos:

1. Selecione dois planos na tabela.
1. Selecione ![Comparar](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]** na barra de ação azul. Você vê a interface do usuário **[!UICONTROL Compare plans]**.


### Excluir planos

Para deletar um plano:

1. Selecione ![Mais](/help/assets/icons/More.svg) para um plano. No menu de contexto, selecione **[!UICONTROL Delete]**. <br/>Como alternativa, selecione um plano na tabela ![SelectBox](/help/assets/icons/SelectBox.svg) e selecione ![Delete](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** da barra de ação azul.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete plan]** para excluir o plano. Selecione **[!UICONTROL Cancel]** para cancelar.

Para excluir vários planos:

1. Selecione vários planos.
1. Na barra de ações azul, selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para excluir os planos.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete *x *planos]**para excluir os planos. Selecione **[!UICONTROL Cancel]**para cancelar.


