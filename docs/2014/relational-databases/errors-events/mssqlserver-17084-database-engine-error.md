---
title: "MSSQLSERVER_17084 | Microsoft Docs"
ms.custom: ""
ms.date: "03/06/2017"
ms.prod: "sql-server-2014"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "database-engine"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "17084 (Database Engine error)"
ms.assetid: e579d104-3307-4edd-8587-b14ecbc02ed9
caps.latest.revision: 8
author: "JennieHubbard"
ms.author: "jhubbard"
manager: "jhubbard"
---
# MSSQLSERVER_17084
    
## Details  
  
|||  
|-|-|  
|Product Name|[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]|  
|Event ID|17084|  
|Event Source|MSSQLSERVER|  
|Component|SQLEngine|  
|Symbolic Name|P3_ATOMIC_WITH_MISSING_OPTION|  
|Message Text|The WITH clause of BEGIN ATOMIC statement must specify a value for the option '%ls'.|  
  
## Explanation  
 The WITH clause of BEGIN ATOMIC statement did not specify a value for an option.  
  
## User Action  
 `ATOMIC` blocks require values for the `WITH` options `TRANSACTION ISOLATION LEVEL` and `LANGUAGE`. For example::  
  
```  
BEGIN ATOMIC WITH (TRANSACTION ISOLATION LEVEL = SNAPSHOT, LANGUAGE= N’us_english’)  
```  
  
 For more information, see [In-Memory OLTP &#40;In-Memory Optimization&#41;](../in-memory-oltp/in-memory-oltp-in-memory-optimization.md).  
  
## See Also  
 [In-Memory OLTP &#40;In-Memory Optimization&#41;](../in-memory-oltp/in-memory-oltp-in-memory-optimization.md)  
  
  