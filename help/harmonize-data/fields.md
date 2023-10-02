---
title: Campos harmonizados
description: Saiba como definir campos para usar como parte da harmonização dos dados no Mix Modeler.
feature: Harmonized Data, Harmonized Fields
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 10%

---


# Campos harmonizados

Campos harmonizados permitem definir campos para os mesmos dados conceitualmente, originários de diferentes fontes, cada uma com sua própria definição desses dados. Por exemplo, uma métrica de cliques pode ser definida e nomeada de forma diferente dependendo da fonte de dados. Um campo harmonizado de cliques permite definir uma nomenclatura comum para uma métrica de cliques com base nessas diferentes fontes de dados de cliques.

Campos harmonizados permitem definir os campos que deseja usar como parte do fluxo de trabalho de dados harmonizados. Os campos definidos podem ser usados na definição de regras do conjunto de dados, pontos de contato de marketing e conversão.

## Domínios de harmonização global

Os campos de harmonização global disponíveis por padrão no Mix Modeler são:


| Nome do campo | Nome de exibição | Categoria | Tipo de dados | Comentário |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| marca | Marca | Dimensão | String |           |
| campaign | Campaign | Dimensão | String |           |
| channel | Canal | Dimensão | String |           |
| channel_id | ID do canal | Dimensão | String |           |
| channel_type_at_source | Tipo De Canal Na Origem | Dimensão | String |           |
| channel | Canal | Dimensão | String |           |
| cliques | Cliques | Métrica | Número |           |
| conversiontype | Tipo de conversão | Dimensão | String |           |
| custo | Custo | Métrica | Moeda |           |
| conjunto de dados | Conjunto de dados | Dimensão | String |           |
| date_type | Tipo de data | Dimensão | String | dia, semana |
| emails enviados | Emails enviados | Métrica | Número |           |
| event_date | Data | Dimensão | DateTime |           |
| demanda_bruta | Demanda Bruta | Métrica | Moeda |           |
| impressões | Impressões | Métrica | Número |           |
| data_da_última_atualização | Data da última atualização | Dimensão | DateTime |           |
| linkvisitors | Vincular visitas | Métrica | Número |           |
| mediatype | Tipo de mídia | Dimensão | String |           |
| net_sales | Vendas Líquidas | Métrica | Moeda |           |
| pedidos | Pedidos | Métrica | Número |           |
| sourcetype | Tipo de origem | Dimensão | String |           |
| gasto | Gastos | Métrica | Moeda |           |
| fonte de tráfego | Traffic Source | Dimensão | String |           |

{style="table-layout:auto"}

É possível adicionar, editar ou excluir seus próprios campos harmonizados sobre esses campos harmonizados globais.

## Gerenciar campos harmonizados

Para ver uma tabela dos campos harmonizados disponíveis, na interface Mix Modeler:

1. Selecionar ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** do painel esquerdo.

1. Selecionar **[!UICONTROL Fields]** na barra superior. Você vê uma tabela dos campos harmonizados.

   As colunas da tabela especificam os detalhes sobre os campos harmonizados

   | Nome da coluna | Detalhes |
   | ---------------------- | ----------|
   | Nome do campo | O nome do campo harmonizado. |
   | Nome de exibição | O nome de exibição do campo harmonizado. Esse nome de exibição é usado ao definir regras de conjunto de dados, ponto de contato de marketing e definições de conversão. |
   | Categoria | Especifica se um campo de dados harmonizado é um [!UICONTROL Dimension], um [!UICONTROL Metric] ou [!UICONTROL Derived]. Uma categoria derivada é um campo harmonizado que usa uma definição de fórmula baseada em métricas. |
   | Proprietário | Indica se um campo harmonizado é padrão ([!UICONTROL Global]), ou seja definido por você ([!UICONTROL Client]). |
   | Tipo de dados | Especifica o tipo de dados ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL DateTime]). |
   | Data e hora de criação | Data e hora de criação do campo harmonizado. |
   | Data e hora da última modificação | Data e hora da última modificação do campo harmonizado. |
   | Fórmula | Especifica a fórmula para um campo harmonizado com base em uma categoria derivada. |

   {style="table-layout:auto"}

1. Para pesquisar um campo harmonizado específico, use ![Pesquisar](../assets/icons/Search.svg) **[!UICONTROL *Pesquisar campo harmonizado *]**.




### Adicionar um campo harmonizado

Para adicionar um campo harmonizado, na variável ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** no Mix Modeler:

1. Selecionar ![Adicionar](../assets/icons/AddCircle.svg)Adicionar campo.

1. No **[!UICONTROL Create]** diálogo:

   1. Insira um **[!UICONTROL Field name]**, por exemplo `region`.
   1. Insira um **[!UICONTROL Display name]**, por exemplo `Region`.
   1. Selecione um **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** ou **[!UICONTROL Derived]**.

      Ao selecionar **[!UICONTROL Derived]**, especifique um **[!UICONTROL Formula]**. Para criar uma expressão aritmética válida, combine uma ou mais métricas de **[!UICONTROL Insert Metric]** com um ou mais operadores **[!UICONTROL + - * / ( )]** . Por exemplo, `[orders]/[impressions]`

   1. Selecione um **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** ou **[!UICONTROL DateTime]**, quando Categoria selecionada for Dimension.
      - **[!UICONTROL Number]** ou **[!UICONTROL Currency]** quando a Categoria selecionada é Métrica ou Derivada.

   1. Selecionar **[!UICONTROL Submit]** para adicionar o campo harmonizado. Selecionar **[!UICONTROL Close]** para fechar a caixa de diálogo sem adicionar o campo harmonizado.

      ![Criar um campo](../assets/create-field.png)


### Editar um campo harmonizado

Só é possível editar campos harmonizados criados anteriormente. Não é possível editar um campo harmonizado global.

Para editar um campo harmonizado, na variável ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** no Mix Modeler:

1. Selecione o campo harmonizado que deseja editar. Por exemplo, **[!UICONTROL Region]**.

1. No **[!UICONTROL Edit harmonization values]** , modifique valores para **[!UICONTROL Display name]**, **[!UICONTROL Category]**, e **[!UICONTROL Data type]**.

1. Selecionar **[!UICONTROL Submit]** para aplicar as alterações ao campo harmonizado.

   ![Editar um campo](../assets/edit-field.png)

### Excluir um campo harmonizado

Só é possível excluir campos harmonizados criados anteriormente. Não é possível excluir um campo harmonizado global.

Para excluir um campo harmonizado, na variável ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** no Mix Modeler:

1. Selecione o campo harmonizado que deseja excluir, por exemplo **[!UICONTROL Region]**.

1. Selecionar ![Excluir](../assets/icons/Delete.svg) **[!UICONTROL Delete]** do **[!UICONTROL Edit harmonization values]** painel esquerdo.


