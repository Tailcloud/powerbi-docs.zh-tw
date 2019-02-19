---
title: 將報表匯出至 PDF
description: 了解如何將 Power BI 報表匯出至 PDF。
author: mihart
manager: kvivek
ms.custom: ''
ms.reviewer: cmfinlan
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 02/04/2019
ms.author: mihart
LocalizationGroup: Share your work
ms.openlocfilehash: c18257f1f4e4e3f325c8d4d895e3b6abf88e900c
ms.sourcegitcommit: 54d44deb6e03e518ad6378656c769b06f2a0b6dc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/07/2019
ms.locfileid: "55794980"
---
# <a name="export-reports-from-power-bi-to-pdf"></a>從 Power BI 將報表匯出至 PDF
有了 Power BI，您就可以將報表發佈至 PDF 格式，並根據 Power BI 報表輕鬆地建立文件。 當您**匯出至 PDF** 時，Power BI 報表中的每個頁面都會變成 PDF 文件中的個別頁面。

## <a name="how-to-export-your-power-bi-report-to-pdf"></a>如何將 Power BI 報表匯出至 PDF
在 Power BI 服務中，選取要顯示在畫布上的報表。 也可以從您的首頁、應用程式，或左側瀏覽窗格上的其他區段選取報表。

1. 從功能表列中選取 [檔案] > [匯出至 PDF]。

    ![從功能表列選取 [檔案]，將箭頭指向 [匯出至 PDF]](media/end-user-pdf/power-bi-export-pdf.png)

    進度列會顯示在右上角。 匯出可能需要幾分鐘的時間，而您可以在報表匯出時繼續使用 Power BI 工作。

    ![匯出進度訊息](media/end-user-pdf/power-bi-export-message.png)

    完成後，通知橫幅隨即變更，讓您知道 Power BI 服務已完成匯出程序。

2. 您可以在瀏覽器顯示下載檔案的位置取得檔案。 在下圖中，是以瀏覽器視窗底部的下載橫幅方式顯示。

    ![下載的檔案位置](media/end-user-pdf/power-bi-save-file.png)

就是這麼簡單。 您可以下載檔案，並以任何 PDF 檢視器開啟它，例如 Microsoft Edge 中提供的 PDF 檢視器。


## <a name="limitations-and-considerations"></a>限制與考量
使用 [匯出至 PDF] 功能時，需牢記幾項考量與限制。

- 匯出至 PDF 時，尚未支援工作階段內互動，例如反白顯示和篩選、向下切入等等。 匯出的 PDF 會顯示原來儲存在報表中的視覺效果。 如果您已套用篩選和交叉分析篩選器，並想要在匯出時保留它們，請儲存報表，然後進行匯出。

* 目前不支援 **R 視覺效果**。 在 PDF 中，這些視覺效果會是空白，並顯示錯誤訊息。  

* 目前已支援**經認證**的**自訂視覺效果**。 如需認證自訂視覺效果，包括如何使自訂視覺效果獲得認證的詳細資訊，請參閱[認證自訂視覺效果](../power-bi-custom-visuals-certified.md)。 不支援未經認證的自訂視覺效果。 在 PDF 中，將會顯示它們並出現錯誤訊息。   

* 目前無法匯出超過 30 頁的報表。

* 將報表匯出至 PDF 的程序需時數分鐘，請耐心等候。 影響所需時間的因素，包括報表結構及 Power BI 服務目前的負載。

* 如果 Power BI 服務中沒有 [匯出至 PDF] 功能表項目，可能是因為租用戶系統管理員停用了此功能。 如需詳細資訊，請連絡您的租用戶系統管理員。

* 背景影像會按圖表的周框區域剪裁。 強烈建議您先移除背景影像，再匯出至 PDF。

* Power BI 租用戶網域外部使用者擁有的報表 (例如，組織外部某人所擁有並與您共用的報表) 無法發佈至 PDF。

* 如果您與組織外部的某人 (也就是不在您 Power BI 租用戶中的使用者) 共用儀表板，該使用者會無法將與共用儀表板的相關報表匯出至 PDF。 舉例來說，如果您是 aaron@contoso.com，您可以和 cassie@cohowinery.com 共用。 但是 cassie@cohowinery.com 無法將相關報表匯出至 PDF。

* Power BI 服務會使用您的 Power BI 語言設定作為 PDF 的輸出語言。 若要查看或設定語言喜好設定，請選取齒輪圖示 > [設定] > [一般] > [語言]。

## <a name="next-steps"></a>後續步驟
[列印報表](end-user-print.md)