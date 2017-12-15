---
title: "3.5 beta2 之前发行说明 |Microsoft 文档"
author: karann-msft
ms.author: karann-msft
manager: ghogen
ms.date: 11/11/2016
ms.topic: article
ms.prod: nuget
ms.technology: 
ms.assetid: 0b76064f-0607-438a-bbf8-dd862690f48e
description: "包括已知的问题、 bug 修复、 增加的功能，以及 DCRs NuGet 3.5 Beta 2 的发行说明。"
keywords: "NuGet 3.5 Beta 2 发行说明，bug 修复的已知问题，添加了一些功能，DCRs"
ms.reviewer:
- karann-msft
- unniravindranathan
ms.openlocfilehash: 6dd388e52308d2f3cd32d4d6c66c2868f0ae2a41
ms.sourcegitcommit: d0ba99bfe019b779b75731bafdca8a37e35ef0d9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2017
---
# <a name="35-beta2-release-notes"></a>3.5 beta2 之前发行说明

[NuGet 3.5 Beta 发行说明](../release-notes/nuget-3.5-Beta.md) | [NuGet 3.5 RC 发行说明](../release-notes/nuget-3.5-RC.md)

NuGet 3.5 Beta 2 RTM Visual Studio 2013 和 nuget.exe 2016 年 6 月 27 日发布

[完整的版本记录](https://github.com/NuGet/NuGet.Client/compare/release-3.5.0-beta...release-3.5.0-beta2)

[问题列表](https://github.com/Nuget/Home/issues?q=is%3Aissue+milestone%3A%223.5+Beta2%22+is%3Aclosed)

# <a name="notable-changes"></a>重大更改

## <a name="bug-fixes"></a>Bug 修复

* 更新的错误消息不支持密码 decrpytion.NET 核心中经过身份验证源- [# 2942年](https://github.com/NuGet/Home/issues/2942)

* 如果.NET 核心项目处于打开状态的程序包管理器控制台 Get-包失败[# 2932年](https://github.com/NuGet/Home/issues/2932)

* NuGet 推送命令中修复的 403 的不正确处理[# 2910年](https://github.com/NuGet/Home/issues/2910)

* 修复在卸载解决方案时设置 disableSourceControlIntegration 绑定到 TFS 源代码管理中的包的问题为 true- [# 2739年](https://github.com/NuGet/Home/issues/2739)

* 修复包更新，必须考虑到帐户非目标包- [# 2724年](https://github.com/NuGet/Home/issues/2724)

* 使用 MSBuild 详细级别设置为 Nuget 包管理器的记录器级别 UI 操作- [# 2705年](https://github.com/NuGet/Home/issues/2705)

* 修复 NuGet 配置是无效的错误，在网站项目中的 VS 2015 VSIX (v3.4.3)- [# 2667年](https://github.com/NuGet/Home/issues/2667)

* 修复从包问题`.csproj`包含的内容文件时[# 2658年](https://github.com/NuGet/Home/issues/2658)

* 中的 DefaultPushSource `NuGetDefaults.Config` (`ProgramData\NuGet`) 不起作用- [# 2653年](https://github.com/NuGet/Home/issues/2653)

* 在 Nuget 3.4.3 版本中的值不能在包创建为 null 的修复问题[# 2648年](https://github.com/NuGet/Home/issues/2648)

* 还原 VSTS 源-使用存储的凭据，从 Nuget.Config [# 2647年](https://github.com/NuGet/Home/issues/2647)

* 性能-版本常量代码中修复过多分配- [# 2632年](https://github.com/NuGet/Home/issues/2632)

* 修复问题，当 nuget.exe 的多个实例尝试并行-安装相同的包时[# 2628年](https://github.com/NuGet/Home/issues/2628)

* 性能-缓存依赖项信息的多项目操作- [# 2619年](https://github.com/NuGet/Home/issues/2619)

* 修复问题在包源无法添加从设置在源列表为空 – [# 2617年](https://github.com/NuGet/Home/issues/2617)

* 当试图安装包依赖于设计时外观-修复 Misleading 错误[# 2594年](https://github.com/NuGet/Home/issues/2594)

* 从 PackageManager 控制台中设置"全部"安装包尝试仅第一个源- [# 2557年](https://github.com/NuGet/Home/issues/2557)

* 修复与具有写入时间在将来的文件 (Mono)-的包问题[# 2518年](https://github.com/NuGet/Home/issues/2518)

* 当出现故障时查找项目中更新命令的显示异常[# 2418年](https://github.com/NuGet/Home/issues/2418)

* 从 nuget v3.3 + 安装的包源具有自变量时，不正确还原包内容-NoCache 当包包含`.nupkg`文件- [# 2354年](https://github.com/NuGet/Home/issues/2354)

* 修复问题包安装 （所有源），从 1 源-缺少包时[# 2322年](https://github.com/NuGet/Home/issues/2322)

* 如果单个源失败授权-安装块[# 2034年](https://github.com/NuGet/Home/issues/2034)

* `.nuspec`版本范围应重写-IncludeReferencedProjects 版本- [# 1983年](https://github.com/NuGet/Home/issues/1983)

* NuGet 3.3.0 更新失败，出现...的其他约束中定义 packages.config 会阻止此操作。 - [#1816](https://github.com/NuGet/Home/issues/1816)

* nuget.exe 更新中删除程序集强名称和私有特性。 - [#1778](https://github.com/NuGet/Home/issues/1778)

* 为"DefaultPushSource"的相对文件路径修复问题[# 1746年](https://github.com/NuGet/Home/issues/1746)

* 提高更新冲突解决程序失败消息- [# 1373年](https://github.com/NuGet/Home/issues/1373)

## <a name="features-and-behavior-changes"></a>功能及行为变化

* nuget.exe 推送的超时参数不起作用- [# 2785年](https://github.com/NuGet/Home/issues/2785)

* 不能生成 nuget.exe 还原`.props`和`.targets`文件`.nuproj`项目 （v3.4.3.855 中的回归）- [# 2711年](https://github.com/NuGet/Home/issues/2711)

* 需要扩展性 API 进行比较导入的框架[# 2633年](https://github.com/NuGet/Home/issues/2633)

* 使用时隐藏依存关系选项`project.json`  -  [# 2486年](https://github.com/NuGet/Home/issues/2486)

* 打印出 nuget.exe 版本标头中详细输出- [# 1887年](https://github.com/NuGet/Home/issues/1887)

* NuGet 应添加对 /runtimes/ {rid} /nativeassets/ {txm} 的支持- [# 2782年](https://github.com/NuGet/Home/issues/2782)