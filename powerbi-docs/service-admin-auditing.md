---
title: "在組織內使用稽核"
description: "了解您可以如何使用 Power BI 的稽核來監視和調查所執行的動作。 您可以使用安全與合規性中心或使用 PowerShell。"
services: powerbi
documentationcenter: 
author: guyinacube
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 11/02/2017
ms.author: asaxton
ms.openlocfilehash: a17bd787a37b7e26ac0b01ab5fc595b835e50b58
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2017
---
# <a name="using-auditing-within-your-organization"></a>在組織內使用稽核
<iframe width="560" height="315" src="https://www.youtube.com/embed/zj4kA39jV_4?showinfo=0" frameborder="0" allowfullscreen></iframe>

了解您可以如何使用 Power BI 的稽核來監視和調查所執行的動作。 您可以使用安全與合規性中心或使用 PowerShell。

了解誰正在對 Power BI 租用戶的哪個項目採取什麼動作，可能對於幫助貴組織符合其需求，例如符合法規合規性與記錄管理等而言極為重要。

您可以依日期範圍、使用者、儀表板、報表、資料集和活動類型來篩選稽核資料。 您也可以用 csv (逗號分隔值) 檔案下載活動以便離線分析。

> [!NOTE]
> Power BI 的稽核功能目前為預覽狀態，且所有資料區域皆可使用。
> 
> 

## <a name="enabling-auditing-functionality-in-the-power-bi-admin-portal"></a>在 Power BI 管理入口網站啟用稽核功能
您必須啟用稽核，貴組織才能使用報表。 您可以在管理入口網站的租用戶設定中完成。

1. 選擇右上角的**齒輪圖示**。
2. 選取 [管理入口網站]。
   
   ![](media/service-admin-auditing/powerbi-admin.png)
3. 選取 [租用戶設定]。
   
   ![](media/service-admin-auditing/powerbi-admin-tenant-settings.png)
4. 開啟 \[Create audit logs for internal activity auditing and compliance purposes] \(建立稽核記錄以用於內部活動稽核和合規性用途)。
5. 選取 [ **套用**]。

