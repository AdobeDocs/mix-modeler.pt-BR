---
title: Regras do conjunto de dados
description: Saiba como definir regras de conjunto de dados para usar como parte da harmonização de seus dados no Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: b631cf8d06fe71d9f5ca547923eb3237c677a915
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 0%

---

# Regras do conjunto de dados

As regras do conjunto de dados ajudam a mapear os campos harmonizados com campos a partir dos dados assimilados no Mix Modeler.

* Para dados agregados assimilados no Adobe Experience Platform, mapeie um ou mais campos do conjunto de dados disponíveis para os campos harmonizados apropriados.
* Para dados do evento, você pode mapear individualmente um ou mais campos harmonizados para campos do conjunto de dados, diretamente ou usando condições.


## Gerenciar regras do conjunto de dados

Para ver uma tabela das regras do conjunto de dados disponíveis, na interface do Mix Modeler:

1. Selecione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** no painel esquerdo.

1. Selecione **[!UICONTROL Dataset rules]** na barra superior. Você verá uma tabela das regras do conjunto de dados.

Você pode pesquisar um conjunto de dados rapidamente usando a ![Pesquisa](/help/assets/icons/Search.svg) **[!UICONTROL _Inserir um nome para o conjunto de dados_]**.

As colunas da tabela especificam detalhes sobre as regras do conjunto de dados:

