---
title: 调试，常规选项对话框 |Microsoft 文档
ms.custom: ''
ms.date: 05/23/2017
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.options.General
- VS.ToolsOptionsPages.Debugger.General
- VS.ToolsOptionsPages.Debugger.ENC
- vs.debug.options.ENC
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- Options dialog box, debugging
ms.assetid: b33aee0b-43c3-4c26-8ed4-bc673f491503
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5b7af8c68764b3a9ed85bf6a52a3a6c4a0568203
ms.sourcegitcommit: 0aafcfa08ef74f162af2e5079be77061d7885cac
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2018
ms.locfileid: "34572045"
---
# <a name="general-debugging-options-dialog-box"></a>“选项”对话框 ->“调试”->“常规”
**工具 > 选项 > 调试 > 常规**页中，可以在本文中设置描述的选项。

如果想要还原默认设置，则可以执行，使用**工具** > **导入和导出设置** > **所有设置重都置**。 如果你只想要重置设置的子集，保存你的设置中**导入和导出设置向导**在你想要测试更改之前，然后导入你已保存的设置更高版本。
  
**在删除所有断点之前询问**完成前需要进行确认**删除所有断点**命令。  
  
**一个进程中断时则中断所有进程**同时中断调试器附加到，发生都中断时中断所有进程。  
  
**当异常跨越应用域或托管/本机边界时中断**在托管或混合模式调试中，公共语言运行时可能会捕获跨越应用程序域边界或托管/本机边界的异常时以下条件为真：  
  
1\)当本机代码使用 COM 互操作调用托管的代码而托管的代码却引发异常。 请参阅[COM 互操作介绍](/dotnet/articles/visual-basic/programming-guide/com-interop/introduction-to-com-interop)。  
  
2\)当在应用程序域 1 中运行的托管的代码调用托管的代码中应用程序域 2，而应用程序域 2 中的代码却引发异常。 请参阅[使用应用程序域编程](/dotnet/articles/framework/app-domains/index)。  

3\)当代码使用反射调用一个函数而该函数却引发异常。 请参阅[反射](/dotnet/framework/reflection-and-codedom/reflection)。  
  
情况 2 和 3 时，异常有时由捕获中的托管代码`mscorlib`而不是公共语言运行时。 此选项不影响在 `mscorlib` 捕获到异常时中断。  
  
**启用地址级调试**启用高级功能在地址级上进行调试 (**反汇编**窗口中，**注册**窗口和地址断点)。  
  
- **如果源不可用时显示反汇编**自动显示**反汇编**窗口，当你尝试调试源的代码时将不可用。  
  
**启用断点筛选器**使您能够在断点上设置筛选器，以便他们将影响特定的进程、 线程或计算机。  
 
**使用新的异常帮助窗口**使替换异常助手异常帮助程序 (Visual Studio 2017)。
  
> [!NOTE]
> 对于托管代码，此选项之前已调用**启用异常助手**。 
  
**启用仅我的代码**调试器显示，并指导仅，用户代码 （"我的代码"） 转换忽略系统代码和其他经过优化或没有调试符号的代码。

- **如果启动 （仅限托管） 没有用户代码，则发出警告**在调试时启动与启用仅我的代码，此选项会发出警告你如果没有用户代码 （"我的代码"）。 

**启用.NET Framework 源代码单步执行**允许调试器单步执行.NET Framework 源代码。 自动启用此选项会禁用“仅我的代码”，.NET Framework 符号将下载到缓存位置。 你可以更改中的缓存位置**选项**对话框中，**调试**类别，**符号**页。  
  
**逐过程执行属性和运算符 （仅限托管）** 使调试器无法单步执行属性和托管代码中的运算符。  
  
**启用属性求值和其他隐式函数调用**打开自动求值的属性和隐式函数调用在变量窗口中和**快速监视**对话框。  
  
- **在变量窗口 （C# 和 JavaScript 仅） 中对对象调用字符串转换函数**在变量窗口中计算对象时，执行隐式字符串转换调用。 结果显示为字符串而不是类型名称。 仅在 C# 代码中进行调试时适用。 此设置可能由 DebuggerDisplay 特性重写 (请参阅[使用 DebuggerDisplay 特性](../debugger/using-the-debuggerdisplay-attribute.md))。  
  
