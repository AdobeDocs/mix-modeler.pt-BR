---
title: Administração
description: Saiba como administrar o Adobe Mix Modeler.
source-git-commit: b5b277e3476bdf6c0c0da85425bba19bea00c594
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---


# Administração

Use o [Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para gerenciar produtos e usuários do Adobe Mix Modeler.

Para que o Adobe Mix Modeler funcione corretamente, é necessário definir as permissões corretas.

Na interface do Adobe Experience Cloud,

1. Selecionar **[!UICONTROL Permissions]** do painel esquerdo, abaixo **[!UICONTROL ADMINISTRATION]**.

1. Selecionar ![Person](assets/icons/User.svg) **[!UICONTROL Roles]** no painel esquerdo.

1. Selecione uma função existente ou crie uma função usando **[!UICONTROL Create role]**. Se você selecionar uma função existente, selecione ![Editar](assets/icons/Edit.svg) **[!UICONTROL Edit]** para editar as permissões da função. Consulte [Gerenciar Funções](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para obter mais informações.

1. Selecione as seguintes permissões para a função:

   * **[!UICONTROL Sandboxes]**: selecione pelo menos uma sandbox.

   * **[!UICONTROL Data Management]**: certifique-se de selecionar as opções **[!UICONTROL View Datasets]** e **[!UICONTROL Manage Datasets]**.

   * **[!UICONTROL Data Modeling]**: certifique-se de selecionar as opções **[!UICONTROL Manage Schemas]** e **[!UICONTROL View Schemas]**.

   * **[!UICONTROL Destinations]**: certifique-se de selecionar **[!UICONTROL Manage and Activate Dataset Destination]**, **[!UICONTROL Destination Authoring]**, **[!UICONTROL Activate Destinations]** e **[!UICONTROL View Destinations]**.

   * **[!UICONTROL Data Ingestion]**: certifique-se de selecionar **[!UICONTROL View Sources]** e **[!UICONTROL Manage Sources]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   As permissões configuradas para a função devem ser semelhantes a:

   ![Permissões](assets/permissions.png)

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Selecionar **[!UICONTROL Save]** para salvar as permissões.

1. Entrada **[!UICONTROL Details]** no prazo de **[!UICONTROL Role]**, adicione o apropriado **[!UICONTROL Users]** e/ou **[!UICONTROL User groups]** para fornecer aos usuários acesso ao Adobe Mix Modeler.
