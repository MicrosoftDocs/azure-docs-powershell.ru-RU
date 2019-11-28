---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: ad7677d703a8512d371d3123dc7e541156b95cb8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2019
ms.locfileid: "72814225"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="71acc-103">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="71acc-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="71acc-104">В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="71acc-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="71acc-105">Эти инструкции применимы для платформ Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="71acc-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="71acc-106">В данный момент другие методы установки не поддерживаются для модуля Az.</span><span class="sxs-lookup"><span data-stu-id="71acc-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="71acc-107">Требования</span><span class="sxs-lookup"><span data-stu-id="71acc-107">Requirements</span></span>

<span data-ttu-id="71acc-108">Azure PowerShell работает с PowerShell 5.1 или более поздней версии на платформе Windows или с PowerShell Core 6.x или более поздней версии на любых платформах.</span><span class="sxs-lookup"><span data-stu-id="71acc-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="71acc-109">Если вы не уверены, установлена ли среда PowerShell, либо используете macOS или Linux, [установите последнюю версию PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="71acc-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="71acc-110">Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="71acc-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="71acc-111">Чтобы запустить Azure PowerShell в PowerShell 5.1 на платформе Windows, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="71acc-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="71acc-112">При необходимости выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="71acc-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="71acc-113">Если вы используете Windows 10, среда PowerShell 5.1 уже установлена.</span><span class="sxs-lookup"><span data-stu-id="71acc-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="71acc-114">[Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="71acc-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="71acc-115">При использовании PowerShell Core для Azure PowerShell нет дополнительных требований.</span><span class="sxs-lookup"><span data-stu-id="71acc-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="71acc-116">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="71acc-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="71acc-117">Для PowerShell 5.1 в Windows __не могут__ одновременно быть установлены модули AzureRM и Az.</span><span class="sxs-lookup"><span data-stu-id="71acc-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="71acc-118">Если в системе нужно оставить модуль AzureRM, установите модуль Az для PowerShell Core версии 6.x или более поздней.</span><span class="sxs-lookup"><span data-stu-id="71acc-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="71acc-119">Чтобы сделать это, [установите PowerShell Core версии 6.x или более поздней](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows), а затем следуйте инструкциям в окне терминала PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="71acc-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="71acc-120">Рекомендуемый метод — установка только для активного пользователя:</span><span class="sxs-lookup"><span data-stu-id="71acc-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="71acc-121">Если вам нужно выполнить установку для всех пользователей в системе, потребуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="71acc-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="71acc-122">В сеансе PowerShell с повышенными привилегиями выполните запуск от имени администратора или используйте команду `sudo` в macOS либо Linux:</span><span class="sxs-lookup"><span data-stu-id="71acc-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="71acc-123">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="71acc-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="71acc-124">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="71acc-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="71acc-125">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="71acc-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="71acc-126">Модуль Az — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71acc-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="71acc-127">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="71acc-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="71acc-128">Установка в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="71acc-128">Install offline</span></span>

<span data-ttu-id="71acc-129">В некоторых средах невозможно подключиться к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71acc-129">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="71acc-130">В таких случаях все же можно выполнить установку в автономном режиме, используя один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="71acc-130">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="71acc-131">Скачайте модули в другое расположение и используйте его в качестве источника установки в сети.</span><span class="sxs-lookup"><span data-stu-id="71acc-131">Download the modules to another location and use that as an installation source on your network.</span></span> <span data-ttu-id="71acc-132">Возможно, этот процесс будет сложным, но так вы сможете поместить в кэш модули PowerShell на отдельном сервере или в общей папке, чтобы развернуть их с помощью PowerShellGet на любой системе без подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="71acc-132">This can be a complicated process, but will let you cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="71acc-133">Сведения о том, как настроить локальный репозиторий и установить его в системах без подключения к сети, см. в статье [Работа с локальными хранилищами PowerShellGet](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="71acc-133">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="71acc-134">[Скачайте MSI для Azure PowerShell](install-az-ps-msi.md) на компьютер, подключенный к сети, а затем скопируйте установщик в системы без доступа к коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71acc-134">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="71acc-135">Помните, что установщик MSI работает только с PowerShell 5.1 в Windows.</span><span class="sxs-lookup"><span data-stu-id="71acc-135">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="71acc-136">С помощью команды [Save-Module](/powershell/module/PowershellGet/Save-Module) сохраните модуль в общую папку или в другом источнике и вручную скопируйте на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="71acc-136">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="71acc-137">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="71acc-137">Troubleshooting</span></span>

<span data-ttu-id="71acc-138">Ниже описаны некоторые распространенные проблемы с установкой модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71acc-138">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="71acc-139">Если у вас возникла проблема, не описанная здесь, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="71acc-139">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="71acc-140">Прокси-сервер блокирует подключения</span><span class="sxs-lookup"><span data-stu-id="71acc-140">Proxy blocks connection</span></span>

<span data-ttu-id="71acc-141">Если командлет `Install-Module` возвращает ошибки о том, что коллекция PowerShell недоступна, возможно, ваша система находится за прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="71acc-141">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="71acc-142">Требования к настройке прокси-сервера на уровне системы в разных операционных системах могут отличаться. Эти требования не рассматриваются здесь.</span><span class="sxs-lookup"><span data-stu-id="71acc-142">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="71acc-143">Обратитесь к системному администратору, чтобы узнать о параметрах своего прокси-сервера и о том, как настроить их для своей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71acc-143">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="71acc-144">Возможно, среду PowerShell нельзя настроить для автоматического использования этого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="71acc-144">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="71acc-145">В PowerShell версии 5.1 и более поздних настройте использование прокси-сервера для сеанса PowerShell с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="71acc-145">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="71acc-146">Если учетные данные операционной системы настроены правильно, в результате выполнения приведенной выше команды запросы PowerShell будут направляться через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="71acc-146">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="71acc-147">Чтобы эта настройка сохранялась между сеансами, добавьте команду в [профиль PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="71acc-147">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="71acc-148">Чтобы установить пакет, ваш прокси-сервер должен разрешать HTTPS-подключения по следующему адресу:</span><span class="sxs-lookup"><span data-stu-id="71acc-148">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="71acc-149">Вход</span><span class="sxs-lookup"><span data-stu-id="71acc-149">Sign in</span></span>

<span data-ttu-id="71acc-150">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="71acc-150">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="71acc-151">Если вы отключили автоматическую загрузку модулей, вручную импортируйте модуль с помощью `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="71acc-151">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="71acc-152">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="71acc-152">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="71acc-153">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71acc-153">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="71acc-154">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="71acc-154">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="71acc-155">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="71acc-155">Update the Azure PowerShell module</span></span>

<span data-ttu-id="71acc-156">Команда [Update-Module](/powershell/module/powershellget/update-module) не обновит установку надлежащим образом из-за способа упаковки модуля Az.</span><span class="sxs-lookup"><span data-stu-id="71acc-156">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="71acc-157">Установленный модуль Az фактически собирает и устанавливает все зависимые подмодули, чтобы предоставлять командлеты для каждой службы.</span><span class="sxs-lookup"><span data-stu-id="71acc-157">When you install the Az module, it actually collects and installs all of its dependent submodules, and which provide the cmdlets for each service.</span></span>
<span data-ttu-id="71acc-158">Это означает, что для обновления модуля Azure PowerShell его необходимо __переустановить__, а не просто __выполнить обновление__.</span><span class="sxs-lookup"><span data-stu-id="71acc-158">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="71acc-159">Эта процедура ничем не отличается от установки, но может потребоваться добавить аргумент `-Force`:</span><span class="sxs-lookup"><span data-stu-id="71acc-159">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="71acc-160">Хотя это может перезаписать установленные модули, в системе по-прежнему могут остаться более старые версии.</span><span class="sxs-lookup"><span data-stu-id="71acc-160">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="71acc-161">Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Uninstall the Azure PowerShell module](uninstall-az-ps.md) (Удаление модуля Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="71acc-161">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="71acc-162">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="71acc-162">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="71acc-163">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71acc-163">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="71acc-164">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="71acc-164">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="71acc-165">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="71acc-165">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="71acc-166">Определенную версию модуля `Az` можно установить или загрузить с помощью аргумента `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="71acc-166">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="71acc-167">Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71acc-167">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="71acc-168">Отзывы</span><span class="sxs-lookup"><span data-stu-id="71acc-168">Provide feedback</span></span>

<span data-ttu-id="71acc-169">Если вы нашли ошибку при работе с Azure Powershell, сообщите о ней [на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="71acc-169">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="71acc-170">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="71acc-170">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="71acc-171">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="71acc-171">Next Steps</span></span>

<span data-ttu-id="71acc-172">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="71acc-172">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="71acc-173">Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).</span><span class="sxs-lookup"><span data-stu-id="71acc-173">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>