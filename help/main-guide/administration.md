---
title: Administração
description: Saiba como administrar o Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
TQID: https://experienceleague.adobe.com/0MxMv6Due-i9-8JxKTb3vk2NDZ5mc6Pj4yEe-liCszg
autotag-review: '2026-05-01T09:07:55.299Z'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2:
  - id: abe9e290-7d2f-4131-b71e-ef9900865044
  - id: a6da0571-746e-4d59-89a4-7b691b1c3b9a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 7%

---

# Administração

Use o [Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para gerenciar produtos e usuários do Mix Modeler.

Para que o Mix Modeler funcione corretamente, você deve definir as permissões corretas.

Na interface do Adobe Experience Cloud:

1. Selecione **[!UICONTROL Permissions]** no painel esquerdo, abaixo de **[!UICONTROL ADMINISTRATION]**.

1. Selecione ![Usuário](/help/assets/icons/User.svg) **[!UICONTROL Roles]** no painel esquerdo.

1. Selecione uma função existente ou crie uma função usando **[!UICONTROL Create role]** (por exemplo, **Mix Modeler**). Se você selecionar uma função existente, selecione ![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** para editar as permissões da função. Consulte [Gerenciar funções](https://helpx.adobe.com/br/enterprise/using/admin-console.html) para obter mais informações.

1. Verifique se você selecionou uma ou mais sandboxes para a função.

1. Adicione o recurso **Adobe Mix Modeler** à lista de recursos para a função.

1. Verifique se você selecionou as permissões **[!UICONTROL Adobe Mix Modeler]** corretas para a função que você está configurando. Você pode selecionar uma ou mais das seguintes funções:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler RBAC](/help/assets/mix-modeler-rbac.png)


1. Certifique-se de selecionar permissões adicionais para a função. Por exemplo, para exibir ou gerenciar conjuntos de dados e esquemas, você selecionaria:

   - **[!UICONTROL Data Management]**: selecione as opções relevantes: **[!UICONTROL View Datasets]** ou **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: selecione as opções relevantes: **[!UICONTROL Manage Schemas]** ou **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Selecione **[!UICONTROL Save]** para salvar as permissões.

1. Em **[!UICONTROL Details]** em **[!UICONTROL Role]**, adicione o **[!UICONTROL Users]** ou o **[!UICONTROL User groups]** apropriado para fornecer aos usuários acesso ao Mix Modeler.