**启用源服务器支持**告知 Visual Studio 调试器从实现 SrcSrv 源服务器中获取源文件 (`srcsrv.dll`) 协议。 Team Foundation Server 和 Windows 的调试工具是实现协议的两个源服务器。 有关 SrcSrv 设置的详细信息，请参阅[SrcSrv](https://msdn.microsoft.com/library/windows/hardware/ff558791(v=vs.85).aspx)文档。 此外，请参阅[指定符号 (.pdb) 和源文件](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)。  
  
> [!IMPORTANT]
>  由于读取 .pdb 文件会执行文件中的任意代码，因此请确保你信任此服务器。  
  
- **源服务器诊断消息打印到输出窗口**启用源服务器支持后，此设置会打开诊断显示。  
  
- **允许源服务器中的部分信任程序集 （仅限托管）** 启用源服务器支持后，此设置将替代不需要的部分信任程序集检索源的默认行为。  

**启用源链接支持**告知 Visual Studio 调试器，以下载包含源链接信息的.pdb 文件的源文件。 有关源链接的详细信息，请参阅[源链接规范](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/source_link.md)。

    > [!IMPORTANT]
    >  Because Source Link will download files using http or https, make sure you trust the .pdb file.  
  
**为突出显示整个行断点和当前语句 （c + +）** 时调试器会突出显示断点或当前语句，会突出显示整个行。  
  
**需要源文件到完全匹配的原始版本**指示调试器验证源文件是否与用于生成正在调试的可执行文件的源代码的版本匹配。 如果版本不匹配，系统将提示来查找匹配的源。 如果未找到匹配源，则在调试过程中不会显示源代码。 
  
**将所有输出窗口文本重都定向到即时窗口**发送所有调试器消息通常显示在**输出**窗口**即时**窗口相反。  
  
**变量窗口中显示对象的原始结构**关闭所有对象结构视图自定义。 有关视图自定义项的详细信息，请参阅[创建.managed 对象的自定义视图](../debugger/create-custom-views-of-dot-managed-objects.md)。  
  
**在模块加载 （仅限托管） 取消 JIT 优化**加载模块并编译 JIT 后，在附加调试器时，禁用托管代码的 JIT 优化。 禁用优化可能更易于调试某些问题，尽管这会降低性能。 如果正在使用“仅我的代码”，则禁用 JIT 优化会导致非用户代码显示为用户代码（“我的代码”）。 有关详细信息，请参阅[JIT 优化和调试](../debugger/jit-optimization-and-debugging.md)。

**启用 JavaScript 调试 asp.net （Chrome 和 IE）** 启用 ASP.NET 应用程序脚本调试器。 在 Chrome 中的第一次使用，你可能需要登录到第一次使用，以启用你已安装的 Chrome 扩展上的浏览器。 禁用此选项以恢复到旧行为。    

**加载 dll 导出**加载 dll 导出表。 处理 Windows 消息、Windows 过程 (WindowProc)、COM 对象、封送或不具有其符号的任何 DLL 时，DLL 导出表中的符号信息将很有用。 读取 DLL 导出信息会占用一些系统开销。 因此，默认情况下此功能被禁用。  
  
若要查看可用的 dll 导出表中的哪些符号，请使用`dumpbin /exports`。 符号可用于任何 32 位系统 DLL。 从 `dumpbin /exports` 输出中，可以查看到精确的函数名，包括非字母数字字符。 这对于在函数上设置断点很有用。 DLL 导出表中的函数名在调试器的其他位置似乎被截断了。 调用将按调用顺序列出，当前函数（嵌套最深的函数）位于顶端。 有关详细信息，请参阅 [dumpbin /exports](/cpp/build/reference/dash-exports)。  
  
**显示并行堆栈关系图自下而上**控制堆栈在中的显示方向**并行堆栈**窗口。
  
**如果写入的数据未更改值，则忽略 GPU 内存访问异常**忽略调试如果数据未更改期间检测到的争用条件。 有关详细信息，请参阅[调试 GPU 代码](../debugger/debugging-gpu-code.md)。  
  
**使用托管兼容模式**替换默认调试引擎为旧版本，以支持以下方案：  
  
- 使用除 C#、VB 或 F# 之外，拥有自己的表达式计算器（包括 C++/CLI）的其他 .NET Framework 语言。  
  
- 在执行混合模式调试时，你想要为 C++ 项目启用“编辑并继续”。  
  
> [!NOTE]
> 选择托管兼容模式会禁用仅可在默认调试引擎中实现某些功能。 

**使用旧的 C# 和 VB 表达式计算器**调试器将使用 Visual Studio 2013 C# /VB 表达式计算器，而不是基于 Visual Studio 2015 Roslyn 的表达式计算器。    
  
**当使用针对可能不安全的进程 （仅限托管） 的自定义调试器可视化工具时会发出警告**Visual Studio 会警告你，当你使用自定义调试器可视化工具是在调试对象进程中运行代码，因为它无法运行不安全代码。  
  
**启用 Windows 调试堆分配器 （仅限本机）** 启用 windows 调试堆以改进堆诊断。 启用此选项会影响调试性能。  
  
**启用 xaml UI 调试工具**启动时调试 (F5) 支持的项目类型，将显示实时可视化树和实时属性资源管理器窗口。 有关详细信息，请参阅[进行调试时检查 XAML 属性](../debugger/inspect-xaml-properties-while-debugging.md)。  
  
- **预览实时可视化树中的所选的元素**选定了其上下文的 XAML 元素也会选中**实时可视化树**窗口。  
  
- **在应用程序中显示运行时工具**显示**实时可视化树**在 XAML 应用程序正在调试的主窗口工具栏中的命令。 Visual Studio 2015 Update 2 中引入了此选项。 

- **启用 XAML 编辑并继续**，可使用编辑并继续 XAML 代码的功能。 
  
**在调试时启用诊断工具****诊断工具**进行调试时，将显示窗口。
  
**在调试时显示经过的时间过程**进行调试时，代码窗口会显示占用时间的给定的方法调用。  
  
**启用编辑并继续**可以使用编辑并继续调试时的功能。  
  
- **启用本机编辑并继续**可以使用编辑并继续调试本机 c + + 代码时的功能。 有关详细信息，请参阅[编辑并继续 （Visual c + +）](../debugger/edit-and-continue-visual-cpp.md)。  
  
- **将更改应用上继续 （仅限本机）** Visual Studio 会自动编译并应用时从中断状态继续该过程所做的任何未完成的代码更改。 如果未选择，你可以选择使用调试菜单下的"应用代码更改"项来应用更改。  
  
- **就陈旧的代码 （仅限本机），则发出警告**收到关于陈旧代码的警告。    

**显示运行若要在调试时单击在编辑器中的按钮**选中此选项后，[运行到单击](debugger-feature-tour.md#run-to-a-point-in-your-code-quickly-using-the-mouse)按钮将显示在调试时。

## <a name="options-supported-in-older-versions-of-visual-studio"></a>在 Visual Studio 早期版本中受支持的选项

如果你使用的较旧版本的 Visual Studio，某些其他选项可能会显示。

**启用异常助手**对于托管代码，启用异常助手。 在 Visual Studio 自 2017 年 1，异常帮助器取代异常助手。

**展开调用堆栈上未经处理的异常**导致**调用堆栈**窗口调用堆栈回滚到点之前未处理的异常。 

**如果启动 （仅限本机） 无符号，则发出警告**显示警告对话框中，当你尝试调试调试器没有对应符号信息为其的程序时。 

**启动时禁用脚本调试，则发出警告**禁用了脚本调试启动调试器时会显示一个警告对话框。

**使用本机兼容模式**时选择此选项，则调试器使用 Visual Studio 2010 本机调试器而不是新的本机调试器。  
  
因为新的调试引擎不支持计算 .NET C++ 表达式，因此应在调试 .NET C++ 代码时使用此选项。 但是，启用本机兼容模式会禁用依赖于当前调试器实现来操作的许多功能。 例如，旧引擎缺少很多可视化工具内置类型等`std::string`Visual Studio 2015 项目中。   使用 Visual Studio 2013 项目以在这些情况下获得最佳的调试体验。
  
## <a name="see-also"></a>请参阅  
 [在 Visual Studio 中进行调试](../debugger/index.md)  
 [调试器功能简介](../debugger/debugger-feature-tour.md)
