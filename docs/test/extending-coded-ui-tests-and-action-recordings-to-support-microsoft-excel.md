---
title: 扩展编码的 UI 测试和操作录制
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: conceptual
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 97d49c44a2ab7b81a0241366ec9cc6e74401d6f5
ms.sourcegitcommit: 5b767247b3d819a99deb0dbce729a0562b9654ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/20/2018
ms.locfileid: "39180485"
---
# <a name="extend-coded-ui-tests-and-action-recordings"></a>扩展编码的 UI 测试和操作录制

编码的 UI 测试和操作录制的测试框架不支持的每个可能的用户界面。 它可能不支持你想要测试的特定 UI。 例如，不能立即创建编码的 UI 测试或 Microsoft Excel 电子表格的操作录制。 但是，可以为编码的 UI 测试框架创建自己的扩展，该扩展通过利用编码的 UI 测试框架的扩展性来支持特定的 UI。

![UI 测试体系结构](../test/media/ui_testarch.png)

## <a name="sample-extension-to-test-microsoft-excel"></a>测试 Microsoft Excel 的示例扩展

此[博客文章](https://blogs.msdn.microsoft.com/gautamg/2010/01/05/3-introducing-sample-excel-extension/)包含指向编码的 UI 测试框架的[示例扩展](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Components.PostAttachments/00/09/94/38/24/ExcelPluginSample.zip)的链接。 还可以查看整个[编码的 UI 测试扩展性的博客文章系列](https://blogs.msdn.microsoft.com/gautamg/2010/01/05/series-on-coded-ui-test-extensibility/)。

> [!NOTE]
> 该示例旨在与 Microsoft Excel 2010 配合使用。 它可能适用或不适用于其他版本的 Excel。

## <a name="see-also"></a>请参阅

- <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>
- <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement>
- <xref:Microsoft.VisualStudio.TestTools.UITest.Common.UITestActionFilter>
- <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage>
- [使用 UI 自动化来测试代码](../test/use-ui-automation-to-test-your-code.md)
- [编码的 UI 测试的最佳做法](../test/best-practices-for-coded-ui-tests.md)
- [支持编码的 UI 测试和操作录制的配置和平台](../test/supported-configurations-and-platforms-for-coded-ui-tests-and-action-recordings.md)