---
title: NuGet 4.6 RTM 发行说明 | Microsoft Docs
author: anangaur
ms.author: anangaur
manager: unnir
ms.date: 3/7/2018
ms.topic: article
ms.prod: nuget
ms.technology: ''
description: NuGet 4.6.0 的发行说明，包括已知问题、bug 修复、新增功能和 DCR。
keywords: NuGet 4.6.0 发行说明, bug 修复, 已知问题, 新增功能, DCR
ms.reviewer:
- karann-msft
- unniravindranathan
- anangaur
ms.workload:
- dotnet
- aspnet
ms.openlocfilehash: 004ad16018443292840b00fa88aa78350e371414
ms.sourcegitcommit: beb229893559824e8abd6ab16707fd5fe1c6ac26
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/28/2018
---
# <a name="nuget-46-rtm-release-notes"></a><span data-ttu-id="f3db2-104">NuGet 4.6 RTM 发行说明</span><span class="sxs-lookup"><span data-stu-id="f3db2-104">NuGet 4.6 RTM Release Notes</span></span>

<span data-ttu-id="f3db2-105">[Visual Studio 2017 15.6 RTW](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes) 附带 [NuGet 4.6.0](https://dist.nuget.org/win-x86-commandline/v4.6.0/nuget.exe)。</span><span class="sxs-lookup"><span data-stu-id="f3db2-105">[Visual Studio 2017 15.6 RTW](https://www.visualstudio.com/news/releasenotes/vs2017-relnotes) comes with [NuGet 4.6.0](https://dist.nuget.org/win-x86-commandline/v4.6.0/nuget.exe).</span></span>

## <a name="summary-whats-new-in-this-release"></a><span data-ttu-id="f3db2-106">摘要：此版本中的新增功能</span><span class="sxs-lookup"><span data-stu-id="f3db2-106">Summary: What's New in this Release</span></span>
* <span data-ttu-id="f3db2-107">添加了对[给包签名](https://docs.microsoft.com/en-us/nuget/create-packages/sign-a-package)的支持。</span><span class="sxs-lookup"><span data-stu-id="f3db2-107">We have added support for [signing packages](https://docs.microsoft.com/en-us/nuget/create-packages/sign-a-package).</span></span>  
* <span data-ttu-id="f3db2-108">Visual Studio 2017 和 nuget.exe 现将在安装包、为[已签名包](https://docs.microsoft.com/en-us/nuget/reference/signed-packages-reference)还原包之前，验证包的完整性。</span><span class="sxs-lookup"><span data-stu-id="f3db2-108">Visual Studio 2017 and nuget.exe now verifies package integrity before installing, restoring packages for [signed packages](https://docs.microsoft.com/en-us/nuget/reference/signed-packages-reference).</span></span>
* <span data-ttu-id="f3db2-109">改进了连续还原的性能。</span><span class="sxs-lookup"><span data-stu-id="f3db2-109">We have improved performance of successive restores.</span></span>

## <a name="known-issues"></a><span data-ttu-id="f3db2-110">已知问题</span><span class="sxs-lookup"><span data-stu-id="f3db2-110">Known issues</span></span>
### <a name="issues-with-net-standard-20-with-net-framework--nuget"></a><span data-ttu-id="f3db2-111">使用 .NET Framework 和 NuGet 的 .NET Standard 2.0 的问题</span><span class="sxs-lookup"><span data-stu-id="f3db2-111">Issues with .NET Standard 2.0 with .NET Framework & NuGet</span></span> 

<span data-ttu-id="f3db2-112">.NET Standard 及其工具旨在使面向 .NET Framework 4.6.1 的项目可使用面向 .NET Standard 2.0 或更早版本的 NuGet 包和项目。</span><span class="sxs-lookup"><span data-stu-id="f3db2-112">.NET Standard & its tooling was designed such that projects targeting .NET Framework 4.6.1 can consume NuGet packages & projects targeting .NET Standard 2.0 or earlier.</span></span> <span data-ttu-id="f3db2-113">[本文档](https://github.com/dotnet/standard/issues/481)总结了该方案相关问题、解决问题的计划以及可使用当前工具状态部署的变通方法。</span><span class="sxs-lookup"><span data-stu-id="f3db2-113">[This document](https://github.com/dotnet/standard/issues/481) summarizes the issues around that scenario, the plan for addressing them, and workarounds you can deploy with today's state of the tooling.</span></span>

## <a name="top-issues-fixed-in-this-release"></a><span data-ttu-id="f3db2-114">此版本中已修复的主要问题</span><span class="sxs-lookup"><span data-stu-id="f3db2-114">Top issues fixed in this release</span></span>

<span data-ttu-id="f3db2-115">**性能修复**</span><span class="sxs-lookup"><span data-stu-id="f3db2-115">**Performance fixes**</span></span>
* <span data-ttu-id="f3db2-116">没有更改时，无法写入资产文件 - [#6491](https://github.com/NuGet/Home/issues/6491)</span><span class="sxs-lookup"><span data-stu-id="f3db2-116">Don't write asset files when there is no change - [#6491](https://github.com/NuGet/Home/issues/6491)</span></span>
* <span data-ttu-id="f3db2-117">当子项目的 TFM 与父项目的 TFM 不匹配时，还原会导致额外的 MSBuild 计算 - [#6311](https://github.com/NuGet/Home/issues/6311)</span><span class="sxs-lookup"><span data-stu-id="f3db2-117">Restore causes extra MSBuild evaluations when child projects' TFM do not match with the parent project's - [#6311](https://github.com/NuGet/Home/issues/6311)</span></span>
* <span data-ttu-id="f3db2-118">通过优化依赖项关系图创建规范来提高 NoOp 还原性能 - [#6252](https://github.com/NuGet/Home/issues/6252)</span><span class="sxs-lookup"><span data-stu-id="f3db2-118">Improve NoOp restore perf by optimizing dependency graph spec creation - [#6252](https://github.com/NuGet/Home/issues/6252)</span></span>

<span data-ttu-id="f3db2-119">**Bug**</span><span class="sxs-lookup"><span data-stu-id="f3db2-119">**Bugs**</span></span>
* <span data-ttu-id="f3db2-120">推送到本地文件夹导致 nupkg 锁定 - [#6325](https://github.com/NuGet/Home/issues/6325)</span><span class="sxs-lookup"><span data-stu-id="f3db2-120">Push to local folder leaves nupkg locked - [#6325](https://github.com/NuGet/Home/issues/6325)</span></span>
* <span data-ttu-id="f3db2-121">NuGet 插件实现：多个问题 - [#6149](https://github.com/NuGet/Home/issues/6149)</span><span class="sxs-lookup"><span data-stu-id="f3db2-121">NuGet Plugin implementation:  multiple issues - [#6149](https://github.com/NuGet/Home/issues/6149)</span></span>
* <span data-ttu-id="f3db2-122">UIHang - 从 VSSolutionManager 的 MEF 初始化中删除查询服务调用 - [#6110](https://github.com/NuGet/Home/issues/6110)</span><span class="sxs-lookup"><span data-stu-id="f3db2-122">UIHang - Remove query service call from MEF initialization in VSSolutionManager - [#6110](https://github.com/NuGet/Home/issues/6110)</span></span>
* <span data-ttu-id="f3db2-123">错误报告已取消的包下载任务发生异常 - [#6096](https://github.com/NuGet/Home/issues/6096)</span><span class="sxs-lookup"><span data-stu-id="f3db2-123">Error reporting exception for cancelled package download task - [#6096](https://github.com/NuGet/Home/issues/6096)</span></span>
* <span data-ttu-id="f3db2-124">NuGet.exe 在程序集名称中用“%2B”替换“+”- [#5956](https://github.com/NuGet/Home/issues/5956)</span><span class="sxs-lookup"><span data-stu-id="f3db2-124">NuGet.exe replaces '+' with '%2B' in assembly name - [#5956](https://github.com/NuGet/Home/issues/5956)</span></span>
* <span data-ttu-id="f3db2-125">Fn+F1 无法转到 PM UI 和控制台的正确帮助页面 - [#5912](https://github.com/NuGet/Home/issues/5912)</span><span class="sxs-lookup"><span data-stu-id="f3db2-125">Fn+F1 does not take to the right help page for PM UI and Console - [#5912](https://github.com/NuGet/Home/issues/5912)</span></span>
* <span data-ttu-id="f3db2-126">VS NuGet 在特定情况下会将绝对路径写入项目文件 - [#5888](https://github.com/NuGet/Home/issues/5888)</span><span class="sxs-lookup"><span data-stu-id="f3db2-126">VS NuGet writes absolute paths into project files under specific circumstances - [#5888](https://github.com/NuGet/Home/issues/5888)</span></span>
* <span data-ttu-id="f3db2-127">修复 4.3 回归 - 无法通过转换在内容文件中替换占位符 $product$ 和 $AssemblyGuid$ - [#5880](https://github.com/NuGet/Home/issues/5880)</span><span class="sxs-lookup"><span data-stu-id="f3db2-127">Fix 4.3 regression - Placeholders $product$ and $AssemblyGuid$ not replaced in contentfile through transformation - [#5880](https://github.com/NuGet/Home/issues/5880)</span></span>
* <span data-ttu-id="f3db2-128">dotnet 还原出现多个源故障 - [#5817](https://github.com/NuGet/Home/issues/5817)</span><span class="sxs-lookup"><span data-stu-id="f3db2-128">dotnet restore with multiple sources crashes - [#5817](https://github.com/NuGet/Home/issues/5817)</span></span>
* <span data-ttu-id="f3db2-129">包应重新评估项目版本以允许 git 版本控制 - [#4790](https://github.com/NuGet/Home/issues/4790)</span><span class="sxs-lookup"><span data-stu-id="f3db2-129">Pack should re-evaluate project versions to allow git versioning - [#4790](https://github.com/NuGet/Home/issues/4790)</span></span>
* <span data-ttu-id="f3db2-130">改善在安装不兼容包时出现的难以理解的错误 - [#4555](https://github.com/NuGet/Home/issues/4555)</span><span class="sxs-lookup"><span data-stu-id="f3db2-130">Improve hard to understand errors when you install an incompatible package - [#4555](https://github.com/NuGet/Home/issues/4555)</span></span>
* <span data-ttu-id="f3db2-131">TemplateWizard 需要将包安装为 PackageReferences 的选项 - [#4549](https://github.com/NuGet/Home/issues/4549)</span><span class="sxs-lookup"><span data-stu-id="f3db2-131">TemplateWizard needs option to install packages as PackageReferences - [#4549](https://github.com/NuGet/Home/issues/4549)</span></span>
* <span data-ttu-id="f3db2-132">从开发人员命令提示符以外运行 MSBuild.exe 时，包传递的属性文件被忽略 - [#4530](https://github.com/NuGet/Home/issues/4530)</span><span class="sxs-lookup"><span data-stu-id="f3db2-132">Package-delivered props files ignored when MSBuild.exe is run from outside a Developer Command Prompt - [#4530](https://github.com/NuGet/Home/issues/4530)</span></span>
* <span data-ttu-id="f3db2-133">修复在引用不适用于项目的 .NET Standard 库时出现的不当错误消息 - [#4423](https://github.com/NuGet/Home/issues/4423)</span><span class="sxs-lookup"><span data-stu-id="f3db2-133">Fix poor error message when referencing .NET Standard Library that is not applicable to project - [#4423](https://github.com/NuGet/Home/issues/4423)</span></span>
* <span data-ttu-id="f3db2-134">dotnet add package 无法为面向可移植配置文件的包提供指导 - [#4349](https://github.com/NuGet/Home/issues/4349)</span><span class="sxs-lookup"><span data-stu-id="f3db2-134">dotnet add package fails for package targeting portable profile with little guidance - [#4349](https://github.com/NuGet/Home/issues/4349)</span></span>
* <span data-ttu-id="f3db2-135">dotnet 包 - ProjectReference 缺少版本后缀 - [#4337](https://github.com/NuGet/Home/issues/4337)</span><span class="sxs-lookup"><span data-stu-id="f3db2-135">dotnet pack - version suffix missing from ProjectReference - [#4337](https://github.com/NuGet/Home/issues/4337)</span></span>
* <span data-ttu-id="f3db2-136">有关 .NET Core 模板的生成错误和 VS 崩溃 - [#3973](https://github.com/NuGet/Home/issues/3973)</span><span class="sxs-lookup"><span data-stu-id="f3db2-136">Build errors and VS crash with .NET Core template - [#3973](https://github.com/NuGet/Home/issues/3973)</span></span>
* <span data-ttu-id="f3db2-137">无法加载源 https:\* 的服务索引 - [#3681](https://github.com/NuGet/Home/issues/3681)</span><span class="sxs-lookup"><span data-stu-id="f3db2-137">Unable to load the service index for source https:\* - [#3681](https://github.com/NuGet/Home/issues/3681)</span></span>
* <span data-ttu-id="f3db2-138">nuget.exe list -allversions 无法正常工作 - [#3441](https://github.com/NuGet/Home/issues/3441)</span><span class="sxs-lookup"><span data-stu-id="f3db2-138">nuget.exe list -allversions doesn't work - [#3441](https://github.com/NuGet/Home/issues/3441)</span></span>
* <span data-ttu-id="f3db2-139">误导性的依赖项解析错误信息 - [#2984](https://github.com/NuGet/Home/issues/2984)</span><span class="sxs-lookup"><span data-stu-id="f3db2-139">Misleading dependency resolution error message - [#2984](https://github.com/NuGet/Home/issues/2984)</span></span>
* <span data-ttu-id="f3db2-140">nuget.exe 还原不会为 .msbuildproj 生成 .props 和 .targets 文件（在 v3.3.0-3.4.4 升级中回归） - [#2921](https://github.com/NuGet/Home/issues/2921)</span><span class="sxs-lookup"><span data-stu-id="f3db2-140">nuget.exe restore doesn't produce .props and .targets files for .msbuildproj (regression in v3.3.0-3.4.4 upgrade) - [#2921](https://github.com/NuGet/Home/issues/2921)</span></span>
* <span data-ttu-id="f3db2-141">更新打开了 XAML 文件的 NuGet 包时出现 UI 延迟 - [#2878](https://github.com/NuGet/Home/issues/2878)</span><span class="sxs-lookup"><span data-stu-id="f3db2-141">UI delay when updating a NuGet package with XAML file open - [#2878](https://github.com/NuGet/Home/issues/2878)</span></span>
* <span data-ttu-id="f3db2-142">来自 IIS 的 WebSite 项目失败，路径中包含非法字符 - [#2798](https://github.com/NuGet/Home/issues/2798)</span><span class="sxs-lookup"><span data-stu-id="f3db2-142">WebSite project from IIS fails with illegal characters in path - [#2798](https://github.com/NuGet/Home/issues/2798)</span></span>
* <span data-ttu-id="f3db2-143">Nuget 添加在 CentOS 上挂起 - [#2708](https://github.com/NuGet/Home/issues/2708)</span><span class="sxs-lookup"><span data-stu-id="f3db2-143">Nuget add hangs on CentOS - [#2708](https://github.com/NuGet/Home/issues/2708)</span></span>
* <span data-ttu-id="f3db2-144">使用 packagesavemode -nupkg 还原 json.net 失败 - [#2706](https://github.com/NuGet/Home/issues/2706)</span><span class="sxs-lookup"><span data-stu-id="f3db2-144">Restore with packagesavemode -nupkg fails for json.net - [#2706](https://github.com/NuGet/Home/issues/2706)</span></span>
* <span data-ttu-id="f3db2-145">包管理器筛选器在 vs 输出窗口中不可用于还原命令 - [#2704](https://github.com/NuGet/Home/issues/2704)</span><span class="sxs-lookup"><span data-stu-id="f3db2-145">Package Manager filter not available in vs output window for restore command - [#2704](https://github.com/NuGet/Home/issues/2704)</span></span>


[<span data-ttu-id="f3db2-146">此版本中所有已修复问题的列表</span><span class="sxs-lookup"><span data-stu-id="f3db2-146">List of all issues fixed in this release</span></span>](https://github.com/NuGet/Home/issues?q=is%3Aissue+is%3Aclosed+milestone%3A%224.6")