---
title: MSBuild 响应文件 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- response files, MSBuild
- MSBuild, response files
- MSBuild, .rsp files
- .rsp files
ms.assetid: 9f53987b-20ee-470a-ab62-fce997bb5e15
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 83f8e5ad4522a47eaea978b14678fe134b4faa8e
ms.sourcegitcommit: 8ee7efb70a1bfebcb6dd9855b926a4ff043ecf35
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2018
ms.locfileid: "39081587"
---
# <a name="msbuild-response-files"></a>MSBuild 响应文件
响应 (.rsp) 文件是包含 MSBuild.exe 命令行开关的文本文件。 每个开关可以单独占一行，或者所有开关仅占一行。 注释行以 # 符号开头。 @ 开关用于将另一个响应文件传递给 MSBuild.exe。  
  
## <a name="msbuildrsp"></a>MSBuild.rsp
自动响应文件是在生成项目时 MSBuild.exe 自动使用的特殊 .rsp 文件。 MSBuild.rsp 文件必须位于 MSBuild.exe 所在的目录中，否则无法找到该文件。 可以编辑此文件，向 MSBuild.exe 指定默认命令行开关。 例如，如果每次生成项目时使用相同的记录器，则可将 /logger 开关添加到 MSBuild.rsp，每次生成项目后，MSBuild.exe 都会使用该记录器。  

## <a name="directorybuildrsp"></a>Directory.Build.rsp
在版本 15.6 及更高版本中，MSBuild 会在该项目的父级目录中搜索名为 Directory.Build.rsp 的文件。  这可以帮助源代码存储库在命令行生成过程中提供默认参数。  此外，它还可以用于指定托管生成的命令行参数。

## <a name="see-also"></a>请参阅  
 [MSBuild 参考](../msbuild/msbuild-reference.md)   
 [命令行参考](../msbuild/msbuild-command-line-reference.md)