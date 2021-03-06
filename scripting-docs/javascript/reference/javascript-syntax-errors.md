---
title: JavaScript 语法错误 |Microsoft 文档
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-javascript
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- JavaScript
dev_langs:
- JavaScript
- TypeScript
- DHTML
helpviewer_keywords:
- errors [JavaScript]
- syntax errors, JavaScript
ms.assetid: 0343dc19-5f5e-4a4c-83da-630b4fbcb3b6
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3bc3398d6a90ef308fd2b4b367bc1006ad95f5b1
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2017
ms.locfileid: "24639777"
---
# <a name="javascript-syntax-errors"></a>JavaScript 语法错误
[!INCLUDE[javascript](../../javascript/includes/javascript-md.md)]语法错误发生时之一的结构你[!INCLUDE[javascript](../../javascript/includes/javascript-md.md)]语句违反了一个或多个语法规则。  
  
## <a name="errors"></a>错误  
  
|错误号|描述|  
|------------------|-----------------|  
|1019|[“break”不能位于循环外](../../javascript/misc/can-t-have-break-outside-of-loop.md)|  
|1020|[“continue”不能位于循环外](../../javascript/misc/can-t-have-continue-outside-of-loop.md)|  
|1030|[条件编译已关闭](../../javascript/misc/conditional-compilation-is-turned-off.md)|  
|1027|[“default”只能在“switch”语句中出现一次](../../javascript/misc/default-can-only-appear-once-in-a-switch-statement.md)|  
|1005|[预期 (](../../javascript/misc/expected-left-parenthesis-javascript.md)|  
|1006|[预期)](../../javascript/misc/expected-right-parenthesis-javascript.md)|  
|1012|[预期 '/'](../../javascript/misc/expected-minus.md)|  
|1003|[缺少“:”](../../javascript/misc/expected-colon.md)|  
|1004|[缺少“;”](../../javascript/misc/expected-semicolon.md)|  
|1032|[缺少“@”](../../javascript/misc/expected-at.md)|  
|1029|[缺少“@end”](../../javascript/misc/expected-at-end.md)|  
|1007|[预期 &#93;](../../javascript/misc/expected-right-square-bracket.md)|  
|1008|[缺少“{”](../../javascript/misc/expected-left-curly-brace.md)|  
|1009|[缺少“}”](../../javascript/misc/expected-right-curly-brace.md)|  
|1011|[应有 =](../../javascript/misc/expected-equal-javascript.md)|  
|1033|[缺少“catch”](../../javascript/misc/expected-catch.md)|  
|1031|[缺少常量](../../javascript/misc/expected-constant.md)|  
|1023|[缺少十六进制数字](../../javascript/misc/expected-hexadecimal-digit.md)|  
|1010|[应为标识符](../../javascript/misc/expected-identifier-javascript.md)|  
|1028|[缺少标识符、字符串或数字](../../javascript/misc/expected-identifier-string-or-number.md)|  
|1024|[缺少“while”](../../javascript/misc/expected-while.md)|  
|1014|[无效的字符](../../javascript/misc/invalid-character-javascript.md)|  
|1026|[未找到标签](../../javascript/misc/label-not-found.md)|  
|1025|[标签已重定义](../../javascript/misc/label-redefined.md)|  
|1018|[“return”语句在函数外](../../javascript/misc/return-statement-outside-of-function.md)|  
|1002|[语法错误](../../javascript/misc/syntax-error-javascript.md)|  
|1035|[同一源行中 throw 之后必须有表达式](../../javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line.md)|  
|1016|[未终止的注释](../../javascript/misc/unterminated-comment.md)|  
|1015|[未终止的字符串常量](../../javascript/misc/unterminated-string-constant-javascript.md)|  
  
### <a name="script-host-errors"></a>脚本主机错误  
 以下的错误正确讲到脚本主机后，相关的错误，但你偶尔可能会看到它们。  
  
|错误|HRESULT|描述|  
|-----------|-------------|-----------------|  
|SCRIPT_E_RECORDED|0x86664004|已将错误记录脚本引擎和主机之间传递。 主机需要要传递给调用方的错误代码。|  
|SCRIPT_E_REPORTED|0x80020101|脚本引擎已报告主机可通过 IActiveScriptSite::OnScriptError 未经处理的异常。 主机可以忽略此错误。|  
|SCRIPT_E_PROPAGATE|0x8002010|脚本错误被传播到调用方这可能是在不同线程中。 主机应将错误代码传递到调用方。|  
  
## <a name="see-also"></a>另请参阅  
 [JavaScript 运行时错误](../../javascript/reference/javascript-run-time-errors.md)