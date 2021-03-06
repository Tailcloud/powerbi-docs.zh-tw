---
title: 使用 PowerShell 變更資料來源連接字串
description: 在 PowerShell 中使用 API 變更資料來源連接字串 - Power BI 報表伺服器。
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 01/21/2020
ms.author: maggies
ms.openlocfilehash: 9ca5d47a938210c10903c916c54713b89923e287
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "80751530"
---
# <a name="change-data-source-connection-strings-in-power-bi-reports-with-powershell---power-bi-report-server"></a>在 PowerShell 報表中使用 PowerShell 變更資料來源連接字串 - Power BI 報表伺服器


您可以在 PowerShell 中使用 API，在 Power BI 報表伺服器的 Power BI 報表中變更資料來源連接字串。 

> [!NOTE]
> 此功能目前僅適用於 DirectQuery。 即將推出匯入和資料重新整理的支援。

1. 安裝 Power BI 報表伺服器 PowerShell commandlet。 在 [https://github.com/Microsoft/ReportingServicesTools](https://github.com/Microsoft/ReportingServicesTools) 尋找 commandlet 和安裝指示。 

2. 透過 PowerShell commandlet，擷取 Power BI 檔案的現有資料來源資訊：

    ```powershell
    Get-RsRestItemDataSource -RsItem '/MyPbixReport'
    ```

    檢視 Power BI 報表中包含的第一個資料來源相關資訊： 

    ```powershell
    $dataSources[0]
    ```

3. 視需要更新連接和認證資訊。 如果更新連接字串，且資料來源會使用預存認證，您就必須提供帳戶密碼。 

    更新資料來源連接字串：

    ```powershell
    $dataSources[0].ConnectionString = 'data source=myCatalogServer;initial catalog=ReportServer;persist security info=False' 
    ```

    變更資料來源認證類型：

    ```powershell
    $dataSources[0].DataModelDataSource.AuthType = 'Integrated'
    ```

    變更資料來源使用者名稱/密碼：

    ```powershell
    $dataSources[0].DataModelDataSource.Username = 'domain\user'
    ```
    ```powershell
    $dataSources[0].DataModelDataSource.Secret = 'password'
    ```

4. 將更新的認證儲存回伺服器。

    ```powershell
    Set-RsRestItemDataSource -RsItem '/MyPbixReport' -RsItemType 'PowerBIReport' -DataSources $dataSources
    ```

## <a name="next-steps"></a>後續步驟

[Power BI 報表伺服器中的分頁報表資料來源](connect-data-sources.md) 

有其他問題嗎？ [嘗試在 Power BI 社群提問](https://community.powerbi.com/)
