---
title: Visão geral dos modelos
description: Saiba como criar e usar modelos no Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 4a154ec4c81cb6b2361a05440c56b7946f748d8c
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 0%

---

# Visão geral dos modelos

A funcionalidade do modelo no Mix Modeler permite configurar, treinar e pontuar modelos específicos para seus objetivos comerciais. O treinamento e a pontuação oferecem suporte ao aprendizado de transferência orientado por IA entre a atribuição multitoque e a modelagem de mix de marketing.

Os modelos são baseados nos dados harmonizados que você cria como parte do fluxo de trabalho do aplicativo do Mix Modeler.

Um modelo no Mix Modeler é um modelo de aprendizado de máquina empregado para medir e prever um resultado especificado com base nos investimentos de um profissional de marketing. Pontos de contato de marketing e dados de nível de resumo podem ser usados como uma entrada. O Mix Modeler permite criar variantes de modelos com base em diferentes conjuntos de variáveis, dimensões e resultados, como receitas, unidades vendidas e clientes potenciais.

Um modelo requer:

* Uma conversão.
* Um ou mais pontos de contato de marketing (canais) compostos de dados de nível de resumo, dados de pontos de contato de marketing (dados do evento) ou ambos.
* Uma janela de pesquisa configurável.
* Uma janela de treinamento configurável.

Um modelo pode incluir opcionalmente:

* Fatores externos.
* Fatores internos.
* Conhecimento prévio das contribuições de marketing de outras fontes, como experiência anterior das partes interessadas, testes incrementais e outros modelos.
* Gastar compartilhamento, que usa compartilhamento de gasto relativo como proxy quando os dados de marketing são escassos.

Quando um modelo é criado pela primeira vez, a criação inicia imediatamente o processo de treinamento e pontuação. Após a conclusão da execução inicial de treinamento e pontuação, os insights do modelo estarão disponíveis para revisão. Um modelo pode ser treinado novamente posteriormente. Além disso, dados podem ser adicionados ao modelo, o que requer que você reclassifique o modelo manualmente. O novo treinamento e a nova pontuação são um processo iterativo à medida que surgem novas descobertas e informações, e são necessários ajustes para obter um modelo mais adequado aos seus objetivos de negócios.


## Criar modelos

Para criar um modelo, use o fluxo de configuração de modelo guiado passo a passo da Mix Modeler disponível ao selecionar **[!UICONTROL Open model canvas]**. Consulte [Criar modelos](build.md) para obter mais detalhes.

## Gerenciar modelos

Para exibir uma tabela dos modelos atuais, na interface do Mix Modeler:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Você verá uma tabela dos modelos atuais.

   As colunas da tabela especificam detalhes sobre o modelo.

   | Nome da coluna | Detalhes |
   |---|---|
   | Nome | Nome do modelo |
   | Descrição | Descrição do modelo |
   | Evento de conversão | A conversão selecionada para o modelo. |
   | Frequência de execução | A frequência de execução do treinamento do modelo. |
   | Última execução | A data e hora do último treinamento do modelo. |
   | Status | O status do modelo. |

   {style="table-layout:auto"}

   O status relatado do modelo depende de onde um modelo está em seu ciclo de vida. Por exemplo, se um modelo é criado, (re)treinado com sucesso ou não, ou (re)pontuado com sucesso ou não.

   Na tabela abaixo:

   * ![Marca de seleção](/help/assets/icons/Checkmark.svg) - indica uma execução bem-sucedida de uma etapa no ciclo de vida do modelo.
   * ![Relógio](/help/assets/icons/Clock.svg) - indica uma execução em andamento atual de uma etapa no ciclo de vida do modelo.
   * ![Fechar](/help/assets/icons/Close.svg) - indica uma falha na execução de uma etapa no ciclo de vida do modelo.

   | Status | Criar | Treinamento | Pontuação | Treinar novamente | Re-pontuação |
   |---|:---:|:---:|:---:|:---:|:---:|
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | | | | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) | | | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) | | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) |
   | Falha no treinamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) | | | |
   | Falha no treinamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) | |
   | Treinamento bem-sucedido | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | | | |
   | Treinamento bem-sucedido | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | |
   | Falha na pontuação | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) | | |
   | Falha na pontuação | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) |
   | Pontuação bem-sucedida | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | | |
   | Pontuação bem-sucedida | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) |

1. Para alterar as colunas exibidas para a lista, selecione ![Configurações de coluna](/help/assets/icons/ColumnSetting.svg) e alterne as colunas em ![Verificar](/help/assets/icons/Checkmark.svg) ou desativar.

Você pode executar as seguintes ações em um modelo específico.

