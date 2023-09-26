---
title: Criar um modelo
description: Saiba como criar um modelo no Adobe Mix Modeler.
feature: Models
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---


# Criar um modelo

Para criar um modelo, na variável ![Modelos](../assets/icons/FileData.svg) **[!UICONTROL Models]** no Adobe Mix Modeler, selecione **[!UICONTROL Guide me]**.

Para criar modelos alimentados por IA personalizada, a interface fornece um fluxo de configuração de modelo guiado passo a passo.

1. No **[!UICONTROL Setup]** etapa:

   1. Insira seu modelo **[!UICONTROL Name]**, por exemplo `Demo model`. Insira um **[!UICONTROL Description]**, por exemplo `Demo model to explore AI featues of Adobe Mix Modeler`.

      ![Nome e descrição do modelo](../assets/model-name-description.png)

   1. Selecionar **[!UICONTROL Next]** para prosseguir para a próxima etapa. Selecionar **[!UICONTROL Cancel]** para cancelar a configuração do modelo.

1. No **[!UICONTROL Configure]** etapa:

   1. No **[!UICONTROL Conversion goal]** seção, no contêiner:

      1. Insira um **[!UICONTROL Conversion name]** para a conversão, por exemplo `Conversion`

      1. Selecione uma conversão de **[!UICONTROL *Selecionar campo harmonizado *]**, contendo as conversões disponíveis que você definiu como parte de [Conversões](../harmonize-data/conversions.md) in [!UICONTROL Harmonized datasets]. Por exemplo,**[!UICONTROL Online Conversion]**.

      1. É possível selecionar ![Responder](../assets/icons/Reply.svg) **[!UICONTROL Create new conversion]** para criar uma conversão diretamente da configuração do modelo.

         ![Modelo - etapa de conversão](../assets/model-conversion-step.png)

   1. No **[!UICONTROL Marketing touchpoints]** , você verá vários contêineres de ponto de contato de marketing, correspondentes aos pontos de contato de marketing definidos como parte de [Pontos de contato de marketing](../harmonize-data/marketing-touchpoints.md) in [!UICONTROL Harmonized datasets].

      * Para cada recipiente:

         1. Você pode modificar a variável **[!UICONTROL Marketing touchpoint name]**.

         1. Selecionar um ponto de contato de marketing em **[!UICONTROL _Selecionar ponto de contato de marketing_]**.

         1. É possível selecionar ![Responder](../assets/icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** para criar um ponto de contato de marketing diretamente da configuração do modelo.

      * Para adicionar um contêiner de ponto de contato de marketing, selecione ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * Para remover um container de ponto de contato de marketing, no container, selecione ![Mais](../assets/icons/More.svg) e selecione **[!UICONTROL Remove container]** no menu de contexto.

        ![Modelo - etapa de pontos de contato de marketing](../assets/model-marketing-touchpoint-step.png)

   1. Por padrão, uma pontuação é gerada para todos os dados na visualização harmonizada. Para pontuar apenas um subconjunto do público, defina um ou mais filtros usando contêineres no **[!UICONTROL Eligible data population]** seção.

      * Para cada container, defina um ou mais eventos.

         1. Para cada evento:

            1. Selecione uma métrica ou dimensão em **[!UICONTROL _Selecionar campo harmonizado_]**.

            1. Selecione o operador apropriado: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** ou **[!UICONTROL is not in]**.

            1. Insira ou selecione um valor em **[!UICONTROL _Inserir ou selecionar valor_]**.

         1. Para adicionar outro evento ao container, selecione ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. Para remover um evento do container, selecione ![Fechar](../assets/icons/Close.svg).

         1. Para filtrar usando todos ou alguns dos vários eventos definidos no container, selecione **[!UICONTROL Any of]** ou **[!UICONTROL All of]**. O rótulo muda de **[!UICONTROL Include ... Or ...]** para **[!UICONTROL Include ... And ...]**.

      * Para adicionar um container de preenchimento de dados elegível, selecione ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

      * Para remover um container de preenchimento de dados elegível, no container, selecione ![Mais](../assets/icons/More.svg) e selecione **[!UICONTROL Remove container]** no menu de contexto.

        ![Modelo - População de dados elegível](../assets/model-eligible-data-population-step.png)

   1. Para adicionar conjuntos de dados contendo fatores externos ao modelo, use um ou mais contêineres no **[!UICONTROL External factors dataset]** seção.

      * Para cada recipiente:

         1. Insira um **[!UICONTROL Factor name]** em **[!UICONTROL _Inserir fator_]**.

         1. Selecionar um conjunto de dados de **[!UICONTROL _Selecionar um conjunto de dados_]**. É possível selecionar ![Dados](../assets/icons/Data.svg) para gerenciar conjuntos de dados. Consulte [Conjuntos de dados](../ingest-data/datasets.md) para obter mais informações.

      * Para adicionar outro container do conjunto de dados de fatores externos, selecione ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * Para remover um contêiner de conjunto de dados de fatores externos, no contêiner, selecione ![Mais](../assets/icons/More.svg) e selecione **[!UICONTROL Remove container]** no menu de contexto.

        ![Modelo - Conjunto de dados de fatores externos](../assets/model-external-factors-dataset-step.png)


   1. Para adicionar conjuntos de dados contendo fatores internos ao modelo, use um ou mais contêineres no **[!UICONTROL Internal factors dataset]** seção.

      * Para cada recipiente:

         1. Insira um **[!UICONTROL Factor name]** em **[!UICONTROL _Inserir fator_]**.

         1. Selecionar um conjunto de dados de **[!UICONTROL _Selecionar um conjunto de dados_]**. É possível selecionar ![Dados](../assets/icons/Data.svg) para gerenciar conjuntos de dados. Consulte [Conjuntos de dados](../ingest-data/datasets.md) para obter mais informações.

      * Para adicionar outro contêiner do conjunto de dados de fatores internos, selecione ![Adicionar](../assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * Para remover um container adicional do conjunto de dados de fatores internos, no container, selecione ![Mais](../assets/icons/More.svg) e **[!UICONTROL Remove container]** no menu de contexto.

        ![Modelo - Conjunto de dados de fatores internos](../assets/model-internal-factors-dataset-step.png)

   1. Para definir a janela de retrospectiva do modelo, insira um valor entre `1` e `52` in **[!UICONTROL Give contribution credit to touchpoints occurring within]** .. **[!UICONTROL weeks prior to the conversion]**.

   1. Selecionar **[!UICONTROL Next]** para prosseguir para a próxima etapa. Se forem necessárias mais configurações, um contorno vermelho e um texto explicarão qual configuração adicional será necessária. <br/>Selecionar **[!UICONTROL Back]** para voltar à etapa anterior. <br/>Selecionar **[!UICONTROL Cancel]** para cancelar a configuração do modelo.

1. No **[!UICONTROL Advanced]** etapa:

   1. No **[!UICONTROL Define training window]** selecione entre

      * **[!UICONTROL Have Adobe Mix Modeler select a helpful training window]** e

      * **[!UICONTROL Manually input a training window]**. Quando selecionado, define o número de anos em **[!UICONTROL Include events the following years prior to a conversion]**.

        ![Modelo - Definir janela de treinamento](../assets/model-define-training-window.png)

   1. No **[!UICONTROL Spend share]** seção:

      * Para usar taxas históricas de investimento em marketing para informar o modelo quando os dados de marketing são escassos, ative **[!UICONTROL Allow spend share]**.

   1. No **[!UICONTROL Prior knowledge]** seção:

      1. Selecione o **[!UICONTROL Rule type]**.

      1. Distribua porcentagens para cada um dos canais listados em **[!UICONTROL Name]**, utilizando o **[!UICONTROL Contribution proportion]** coluna. Verifique se a distribuição total de porcentagens soma 100%.

      1. É possível adicionar para cada canal um **[!UICONTROL Level of confidence]** porcentagem.

      1. Quando necessário, use **[!UICONTROL Clear all]** para apagar todos os valores de entrada para o **[!UICONTROL Contribution proportion]** e **[!UICONTROL Level of confidence]** colunas.

         ![Modelo - Conhecimento prévio](../assets/model-prior-knowledge-step.png)

1. Selecionar **[!UICONTROL Finish]** para concluir a configuração do modelo.

   * No **[!UICONTROL Create instance?]** , selecione **[!UICONTROL Ok]** para acionar o primeiro conjunto de treinamentos e execuções de pontuação imediatamente. Seu modelo está listado com o status <span style="color:orange">●</span> **[!UICONTROL Awaiting training]**.

     Selecionar **[!UICONTROL Cancel]** para cancelar.

   * Se forem necessárias mais configurações, um contorno vermelho e um texto explicarão qual configuração adicional será necessária.

   Selecionar **[!UICONTROL Back]** para voltar à etapa anterior.

   Selecionar **[!UICONTROL Cancel]** para cancelar a configuração do modelo.

