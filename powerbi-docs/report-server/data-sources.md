---
title: Power BI 報表伺服器中的 Power BI 報表資料來源
description: Power BI 報表可以連接到數種資料來源。 根據使用資料的方式而定，可以使用不同的資料來源。
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 04/08/2020
ms.author: maggies
ms.openlocfilehash: 166f72a717c99457e1d6b8e9a1f30535a9b4686f
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "80979837"
---
# <a name="power-bi-report-data-sources-in-power-bi-report-server"></a>Power BI 報表伺服器中的 Power BI 報表資料來源
Power BI 報表可以連接到數種資料來源。 根據使用資料的方式而定，可以使用不同的資料來源。 可以匯入資料，或者使用 DirectQuery 或與 SQL Server Analysis Services 的即時連線，直接查詢資料。

這些資料來源專屬於 Power BI 報表伺服器中使用的 Power BI 報表。 如需支援分頁報表 (.rdl) 的資料來源詳細資訊，請參閱 [Reporting Services 支援的資料來源](https://docs.microsoft.com/sql/reporting-services/report-data/data-sources-supported-by-reporting-services-ssrs)。

> [!IMPORTANT]
> Power BI Desktop 報表中的所有資料來源都必須支援設定排定的重新整理。
>  

## <a name="list-of-supported-data-sources"></a>支援的資料來源清單

其他資料來源可以運作，即使它們不在支援的清單中。

| **資料來源** | **快取資料** | **排程的重新整理** | **即時/DirectQuery** |
| --- | --- | --- | --- |
| SQL Server 資料庫 |有 |有 |有 |
| SQL Server Analysis Services |有 |有 |有 |
| Azure SQL Database |有 |有 |有 |
| Azure SQL 資料倉儲 |有 |有 |有 |
| Excel |有 |有 |否 |
| Access 資料庫 |有 |有 |否 |
| Active Directory |有 |有 |否 |
| Amazon Redshift |有 |否 |否 |
| Azure Blob 儲存體 |有 |有 |否 |
| Azure Data Lake Store |有 |否 |否 |
| Azure HDInsight (HDFS) |有 |否 |否 |
| Azure HDInsight (Spark) |有 |否 |否 |
| Azure 資料表儲存體 |有 |有 |否 |
| Dynamics 365 (線上) |有 |否 |否 |
| Facebook |有 |否 |否 |
| 資料夾 |有 |有 |否 |
| Google Analytics (分析) |有 |否 |否 |
| Hadoop 檔案 (HDFS) |有 |否 |否 |
| IBM DB2 資料庫 |有 |有 |否 |
| Impala |有 |否 |否 |
| JSON |有 |有 |否 |
| Microsoft Exchange |有 |否 |否 |
| Microsoft Exchange Online |有 |否 |否 |
| MySQL 資料庫 |有 |有 |否 |
| OData 摘要 |有 |有 |否 |
| ODBC |有 |有 |否 |
| OLE DB |有 |有 |否 |
| Oracle 資料庫 |有 |有 |有 |
| PostgreSQL 資料庫 |有 |有 |否 |
| Power BI 服務 |否 |否 |否 |
| R Script |有 |否 |否 |
| Salesforce 物件 |有 |否 |否 |
| Salesforce 報表 |有 |否 |否 |
| SAP Business Warehouse 伺服器 |有 |有 |有 |
| SAP HANA 資料庫 |有 |有 |有 |
| SharePoint 資料夾 (內部部署) |有 |有 |否 |
| SharePoint 清單 (內部部署) |有 |有 |否 |
| SharePoint Online 清單 |有 |否 |否 |
| 雪花式 |有 |否 |否 |
| Sybase 資料庫 |有 |有 |否 |
| Teradata |有 |有 |有 |
| 文字/CSV |有 |有 |否 |
| Web |有 |有 |否 |
| XML |有 |有 |否 |
| appFigures (Beta) |有 |否 |否 |
| Azure Analysis Services 資料庫 |有 |否 |有 |
| Azure Cosmos DB (搶鮮版 (Beta)) |有 |否 |否 |
| Azure HDInsight Spark (Beta) |有 |否 |否 |
| Common Data Service (搶鮮版 (Beta)) |有 |否 |否 |
| comScore Digital Analytix (Beta) |有 |否 |否 |
| Dynamics 365 for Customer Insights (搶鮮版 (Beta)) |有 |否 |否 |
| Dynamics 365 for Financials (搶鮮版 (Beta)) |有 |否 |否 |
| GitHub (Beta) |有 |否 |否 |
| Google BigQuery (搶鮮版 (Beta)) |有 |否 |否 |
| IBM Informix 資料庫 (搶鮮版 (Beta)) |有 |否 |否 |
| IBM Netezza (搶鮮版 (Beta)) |有 |否 |否 |
| Kusto (搶鮮版 (Beta)) |有 |否 |否 |
| MailChimp (搶鮮版 (Beta)) |有 |否 |否 |
| Microsoft Azure 使用量見解 (搶鮮版 (Beta)) |有 |否 |否 |
| Mixpanel (搶鮮版 (Beta)) |有 |否 |否 |
| Planview Enterprise (Beta) |有 |否 |否 |
| Projectplace (搶鮮版 (Beta)) |有 |否 |否 |
| QuickBooks Online (搶鮮版 (Beta)) |有 |否 |否 |
| Smartsheet |有 |否 |否 |
| Spark (Beta) |有 |否 |否 |
| SparkPost (搶鮮版 (Beta)) |有 |否 |否 |
| SQL Sentry (Beta) |有 |否 |否 |
| Stripe (搶鮮版 (Beta)) |有 |否 |否 |
| SweetIQ (Beta) |有 |否 |否 |
| Troux (Beta) |有 |否 |否 |
| Twilio (搶鮮版 (Beta)) |有 |否 |否 |
| tyGraph (Beta) |有 |否 |否 |
| Vertica (搶鮮版 (Beta)) |有 |否 |否 |
| Visual Studio Team Services (Beta) |有 |否 |否 |
| Webtrends (Beta) |有 |否 |否 |
| Zendesk (Beta) |有 |否 |否 |

> [!IMPORTANT]
> 在資料來源設定的資料列層級安全性，應該適用於特定 DirectQuery (SQL Server、Azure SQL Database、Oracle 和 Teradata)，且即時連線假設 Kerberos 已在您的環境中適當設定。
> 
> 

## <a name="list-of-supported-authentication-methods-for-model-refresh"></a>模型重新整理支援的驗證方法清單

Power BI 報表伺服器對模型重新整理不支援 OAuth 型驗證。 例如 Excel 或 Access 資料庫等某些資料來源，會使用檔案或 Web 等不同步驟來連線到資料。

| **資料來源** | **匿名驗證** | **金鑰驗證** | **使用者名稱及密碼** | **Windows 驗證** |
| --- | --- | --- | --- | --- |
| SQL Server 資料庫 |否 |否 |有 |有 |
| SQL Server Analysis Services |否 |否 |有 |有 |
| Web |有 |否 |有 |有 |
| Azure SQL Database |否 |否 |有 |否 |
| Azure SQL 資料倉儲 |否 |否 |有 |否 |
| Active Directory |否 |否 |有 |有 |
| Amazon Redshift |否 |否 |否 |否 |
| Azure Blob 儲存體 |有 |有 |否 |否 |
| Azure Data Lake Store |否 |否 |否 |否 |
| Azure HDInsight (HDFS) |否 |否 |否 |否 |
| Azure HDInsight (Spark) |否 |否 |否 |否 |
| Azure 資料表儲存體 |否 |有 |否 |否 |
| Dynamics 365 (線上) |否 |否 |否 |否 |
| Facebook |否 |否 |否 |否 |
| 資料夾 |否 |否 |否 |有 |
| Google Analytics (分析) |否 |否 |否 |否 |
| Hadoop 檔案 (HDFS) |否 |否 |否 |否 |
| IBM DB2 資料庫 |否 |否 |有 |有 |
| Impala |否 |否 |否 |否 |
| Microsoft Exchange |否 |否 |否 |否 |
| Microsoft Exchange Online |否 |否 |否 |否 |
| MySQL 資料庫 |否 |否 |有 |有 |
| OData 摘要 |有 |有 |有 |有 |
| ODBC |有 |否 |有 |有 |
| OLE DB |有 |否 |有 |有 |
| Oracle 資料庫 |否 |否 |有 |有 |
| PostgreSQL 資料庫 |否 |否 |有 |否 |
| Power BI 服務 |否 |否 |否 |否 |
| R Script |否 |否 |否 |否 |
| Salesforce 物件 |否 |否 |否 |否 |
| Salesforce 報表 |否 |否 |否 |否 |
| SAP Business Warehouse 伺服器 |否 |否 |有 |否 |
| SAP HANA 資料庫 |否 |否 |有 |有 |
| SharePoint 資料夾 (內部部署) |有 |否 |否 |有 |
| SharePoint 清單 (內部部署) |有 |否 |否 |有 |
| SharePoint Online 清單 |否 |否 |否 |否 |
| 雪花式 |否 |否 |否 |否 |
| Sybase 資料庫 |否 |否 |有 |有 |
| Teradata |否 |否 |有 |是** |
| appFigures (Beta) |否 |否 |否 |否 |
| Azure Analysis Services 資料庫 (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Azure Cosmos DB (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Azure HDInsight Spark (Beta) |否 |否 |否 |否 |
| Common Data Service (搶鮮版 (Beta)) |否 |否 |否 |否 |
| comScore Digital Analytix (Beta) |否 |否 |否 |否 |
| Dynamics 365 for Customer Insights (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Dynamics 365 for Financials (搶鮮版 (Beta)) |否 |否 |否 |否 |
| GitHub (Beta) |否 |否 |否 |否 |
| Google BigQuery (搶鮮版 (Beta)) |否 |否 |否 |否 |
| IBM Informix 資料庫 (搶鮮版 (Beta)) |否 |否 |否 |否 |
| IBM Netezza (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Kusto (搶鮮版 (Beta)) |否 |否 |否 |否 |
| MailChimp (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Microsoft Azure 使用量見解 (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Mixpanel (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Planview Enterprise (Beta) |否 |否 |否 |否 |
| Projectplace (搶鮮版 (Beta)) |否 |否 |否 |否 |
| QuickBooks Online (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Smartsheet |否 |否 |否 |否 |
| Spark (Beta) |否 |否 |否 |否 |
| SparkPost (搶鮮版 (Beta)) |否 |否 |否 |否 |
| SQL Sentry (Beta) |否 |否 |否 |否 |
| Stripe (搶鮮版 (Beta)) |否 |否 |否 |否 |
| SweetIQ (Beta) |否 |否 |否 |否 |
| Troux (Beta) |否 |否 |否 |否 |
| Twilio (搶鮮版 (Beta)) |否 |否 |否 |否 |
| tyGraph (Beta) |否 |否 |否 |否 |
| Vertica (搶鮮版 (Beta)) |否 |否 |否 |否 |
| Visual Studio Team Services (Beta) |否 |否 |否 |否 |
| Webtrends (Beta) |否 |否 |否 |否 |
| Zendesk (Beta) |否 |否 |否 |否 |

**使用 LDAP 驗證搭配 Teradata (使用命令提示字元命令 'setx PBI_EnableTeradataLdap true' 在 Power BI Desktop 中啟用) 不支援模型重新整理。

## <a name="list-of-supported-authentication-methods-for-directquery"></a>DirectQuery 支援的驗證方法清單

Power BI 報表伺服器對 DirectQuery 不支援 OAuth 型驗證。

| **資料來源** | **匿名驗證** | **金鑰驗證** | **使用者名稱及密碼** | **Windows 驗證** | **整合式 Windows 驗證** |
| --- | --- | --- | --- | --- | --- |
| SQL Server 資料庫 |否 |否 |有 |有 |有 |
| SQL Server Analysis Services |否 |否 |有 |有 |有 |
| Azure SQL Database |否 |否 |有 |否 |否 |
| Azure SQL 資料倉儲 |否 |否 |有 |否 |否 |
| Oracle 資料庫 |否 |否 |有 |有 |有 |
| SAP Business Warehouse 伺服器 |否 |否 |有 |否 |否 |
| SAP HANA 資料庫 |否 |否 |有 |有 |是** |
| Teradata |否 |否 |有 |有 |有 |

**SAP HANA 只有在使用其作為所發佈 Power BI Desktop 檔案 (.pbix) 中的關聯式資料庫時，才支援使用整合式 Windows 驗證的 DirectQuery。

## <a name="next-steps"></a>後續步驟
您現在已經連接到您的資料來源，接著可以使用來自該資料來源的資料[建立 Power BI 報表](quickstart-create-powerbi-report.md)。

有其他問題嗎？ [嘗試在 Power BI 社群提問](https://community.powerbi.com/)