| Nome da coluna | Detalhes |
| ---------------------- | ----------|
| Conjunto de dados | O nome do conjunto de dados.  Use ![Mais](/help/assets/icons/More.svg) para selecionar ações para um conjunto de dados. É possível:<ul><li>![Visualizar](/help/assets/icons/Preview.svg) **[!UICONTROL View]** para exibir a configuração das regras do conjunto de dados. Todos os campos estão desativados.</li><li>![Edite](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** para editar a configuração de regras do conjunto de dados.</li><li>![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para excluir a configuração de regras do conjunto de dados. Você será solicitado a confirmar a exclusão na caixa de diálogo Excluir conjunto de dados. Selecione **[!UICONTROL Delete]** para excluir a configuração da regra do conjunto de dados permanentemente.</li><ul> |
| Fonte | A origem do conjunto de dados: Adobe Analytics, Eventos de experiência, Resumo (agregado) ou Eventos de experiência do consumidor. |
| Esquema | O esquema com o qual o conjunto de dados está em conformidade. Você pode selecionar rapidamente o nome do esquema para abrir o esquema em uma nova guia no editor de esquema no ![Esquema](/help/assets/icons/Schemas.svg) [Esquemas](../ingest-data/schemas.md). |
| Granularidade | A granularidade dos dados no conjunto de dados. Os valores possíveis são Diário, Semanal, Mensal ou Anual. |
| Início da semana | Especifica qual dia da semana é considerado o início de uma nova semana para o conjunto de dados específico. |
| Status | O status do campo: <p><span style="color:gray">●</span> Rascunho ou <p><span style="color:green">●</span> Ativo |
| Última modificação | Data e hora da última modificação da regra do conjunto de dados. |

{style="table-layout:auto"}

### Criar uma regra de conjunto de dados

Para criar uma regra de conjunto de dados, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Mix Modeler, selecione **[!UICONTROL Create a dataset rule]** no assistente **[!UICONTROL Dataset rules configuration]**.

Na tela **[!UICONTROL Create]**,

1. Em **[!UICONTROL Dataset details]**, selecione um conjunto de dados de **[!UICONTROL Select dataset]** para iniciar a configuração. Na lista, os conjuntos de dados são categorizados em **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** e **[!UICONTROL Summary]**.

1. Selecione um dia para **[!UICONTROL Start of the week]**.

1. Selecione **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** ou **[!UICONTROL Yearly]** para **[!UICONTROL Granularity]**.

1. Ao selecionar um conjunto de dados da categoria **[!UICONTROL Summary]**, selecione **[!UICONTROL Aggregation]** ou **[!UICONTROL Replacement]** para **[!UICONTROL Data restatement is by]**.

   Os dados de relatórios dos editores são muito importantes para os analistas de marketing, pois trabalhar com editores geralmente implica gastos significativos, e as alterações nos dados de relatórios podem resultar em insights e planos de investimento muito diferentes. Além disso, os analistas de marketing precisam de dados precisos para obter os insights certos e apresentar propostas convincentes para ganhar a confiança das partes interessadas. No entanto, esses editores, como Google e Facebook, geralmente reafirmam ou excluem dados de relatórios à medida que reconciliam seus dados. O período para a maioria das alterações ocorre dentro de 7 dias do desempenho da mídia relatado. São possíveis alterações adicionais nos dados no prazo de 30 dias. Em geral, após 30 dias, os livros são considerados fechados e os dados são concluídos.

   O Mix Modeler oferece suporte à redeclaração de dados. Para garantir que os dados usados para relatórios, modelagem e planejamento sejam precisos. E que os dados são capazes de suportar as expectativas e necessidades da marca e do analista de marketing.

   Você pode enviar linhas reexpressas de dados de resumo como linhas incrementais em um conjunto de dados do Experience Platform, e o serviço de harmonização atualiza o conjunto de dados harmonizado com esses dados reexpressos. Da mesma forma, também é possível remover linhas de dados de resumo que precisam ser refletidas no serviço de harmonização.

1. Na seção **[!UICONTROL Map to harmonized fields]**:

   1. Selecione um campo harmonizado de **[!UICONTROL Standard harmonized field]**.

   1. Quando o campo harmonizado selecionado for do tipo métrica:

      1. Selecione **[!UICONTROL Count]** ou **[!UICONTROL Sum]** de **[!UICONTROL Mapping type]**.

      1. Selecione um **[!UICONTROL *campo do conjunto de dados do AEP *]**&#x200B;para o qual você deseja mapear o campo harmonizado por padrão.

   1. Quando o campo selecionado é do tipo dimensão:

      1. Selecione **[!UICONTROL Map Into]** ou **[!UICONTROL Case]** de **[!UICONTROL Mapping type]**.

      1. Ao selecionar **[!UICONTROL Map Into]**, selecione **[!UICONTROL Field]** e **[!UICONTROL *campo do conjunto de dados do AEP *]**&#x200B;ou **[!UICONTROL Value]**&#x200B;e um valor padrão para mapear o campo harmonizado por padrão para o campo do conjunto de dados ou valor inserido.

      1. Ao selecionar **[!UICONTROL Case]**, selecione **[!UICONTROL Field]** e **[!UICONTROL *campo do conjunto de dados do AEP *]**&#x200B;ou **[!UICONTROL Value]**&#x200B;e um valor padrão para mapear o campo harmonizado por padrão para o campo do conjunto de dados ou valor inserido.

         1. Para definir valores explicitamente, você define um ou mais casos, que consistem em uma ou mais condições. Cada condição pode verificar um **[!UICONTROL *campo do conjunto de dados do AEP *]**&#x200B;específico, seja ele **[!UICONTROL Exists]**&#x200B;ou **[!UICONTROL Not Exists]**, seja ele **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**&#x200B;ou **[!UICONTROL Ends With]**&#x200B;um valor inserido em&#x200B;**[!UICONTROL * Inserir valor de entrada *]**.

         1. Para adicionar outro caso, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]**. Para adicionar outra condição, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Para excluir uma ocorrência ou condição, selecione ![Fechar](/help/assets/icons/Close.svg) no contêiner correspondente.

         1. Para selecionar se alguma ou todas as condições devem se aplicar a uma ocorrência, selecione **[!UICONTROL Any of]** ou **[!UICONTROL All of]**.

         1. Para definir o valor de resultado de um caso, insira o valor em **[!UICONTROL Then]**.

      O exemplo abaixo

      * usa um **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** para mapear o campo harmonizado **[!UICONTROL Channel Type At Source]** para o campo **[!UICONTROL channel_type]** do conjunto de dados **[!DNL Luma Transactions]**.

      * usa um **[!UICONTROL Case]** **[!UICONTROL Mapping type]** para mapear condicionalmente o valor do campo **[!UICONTROL marketing.campaignName]** no conjunto de dados **[!DNL Luma Transactions]** para o campo harmonizado **[!UICONTROL Campaign]**. O campo Campaign harmonizado está definido como:

         * `Black Friday` quando **[!UICONTROL marketing.campaignName]** é `_black_friday` ou `BlackFriday`.
         * ao valor de **[!UICONTROL marketing.campaignName]** em todos os outros casos.

        ![Evento de regra do conjunto de dados](/help/assets/dataset-create-event.png)

      Ao mapear um campo harmonizado padrão a partir de um conjunto de dados de resumo, o Mix Modeler tenta deduzir o campo do conjunto de dados do Experience Platform correspondente. Quando bem-sucedido:

      * Se o campo for do tipo dimensão, **[!UICONTROL Map into]** será selecionado como **[!UICONTROL Mapping type]**.
      * Se o campo for do tipo métrica, **[!UICONTROL Sum]** será selecionado como **[!UICONTROL Mapping type]**.
      * **[!UICONTROL Field]** está selecionado como o tipo de mapeamento **[!UICONTROL Default]**.
      * O campo correspondente do conjunto de dados do Experience Platform é inserido automaticamente para *Campo do conjunto de dados do AEP*.

      Você pode alterar qualquer um dos valores propostos se eles estiverem incorretos ou não forem compatíveis com seu caso de uso específico.

1. Selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** para definir campos adicionais.

Quando terminar, selecione **[!UICONTROL Save as draft]** para salvar uma versão de rascunho da regra ou **[!UICONTROL Save]** para salvar e ativar a regra. Selecione **[!UICONTROL Cancel]** para cancelar a configuração da regra.

>[!NOTE]
>
>A experiência **[!UICONTROL Map to harmonized fields]** dedicada às regras de conjuntos de dados de resumo está obsoleta. Todas as regras do conjunto de dados agora usam experiência **[!UICONTROL Map to harmonized fields]** semelhante, independentemente do tipo de conjunto de dados. Para conjuntos de dados de resumo para os quais você definiu regras usando a experiência **[!UICONTROL Map to harmonized fields]** obsoleta, talvez você queira verificar essas regras em relação à experiência **[!UICONTROL Map to harmonized field]** genérica.
>



### Editar uma regra de conjunto de dados

Para editar uma regra de conjunto de dados, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Mix Modeler:

1. Selecione ![Mais](/help/assets/icons/More.svg) na coluna **[!UICONTROL Dataset]** para a regra de conjunto de dados que você deseja editar.
1. No menu de contexto, selecione ![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** para começar a editar a regra do conjunto de dados. Consulte [Criar uma regra de conjunto de dados](#create-a-dataset-rule) para obter mais detalhes.


### Excluir uma regra de conjunto de dados

Para excluir uma regra de conjunto de dados, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** no Mix Modeler:

1. Selecione ![Mais](/help/assets/icons/More.svg) na coluna **[!UICONTROL Dataset]** para a regra de conjunto de dados que você deseja excluir.
1. No menu de contexto, selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para excluir a regra do conjunto de dados. Será solicitada uma confirmação. Selecione **[!UICONTROL Delete]** para excluir permanentemente a regra de conjunto de dados selecionada.



## Sincronizar dados

Para sincronizar dados entre seus dados harmonizados e os conjuntos de dados de resumo e/ou evento ao aplicar a lógica nas regras do conjunto de dados:

1. Selecione **[!UICONTROL Sync data]**.

1. Na caixa de diálogo **[!UICONTROL Sync data for dataset rules]**, selecione
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]** ou
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Para iniciar a sincronização com base nas regras do conjunto de dados definido entre os dados harmonizados e os dados em conjuntos de dados, selecione **[!UICONTROL Sync]**. Para cancelar a sincronização, selecione **[!UICONTROL Cancel]**.

   ![Sincronizar dados](/help/assets/sync-data.png)


## Preferências de mesclagem de dados

>[!NOTE]
>
>[!BADGE beta]{type=Informative} As preferências de mesclagem de dados são um recurso beta e sua funcionalidade está sujeita a alterações.

Para garantir previsões de modelo precisas, é possível definir preferências de mesclagem de dados. Essa funcionalidade permite que os usuários resolvam quaisquer conflitos após a mesclagem do nível de resumo e dos dados do nível de evento.

Você pode configurar uma preferência de métrica padrão a ser aplicada em casos de atualizações conflitantes. Essa métrica padrão pode ser uma das três opções:

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

Quando, durante a harmonização, várias fontes de dados tentam atualizar um campo de métrica para um determinado canal, a preferência padrão configurada pelo usuário é aplicada. Essa preferência é aplicada no nível da sandbox, a menos que seja substituída por determinadas preferências baseadas em métricas configuradas adicionalmente.

Em **[!UICONTROL Metric based preferences]**, o usuário pode configurar a origem específica (**[!UICONTROL Summary]** ou **[!UICONTROL Event]**) de uma determinada métrica e o tipo de conversão correspondente para essa métrica.

Os casos de uso típicos são:

* a mesma métrica de publicidade é medida e relatada em vários conjuntos de dados, ou
* a medição de métricas pode estar incompleta em alguns conjuntos de dados, enquanto outro conjunto de dados pode ser um superconjunto de uma métrica específica, resultando em dupla contagem.

### Configurar 

Para configurar as preferências de mesclagem de dados:


1. Selecione ![Preferências de mesclagem de dados](/help/assets/icons/Merge.svg) [!BADGE beta].

1. No **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative} diálogo:

   ![Preferências de mesclagem de dados](/help/assets/data-merge-preferences.png)

   * Selecione um **[!UICONTROL Default metric preference]**. A preferência de métrica padrão selecionada é aplicada quando, durante a harmonização, várias fontes de dados atualizam um campo de métrica para um determinado canal. A preferência é aplicada no nível da sandbox, a menos que seja substituída por preferências específicas baseadas em métricas. Você pode selecionar entre **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** e **[!UICONTROL Sum of summary and event data]**.

   * Para adicionar preferências específicas baseadas em métricas:

      1. Selecione ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Selecione uma métrica na lista **[!UICONTROL *Seleção de métrica *]**.
         1. Selecione **[!UICONTROL CHANNELS]** ou **[!UICONTROL CONVERSION TYPES]**. Na lista, selecione **[!UICONTROL All]**, um canal específico ou um tipo de conversão.
         1. Selecione **[!UICONTROL Summary]** ou **[!UICONTROL Event]** para especificar se os dados de resumo ou os dados de evento são preferidos para a métrica (e para todos ou para o canal selecionado) ao mesclar os dados.

         Para adicionar um ou mais canais ou tipos de conversão adicionais:

         1. Selecione ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** ou ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Selecione **[!UICONTROL Summary]** ou **[!UICONTROL Event]**.

         Para excluir um canal ou tipo de conversão, selecione ![Cruz](/help/assets/icons/Close.svg).

      1. Para adicionar preferências mais específicas baseadas em métricas, repita a etapa anterior.

   * Para excluir uma preferência baseada em métrica específica existente, selecione ![Excluir](/help/assets/icons/Delete.svg).

1. Selecione **[!UICONTROL Save]** para salvar as preferências de mesclagem de dados. Uma ressincronização dos dados é iniciada. <br/>Selecione **[!UICONTROL Cancel]** para cancelar.

## Excluir um conjunto de dados de origem

Ao excluir um conjunto de dados de origem que é usado em seus dados harmonizados, as entradas subjacentes nesse conjunto de dados de origem são removidas do [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md). No entanto, a regra de conjunto de dados com o conjunto de dados de origem excluído permanece na lista de configuração de regra de conjunto de dados com um ícone ![DataRemove](/help/assets/icons/DataRemove.svg) indicando que o conjunto de dados de origem foi excluído. Para obter mais detalhes:

* Selecione ![Mais](/help/assets/icons/More.svg) e ![Visualizar](/help/assets/icons/Preview.svg) **[!UICONTROL View]** no menu de contexto.
A caixa de diálogo **[!UICONTROL Dataset rule mapping - Fields]** exibe informações sobre o conjunto de dados de origem excluído e os campos usados na configuração da regra do conjunto de dados.

Ao retornar à configuração do **[!UICONTROL Dataset rules]**, você verá uma caixa de diálogo explicando que um ou mais conjuntos de dados de origem foram excluídos. Os dados harmonizados são afetados em uma próxima sincronização ad hoc ou agendada. Revise a configuração da regra do conjunto de dados.

Os dados harmonizados são atualizados sem os dados de origem excluídos na próxima sincronização ad hoc ou sincronização agendada. No entanto, você continua vendo caixas de diálogo de alerta que solicitam a exclusão da regra de conjunto de dados com base no conjunto de dados de origem excluído. Esse alerta permite que os usuários visualizem e avaliem os campos afetados no conjunto de dados excluído. E para determinar o impacto nos pontos de contato ou conversões de marketing que podem ser usados em qualquer modelo. Depois de revisar e atenuar esse impacto, você deve excluir a regra do conjunto de dados da lista de configuração de regras do conjunto de dados.
