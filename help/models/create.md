---
title: Criar um modelo
description: Saiba como criar um modelo no Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Criar um modelo

Para criar um modelo, na interface ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no Mix Modeler, selecione **[!UICONTROL Open model canvas]**.

Para criar modelos alimentados por IA personalizada, a interface fornece um fluxo de configuração de modelo guiado passo a passo.

1. Na etapa **[!UICONTROL Setup]**:

   1. Insira seu modelo **[!UICONTROL Name]**, por exemplo `Demo model`. Digite um **[!UICONTROL Description]**, por exemplo `Demo model to explore AI featues of Mix Modeler`.

      ![Nome e descrição do modelo](/help/assets/model-name-description.png)

   1. Selecione **[!UICONTROL Next]** para continuar com a próxima etapa. Selecione **[!UICONTROL Cancel]** para cancelar a configuração do modelo.

1. Na etapa **[!UICONTROL Configure]**:

   1. Na seção **[!UICONTROL Conversion goal]**, no contêiner:

      1. Digite um **[!UICONTROL Conversion name]** para a conversão, por exemplo `Conversion`

      1. Selecione uma conversão de **[!UICONTROL *Selecionar campo harmonizado *]**, contendo as conversões disponíveis que você definiu como parte de [Conversões](../harmonize-data/conversions.md) em [!UICONTROL Harmonized datasets]. Por exemplo,**[!UICONTROL Online Conversion]**.

      1. Você pode selecionar ![Responder](/help/assets/icons/Reply.svg) **[!UICONTROL Create new conversion]** para criar uma conversão diretamente de dentro da configuração do modelo.

         ![Modelo - etapa de conversão](/help/assets/model-conversion-step.png)

   1. Na seção **[!UICONTROL Marketing touchpoints]**, você verá vários contêineres de ponto de contato de marketing, correspondentes aos pontos de contato de marketing definidos como parte dos [Pontos de contato de marketing](../harmonize-data/marketing-touchpoints.md) em [!UICONTROL Harmonized datasets].

      * Para cada recipiente:

         1. Você pode modificar o **[!UICONTROL Marketing touchpoint name]**.

         1. Selecione um ponto de contato de marketing a partir de **[!UICONTROL _Selecionar ponto de contato de marketing_]**.

         1. Você pode selecionar ![Responder](/help/assets/icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** para criar um ponto de contato de marketing diretamente de dentro da configuração do modelo.

      * Para adicionar um contêiner de ponto de contato de marketing, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * Para remover um contêiner de ponto de contato de marketing, no contêiner, selecione ![Mais](/help/assets/icons/More.svg) e selecione **[!UICONTROL Remove container]** no menu de contexto.

        ![Modelo - etapa de pontos de contato de marketing](/help/assets/model-marketing-touchpoint-step.png)

   1. Por padrão, uma pontuação é gerada para todos os dados na visualização harmonizada. Para pontuar apenas um subconjunto da população, defina um ou mais filtros usando containers na seção **[!UICONTROL Eligible data population]**.

      * Para cada container, defina um ou mais eventos.

         1. Para cada evento:

            1. Selecione uma métrica ou dimensão em **[!UICONTROL _Selecionar campo harmonizado_]**.

            1. Selecione o operador apropriado: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** ou **[!UICONTROL is not in]**.

            1. Insira ou selecione um valor em **[!UICONTROL _Insira ou selecione o valor_]**.

         1. Para adicionar outro evento ao contêiner, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. Para remover um evento do container, selecione ![Fechar](/help/assets/icons/Close.svg).

         1. Para filtrar usando todos ou alguns dos vários eventos definidos no container, selecione **[!UICONTROL Any of]** ou **[!UICONTROL All of]**. O rótulo foi alterado de **[!UICONTROL Include ... Or ...]** para **[!UICONTROL Include ... And ...]**.

      * Para adicionar um contêiner de preenchimento de dados qualificado, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

      * Para remover um contêiner de preenchimento de dados qualificado, no contêiner, selecione ![Mais](/help/assets/icons/More.svg) e selecione **[!UICONTROL Remove marketing touchpoint]** no menu de contexto.

        ![Modelo - População de dados qualificada](/help/assets/model-eligible-data-population-step.png)

   1. Para adicionar conjuntos de dados contendo fatores externos ao seu modelo, use um ou mais contêineres na seção **[!UICONTROL External factors dataset]**.

      * Para cada recipiente:

         1. Insira um **[!UICONTROL Factor name]** em **[!UICONTROL _Inserir fator_]**.

         1. Selecione um conjunto de dados de **[!UICONTROL _Selecione um conjunto de dados_]**. Você pode selecionar ![Dados](/help/assets/icons/Data.svg) para gerenciar conjuntos de dados. Consulte [Conjuntos de dados](../ingest-data/datasets.md) para obter mais informações.

      * Para adicionar outro contêiner de conjunto de dados de fatores externos, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * Para remover um contêiner de conjunto de dados de fatores externos, no contêiner, selecione ![Mais](/help/assets/icons/More.svg) e selecione **[!UICONTROL Remove external factor]** no menu de contexto.

        ![Modelo - Conjunto de dados de fatores externos](/help/assets/model-external-factors-dataset-step.png)


   1. Para adicionar conjuntos de dados contendo fatores internos ao seu modelo, use um ou mais contêineres na seção **[!UICONTROL Internal factors dataset]**.

      * Para cada recipiente:

         1. Insira um **[!UICONTROL Factor name]** em **[!UICONTROL _Inserir fator_]**.

         1. Selecione um conjunto de dados de **[!UICONTROL _Selecione um conjunto de dados_]**. Você pode selecionar ![Dados](/help/assets/icons/Data.svg) para gerenciar conjuntos de dados. Consulte [Conjuntos de dados](../ingest-data/datasets.md) para obter mais informações.

      * Para adicionar outro contêiner do conjunto de dados de fatores internos, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * Para remover um contêiner adicional do conjunto de dados de fatores internos, no contêiner, selecione ![Mais](/help/assets/icons/More.svg) e **[!UICONTROL Remove internal factor]** no menu de contexto.

        ![Modelo - Conjunto de dados de fatores internos](/help/assets/model-internal-factors-dataset-step.png)

   1. Para definir a janela de pesquisa do modelo, insira um valor entre `1` e `52` em **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

   1. Selecione **[!UICONTROL Next]** para continuar com a próxima etapa. Se forem necessárias mais configurações, um contorno vermelho e um texto explicarão qual configuração adicional será necessária. <br/>Selecione **[!UICONTROL Back]** para voltar à etapa anterior. <br/>Selecione **[!UICONTROL Cancel]** para cancelar a configuração do modelo.

1. Na etapa **[!UICONTROL Advanced]**:

   1. Na seção **[!UICONTROL Define training window]**, selecione entre

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** e

      * **[!UICONTROL Manually input a training window]**. Quando selecionado, defina o número de anos em **[!UICONTROL Include events the following years prior to a conversion]**.

        ![Modelo - Definir janela de treinamento](/help/assets/model-define-training-window.png)

   1. Na seção **[!UICONTROL Spend share]**:

      * Para usar taxas históricas de investimento em marketing para informar o modelo quando os dados de marketing são escassos, ative **[!UICONTROL Allow spend share]**.

   1. Na seção **[!UICONTROL Prior knowledge]**:

      1. Selecione o **[!UICONTROL Rule type]**.

      1. Especifique porcentagens de contribuição para qualquer um dos canais listados em **[!UICONTROL Name]**, usando a coluna **[!UICONTROL Contribution proportion]**.

      1. Quando apropriado, você pode adicionar uma porcentagem de **[!UICONTROL Level of confidence]** para cada canal.

      1. Quando necessário, use **[!UICONTROL Clear all]** para limpar todos os valores de entrada para as colunas **[!UICONTROL Contribution proportion]** e **[!UICONTROL Level of confidence]**.

         ![Modelo - Conhecimento anterior](/help/assets/model-prior-knowledge-step.png)

1. Selecione **[!UICONTROL Finish]** para concluir a configuração do modelo.

   * Na caixa de diálogo **[!UICONTROL Create instance?]**, selecione **[!UICONTROL Ok]** para acionar o primeiro conjunto de treinamentos e execuções de pontuação imediatamente. Seu modelo está listado com o status <span style="color:orange"> ●</span> **[!UICONTROL Awaiting training]**.

     Selecione **[!UICONTROL Cancel]** para cancelar.

   * Se forem necessárias mais configurações, um contorno vermelho e um texto explicarão qual configuração adicional será necessária.

   Selecione **[!UICONTROL Back]** para voltar à etapa anterior.

   Selecione **[!UICONTROL Cancel]** para cancelar a configuração do modelo.
