---
title: Controles de acesso
description: Saiba como configurar controles de acesso no Mix Modeler.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# Controles de acesso

O controle de acesso para o Mix Modeler é fornecido por meio do Experience Platform no [Adobe Admin Console](https://adminconsole.adobe.com/) e por meio de [Permissões](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) no Experience Platform. Essa funcionalidade aproveita perfis de produto no Admin Console, que vinculam usuários com permissões e sandboxes.

Para obter mais informações sobre o controle de acesso, consulte [Visão geral do controle de acesso](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Controle de acesso baseado em função

Consulte [Administração](../main-guide/administration.md) sobre como configurar permissões de acesso com base em função para usuários do Mix Modeler e grupos de usuários no Experience Platform.

## Controle de acesso baseado em atributos

[O controle de acesso baseado em atributos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) é um recurso do Experience Platform que permite aos administradores controlar o acesso a objetos específicos e/ou recursos baseados em atributos. Os atributos podem ser metadados adicionados a um objeto, como um rótulo adicionado a um campo ou segmento de esquema. Um administrador define políticas de acesso que incluem atributos para gerenciar permissões de acesso do usuário.

Essa funcionalidade permite rotular campos de esquema do Experience Data Model (XDM) com rótulos que definem escopos organizacionais ou de uso de dados. Em paralelo, os administradores podem usar a interface de administração de usuários e funções para definir políticas de acesso em campos de esquema XDM. E gerencie melhor o acesso fornecido aos usuários ou grupos de usuários (usuários internos, externos ou de terceiros). Além disso, o controle de acesso baseado em atributos permite que os administradores gerenciem o acesso a segmentos específicos.

Por meio do controle de acesso baseado em atributos, os administradores podem controlar o acesso dos usuários a dados pessoais confidenciais (SPD) e a informações de identificação pessoal (PII) em todos os fluxos de trabalho e recursos da plataforma. Os administradores podem definir funções de usuário que tenham acesso somente a campos e dados específicos que correspondam a esses campos.

Ao configurar regras de conjunto de dados para conjuntos de dados harmonizados, o controle de acesso baseado em [atributo](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) do Experience Platform é aplicado em nível de campo. Um campo é restrito quando um rótulo é anexado a um campo de esquema. E uma política ativa é ativada para negar acesso a esse campo. Como resultado:

* você não vê os campos de esquema restritos ao criar uma regra de conjunto de dados,
* não é possível exibir ou editar o mapeamento de um ou mais campos de esquema restritos para você. Ao editar ou exibir uma regra de conjunto de dados contendo esses campos restritos, você verá a tela a seguir.
  ![Ação não permitida](/help/assets/action-not-permitted.png)
