---
title: Modelos
description: Saiba como configurar e usar modelos no Mix Modeler.
feature: Models
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---


# Modelos

A funcionalidade do modelo no Mix Modeler permite configurar, treinar e pontuar modelos de IA/ML específicos para seus objetivos de negócios e compatíveis com aprendizado de transferência orientado por IA entre a atribuição multitoque e a modelagem de mix de marketing.

Os modelos são baseados nos dados harmonizados que você cria como parte do fluxo de trabalho do aplicativo Mix Modeler.

Para criar um modelo, use o fluxo de configuração do modelo guiado passo a passo do Mix Modeler disponível ao selecionar **[!UICONTROL Guide me]**. Consulte [Criar um modelo](create.md) para obter mais detalhes.

## Gerenciar modelos

Para exibir uma tabela dos modelos atuais, na interface do Mix Modeler:

1. Selecionar ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** do painel esquerdo.

1. Você verá uma tabela dos modelos atuais.

   As colunas da tabela especificam detalhes sobre o modelo.

   | Nome da coluna | Detalhes |
   |---|---|
   | Nome | Nome do modelo |
   | Descrição | Descrição do modelo |
   | Eventos de conversão | A conversão selecionada para o modelo. |
   | Conjunto de dados | O conjunto de dados que o modelo usa para treinar e pontuar. Esse é, por padrão, o conjunto de dados harmonizado. |
   | Frequência de execução | A frequência de execução do treinamento do modelo. |
   | Última execução | A data e hora do último treinamento do modelo. |
   | Status da última execução | O status da última execução do treinamento do modelo. <br/><span style="color:green">●</span> Sucesso<br/><span style="color:orange">●</span> Problema de treinamento<br/> <span style="color:orange">●</span> Aguardando treinamento <br/><span style="color:red">●</span> Failed |

   {style="table-layout:auto"}

1. Para alterar as colunas exibidas para a lista, selecione ![Configurações de coluna](../assets/icons/ColumnSetting.svg) e ativar colunas ![Marcar](../assets/icons/Checkmark.svg) ou desativado.

### Excluir um modelo

Para excluir um modelo:

1. Selecione o nome do modelo que deseja excluir.

1. No menu de contexto, selecione **[!UICONTROL Delete]** para excluir o modelo.

### Exibir detalhes de um modelo

Para exibir mais detalhes de um modelo:

1. Selecione o nome do modelo do qual deseja exibir mais detalhes.

1. No menu de contexto, selecione **[!UICONTROL More]**. Você verá detalhes do modelo selecionado no painel direito.



### Insights do modelo

>[!NOTE]
>
>Essa seleção só está disponível em modelos treinados com sucesso.
>

Para exibir insights de um modelo, na interface do Mix Modeler:

1. Selecionar ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** do painel esquerdo.

1. Selecione o nome de um modelo com um **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** do **[!UICONTROL Models]** tabela.

1. No menu de contexto, selecione **[!UICONTROL Model Insights]**. Você será redirecionado para [Informações do modelo](insights.md).


