---
title: Criar modelos
description: Saiba como criar modelos no Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: b08a24856e28a1377728bc2c511f6ea483cbd0fd
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# Criar modelos

Para criar modelos alimentados por IA personalizada, a interface fornece um fluxo de configuração de modelo guiado passo a passo.

Na interface ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no Mix Modeler, selecione **[!UICONTROL Open model canvas]**.

## Configuração

Você define o nome e a descrição na etapa **[!UICONTROL Setup]**:

1. Insira seu modelo **[!UICONTROL Name]**, por exemplo `Demo model`. Digite um **[!UICONTROL Description]**, por exemplo `Demo model to explore AI featues of Mix Modeler`.

   ![Nome e descrição do modelo](/help/assets/model-name-description.png)

1. Selecione **[!UICONTROL Next]** para continuar com a próxima etapa. Selecione **[!UICONTROL Cancel]** para cancelar a configuração do modelo.

## Configurar 

Configure seu modelo na etapa **[!UICONTROL Configure]**. A configuração envolve a definição de metas de conversão, pontos de contato de marketing, a população de dados elegível, fatores externos e internos e muito mais.

1. Na seção **[!UICONTROL Conversion goal]**:

   ![Modelo - etapa de conversão](/help/assets/model-conversion-step.png)

   1. Selecione uma conversão no menu suspenso **[!UICONTROL Conversion]**. As conversões disponíveis são a conversão definida como parte de [Conversões](../harmonize-data/conversions.md) em [!UICONTROL Harmonized datasets]. Por exemplo, **[!UICONTROL Online Conversion]**.

   1. Você pode selecionar ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a conversion]** para criar uma conversão diretamente da configuração do modelo.



1. Na seção **[!UICONTROL Marketing touchpoints]**, você pode selecionar um ou mais pontos de contato de marketing, correspondentes aos pontos de contato de marketing definidos como parte dos [Pontos de contato de marketing](../harmonize-data/marketing-touchpoints.md) em [!UICONTROL Harmonized datasets].


   ![Modelo - etapa do ponto de contato de marketing](/help/assets/model-marketing-touchpoint-step.png)

   1. Selecione um ou mais pontos de contato de marketing no menu suspenso **[!UICONTROL Touchpoint include]**.

      * Você pode usar ![CrossSize75](/help/assets/icons/CrossSize75.svg) para remover um ponto de contato.
      * Você pode usar **[!UICONTROL Clear all]** para remover todos os pontos de contato.

   1. Você pode selecionar ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a touchpoint]** para criar um ponto de contato de marketing diretamente da configuração do modelo.

   >[!NOTE]
   >
   >Você não pode configurar o modelo com pontos de contato que tenham dados sobrepostos e deve haver pelo menos um ponto de contato com gasto.

1. Por padrão, uma pontuação é gerada para todos os dados na visualização harmonizada. Para pontuar apenas um subconjunto da população, defina um ou mais filtros usando containers na seção **[!UICONTROL Eligible data population]**.

   ![Modelo - População de dados qualificada](/help/assets/model-eligible-data-population-step.png)

   * Para cada container, defina um ou mais eventos.

      1. Para cada evento:

         1. Selecione uma métrica ou dimensão em **[!UICONTROL _Selecionar campo harmonizado_]**.

         1. Selecione o operador apropriado: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** ou **[!UICONTROL is not in]**.

         1. Insira ou selecione um valor em **[!UICONTROL _Insira ou selecione o valor_]**.

      1. Para adicionar outro evento ao contêiner, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

      1. Para remover um evento do container, selecione ![Fechar](/help/assets/icons/CrossSize75.svg).

      1. Para filtrar usando todos ou alguns dos vários eventos definidos no container, selecione **[!UICONTROL Any of]** ou **[!UICONTROL All of]**. O rótulo foi alterado de **[!UICONTROL Include ... Or ...]** para **[!UICONTROL Include ... And ...]**.

   * Para adicionar um contêiner de preenchimento de dados qualificado, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

   * Para remover um contêiner de preenchimento de dados qualificado, no contêiner, selecione ![Mais](/help/assets/icons/More.svg) e selecione **[!UICONTROL Remove marketing touchpoint]** no menu de contexto.

   * Selecione **And** e **Or** entre contêineres para criar definições mais complexas para a população de dados qualificada.


1. Para adicionar conjuntos de dados contendo fatores externos ao seu modelo, use um ou mais contêineres na seção **[!UICONTROL External factors dataset]**. Um exemplo de fatores externos são os índices S&amp;P.

   ![Modelo - Conjunto de dados de fatores externos](/help/assets/model-external-factors-dataset-step.png)

   * Para cada recipiente:

      1. Digite um **[!UICONTROL External factor name]**, por exemplo `External Factors`.

      1. Selecione um conjunto de dados no menu suspenso **[!UICONTROL Dataset]**. Você pode selecionar ![Dados](/help/assets/icons/Data.svg) para gerenciar conjuntos de dados. Consulte [Conjuntos de dados](../ingest-data/datasets.md) para obter mais informações.

      1. Selecione uma opção no menu suspenso **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** ou **[!UICONTROL Negative]**. A opção padrão é **[!UICONTROL Auto select]**, que permite que o modelo determine o impacto. Você pode substituir o padrão.

   * Para adicionar outro contêiner de conjunto de dados de fatores externos, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Para remover um contêiner de conjunto de dados de fatores externos, selecione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).




