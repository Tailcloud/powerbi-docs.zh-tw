---
title: "在 Power BI Desktop 中連接至 CSV 檔案"
description: "在 Power BI Desktop 中輕鬆地連接至 CSV 檔案資料並加以使用"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 8fa6870a7ca7b362b9ce71224845a4194805bae8
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/06/2017
---
# <a name="connect-to-csv-files-in-power-bi-desktop"></a>在 Power BI Desktop 中連接至 CSV 檔案
從 Power BI Desktop 連接至以逗號分隔的值 (*CSV*) 檔案與連接至 Excel 活頁簿十分相似。 兩者都很簡單，而本文章會引導您了解如何連接至任何您具有存取權的 CSV 檔案。

首先，在 Power BI Desktop 中，從 [主資料夾] 功能區選取 [取得資料] > [CSV]。

![](media/desktop-connect-csv/connect-to-csv_1.png)

從出現的 [開啟] 對話方塊中選取您的 CSV 檔。

![](media/desktop-connect-csv/connect-to-csv_2.png)

當您選取 [開啟] 時，Power BI Desktop 會存取檔案並判斷特定的檔案屬性，例如檔案來源、分隔符號類型，以及應該使用多少資料列來偵測檔案中的資料類型。

這些檔案屬性和選項會顯示在 [CSV 匯入] 對話方塊視窗頂端的下拉式清單選取項目中，如下所示。 藉由從任何下拉式清單選取器中選擇另一個選項，您可以手動變更任何偵測到的設定。

![](media/desktop-connect-csv/connect-to-csv_3.png)

當您滿意所做的選擇時，您可以選取 [載入] 將檔案匯入 Power BI Desktop，或者您可以選取 [編輯] 開啟 [查詢編輯器]，並且在匯入之前進一步修改或轉換資料。

一旦您將資料載入 Power BI Desktop，您會看到 [欄位] 窗格中的資料表和其資料行 (其會顯示為 Power BI Desktop 中的欄位)，就位於 Power BI Desktop 中 [報告檢視] 的右側。

![](media/desktop-connect-csv/connect-to-csv_4.png)

這樣就完成了 – 您 CSV 檔案中的資料現在已經位在 Power BI Desktop 之中了。

您可以使用 Power BI Desktop 中的資料來建立視覺效果、報表，或與您可能會想要連接和匯入的其他資料進行互動，例如 Excel 活頁簿、資料庫或任何其他資料來源。

### <a name="next-steps"></a>後續步驟
您可以使用 Power BI Desktop 連接至各式各樣的資料。 如需有關資料來源的詳細資訊，請參閱下列資源︰

* [開始使用 Power BI Desktop](desktop-getting-started.md)
* [Power BI Desktop 中的資料來源](desktop-data-sources.md)
* [使用 Power BI Desktop 合併資料並使其成形](desktop-shape-and-combine-data.md)
* [在 Power BI Desktop 中連接至 Excel 活頁簿](desktop-connect-excel.md)   
* [直接將資料輸入 Power BI Desktop 中](desktop-enter-data-directly-into-desktop.md)   
