---
description: "sys.dm_db_xtp_index_stats (Transact-SQL)"
title: "sys.dm_db_xtp_index_stats (Transact-SQL) | Microsoft Docs"
ms.custom: ""
ms.date: "08/29/2016"
ms.prod: sql
ms.prod_service: "database-engine, sql-database"
ms.reviewer: ""
ms.technology: system-objects
ms.topic: "reference"
f1_keywords: 
  - "sys.dm_db_xtp_index_stats"
  - "dm_db_xtp_index_stats"
  - "sys.dm_db_xtp_index_stats_TSQL"
  - "dm_db_xtp_index_stats_TSQL"
dev_langs: 
  - "TSQL"
helpviewer_keywords: 
  - "sys.dm_db_xtp_index_stats dynamic management view"
ms.assetid: 8d0a50b8-2015-4576-930f-e3307dfc888e
author: WilliamDAssafMSFT
ms.author: wiassaf
monikerRange: ">=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current"
---
# sys.dm_db_xtp_index_stats (Transact-SQL)
[!INCLUDE[sql-asdb-asdbmi](../../includes/applies-to-version/sql-asdb-asdbmi.md)]

  Contains statistics collected since the last database restart.  
  
 For more information, see [In-Memory OLTP &#40;In-Memory Optimization&#41;](../in-memory-oltp/overview-and-usage-scenarios.md) and [Guidelines for Using Indexes on Memory-Optimized Tables](/previous-versions/sql/sql-server-2016/dn133166(v=sql.130)).  

  
|Column name|Data type|Description|  
|-----------------|---------------|-----------------|  
|object_id|**bigint**|ID of the object to which this index belongs.|  
|xtp_object_id|**bigint**|Internal ID corresponding to the current version of the object.<br /><br /> Note: Applies to [!INCLUDE[sssql16-md](../../includes/sssql16-md.md)].|  
|index_id|**bigint**|ID of the index. The index_id is unique only within the object.|  
|scans_started|**bigint**|Number of In-Memory OLTP index scans performed. Every select, insert, update, or delete requires an index scan.|  
|scans_retries|**bigint**|Number of index scans that needed to be retried,|  
|rows_returned|**bigint**|Cumulative number of rows returned since the table was created or the start of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].|  
|rows_touched|**bigint**|Cumulative number of rows accessed since the table was created or the start of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].|  
|rows_expiring|**bigint**|Internal use only.|  
|rows_expired|**bigint**|Internal use only.|  
|rows_expired_removed|**bigint**|Internal use only.|  
|phantom_scans_started|**bigint**|Internal use only.|  
|phatom_scans_retries|**bigint**|Internal use only.|  
|phantom_rows_touched|**bigint**|Internal use only.|  
|phantom_expiring_rows_encountered|**bigint**|Internal use only.|  
|phantom_expired_rows_encountered|**bigint**|Internal use only.|  
|phantom_expired_removed_rows_encountered|**bigint**|Internal use only.|  
|phantom_expired_rows_removed|**bigint**|Internal use only.|  
|object_address|**varbinary(8)**|Internal use only.|  
  
## Permissions  
 Requires VIEW DATABASE STATE permission on the current database.  
  
## See Also  
 [Memory-Optimized Table Dynamic Management Views &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/memory-optimized-table-dynamic-management-views-transact-sql.md)  