1. Para adicionar conjuntos de dados contendo fatores internos ao seu modelo, use um ou mais contêineres na seção **[!UICONTROL Internal factors dataset]**. Um exemplo de fatores internos são os dados de marketing por email.

   ![Modelo - Conjunto de dados de fatores internos](/help/assets/model-internal-factors-dataset-step.png)

   * Para cada recipiente:

      1. Digite um **[!UICONTROL Internal factor name]**, por exemplo `Email Marketing Data`.

      1. Selecione um conjunto de dados de **[!UICONTROL _Selecione um conjunto de dados_]**. Você pode selecionar ![Dados](/help/assets/icons/Data.svg) para gerenciar conjuntos de dados. Consulte [Conjuntos de dados](../ingest-data/datasets.md) para obter mais informações.

      1. Selecione uma opção no menu suspenso **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** ou **[!UICONTROL Negative]**.

   * Para adicionar outro contêiner do conjunto de dados de fatores internos, selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

   * Para remover um contêiner do conjunto de dados de fatores internos, selecione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).



1. Para definir a janela de pesquisa do modelo, insira um valor entre `1` e `52` em **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

1. Selecione **[!UICONTROL Next]** para continuar com a próxima etapa. Se forem necessárias mais configurações, um contorno vermelho e um texto explicarão qual configuração adicional será necessária. <br/>Selecione **[!UICONTROL Back]** para voltar à etapa anterior. <br/>Selecione **[!UICONTROL Cancel]** para cancelar a configuração do modelo.


## Avançado

Você pode especificar configurações avançadas na etapa **[!UICONTROL Advanced]**. Nesta etapa, é possível ativar o modelo para MTA (atribuição multitoque).

1. Na seção **[!UICONTROL Spend share]**:

   * Para usar taxas históricas de investimento em marketing para informar o modelo quando os dados de marketing são escassos, ative **[!UICONTROL Allow spend share]**. Essa configuração é recomendada, especialmente nos seguintes cenários:
      * Um canal não tem observações suficientes (por exemplo, baixa frequência de gastos, impressões ou cliques).
      * Você está modelando mídia pontual, mas regular e potencialmente de alto gasto (como TV para algumas marcas), em que os dados podem ser escassos.

     >[!NOTE]
     >
     >Para investimentos únicos (por exemplo, um anúncio de Super Bowl), considere incorporar esses dados como um fator em vez de depender da participação nos gastos.
     >


1. Na seção **[!UICONTROL MTA enabled]**:

   * Para habilitar recursos de MTA para o modelo, ative **[!UICONTROL MTA enabled]**. Se você tiver ativado o MTA, os insights de atribuição multitoque estarão disponíveis após treinar e pontuar seu modelo. Consulte a guia [Atribuição](insights.md#attribution) em [Insights de modelo](insights.md).

1. Na seção **[!UICONTROL Prior knowledge]**:

   ![Modelo - Conhecimento anterior](/help/assets/model-prior-knowledge-step.png)

   1. Selecione o **[!UICONTROL Rule type]**, que é por padrão **[!UICONTROL Absolute values]**.

   1. Especifique porcentagens de contribuição para qualquer um dos canais listados em **[!UICONTROL Name]**, usando a coluna **[!UICONTROL Contribution proportion]**.

   1. Quando apropriado, você pode adicionar uma porcentagem de **[!UICONTROL Level of confidence]** para cada canal.

   1. Quando necessário, use **[!UICONTROL Clear all]** para limpar todos os valores de entrada para as colunas **[!UICONTROL Contribution proportion]** e **[!UICONTROL Level of confidence]**.


## Agendar

Você pode agendar o treinamento e a pontuação para seu modelo na etapa **[!UICONTROL Schedule]**.

1. Na seção **[!UICONTROL Schedule]**, você pode agendar o treinamento e a pontuação do modelo.

   ![Modelo de agendamento](../assets/model-schedule.png)

   Para programar a pontuação e o treinamento do modelo:

   1. Ligue o **[!UICONTROL Enable scheduled model scoring and training]**.
   1. Selecione um **[!UICONTROL Scoring frequency]**:

      * **[!UICONTROL Daily]**: Insira uma hora válida (por exemplo `05:22 pm`) ou use ![Clock](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Weekly]**: Selecione um dia da semana e insira um horário válido (por exemplo `05:22 pm`) ou use ![Relógio](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Monthly]**: Selecione um dia do mês no menu suspenso Executar em cada e insira um horário válido (por exemplo `05:22 pm`) ou use ![Relógio](/help/assets/icons/Clock.svg).

   1. Selecione um **[!UICONTROL Training frequency]** no menu suspenso: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

1. Na seção **[!UICONTROL Define training window]**, selecione entre:

   ![Modelo - Definir janela de treinamento](/help/assets/model-define-training-window.png)

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** e

   * **[!UICONTROL Manually input a training window]**. Quando selecionado, defina o número de anos em **[!UICONTROL Include events the following years prior to a conversion]**.


1. Selecione **[!UICONTROL Finish]** para concluir a configuração do modelo.

   * Na caixa de diálogo **[!UICONTROL Create instance?]**, selecione **[!UICONTROL Ok]** para acionar o primeiro conjunto de treinamentos e execuções de pontuação imediatamente. Seu modelo está listado com o status ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Selecione **[!UICONTROL Cancel]** para cancelar.

   * Se forem necessárias mais configurações, um contorno vermelho e um texto explicarão qual configuração adicional será necessária.

   Selecione **[!UICONTROL Back]** para voltar à etapa anterior.

   Selecione **[!UICONTROL Cancel]** para cancelar a configuração do modelo.
