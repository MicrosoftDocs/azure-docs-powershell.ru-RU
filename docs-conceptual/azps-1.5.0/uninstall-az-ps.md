---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: fcec2c713d1967a5a70df9b13aa30d9ff4625e9d
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882366"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="13c1a-103">Удаление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c1a-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="13c1a-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="13c1a-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="13c1a-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="13c1a-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="13c1a-106">Если вы обнаружите ошибку, пожалуйста, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="13c1a-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="13c1a-107">Удаление модуля Az</span><span class="sxs-lookup"><span data-stu-id="13c1a-107">Uninstall the Az module</span></span>

<span data-ttu-id="13c1a-108">Чтобы удалить модули Az, используйте командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="13c1a-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="13c1a-109">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="13c1a-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="13c1a-110">Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="13c1a-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="13c1a-111">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13c1a-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="13c1a-112">Чтобы проверить, какие версии Azure PowerShell у вас установлены, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="13c1a-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="13c1a-113">Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="13c1a-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="13c1a-114">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="13c1a-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="13c1a-115">Необходимы права доступа администратора для запуска этого скрипта в области, отличающейся от `Process` или `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="13c1a-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="13c1a-116">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13c1a-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="13c1a-117">В примере ниже показано, как запустить функцию, чтобы удалить предыдущую версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13c1a-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="13c1a-118">Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="13c1a-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="13c1a-119">Чтобы запустить скрипт для просмотра только удаляемых компонентов без удаления, используйте параметр `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="13c1a-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="13c1a-120">Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="13c1a-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="13c1a-121">Для удобства следующий скрипт удалит все версии Az, __за исключением__ последней.</span><span class="sxs-lookup"><span data-stu-id="13c1a-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="13c1a-122">Удаление модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="13c1a-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="13c1a-123">Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, существуют два простых метода, которые не требуют запуска сценария `Uninstall-AllModules`, описанного выше.</span><span class="sxs-lookup"><span data-stu-id="13c1a-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two simple options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="13c1a-124">Выбор метода зависит от того, как был установлен AzureRM.</span><span class="sxs-lookup"><span data-stu-id="13c1a-124">Which method you follow depends on how you installed AzureRM.</span></span>
<span data-ttu-id="13c1a-125">Если вы этого не знаете, сперва проверьте действия по удалению MSI.</span><span class="sxs-lookup"><span data-stu-id="13c1a-125">If you're not sure, check the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="13c1a-126">Удаление Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="13c1a-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="13c1a-127">Если вы установили модули AzureRM Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13c1a-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="13c1a-128">платформа</span><span class="sxs-lookup"><span data-stu-id="13c1a-128">Platform</span></span> | <span data-ttu-id="13c1a-129">Указания</span><span class="sxs-lookup"><span data-stu-id="13c1a-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="13c1a-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="13c1a-130">Windows 10</span></span> | <span data-ttu-id="13c1a-131">"Пуск" > "Параметры" > "Приложения"</span><span class="sxs-lookup"><span data-stu-id="13c1a-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="13c1a-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13c1a-132">Windows 7</span></span> </br><span data-ttu-id="13c1a-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="13c1a-133">Windows 8</span></span> | <span data-ttu-id="13c1a-134">"Пуск" > "Панель управления" > "Программы" > "Удаление программы"</span><span class="sxs-lookup"><span data-stu-id="13c1a-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="13c1a-135">В этом окне в списке программ вы должны увидеть модуль __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="13c1a-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="13c1a-136">Это программа, которую можно удалить.</span><span class="sxs-lookup"><span data-stu-id="13c1a-136">This is the app to uninstall.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="13c1a-137">Удаление с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c1a-137">Uninstall from PowerShell</span></span>

<span data-ttu-id="13c1a-138">Если вы установили AzureRM из PowerShellGet, то можете удалить модули с помощью новой команды `Uninstall-AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="13c1a-138">If you installed AzureRM from PowerShellGet, then you can remove the modules with the new `Uninstall-AzureRM` command.</span></span> <span data-ttu-id="13c1a-139">С вашего компьютера удалятся _все_ модули AzureRM, но для этого требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="13c1a-139">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="13c1a-140">Если вам не удается запустить команду `Uninstall-AzureRM`, то вместо нее используйте скрипт `Uninstall-AllModules`, приведенный в этой статье.</span><span class="sxs-lookup"><span data-stu-id="13c1a-140">If you can't successfully run the `Uninstall-AzureRM` command, use the `Uninstall-AllModules` script provided in this article instead.</span></span>