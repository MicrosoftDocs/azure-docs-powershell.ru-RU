---
title: Вопросы и ответы
description: Часто задаваемые вопросы об Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239389"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="b74a9-103">Часто задаваемые вопросы об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b74a9-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="b74a9-104">Что такое Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="b74a9-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="b74a9-105">Azure PowerShell — это набор командлетов для управления ресурсами Azure непосредственно с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b74a9-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="b74a9-106">В декабре 2018 года модуль PowerShell Az стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="b74a9-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="b74a9-107">Теперь это рекомендуемый модуль PowerShell для взаимодействия с Azure.</span><span class="sxs-lookup"><span data-stu-id="b74a9-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="b74a9-108">Дополнительные сведения о модуле PowerShell Az см. в статье [Знакомство с новым модулем Az для Azure PowerShell](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="b74a9-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="b74a9-109">Как отключить предупреждения о критических изменениях в Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="b74a9-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="b74a9-110">Чтобы отключить предупреждения о критических изменениях в Azure PowerShell, необходимо задать для переменной среды `SuppressAzurePowerShellBreakingChangeWarnings` значение `true`.</span><span class="sxs-lookup"><span data-stu-id="b74a9-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```