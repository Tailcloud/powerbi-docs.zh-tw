---
title: 在儀表板圖格上執行及檢視見解
description: 以 Power BI 使用者角色了解如何取得和儀表板圖格有關的見解。
author: mihart
ms.reviewer: ''
featuredvideoid: et_MLSL2sA8
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 03/11/2020
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: 891a9b1a5afee26bdb2d6b363ccd2cee5f2461cb
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "79377275"
---
# <a name="view-data-insights-on-dashboard-tiles-with-power-bi"></a>使用 Power BI 在儀表板圖格上檢視資料見解

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]

儀表板上每個視覺效果[磚](end-user-tiles.md)都是資料探索的入口。 當您選取磚時，磚會開啟報表或[開啟問與答](end-user-q-and-a.md)，您可以在其中篩選和排序報表後方的資料集，並深入挖掘。 當您執行見解時，Power BI 會為您探索資料。

![省略符號功能表](./media/end-user-insights/power-bi-insight.png)

您可以執行見解以根據資料產生相關的互動式視覺效果。 您可對特定的儀表板磚執行見解，甚至可以對見解執行深入解析！

見解功能的建置基礎是一組會持續完善的[進階分析演算法](end-user-insight-types.md)，該演算法是與 Microsoft Research 合作開發，且會持續使用，讓更多人能透過全新的直覺式方式在資料中尋找見解。

## <a name="run-insights-on-a-dashboard-tile"></a>對儀表板磚執行深入解析
當您對儀表板磚執行見解時，Power BI 只會搜尋用來建立這一個儀表板磚的資料。 

1. [開啟儀表板](end-user-dashboards.md)。
2. 將游標停留在磚上方， 選取 [更多選項]  (...)，然後選擇 [檢視見解]  。 

    ![省略符號功能表](./media/end-user-insights/power-bi-hovers.png)


3. 隨即在[焦點模式](end-user-focus.md)中開啟磚，而深入解析卡片會沿著右側顯示。    
   
    ![焦點模式](./media/end-user-insights/power-bi-insights-tile.png)    
4. 一個深入剖析是否引起您的興趣？ 選取該資訊摘要卡片可挖掘更深入的資料。 選取的資訊摘要會顯示於左側，只以該單一資訊摘要中資料為依據的新資訊摘要卡片則沿著右側顯示。    

 ## <a name="interact-with-the-insight-cards"></a>與深入解析卡片互動
在您開啟見解之後，請繼續探索。

   * 篩選畫布上的視覺效果。  若要顯示篩選，請選取右上角的箭號來展開 [篩選] 窗格。

      ![展開 [篩選] 功能表的見解](./media/end-user-insights/power-bi-filters.png)
   
   * 對見解卡片本身執行見解。 這通常是指**相關的見解**。 選取要啟用的見解卡片。 它會顯示在您的報表畫布上。
   
      ![展開 [篩選] 功能表的見解](./media/end-user-insights/power-bi-insight-card.png)
   
   * 在右上角，選取燈泡圖示 ![取得見解圖示](./media/end-user-insights/power-bi-bulb-icon.png) 或 [取得見解]  。 深入解析會顯示於左側，而只以該單一深入解析資料為依據的新卡片則沿著右側顯示。
     
     ![顯示取得深入資訊圖示的功能表列](./media/end-user-insights/power-bi-related.png)
     
若要返回您的報表，請選取左上角的 [結束焦點模式]  。

## <a name="considerations-and-troubleshooting"></a>考量與疑難排解
- **檢視見解**並不適用於所有類型的儀表板磚。 例如，其不適用於 Power BI 視覺效果。<!--[Power BI visuals](end-user-custom-visuals.md)-->


## <a name="next-steps"></a>後續步驟
深入了解[可用深入資訊摘要類型](end-user-insight-types.md)

