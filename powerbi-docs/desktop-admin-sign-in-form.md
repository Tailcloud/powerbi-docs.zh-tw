---
title: 管理員如何管理 Power BI Desktop 登入表單
description: 了解開啟 Power BI Desktop 時，如何管理初始登入表單。
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 04/15/2019
ms.author: davidi
ms.openlocfilehash: 934827311e089e34e56fbcffe4d4c58a056df4ad
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "75761695"
---
# <a name="administrators-manage-the-power-bi-desktop-sign-in-form"></a>系統管理員：管理 Power BI Desktop 登入表單
Power BI Desktop 第一次啟動時，會顯示登入表單。 您可以填入資訊，或登入 Power BI 以繼續。 系統管理員使用登錄機碼來管理此表單。 

![Power BI desktop 的初始登入表單](media/desktop-admin-sign-in-form/sign-in-form.png)

系統管理員使用下列登錄機碼停用登入表單。 這也可以使用全域原則推送到全組織。

```
Key: HKEY_CURRENT_USER\SOFTWARE\Policies\Microsoft\Microsoft Power BI Desktop
valueName: ShowLeadGenDialog
```
您也可以嘗試以下登錄機碼，這些金鑰根據一些客戶的設定已成功：

```
Key: HKEY_CURRENT_USER\SOFTWARE\Microsoft\Microsoft Power BI Desktop
valueName: ShowLeadGenDialog
```

0 值會停用對話方塊。




有其他問題嗎？ [嘗試在 Power BI 社群提問](https://community.powerbi.com/)

