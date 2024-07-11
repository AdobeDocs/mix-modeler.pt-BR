---
title: Modelos
description: Saiba como configurar e usar modelos no Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Modelos

A funcionalidade do modelo no Mix Modeler permite configurar, treinar e pontuar modelos de IA/ML específicos para seus objetivos de negócios e compatíveis com aprendizado de transferência orientado por IA entre a atribuição multitoque e a modelagem de mix de marketing.

Os modelos são baseados nos dados harmonizados que você cria como parte do fluxo de trabalho do aplicativo Mix Modeler.

Um modelo em Mix Modeler é um modelo de aprendizado de máquina empregado para medir e/ou prever um resultado especificado com base nos investimentos de um profissional de marketing. Pontos de contato de marketing e dados de nível de resumo podem ser usados como uma entrada. O Mix Modeler permite criar variantes de modelos com base em diferentes conjuntos de variáveis, dimensões e resultados, como receitas, unidades vendidas e leads.

Um modelo requer:

* uma conversão,
* um ou mais pontos de contato de marketing (canais) compostos por dados a nível de resumo, dados de pontos de contato de marketing (dados do evento) ou ambos,
* uma janela de retrospectiva configurável para
* uma janela de treinamento configurável.

Um modelo pode incluir opcionalmente:

* fatores externos,
* fatores internos,
* os chamados &quot;antecedentes&quot; (distribuição de probabilidades que representa o conhecimento ou a incerteza dos dados anteriores ou anteriores à observação desses dados), que indexam conversões anteriores por canal,
* gastar compartilhamento, que usa compartilhamento de gasto relativo como proxy quando os dados de marketing são escassos.


## Criar um modelo

Para criar um modelo, use o fluxo de configuração do modelo guiado passo a passo do Mix Modeler disponível ao selecionar **[!UICONTROL Open model canvas]**. Consulte [Criar um modelo](create.md) para obter mais detalhes.

## Gerenciar modelos

Para exibir uma tabela dos modelos atuais, na interface do Mix Modeler:

1. Selecionar ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** do painel esquerdo.

1. Você verá uma tabela dos modelos atuais.

   As colunas da tabela especificam detalhes sobre o modelo.

   | Nome da coluna | Detalhes |
   |---|---|
   | Nome | Nome do modelo |
   | Descrição | Descrição do modelo |
   | Evento de conversão | A conversão selecionada para o modelo. |
   | Frequência de execução | A frequência de execução do treinamento do modelo. |
   | Última execução | A data e hora do último treinamento do modelo. |
   | Status | O status da última execução do treinamento do modelo. <br/><span style="color:green">●</span> Sucesso<br/><span style="color:orange">●</span> Problema de treinamento<br/> <span style="color:orange">●</span> Aguardando treinamento <br/><span style="color:red">●</span> Failed <br/><span style="color:gray">●</span> _ (quando uma última execução está em andamento) |

   {style="table-layout:auto"}

1. Para alterar as colunas exibidas para a lista, selecione ![Configurações de coluna](/help/assets//icons/ColumnSetting.svg) e ativar colunas ![Marcar](/help/assets//icons/Checkmark.svg) ou desativado.


### Exibir detalhes de um modelo

Para exibir mais detalhes de um modelo:

1. Selecionar ![Informações](/help/assets//icons/Info.svg) para um modelo mostrar um pop-up com detalhes.



### Insights do modelo

Para exibir insights de um modelo, na interface do Mix Modeler:

1. Selecionar ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** do painel esquerdo.

1. Selecione o nome de um modelo com um **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** do **[!UICONTROL Models]** tabela. Os insights do modelo só estão disponíveis em modelos treinados com êxito.

1. No menu de contexto, selecione **[!UICONTROL Model Insights]**. Você será redirecionado para [Informações do modelo](insights.md).


### Re-pontuação


Para pontuar novamente um modelo, na interface do Mix Modeler:

1. Selecionar ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** do painel esquerdo.

1. Selecione o nome de um modelo com um **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** do **[!UICONTROL Models]** tabela. A re-pontuação só está disponível em modelos treinados com sucesso.

1. No menu de contexto, selecione **[!UICONTROL Re-score]**. Pode levar alguns minutos para mostrar um status atualizado do modelo.


### Excluir um modelo

Para excluir um modelo:

1. Selecione o nome do modelo que deseja excluir.

1. No menu de contexto, selecione **[!UICONTROL Delete]** para excluir o modelo.

   >[!WARNING]
   >
   >O modelo é excluído imediatamente.