### Insights do modelo

A funcionalidade de insights do modelo só está disponível em modelos treinados e pontuados com êxito.

Para exibir os insights de um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione o nome do modelo.

Você foi redirecionado para [Informações sobre Modelos](insights.md).


### Exibir detalhes

Para exibir mais detalhes de um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Informações](/help/assets/icons/Info.svg) para que um modelo mostre um pop-up com detalhes.


### Duplicar

É possível duplicar um modelo rapidamente.

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Duplicate]**.

Você é redirecionado para as etapas de criação de um novo modelo, com um nome proposto composto pelo nome do modelo original anexado com **[!UICONTROL (Copy)](_n_)**.

### Editar

É possível editar o nome, a descrição e a programação de treinamento e pontuação de um modelo.

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Edit]**.

   No diálogo **[!UICONTROL Edit model]**:

   * Insira um(a) novo(a) **[!UICONTROL Name]** e **[!UICONTROL Description]**.

   * Para habilitar o agendamento, habilite **[!UICONTROL Status]**. Você só pode habilitar a programação para modelos treinados e pontuados.

      1. Selecione um **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: Insira uma hora válida (por exemplo `05:22 pm`) ou use ![Clock](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: Selecione um dia da semana e insira um horário válido (por exemplo `05:22 pm`) ou use ![Relógio](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: Selecione um dia do mês no menu suspenso Executar em cada e insira um horário válido (por exemplo `05:22 pm`) ou use ![Relógio](/help/assets/icons/Clock.svg).

      1. Selecione um **[!UICONTROL Training frequency]** no menu suspenso: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

     ![Editar um modelo](../assets/model-edit.png)

1. Selecione **[!UICONTROL Save]**.



### Treinar novamente


Treinar novamente um modelo só está disponível em modelos treinados com êxito.

Considere treinar novamente um modelo quando quiser:

* Inclua novos dados de marketing incremental e de fatores. Por exemplo, durante o último trimestre, a dinâmica do mercado mudou ou sua distribuição de dados de marketing mudou significativamente.

Para treinar novamente um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Train]**. Como alternativa, selecione ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** na barra de ação azul.

   Na caixa de diálogo **[!UICONTROL Train model]**, selecione a opção para:

   * **[!UICONTROL Train model with last 2 years of marketing data]** ou
   * **[!UICONTROL Train model using specific date range of data]**.
Especifique o intervalo de datas. Você pode usar o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de datas. Você deve selecionar um intervalo de dados com no mínimo um ano.

   ![Treinar novamente um modelo](../assets/re-train-model.png)

1. Selecione **[!UICONTROL Train]** para treinar novamente o modelo.


### Pontuação ou repontuação


Você pode pontuar incrementalmente um modelo com base em novos dados de marketing ou repontuar um modelo para um intervalo de datas específico.

Considere pontuar novamente um modelo quando quiser:

* Corrija dados de marketing incorretos. Por exemplo, os dados de pesquisa paga recentes incluídos no treinamento e na pontuação do modelo perderam uma semana de dados.
* Use os novos dados de marketing incrementais que se tornaram disponíveis por meio de atualizações nos conjuntos de dados configurados como parte de seus dados harmonizados.

Para pontuar ou repontuar um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Score]**. Como alternativa, selecione ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** na barra de ação azul.

   Na caixa de diálogo **[!UICONTROL Score marketing data]**, selecione a opção para:

   * **[!UICONTROL Score new marketing data from *mm/dd/aaaa *]**, para pontuar seu modelo de forma incremental usando novos dados de marketing, ou
   * **[!UICONTROL Score specific date range of marketing data]** para pontuar novamente para um intervalo de datas específico.
Especifique o intervalo de datas. Você pode usar o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de datas.

   ![Treinar novamente um modelo](../assets/re-score-model.png)

1. Selecione **[!UICONTROL Score]**. Ao pontuar novamente um modelo usando um intervalo de dados específico, você verá uma caixa de diálogo **[!UICONTROL Existing model is replaced]**, solicitando a confirmação para substituir o modelo por novas pontuações para o intervalo de datas selecionado. Selecione **[!UICONTROL Replace model]** para confirmar.


### Excluir modelos

Para excluir um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.
1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Delete]**. Como alternativa, selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** da barra de ação azul.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete model]** para excluir o modelo. Selecione **[!UICONTROL Cancel]** para cancelar.

Para excluir vários modelos:

1. Selecione vários modelos.
1. Na barra de ação azul, selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para excluir os modelos.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete *x *modelos]**para excluir os modelos. Selecione **[!UICONTROL Cancel]**para cancelar.

