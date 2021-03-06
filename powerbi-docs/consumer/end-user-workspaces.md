---
title: 如何在工作區中組織內容
description: 了解工作區和工作區角色
author: mihart
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 04/22/2020
ms.author: mihart
LocalizationGroup: Consumers
ms.openlocfilehash: 801b5cf5400bbe1cc0487eef596ea3d1cdc5fb1e
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "82120137"
---
# <a name="collaborate-in-workspaces"></a>在工作區中共同作業

 「工作區」  是與同事在特定內容上共同作業的地方。 工作區是使用 Power BI「設計工具」  所建立，用來保存儀表板和報表的集合。 然後，設計工具再將該集合組合到「應用程式」  ，並散發給整個組織或特定的人員或群組。 

 所有使用 Power BI 服務的人員也都會有 [我的工作區]  。  [我的工作區] 是個人沙箱，您可在此建立自己的內容。

 您可從 Power BI 的**首頁**，或從左側功能窗格中選取 [工作區]  或 [我的工作區]  來查看工作區。

 ![顯示兩種工作區類型的功能窗格](media/end-user-workspaces/power-bi-home.png)

## <a name="types-of-workspaces"></a>工作區類型
[我的工作區]  會儲存您擁有並建立的所有內容。 請將它視為您專屬內容的個人沙箱或工作區域。 對於許多 Power BI「取用者」  ，[我的工作區]  會保持空白，因為您的工作不會牽涉到建立新內容。 根據定義，「取用者」  會取用其他人所建立的資料，並使用該資料來制定商務決策。 如果您發現正在建立內容，請考慮改為閱讀[適用於「設計師」的 Power BI 文章](../create-reports/index.yml)。

[應用程式工作區]  包含特定應用程式的所有內容。 當「設計師」  建立應用程式時，會將該應用程式所需的所有內容組合在一起，以供使用。 內容可包含儀表板、報表和資料集。 並非所有應用程式都會包含這三種內容。 一個應用程式可以只包含一個儀表板、包含這三種內容類型，或甚至包含二十個報表。 這全都取決於「設計師」  包含在應用程式中的內容。 「取用者」  的應用程式工作區通常不包含資料集。

以下的無花果銷售應用程式工作區包含三份報表和一個儀表板。 

![顯示兩種工作區類型的功能窗格](media/end-user-workspaces/power-bi-app-workspace.png)

## <a name="roles-in-the-workspaces"></a>工作區中的角色

角色可決定您可以在工作區中做什麼，因此小組可以共同作業。  授與新工作區的存取權時，設計師  會將個人或群組新增至其中一個工作區角色：**檢視人員**、**成員**、**參與者**或**管理員**。 


身為 Power BI 的「取用者」  ，您在工作區中互動時一般會使用**檢視者**角色。 但是「設計工具」  也可能將您指派給**成員**或**參與者**角色。 檢視者角色可供檢視由其他人建立並與您共用的互動內容 (儀表板、報表、應用程式)。 而且因為檢視者角色不能存取基礎資料集，所以這是與內容互動的安全方式，不必擔心會「傷害」基礎資料。


如需以「取用者」  身分可使用檢視者角色執行操作的詳細清單，請參閱[取用者的 Power BI 功能](end-user-features.md)。


### <a name="workspace-roles"></a>工作區角色
以下是四種角色的功能：系統管理員、成員、參與者和檢視者。 除了檢視和互動功能以外，所有這些功能都需要 Power BI Pro 授權。

|功能   | 系統管理員  | 成員  | 參與者  | 檢視者 |
|---|---|---|---|---|
| 更新和刪除工作區。  | X  |   |   |   | 
| 新增/移除人員，包括其他系統管理員。  | X  |   |   |   |
| 新增具有較低權限的成員或其他人。  |  X | X  |   |   |
| 發佈和更新應用程式。 |  X | X  |   |   |
| 共用項目或共用應用程式。<sup>1</sup> |  X | X  |   |   |
| 允許其他人再次共用項目。<sup>1</sup> |  X | X  |   |   |
| 在同事的首頁上精選應用程式 |  X | X  |   |   |
| 在同事的首頁上精選儀表板和報表 |  X | X  | X |   |
| 建立、編輯和刪除工作區中的內容。  |  X | X  | X  |   |
| 將報表發佈至工作區、刪除內容。  |  X | X  | X  |   |
| 根據此工作區中的資料集，在另一個工作區中建立報表。<sup>1</sup> |  X | X  | X  |   |
| 複製報表。 | X | X | X |  |
| 檢視項目並與其互動。<sup>2</sup> |  X | X  | X  | X  |
| 讀取儲存在工作區資料流程中的資料 | X | X | X | X |

1. 如果參與者和成員都有 [再次共用] 權限，即可共用工作區中的項目。

2. 如果項目位於 Premium 容量的工作區中，則即使沒有 Power BI Pro 授權，您也可在 Power BI 服務中檢視項目並與其互動。

## <a name="licensing-workspaces-and-capacity"></a>授權、工作區和容量
授權還決定了您可以在工作區中執行及無法執行的動作。 許多功能都要求使用者具備 Power BI *Pro* 授權。 大部分的「取用者」  使用*免費*授權。 

如有免費授權，且工作區儲存在 *Premium 容量*中，即可檢視該工作區中的內容並與其互動。 菱形圖示表示工作區和應用程式儲存在 Premium 容量中。

![選取的工作區](media/end-user-workspaces/power-bi-diamond.png) 若要深入了解，請參閱[我擁有哪些授權？](end-user-license.md)



## <a name="next-steps"></a>後續步驟
* [Power BI 中的應用程式](end-user-apps.md)    

* 有問題嗎？ [嘗試在 Power BI 社群提問](https://community.powerbi.com/)

