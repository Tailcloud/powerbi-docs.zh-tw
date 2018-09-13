---
title: 監視您組織中的 Power BI Premium 容量
description: 使用 Power BI 系統管理入口網站與 Power BI Premium 容量計量應用程式
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 08/29/2018
LocalizationGroup: Premium
ms.openlocfilehash: 8e19bc596bef3862dca79ac92ffbd74954a9c756
ms.sourcegitcommit: 6be2c54f2703f307457360baef32aee16f338067
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/30/2018
ms.locfileid: "43300153"
---
# <a name="monitor-power-bi-premium-capacities-in-your-organization"></a>監視您組織中的 Power BI Premium 容量

此文章提供為您的 Power BI Premium 容量監視計量的概觀。 監視容量使用狀況可讓您據以管理您的容量。 

您可以使用 Power BI Premium 容量計量應用程式或在系統管理入口網站中監視容量。 我們建議使用該應用程式，因為它提供更多詳細資料，但此文章同時涵蓋這兩個選項。

## <a name="install-the-premium-capacity-metrics-app"></a>安裝 Premium 容量計量應用程式

您可以直接移至 [Premium 容量計量應用程式](https://app.powerbi.com/groups/me/getapps/services/capacitymetrics)，或在 Power BI 中如同安裝其他應用程式一樣安裝它。

> [!IMPORTANT]
> 若要安裝並使用此應用程式，您必須是至少一個容量的容量系統管理員。 光成為 Power BI 系統管理員並不夠。 

1. 在 Power BI 中，按一下 [應用程式]。

    ![移至 [應用程式]](media/service-admin-premium-monitor-capacity/apps.png)

2. 在右側，按一下 [取得應用程式]。

3. 在 [應用程式] 類別中，搜尋 **Power BI Premium 容量計量應用程式**。

4. 訂閱以安裝該應用程式。

現在您已安裝該應用程式，您可以查看您組織中關於容量的計量。 讓我們看看一些可用的重要計量。

## <a name="use-the-metrics-app"></a>使用計量應用程式 
當您開啟應用程式時，它會先顯示一個儀表板，其中包含您擁有系統管理權限之所有容量的摘要。

![Premium 報表概觀](media/service-admin-premium-monitor-capacity/app-dashboard.png)

### <a name="filtering"></a>篩選

[Filters applied to all pages] \(套用到所有頁面的篩選\) 索引標籤可讓您選取容量、資料集和/或過去七天內的日期範圍。 這些篩選會將選取範圍套用到此報表中的所有相關頁面與圖格。 若未選取任何項目，報表預設為顯示您擁有的每個容量過去一週的計量。

![Premium 報表概觀](media/service-admin-premium-monitor-capacity/premium-report-overview.png)

### <a name="summary-tab"></a>[摘要] 索引標籤

[摘要] 索引標籤會根據實體、系統與資料集顯示容量檢視。

![套用到所有頁面的篩選](media/service-admin-premium-monitor-capacity/premium-summary-report.png)

| **區域** | **計量** |
| --- | --- |
| **匙體** | * 您擁有的容量數目<br> * 您容量中的相異資料集數目<br> * 您容量中的相異工作區數目 |
| **系統** | * 過去七天內的平均記憶體使用量 (GB)<br> * 過去七天內最高記憶體使用量 (GB) 與發生的當地時間<br> * 過去七天內 CPU 超過閾值 80% 的次數 (分割為三分鐘的貯體)<br> * 過去七天內 CPU 超過 80% 的大部分次數 (分割為一小時的貯體) 與發生的當地時間<br> * 過去七天內直接查詢/即時連線超過閾值 80% 的次數 (分割為三分鐘的貯體)<br> * 過去七天內直接查詢/即時連線超過 80% 的大部分次數 (分割為一小時的貯體) 與發生的當地時間 |
| **資料集工作負載** | * 過去七天內的重新整理總數<br> * 過去七天內的成功重新整理總數<br> * 過去七天內的失敗重新整理總數<br> * 由於記憶體不足而失敗的重新整理總數<br> * 平均重新整理期間是以分鐘為單位來計量，完成作業的時間<br> * 平均重新整理等候時間是以分鐘為單位來計量，已排定的時間與作業開始之間的平均延隔時間<br> * 過去七天內執行的查詢總數<br> * 過去七天內的成功查詢總數<br> * 過去七天內的失敗查詢總數<br> * 平均查詢期間是以分鐘為單位來計量，完成作業的時間<br> * 由於記憶體壓力而撤出的模型總數 |
|  |  |

### <a name="refreshes-tab"></a>[重新整理] 索引標籤

[重新整理] 索引標籤列出過去七天內完成的重新整理次數、成功的計量次數、平均/最大重新整理等候時間與平均/最大重新整理間隔 (由資料集分割)。 底部的兩個圖表顯示重新整理與記憶體耗用量 (GB) 和分割為一小時貯體之平均等候時間 (以當地時間回報) 的比較。 頂端的橫條圖列出完成資料集重新整理 (重新整理期間) 與最大重新整理等候時間的前五個資料集與最大時間總計。 多個高重新整理等候時間突增表示容量使用率很高。

![Premium 重新整理報表](media/service-admin-premium-monitor-capacity/premium-refresh-report.png)

### <a name="datasets-tab"></a>[資料集] 索引標籤

[資料集] 索引標籤顯示過去一小時內由於記憶體壓力而撤出的完整資料集。

![Premium 資料集報表](media/service-admin-premium-monitor-capacity/premium-datasets-report.png)

### <a name="system-tab"></a>[系統] 索引標籤

[系統] 索引標籤顯示 CPU 高使用率 (超過 80% 使用率的次數)、直接查詢/即時連線高使用率與記憶體耗用。

![Premium 系統報表](media/service-admin-premium-monitor-capacity/premium-system-report.png)

## <a name="monitor-power-bi-embedded-capacity"></a>監視 Power BI Embedded 容量

我們也使用 Power BI Premium 容量計量應用程式來監視 Power BI Embedded 中的 *A SKU* 容量。 只要您是容量的系統管理員，那些容量就會顯示在報表中。 不過，除非您在 A SKU 上獲授與 Power BI 的特定權限，否則報表重新整理作業會失敗。

1. 在 Azure 入口網站中開啟您的容量。
1. 按一下 [存取控制 (IAM)]，並將 “Power BI Premium” 應用程式新增到讀者角色。 若您無法依名稱找到該應用程式，您也可以透過其用戶端識別碼來新增它：cb4dc29f-0bf4-402a-8b30-7511498ed654。

    ![Power BI Embedded 的權限](media/service-admin-premium-monitor-capacity/embedded-permissions.png)

> [!NOTE]
> 您可以在應用程式中或 Azure 入口網站中監視 Power BI Embedded 容量使用狀況，但無法在 Power BI 系統管理入口網站中這樣做。

## <a name="basic-monitoring-in-the-admin-portal"></a>系統管理入口網站中的基本監視

系統管理入口網站的 [容量設定] 區域提供四個量測計，這些量測計指出過去七天內您的容量所產生的負載與使用的資源量。 這四個圖格每小時更新一次，而且會指出過去七天內對應的計量超過 80% 的時數。 此計量指出可能的使用者體驗降級。

![7 天內的使用狀況](media/service-admin-premium-monitor-capacity/usage-in-days.png)

| **計量** | **描述** |
| --- | --- |
| CPU |CPU 超過 80% 使用率的次數。 |
| 記憶體過度置換 |代表後端核心的記憶體壓力。 具體而言，這個計量是因使用多個資料集的記憶體壓力而從記憶體收回資料集的次數。 |
| 記憶體使用量 |平均記憶體使用量，以吉位元組 (GB) 表示。 |
| DQ/s | 「直接查詢」和「即時連線」計數超過 80% 限制的次數。 <br> * 我們限制每秒的 DirectQuery 和即時連線查詢總數。* P1 的限制為每秒 30 個、P2 的限制為每秒 60 個，而 P3 的限制為每秒 120 個。 *「直接查詢」和即時連線查詢計數會新增至上面的節流。 例如，如果您每秒有 15 個 DirectQuery 和 15 個即時連線，您就達到節流標準。<br>* 這會平均套用至內部部署和雲端連線。 |
|  |  |

計量會反映過去一週的使用率。  如果您想要看到更詳細的計量檢視，則可以按一下任何摘要磚。  這會將您帶往進階容量之每個計量的詳細圖表。 下圖顯示 CPU 計量的詳細資料。

![詳細使用量圖表 CPU](media/service-admin-premium-monitor-capacity/premium-usage-detailed-chart-cpu.png)

這些圖表在過去一週每小時都會彙總一次，並有助於找出您何時可能已有進階容量的特定效能相關事件。

您也可以將任何計量的基礎資料匯出至 csv 檔案。  這個匯出會依每三分鐘的間隔提供過去一週每天的詳細資訊。

## <a name="next-steps"></a>後續步驟

現在您已了解如何監視 Power BI Premium 容量，請繼續學習如何最佳化容量。

> [!div class="nextstepaction"]
> [Power BI Premium 容量資源管理與最佳化](service-premium-understand-how-it-works.md)