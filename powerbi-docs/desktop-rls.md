---
title: 使用 Power BI Desktop 的資料列層級安全性 (RLS) 來限制資料存取
description: 如何在 Power BI Desktop 內，為匯入的資料集和 DirectQuery 設定資料列層級安全性。
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.custom: ''
ms.date: 01/31/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 7a9aa0ca62ae4f1008d4cf47caa909841f9ec495
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "77464337"
---
# <a name="restrict-data-access-with-row-level-security-rls-for-power-bi-desktop"></a>使用 Power BI Desktop 的資料列層級安全性 (RLS) 來限制資料存取

您可以搭配資料列層級安全性 (RLS) 使用 Power BI Desktop 來限制指定使用者的資料存取權限。 篩選會限制資料列層級的資料。 您可以在角色中定義篩選。

您現在可以使用 Power BI Desktop 為匯入 Power BI 的資料模型設定 RLS。 您也可以設定使用 [DirectQuery](desktop-use-directquery.md) 資料集上的 RLS，例如 SQL Server。 先前，您只能夠在 Power BI 外部的內部部署 Analysis Services 模型內實作 RLS。 您可以在內部部署模型上，為 Analysis Services 即時連線設定資料列層級安全性。 即時連線資料集不會顯示安全性選項。

> [!IMPORTANT]
> 如果您在 Power BI 服務中定義角色與規則，就必須在 Power BI Desktop 中重新建立這些角色，並將報表發佈至服務。 深入了解 [Power BI 服務內的 RLS](service-admin-rls.md) 選項。

[!INCLUDE [include-short-name](./includes/rls-desktop-define-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-desktop-view-as-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-limitations.md)]

[!INCLUDE [include-short-name](./includes/rls-faq.md)]

## <a name="next-steps"></a>後續步驟

[使用 Power BI 服務的資料列層級安全性 (RLS)](service-admin-rls.md)  

有其他問題嗎？ [嘗試在 Power BI 社群提問](https://community.powerbi.com/)。