---
title: "dotNet NuGet 命令 |Microsoft 文档"
author: kraigb
ms.author: kraigb
manager: ghogen
ms.date: 12/08/2017
ms.topic: article
ms.prod: nuget
ms.technology: 
ms.assetid: 0c81dbc4-2c14-4ec8-b87a-b802a899c3ea
description: "使用 dotnet 命令行界面的 NuGet 相关命令短引用。"
keywords: "dotnet NuGet 命令、 dotnet 包、 dotnet 还原、 dotnet nuget 局部变量、 dotnet nuget 推送和 dotnet nuget 删除"
ms.reviewer:
- karann-msft
- unniravindranathan
ms.openlocfilehash: 7ff4779f46db102f1384650d82118b34fedd4413
ms.sourcegitcommit: d0ba99bfe019b779b75731bafdca8a37e35ef0d9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2017
---
# <a name="dotnet-commands"></a>dotNet 命令

DotNet 命令行界面，在 Windows、 Mac OS X 和 Linux 上运行，提供了大量基本 nuget.exe 命令如下所示。 其中 dotnet 提供了所需的命令，不需要下载 nuget.exe。

- [**dotnet 包**](https://docs.microsoft.com/dotnet/core/tools/dotnet-pack?tabs=netcore2x)： 包代码 NETCore SDK 项目为 NuGet 包。 应使用所有其他项目类型[`nuget pack`](cli-ref-pack.md)
- [**dotnet 还原**](https://docs.microsoft.com/dotnet/core/tools/dotnet-restore?tabs=netcore2x)： 还原的依赖关系和项目的工具。 截至 NuGet 4.0 中，这将运行的相同代码`nuget restore`。
- [**dotnet nuget 局部变量**](https://docs.microsoft.com/dotnet/core/tools/dotnet-nuget-locals)： 清除或列出-请求的本地 NuGet 资源，如 http 缓存、 临时缓存或计算机范围全局包文件夹。
- [**dotnet nuget 推送**](https://docs.microsoft.com/dotnet/core/tools/dotnet-nuget-push)： 将包推送到服务器并发布它适用于 nuget.org、 Visual Studio Team Services 或任何第三方 NuGet 服务器。
- [**dotnet nuget 删除**](https://docs.microsoft.com/dotnet/core/tools/dotnet-nuget-delete)： 删除或 unlists 程序包的来源的服务器，适用于 nuget.org、 Visual Studio Team Services 或任何第三方 NuGet 服务器。