---
title: Regras do conjunto de dados
description: Saiba como definir regras de conjunto de dados para usar como parte da harmonização de seus dados no Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# Regras do conjunto de dados

As regras do conjunto de dados ajudam a mapear os campos harmonizados com campos dos dados assimilados no Mix Modeler.

* Para dados agregados assimilados no Adobe Experience Platform, mapeie um ou mais campos do conjunto de dados disponíveis para os campos harmonizados apropriados.
* Para dados do evento, você pode mapear individualmente um ou mais campos harmonizados para campos do conjunto de dados, diretamente ou usando condições.


## Gerenciar regras do conjunto de dados

Para ver uma tabela das regras do conjunto de dados disponíveis, na interface do Mix Modeler:

1. Selecione ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** no painel esquerdo.

1. Selecione **[!UICONTROL Dataset rules]** na barra superior. Você verá uma tabela das regras do conjunto de dados.

As colunas da tabela especificam detalhes sobre as regras do conjunto de dados:

| Nome da coluna | Detalhes |
| ---------------------- | ----------|
| Conjunto de dados | O nome do conjunto de dados. |
| Fonte | A origem do conjunto de dados: Adobe Analytics, Eventos de experiência, Resumo (agregado) ou Eventos de experiência do consumidor. |
| Esquema | O esquema com o qual o conjunto de dados está em conformidade. Você pode selecionar rapidamente o nome do esquema para abrir o esquema em uma nova guia no editor de esquema no ![Esquema](/help/assets//icons/Schemas.svg) [Esquemas](../ingest-data/schemas.md). |
| Granularidade | A granularidade dos dados no conjunto de dados. Os valores possíveis são Diário, Semanal, Mensal ou Anual. |
| Início da semana | Especifica qual dia da semana é considerado o início de uma nova semana para o conjunto de dados específico. |
| Status | O status do campo: <p><span style="color:gray"> ●</span> Rascunho ou <p><span style="color:green"> ●</span> Ativo |
| Última modificação | Data e hora da última modificação da regra do conjunto de dados. |

{style="table-layout:auto"}

### Criar uma regra de conjunto de dados

Para criar uma regra de conjunto de dados, na interface ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Mix Modeler, selecione **[!UICONTROL Create a dataset rule]** no assistente **[!UICONTROL Dataset rules configuration]**.

Na tela **[!UICONTROL Create]**,

1. Em **[!UICONTROL Dataset details]**, selecione um conjunto de dados de **[!UICONTROL Select dataset]** para iniciar a configuração. Na lista, os conjuntos de dados são categorizados em **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** e **[!UICONTROL Summary]**.

1. Selecione um dia para **[!UICONTROL Start of the week]**.

1. Selecione **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** para **[!UICONTROL Granularity]**.

1. Ao selecionar um conjunto de dados da categoria **[!UICONTROL Summary]**:

   1. Para definir se os dados do conjunto de dados agregam ou substituem os dados existentes, selecione **[!UICONTROL Aggregation]** ou **[!UICONTROL Replacement]** para **[!UICONTROL Data restatement is by]**.

   1. Mapeie cada **[!UICONTROL Available dataset fields]** para o **[!UICONTROL Standard harmonized fields]** correspondente em **[!UICONTROL Map to harmonized fields]**. Se não quiser mapear um campo de conjunto de dados para um campo harmonizado, selecione explicitamente **[!UICONTROL -- None --]**.

   1. Se precisar de um novo campo harmonizado, não disponível na lista, selecione **[!UICONTROL Create New]** para criar um novo campo harmonizado. Você verá a caixa de diálogo conforme descrito em [Adicionar um novo campo harmonizado](fields.md#add-a-harmonized-field).

   1. Quando o mapeamento for concluído para todos os campos da regra, selecione **[!UICONTROL Save as draft]** para salvar uma versão de rascunho da regra ou **[!UICONTROL Save]** para salvar e ativar a regra. Selecione **[!UICONTROL Cancel]** para cancelar a configuração da regra.

      ![Criar regras do conjunto de dados](/help/assets//dataset-create-summary.png)

1. Ao selecionar um conjunto de dados de categoria de evento (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), na caixa abaixo de **[!UICONTROL Map to harmonized fields]**:

   1. Selecione um campo harmonizado de **[!UICONTROL Standard harmonized field]**.

   1. Quando o campo harmonizado selecionado for do tipo métrica:

      1. Selecione **[!UICONTROL Count]** ou **[!UICONTROL Sum]** de **[!UICONTROL Mapping type]**.

      1. Selecione um **[!UICONTROL *campo do conjunto de dados da AEP *]**para o qual você deseja mapear o campo harmonizado por padrão.

   1. Quando o campo selecionado é do tipo dimensão:

      1. Selecione **[!UICONTROL Map Into]** ou **[!UICONTROL Case]** de **[!UICONTROL Mapping type]**.

      1. Ao selecionar **[!UICONTROL Map Into]**, selecione **[!UICONTROL Field]** e **[!UICONTROL *campo do conjunto de dados da AEP *]**ou **[!UICONTROL Value]**e um valor padrão para mapear o campo harmonizado por padrão para o campo do conjunto de dados ou valor inserido.

      1. Ao selecionar **[!UICONTROL Case]**, selecione **[!UICONTROL Field]** e **[!UICONTROL *campo do conjunto de dados da AEP *]**ou **[!UICONTROL Value]**e um valor padrão para mapear o campo harmonizado por padrão para o campo do conjunto de dados ou valor inserido.

         1. Para definir valores explicitamente, você define um ou mais casos, que consistem em uma ou mais condições. Cada condição pode verificar um **[!UICONTROL *campo do conjunto de dados da AEP *]**específico, seja ele **[!UICONTROL Exists]**ou **[!UICONTROL Not Exists]**, seja ele **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**ou **[!UICONTROL Ends With]**um valor inserido em**[!UICONTROL * Inserir valor de entrada *]**.

         1. Para adicionar outro caso, selecione ![Adicionar](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add case]**. Para adicionar outra condição, selecione ![Adicionar](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Para excluir uma ocorrência ou condição, selecione ![Fechar](/help/assets//icons/Close.svg) no contêiner correspondente.

         1. Para selecionar se alguma ou todas as condições devem se aplicar a uma ocorrência, selecione **[!UICONTROL Any of]** ou **[!UICONTROL All of]**.

         1. Para definir o valor de resultado de um caso, insira o valor em **[!UICONTROL Then]**.

      O exemplo abaixo

      * usa um **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** para mapear o campo harmonizado **[!UICONTROL Channel Type At Source]** para o campo **[!UICONTROL channel_type]** do conjunto de dados **[!DNL Luma Transactions]**.

      * usa um **[!UICONTROL Case]** **[!UICONTROL Mapping type]** para mapear condicionalmente o valor do campo **[!UICONTROL marketing.campaignName]** no conjunto de dados **[!DNL Luma Transactions]** para o campo harmonizado **[!UICONTROL Campaign]**. O campo Campaign harmonizado está definido como:

         * `Black Friday` quando **[!UICONTROL marketing.campaignName]** é `_black_friday` ou `BlackFriday`.
         * ao valor de **[!UICONTROL marketing.campaignName]** em todos os outros casos.

        ![Evento de regra do conjunto de dados](/help/assets//dataset-create-event.png)

1. Selecione ![Adicionar](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add field]** para definir campos adicionais.

Quando terminar, selecione **[!UICONTROL Save as draft]** para salvar uma versão de rascunho da regra ou **[!UICONTROL Save]** para salvar e ativar a regra. Selecione **[!UICONTROL Cancel]** para cancelar a configuração da regra.


### Editar uma regra de conjunto de dados

Para editar uma regra de conjunto de dados, na interface ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Mix Modeler:

1. Selecione ![Mais](/help/assets//icons/More.svg) na coluna **[!UICONTROL Dataset]** para a regra de conjunto de dados que você deseja editar.
1. No menu de contexto, selecione ![Editar](/help/assets//icons/Edit.svg) **[!UICONTROL Edit]** para começar a editar a regra do conjunto de dados. Consulte [Criar uma regra de conjunto de dados](#create-a-dataset-rule) para obter mais detalhes.


### Excluir uma regra de conjunto de dados

Para excluir uma regra de conjunto de dados, na interface ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Mix Modeler:

1. Selecione ![Mais](/help/assets//icons/More.svg) na coluna **[!UICONTROL Dataset]** para a regra de conjunto de dados que você deseja excluir.
1. No menu de contexto, selecione ![Excluir](/help/assets//icons/Delete.svg) **[!UICONTROL Delete]** para excluir a regra do conjunto de dados. Será solicitada uma confirmação. Selecione **[!UICONTROL Delete]** para excluir permanentemente a regra de conjunto de dados selecionada.


## Sincronizar dados

Para sincronizar dados entre seus dados harmonizados e os conjuntos de dados de resumo e/ou evento, siga toda a lógica nas regras do conjunto de dados:

1. Selecione **[!UICONTROL Sync data]**.

1. Na caixa de diálogo **[!UICONTROL Sync data for dataset rules]**, selecione
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]** ou
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Para iniciar a sincronização com base nas regras do conjunto de dados definido entre os dados harmonizados e os dados em conjuntos de dados, selecione **[!UICONTROL Sync]**. Para cancelar a sincronização, selecione **[!UICONTROL Cancel]**.

   ![Sincronizar dados](/help/assets//sync-data.png)


## Preferências de mesclagem de dados

>[!NOTE]
>
>[!BADGE beta]{type=Informative}

As preferências de mesclagem de dados ajudam a resolver conflitos quando os dados de fontes de dados resumidas e de eventos são mesclados. Os casos de uso são:

* a mesma métrica de publicidade é medida e relatada em vários conjuntos de dados, ou
* a medição de métricas pode estar incompleta em alguns conjuntos de dados, enquanto outro conjunto de dados pode ser um superconjunto de uma métrica específica, resultando em dupla contagem.

Para garantir previsões de modelo precisas, é possível definir preferências de mesclagem de dados:

1. Selecione ![Preferências de mesclagem de dados](/help/assets//icons/Merge.svg) [!BADGE beta].

1. No **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative}

   ![Preferências de mesclagem de dados](/help/assets//data-merge-preferences.png)

   * Selecione um **[!UICONTROL Default metric preference]**. A preferência de métrica padrão selecionada é aplicada quando, durante a harmonização, várias fontes de dados atualizam um campo de métrica para um determinado canal. A preferência é aplicada no nível da sandbox, a menos que seja substituída por preferências específicas baseadas em métricas. Você pode selecionar entre **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** e **[!UICONTROL Sum of summmary and event data]**.

   * Para adicionar preferências específicas baseadas em métricas:

      1. Selecione ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Selecione uma métrica na lista **[!UICONTROL *Seleção de métrica *]**.
         1. Selecione **[!UICONTROL CHANNELS]** ou **[!UICONTROL CONVERSION TYPES]**. Na lista, selecione **[!UICONTROL All]**, um canal específico ou um tipo de conversão.
         1. Selecione **[!UICONTROL Summary]** ou **[!UICONTROL Event]** para especificar se os dados de resumo ou os dados de evento são preferidos para a métrica (e para todos ou para o canal selecionado) ao mesclar os dados.

         Para adicionar um ou mais canais ou tipos de conversão adicionais:

         1. Selecione ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a channel]** ou ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Selecione **[!UICONTROL Summary]** ou **[!UICONTROL Event]**.

         Para excluir um canal ou tipo de conversão, selecione ![Cruz](/help/assets//icons/Close.svg).

      1. Para adicionar preferências mais específicas baseadas em métricas, repita a etapa anterior.

   * Para excluir uma preferência baseada em métrica específica existente, selecione ![Excluir](/help/assets//icons/Delete.svg).

1. Selecione **[!UICONTROL Save]** para salvar as preferências de mesclagem de dados. Uma ressincronização dos dados é iniciada. <br/>Selecione **[!UICONTROL Cancel]** para cancelar.


## Controle de acesso em nível de campo

Ao configurar regras de conjunto de dados para conjuntos de dados harmonizados, o controle de acesso baseado em [atributo](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) do Experience Platform é aplicado em nível de campo. Um campo é restrito quando um rótulo é anexado a um campo de esquema e uma política ativa é ativada, negando acesso a esse campo. Como resultado:

* você não vê os campos de esquema restritos ao criar uma regra de conjunto de dados,
* não é possível exibir ou editar o mapeamento de um ou mais campos de esquema restritos para você. Ao editar ou exibir uma regra de conjunto de dados contendo esses campos restritos, você verá a tela a seguir.
  ![Ação não permitida](/help/assets//action-not-permitted.png)
