---
title: Administração
description: Saiba como administrar o Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 995f15b6d2dd99d5304a4cda7b1fa5f8a1d00023
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# Administração

Use o [Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para gerenciar produtos e usuários do Mix Modeler.

Para que o Mix Modeler funcione corretamente, é necessário definir as permissões corretas.

Na interface do Adobe Experience Cloud:

1. Selecionar **[!UICONTROL Permissions]** do painel esquerdo, abaixo **[!UICONTROL ADMINISTRATION]**.

1. Selecionar {{user}} **[!UICONTROL Roles]** no painel esquerdo.

1. Selecione uma função existente ou crie uma função usando **[!UICONTROL Create role]** (por exemplo, **Mix Modeler**). Se você selecionar uma função existente, selecione {{edit}} **[!UICONTROL Edit]** para editar as permissões da função. Consulte [Gerenciar Funções](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para obter mais informações.

1. Verifique se você selecionou uma ou mais sandboxes para a função.

1. Adicione o **Adobe Mix Modeler** para a lista de recursos da função.

1. Certifique-se de selecionar o **[!UICONTROL Adobe Mix Modeler]** permissões para a função que você está configurando. Você pode selecionar uma ou mais das seguintes funções:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![MIX MODELER RBAC](/help/assets/mix-modeler-rbac.png)


1. Certifique-se de selecionar permissões adicionais para a função. Por exemplo, para exibir ou gerenciar conjuntos de dados e esquemas, você selecionaria:

   - **[!UICONTROL Data Management]**: selecione as opções relevantes: **[!UICONTROL View Datasets]** ou **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: selecione as opções relevantes: **[!UICONTROL Manage Schemas]** ou **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Selecionar **[!UICONTROL Save]** para salvar as permissões.

1. Entrada **[!UICONTROL Details]** no prazo de **[!UICONTROL Role]**, adicione o apropriado **[!UICONTROL Users]** ou **[!UICONTROL User groups]** para fornecer aos usuários acesso ao Mix Modeler.