Power BI 會開始記錄您的使用者在 Power BI 中執行的各種活動。 記錄需要 48 小時才會顯示在 O365 安全與規範中心。 如需記錄哪些活動的詳細資訊，請參閱 [Power BI 稽核的活動清單](#list-of-activities-audited-by-power-bi)。

## <a name="licensing-requirements"></a>授權需求
稽核是 Power BI Pro 的功能，稽核事件只適用於 Power BI Pro 使用者　。  Power BI (免費) 授權的使用者將會顯示為**免費使用者**。

如需如何取得和指派 Power BI Pro 授權給組織使用者的詳細資訊，請參閱[購買 Power BI Pro](service-admin-purchasing-power-bi-pro.md)。

如需如何限制免費版使用者註冊的詳細資訊，請參閱[啟用或停用 Azure Active Directory 中的個人使用者註冊](service-admin-service-free-in-your-organization.md#enable-or-disable-individual-user-sign-up-in-azure-active-directory)。

> [!NOTE]
> 若要啟用租用戶中的 Power BI 稽核，您的租用戶中至少必須有一個 Exchange 信箱的授權。
> 
> 

## <a name="accessing-your-audit-logs"></a>存取您的稽核記錄
若要稽核您的 Power BI 記錄，您必須前往 Office 365 安全規範中心。

1. 選擇右上角的**齒輪圖示**。
2. 選取 [管理入口網站]。
   
   ![](media/service-admin-auditing/powerbi-admin.png)
3. 選取 [稽核記錄]。
4. 選取 [前往 O365 系統管理中心]。
   
   ![](media/service-admin-auditing/audit-log-o365-admin-center.png)

或者，您可以瀏覽 [Office 365 | 安全與規範](https://protection.office.com/#/unifiedauditlog)。

> [!NOTE]
> 若要提供非系統管理員帳戶存取稽核記錄的權限，您必須在 Exchange Online 系統管理中心中指派權限。 比方說，您可將使用者指派至現有的角色群組，例如組織管理，或者使用稽核記錄角色建立新的角色群組。 如需詳細資訊，請參閱 [Exchange Online 中的權限](https://technet.microsoft.com/library/jj200692\(v=exchg.150\).aspx)。
> 
> 

## <a name="search-only-power-bi-activities"></a>僅搜尋 Power BI 活動
您可以透過下列方式將結果限制在僅 Power BI 活動。

1. 在 [稽核記錄搜尋] 頁面上，從 [搜尋] 下選取 [活動] 的下拉式清單。
2. 選取 [PowerBI 活動]。
   
   ![](media/service-admin-auditing/audit-log-search-filter-by-powerbi.png)
3. 在選取方塊外面任何地方選取，將它關閉。

您的搜尋現在已篩選為僅限 Power BI 活動。

## <a name="search-the-audit-logs-by-date"></a>依日期搜尋稽核記錄
您可以使用 [開始日期] 和 [結束日期] 欄位，依日期範圍搜尋記錄。 預設會選取過去七天。 日期和時間是以國際標準時間 (UTC) 格式顯示。 您可以指定的最大日期範圍是 90 天。 如果選定的日期範圍超過 90 天，則會顯示錯誤。

> [!NOTE]
> 如果您使用最大的 90 天日期範圍，請選取目前時間作為開始日期。 否則，您會收到錯誤，指出開始日期早於結束日期。 如果您已在過去 90 天內開啟稽核，最大日期範圍的開頭不能在開啟稽核的日期之前。
> 
> 

![](media/service-admin-auditing/search-audit-log-by-date.png)

## <a name="search-the-audit-logs-by-users"></a>依使用者搜尋稽核記錄
您可以搜尋特定使用者所執行活動的稽核記錄項目。 若要這樣做，請在 [使用者] 欄位中輸入一或多個使用者名稱。  這是他們登入 Power BI 所使用的使用者名稱。 看起來像電子郵件地址。
將此方塊保留空白，可傳回貴組織所有使用者 (和服務帳戶) 的項目。

![](media/service-admin-auditing/search-audit-log-by-user.png)

## <a name="viewing-search-results"></a>檢視搜尋結果
一旦您點擊 [搜尋] 按鈕，搜尋結果會載入，並在一段時間後顯示在 [結果] 下。 搜尋完成後時，會顯示找到的結果數目。 

> [!NOTE]
> 將顯示最多 1000 個事件；如果超過 1000 個事件符合搜尋準則，則會顯示最新的 1000 個事件。
> 
> 

結果包含搜尋所傳回之每個事件的下列相關資訊。

| **資料行** | **定義** |
| --- | --- |
| 日期 |發生事件時的日期和時間 (UTC 格式)。 |
| IP 位址 |記錄活動時所用裝置的 IP 位址。 IP 位址會以 IPv4 或 IPv6 位址格式顯示。 |
| 使用者 |執行觸發事件之動作的使用者 (或服務帳戶)。 |
| 活動 |使用者所執行的活動。 這個值會對應至您在 [活動] 下拉式清單中選取的活動。 對於來自 Exchange 系統管理員稽核記錄的事件，此資料行中的值會是 Exchange Cmdlet。 |
| 項目 |因為對應活動而建立或修改的物件。 例如，被檢視或修改的檔案，或是被更新的使用者帳戶。 並非所有活動在此資料行中都有值。 |
| 詳細資料 |關於活動的其他詳細資料。 同樣地，並非所有活動都有值。 |

> [!NOTE]
> 選取 [結果] 下的資料行標頭可排序結果。 您可以將結果從 A 到 Z 或從 Z 到 A 排序。按一下 [日期] 標頭可以將結果從最舊到最新或從最新到最舊排序。
> 
> 

## <a name="view-the-details-for-an-event"></a>檢視事件的詳細資料
您可以選取搜尋結果清單中的事件記錄，檢視事件的詳細資料。 [詳細資料] 頁面隨即出現，其中包含事件記錄的詳細屬性。 所顯示的屬性取決於發生事件的 Office 365 服務。 若要顯示其他詳細資料，請選取 [更多資訊]。

下表提供您會看到顯示出來之項目的詳細資料。

| **參數** | **描述** |
| --- | --- |
| Id |稽核記錄的唯一識別碼。 |
| RecordType |記錄所指出的作業類型。 如需稽核記錄記錄類型的詳細資料，請參閱 AuditLogRecordType 資料表。 |
| CreationTime |使用者執行活動時的日期和時間，國際標準時間 (UTC) 格式。 |
| Operation |使用者或管理員活動的名稱。 |
| OrganizationId |發生事件的組織 Office 365 服務的 GUID。 |
| UserType |執行作業的使用者類型。 如需使用者類型的詳細資料，請參閱使用者類型資料表。 |
| UserKey |執行活動之使用者的 Passport 唯一識別碼。 |
| ResultStatus |指出動作 (在 Operation 屬性中指定) 是否已成功。 可能的值為 Succedded、PartiallySucceded 或 Failed。 |
| ObjectId |對於 SharePoint 和商務用 OneDrive 活動，這是使用者存取的檔案或資料夾的完整路徑名稱。 |
| UserId |執行導致記錄該筆記錄之動作 (在 Operation 屬性中指定) 的使用者 UPN (使用者主體名稱)，例如 my_name@my_domain_name。 請注意，系統帳戶 (例如 SHAREPOINT\system 或 NT AUTHORITY\SYSTEM) 所執行的活動記錄也包含在內。 |
| ClientIp |記錄活動時所用裝置的 IP 位址。 IP 位址會以 IPv4 或 IPv6 位址格式顯示。 |

下表提供您可能會看到之事件的詳細資料。

| **事件** | **描述** | **其他詳細資料** |
| --- | --- | --- |
| 下載 Power BI 報表 |每次下載報表時，會記錄此活動 |報表名稱、資料集名稱 |
| 建立報表 |每次建立新報表時，會記錄此活動。 |報表名稱、資料集名稱 |
| 編輯報表 |每次編輯報表時，會記錄此活動。 |報表名稱、資料集名稱 |
| 建立資料集 |每次建立資料集時，會記錄此活動。 |資料集名稱、DataConnectivityMode |
| 刪除資料集 |每次刪除資料集時，會記錄此活動。 |資料集名稱、DataConnectivityMode |
| 建立 Power BI 應用程式 |每次建立 Power BI 應用程式時，會記錄此活動 |應用程式名稱、權限、工作區名稱 |
| 安裝 Power BI 應用程式 |每次安裝 Power BI 應用程式時，會記錄此活動 |應用程式名稱 |
| 更新 Power BI 應用程式 |每次更新 Power BI 應用程式時，會記錄此活動 |應用程式名稱、權限、工作區名稱 |
| 已啟動 Power BI 延長試用版 |每次使用者接受會執行直到 2018 年 5 月 31 日的延長 Pro 試用版時，會記錄此活動 | |
| 已分析 Power BI 資料集 |每次在 Excel 中分析 Power BI 資料集時，會記錄此活動。 | |
| 已建立 Power BI 閘道 |每次建立新閘道時，會記錄此活動。 |閘道名稱、閘道類型 |
| 已刪除 Power BI 閘道 |每次刪除閘道時，會記錄此活動。 |閘道名稱、閘道類型 |
| 已將資料來源新增至 Power BI 閘道 |每次將資料來源新增至閘道時，會記錄此活動 |閘道名稱、閘道類型、資料來源名稱、資料來源類型 |
| 已從 Power BI 閘道移除資料來源 |每次從閘道移除資料來源時，會記錄此活動 |閘道名稱、閘道類型、資料來源名稱、資料來源類型 |
| 已變更 Power BI 閘道管理員 |每次變更 (新增/移除) 閘道管理員時，會記錄此活動 |閘道名稱、已新增使用者、已移除使用者 |
| 已變更 Power BI 閘道資料來源使用者 |每次變更 (新增/移除) 閘道使用者時，會記錄此活動 |閘道名稱、已新增使用者、已移除使用者 |
| SetScheduledRefresh |每次為資料集排程新的重新整理時，會記錄此活動 |資料集名稱、重新整理頻率 (以分鐘為單位) |

## <a name="using-powershell-to-search"></a>使用 PowerShell 進行搜尋
您可以使用 PowerShell，依據您的登入存取稽核記錄。 這是藉由存取 Exchange Online 來執行的。 以下是提取 Power BI 稽核記錄項目的命令範例。

> [!NOTE]
> 若要使用 New-PSSession 命令，您的帳戶需要獲指派 Exchange Online 授權，而且您需要存取租用戶的稽核記錄檔。
> 
> 

```
Set-ExecutionPolicy RemoteSigned

$UserCredential = Get-Credential

$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection

Import-PSSession $Session
Search-UnifiedAuditLog -StartDate 9/11/2016 -EndDate 9/15/2016 -RecordType PowerBI -ResultSize 1000 | Format-Table | More
```

如需如何連線至 Exchange Online 的詳細資訊，請參閱[連線至 Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289\(v=exchg.160\).aspx)。

如需參數和 Search-UnifiedAuditLog 命令使用方式的詳細資訊，請參閱 [Search-UnifiedAuditLog](https://technet.microsoft.com/library/mt238501\(v=exchg.160\).aspx)。

若要查看使用 PowerShell 搜尋稽核記錄檔後再根據項目指派 Power BI Pro 授權的範例，請參閱 [Using Power BI audit log and PowerShell to assign Power BI Pro licenses](https://powerbi.microsoft.com/blog/using-power-bi-audit-log-and-powershell-to-assign-power-bi-pro-licenses/) (使用 Power BI 稽核記錄檔和 PowerShell 指派 Power BI Pro 授權)。

## <a name="export-the-power-bi-audit-log"></a>匯出 Power BI 稽核記錄
您可以將 Power BI 稽核記錄匯出至 csv 檔案。

1. 選取 [匯出結果]。
2. 選取 \[Save loaded results] \(儲存載入結果) 或 \[Download all results] \(下載所有結果)。
   
   ![](media/service-admin-auditing/export-auditing-results.png)

## <a name="record-and-user-types"></a>記錄和使用者類型
作為項目詳細資料的一部分，稽核記錄項目會具有 RecordType 和 UserType。 所有 Power BI 項目的 RecordType 都是 20。

如需完整清單，請參閱 [Detailed properties in the Office 365 audit log](https://support.office.com/article/Detailed-properties-in-the-Office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3) (Office 365 稽核記錄的詳細內容)

## <a name="list-of-activities-audited-by-power-bi"></a>Power BI 稽核的活動清單
| 活動 | 描述 | 其他詳細資料 |
| --- | --- | --- |
| CreateDashboard |每次建立新的儀表板時，會記錄此活動。 |- 儀表板名稱。 |
| EditDashboard |每次重新命名儀表板時，會記錄此活動。 |- 儀表板名稱。 |
| DeleteDashboard |每次刪除儀表板時，會記錄此活動。 |- 儀表板名稱。 |
| PrintDashboard |每次列印儀表板時，都會記錄此事件。 |- 儀表板名稱。<br/>- 資料集名稱 |
| ShareDashboard |每次共用儀表板時，會記錄此活動。 |- 儀表板名稱。<br/>- 收件者電子郵件。<br/>- 資料集名稱。<br>- 再次共用權限。 |
| ViewDashboard |每次檢視儀表板時，都會記錄此活動。 |- 儀表板名稱。 |
| ExportTile |每次從儀表板磚匯出資料時，都會記錄此事件。 |- 磚名稱。<br/>- 資料集名稱。 |
| DeleteReport |每次刪除報表時，會記錄此活動。 |- 報表名稱。 |
| ExportReport |每次從報表磚匯出資料時，都會記錄此事件。 |- 報表名稱。<br/>- 資料集名稱。 |
| PrintReport |每次列印報表時，都會記錄此事件。 |- 報表名稱。<br/>- 資料集名稱。 |
| PublishToWebReport |每次將報表發行至 Web 時，都會記錄此事件。 |- 報表名稱。<br/>- 資料集名稱。 |
| ViewReport |每次檢視報表時，都會記錄此活動。 |- 報表名稱。 |
| ExploreDataset |每次您選取資料集以進行瀏覽時，都會記錄此活動。 |- 資料集名稱 |
| DeleteDataset |每次刪除資料集時，都會記錄此事件。 |- 資料集名稱。 |
| CreateOrgApp |每次建立組織內容套件時，會記錄此活動。 |- 組織內容套件名稱。<br/>- 儀表板名稱。<br/>- 報表名稱。<br/>- 資料集名稱。 |
| CreateGroup |每次建立群組時，就會引發這項活動。 |- 群組名稱。 |
| AddGroupMembers |每次成員加入 Power BI 群組工作區時，會記錄此活動。 |- 群組名稱。<br/>- 電子郵件地址。 |
| UpdatedAdminFeatureSwitch |每次變更管理功能參數時，都會記錄此事件。 |- 參數名稱。<br/>- 新的參數狀態。 |
| OptInForProTrial |當使用者選擇在服務中試用 Power BI Pro 時，就會記錄此事件。 |- 電子郵件地址 |

## <a name="next-steps"></a>後續步驟
[Power BI 管理入口網站](service-admin-portal.md)  
[Power BI Premium - 這是什麼？](service-premium.md)  
[購買 Power BI Pro](service-admin-purchasing-power-bi-pro.md)  
[Exchange Online 中的權限](https://technet.microsoft.com/library/jj200692\(v=exchg.150\).aspx)  
[連線至 Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289\(v=exchg.160\).aspx)  
[Search-UnifiedAuditLog](https://technet.microsoft.com/library/mt238501\(v=exchg.160\).aspx)  
[Office 365 稽核記錄的詳細內容](https://support.office.com/article/Detailed-properties-in-the-Office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3)  

有其他問題嗎？ [嘗試在 Power BI 社群提問](http://community.powerbi.com/)
