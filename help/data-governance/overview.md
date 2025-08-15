---
title: Visão geral da governança de dados
description: Saiba como usar os serviços e as ferramentas do Experience Platform que permitem controlar os dados de experiência coletados. Assim, você cumpre com suas práticas comerciais, suas obrigações legais e seu processo de desenvolvimento.
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
source-git-commit: bdde574b150bda2b0c82a9f5a20160fed26cb69d
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 2%

---

# Visão geral da governança de dados

A integração entre o Mix Modeler e o Experience Platform fornece ao Mix Modeler os recursos para aproveitar os recursos intrínsecos de governança de dados do Experience Platform. Esta seção da documentação detalha as especificidades dos recursos de governança de dados disponíveis no Mix Modeler.

A Governança de dados da Experience Platform oferece a capacidade de controlar e compreender seus dados em toda a jornada que os dados recebem pelo Experience Platform. Essa jornada envolve a manutenção da qualidade, da linhagem de dados, da catalogação de dados e muito mais.

Os rótulos e políticas de uso de dados que são criados em conjuntos de dados consumidos pela superfície do Experience Platform na Mix Modeler, quando apropriado. Por exemplo, esses rótulos interrompem ou avisam os usuários ao excluir conjuntos de dados que fazem parte de uma regra de conjunto de dados nos dados harmonizados. Ou ocultar campos de esquema restritos para usuários ao criar uma regra de conjunto de dados.

A integração de governança de dados permite gerenciar a conformidade com mais eficiência. Os administradores de dados da sua organização podem definir políticas de restrição de uso. Como resultado, você pode usar dados que estejam em conformidade com as políticas definidas pelos administradores de dados. Leia a documentação em [Rótulos e políticas](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-dataviews/data-governance) para saber mais.

Os seguintes recursos de governança de dados estão disponíveis:

| Recurso | Detalhes |
|---|---|
| Controles de acesso | O controle de acesso baseado em função e o controle de acesso baseado em atributo (nível de campo) são compatíveis. Consulte [Controles de acesso](access-controls.md) para obter mais informações. |
| Logs de auditoria | Quando os usuários criam, atualizam ou excluem categorias específicas do Mix Modeler, a funcionalidade de Auditoria do Experience Platform registra a atividade nos logs de auditoria. Consulte [Logs de auditoria](audit-logs.md) para obter mais informações. |
| Políticas | Como parte do fluxo de trabalho de dados harmonizado, as políticas definidas pela Experience Platform são aplicadas. Qualquer violação dos rótulos de uso de dados é relatada e exibida ao usuário. Consulte [Políticas](policies.md) para obter mais informações. |
| Criptografia | Todos os conjuntos de dados usados para entrada e saída de modelos seguem as diretrizes do Experience Platform. A criptografia de dados da Experience Platform se aplica a dados inativos e em trânsito. |
| Higiene de dados | Todos os conjuntos de dados usados para entrada e saída de modelos seguem as diretrizes do Experience Platform. A Experience Platform fornece um conjunto de ferramentas para gerenciar o ciclo de vida dos dados do cliente, incluindo o suporte a diferentes tipos de expiração de dados. Ao excluir um conjunto de dados de origem da Experience Platform, que é usado como parte de seus dados harmonizados, você é notificado. Consulte [Regras do conjunto de dados](/help/harmonize-data/dataset-rules.md) para obter mais informações. |
| Customer Managed Keys | Ao licenciar o Mix Modeler com o complemento Privacy Security Shield, você pode usar o recurso Chaves gerenciadas pelo cliente para aproveitar o Cofre de chaves do Azure para trazer suas próprias chaves por meio de APIs. Você tem o gerenciamento completo dos dados que estão sendo processados nos modelos na Mix Modeler. |
