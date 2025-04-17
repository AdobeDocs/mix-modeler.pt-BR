---
title: Logs de auditoria
description: Saiba como acessar logs de auditoria do Mix Modeler.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 85f9b42a775006cd3566447b2bb9d0a806fa3e73
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 5%

---

# Logs de auditoria

Para aumentar a transparência e a visibilidade das atividades realizadas no sistema, a atividade do usuário no fluxo de trabalho do Mix Modeler é capturada nos logs de auditoria do Experience Platform para entender quaisquer alterações orientadas pelo usuário nas categorias do Mix Modeler. Esses registros formam uma trilha de auditoria que pode ajudar na solução de problemas e ajudar sua empresa a cumprir com as políticas corporativas de gerenciamento de dados e os requisitos normativos.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Um log de auditoria informa quem executou qual ação e quando. Cada ação registrada em um log contém metadados que indicam o tipo de ação, a data e a hora, a ID do email do usuário que executou a ação e atributos adicionais relevantes ao tipo de ação. Ele rastreia as ações de criação, atualização e exclusão realizadas pelos usuários no Mix Modeler.

Para inspecionar o log de auditoria, na interface do Mix Modeler:

1. Selecione ![Lista de Tarefas](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** de **[!UICONTROL PRIVACY]**.

1. Em **[!UICONTROL Audits]**, você pode encontrar o **[!UICONTROL Activity log]**. O log de atividades mostra entradas para as seguintes categorias, ações e status do Mix Modeler.

   | Categoria | Ação | Status |
   |---|---|---|
   | Regra do conjunto de dados do Mix Modeler | Criar | Permitir ou negar |
   | Regra do conjunto de dados do Mix Modeler | Atualização | Permitir ou negar |
   | Regra do conjunto de dados do Mix Modeler | Excluir | Permitir ou negar |
   | Campo do Mix Modeler | Criar | Permitir ou negar |
   | Campo do Mix Modeler | Atualização | Permitir ou negar |
   | Campo do Mix Modeler | Excluir | Permitir ou negar |
   | Mix Modeler Marketing Touchpoint | Criar | Permitir ou negar |
   | Mix Modeler Marketing Touchpoint | Atualização | Permitir ou negar |
   | Mix Modeler Marketing Touchpoint | Excluir | Permitir ou negar |
   | Conversão do Mix Modeler | Criar | Permitir ou negar |
   | Conversão do Mix Modeler | Atualização | Permitir ou negar |
   | Conversão do Mix Modeler | Excluir | Permitir ou negar |
   | Modelo do Mix Modeler | Criar | Permitir ou negar |
   | Modelo do Mix Modeler | Atualização | Permitir ou negar |
   | Modelo do Mix Modeler | Excluir | Permitir ou negar |
   | Modelo do Mix Modeler | Pontuação | Permitir ou negar |
   | Modelo do Mix Modeler | Clonar | Permitir ou negar |
   | Modelo do Mix Modeler | Treinar / Treinar novamente | Permitir ou negar |
   | Modelo do Mix Modeler | Baixar / Salvar metadados | Permitir ou negar |
   | Plano do Mix Modeler | Criar | Permitir ou negar |
   | Plano do Mix Modeler | Atualização | Permitir ou negar |
   | Plano do Mix Modeler | Alterar modelo associado | Permitir ou negar |
   | Harmonização de dados do Mix Modeler | Sincronização do acionador | Permitir ou negar |


1. Selecione uma entrada no Log de atividades para abrir um painel e obter mais detalhes.

   ![Auditoria do Mix Modeler](/help/assets/mix-modeler-audit.png)

1. Para filtrar no intervalo **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** ou **[!UICONTROL Date]**, selecione ![Filtro](/help/assets/icons/Filter.svg).

1. Para modificar as colunas exibidas no Log de atividades, selecione ![Colunas](/help/assets/icons/ColumnSetting.svg) e, na caixa de diálogo **[!UICONTROL Customize table]**, selecione as colunas a serem exibidas. Selecione **[!UICONTROL Apply]** para aplicar a seleção, **[!UICONTROL Cancel]** para cancelar a seleção.

1. Para baixar o log de auditoria, selecione ![Baixar](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. Na caixa de diálogo **[!UICONTROL Download log]**, selecione **[!UICONTROL CSV]** ou **[!UICONTROL JSON]** como o formato e selecione **[!UICONTROL Download]**.

## Acesso a logs de auditoria

Quando o recurso é ativado para sua organização, os logs de auditoria são coletados automaticamente conforme a atividade ocorre. Não é necessário ativar a coleta de log de auditoria manualmente.

Para exibir e exportar logs de auditoria, você deve ter recebido a permissão de controle Acesso aos logs de auditoria. Para saber como gerenciar permissões individuais para recursos do Mix Modeler, consulte a [documentação de controle de acesso](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).
