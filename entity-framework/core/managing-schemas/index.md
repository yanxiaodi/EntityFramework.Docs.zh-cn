---
title: 管理数据库架构 - EF Core
author: bricelam
ms.date: 10/30/2017
ms.openlocfilehash: 2da17865cb0192fb3e6e3396e4ca5f31fde9c52a
ms.sourcegitcommit: cc0ff36e46e9ed3527638f7208000e8521faef2e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2020
ms.locfileid: "78412732"
---
# <a name="managing-database-schemas"></a>管理数据库架构

EF Core 提供两种主要方法来保持 EF Core 模型和数据库架构同步。至于我们应该选用哪个方法，请确定你是希望以 EF Core 模型为准还是以数据库为准。

如果希望以 EF Core 模型为准，请使用[迁移][1]。 对 EF Core 模型进行更改时，此方法会以增量方式将相应架构更改应用到数据库，以使数据库保持与 EF Core 模型兼容。

如果希望以数据库架构为准，请使用[反向工程][2]。 使用此方法，可通过将数据库架构反向工程到 EF Core 模型来生成相应的 DbContext 和实体类型。

> [!NOTE]
> [创建和删除 API][3] 也可从 EF Core 模型创建数据库架构。 但是，它们主要适用于允许删除数据库的场景，比如测试、原型制作等。


  [1]: migrations/index.md
  [2]: scaffolding.md
  [3]: ensure-created.md
