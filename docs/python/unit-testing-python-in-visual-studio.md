---
title: Python 的单元测试
description: 在 Visual Studio 中为 Python 代码设置单元测试，以充分利用测试资源管理器功能来发现、运行和调试测试。
ms.date: 06/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-python
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: douge
ms.workload:
- python
- data-science
ms.openlocfilehash: 37d545adf33a6350f3d2484e4f820ebca8f7353d
ms.sourcegitcommit: 0bf2aff6abe485e3fe940f5344a62a885ad7f44e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/27/2018
ms.locfileid: "37056418"
---
# <a name="setting-up-unit-testing-for-python-code"></a>为 Python 代码设置单元测试

单元测试是测试应用程序中其他代码单元的代码片段，通常为独立函数、类等。 应用程序通过其所有单元测试后，至少可以相信其低级功能正确无误。

Python 单元测试广泛应用于在程序设计期间验证方案。 针对 Visual Studio 的 Python 支持包括在开发过程的上下文中发现、执行和调试单元测试，无需单独运行单元测试。

本文简要介绍了适用于 Python 语言的 Visual Studio 中的单元测试功能。 有关单元测试的的更多常见信息，请参阅[对代码进行单元测试](../test/unit-test-your-code.md)。

|   |   |
|---|---|
| ![视频的摄像机图标](../install/media/video-icon.png "观看视频") | 有关 Python 中的单元测试，请[观看视频（Microsoft 虚拟学院）](https://mva.microsoft.com/en-US/training-courses-embed/python-tools-for-visual-studio-2017-18121/Video-Testing-Python-hb46k6LWE_405918567)（2 分 31 秒）。 |

## <a name="discovering-and-viewing-tests"></a>发现和查看测试

根据惯例，Visual Studio 将测试标识为名称以“`test`”开头的方法。 若要查看此行为，请执行以下操作：

1. 打开一个 Visual Studio 中加载的 [Python 项目](managing-python-projects-in-visual-studio.md)，右键单击该项目，选择“添加”>“新建项目...”，然后选择其后有“添加”的“Python 单元测试”。

1. 如果直接运行脚本，此操作将创建具有导入标准 `unittest` 模块的代码的 `test1.py` 文件，从 `unittest.TestCase` 派生一个测试类，并调用 `unittest.main()`：

    ```python
    import unittest

    class Test_test1(unittest.TestCase):
        def test_A(self):
            self.fail("Not implemented")

    if __name__ == '__main__':
        unittest.main()
    ```

1. 根据需要保存该文件，然后通过“测试”>“窗口”>“测试资源管理器”菜单命令打开测试资源管理器。

1. 测试资源管理器会搜索要测试的项目并进行显示，如下所示。 双击测试打开其源文件。

    ![显示默认 test_A 的测试资源管理器](media/unit-test-A.png)

1. 向项目添加更多测试时，可以使用工具栏上的“分组”菜单整理测试资源管理器中视图：

    ![测试资源管理器分组工具栏菜单](media/unit-test-group-menu.png)

1. 还可以在搜索字段中输入文本以按名称筛选测试。

有关 `unittest` 模块和编写测试的详细信息，请参阅 [Python 2.7 文档](https://docs.python.org/2/library/unittest.html)或 [Python 3.4 文档](https://docs.python.org/3/library/unittest.html) (python.org)。

## <a name="running-tests"></a>运行测试

在测试资源管理器中，可以通过多种方式来运行测试：

- “运行所有”将运行所有显示的测试（取决于筛选器）。
- “运行...”菜单提供以下命令：运行失败的、通过的或未作为一组运行的测试。
- 可以选择一个或多个测试，右键单击，然后选择“运行选定测试”。

测试在后台运行，每个测试完成后，测试资源管理器将更新其状态：

- 通过的测试将显示一个绿勾和运行测试所花费的时间：

    ![test_A 通过状态](media/unit-test-A-pass.png)

- 失败的测试将显示带有**输出**链接的红叉，该链接显示控制台输出和测试运行中的 `unittest` 输出：

    ![test_A 失败状态](media/unit-test-A-fail.png)

    ![test_A 失败及原因](media/unit-test-A-fail-reason.png)

## <a name="debugging-tests"></a>调试测试

因为单元测试是代码片段，所以和任何其他代码一样会受到 bug 的影响，有时需要在调试器中运行。 在调试程序中，可以设置断点、检查变量和逐行执行代码。 Visual Studio 还提供了用于单元测试的诊断工具。

若要开始调试，请在代码中设置初始断点，然后在测试资源管理器中右键单击测试（或所做选择），然后选择“调试所选测试”。 Visual Studio 会启动 Python 调试程序，与为应用程序代码启动 Python 调试器一样。

![调试测试](media/unit-test-debugging.png)

还可使用“分析所选测试的代码覆盖率”和“配置文件测试”命令，具体取决于 Visual Studio 版本（请参阅[功能矩阵](overview-of-python-tools-for-visual-studio.md#features-matrix)）。

### <a name="known-issues"></a>已知问题

- 启动调试时，Visual Studio 会显示启动和停止调试，然后重新启动。 此行为是预期的行为。
- 调试多个测试时，因为每个测试都是独立运行，所以会中断调试会话。
- 调试时，Visual Studio 启动测试会间歇性地失败。 通常情况下，尝试再次调试测试会成功。
- 调试时，可能会跳出测试转到 `unittest` 实现。 通常情况下，下一步会运行到程序结束，然后停止调试。
