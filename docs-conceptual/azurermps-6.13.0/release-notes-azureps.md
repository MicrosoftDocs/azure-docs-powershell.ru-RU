---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52260005"
---
# <a name="release-notes"></a><span data-ttu-id="ced30-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="ced30-103">Release notes</span></span>

<span data-ttu-id="ced30-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="ced30-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="ced30-105">6.13.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-106">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-107">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ced30-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced30-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ced30-109">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ced30-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ced30-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ced30-110">AzureRM.Automation</span></span>
* <span data-ttu-id="ced30-111">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="ced30-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ced30-112">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="ced30-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ced30-113">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="ced30-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ced30-114">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="ced30-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ced30-115">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="ced30-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-116">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-117">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="ced30-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ced30-118">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ced30-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ced30-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ced30-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ced30-120">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ced30-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ced30-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ced30-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ced30-122">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ced30-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-123">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-124">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="ced30-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ced30-125">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="ced30-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ced30-126">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ced30-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ced30-127">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ced30-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ced30-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ced30-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ced30-129">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="ced30-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ced30-130">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="ced30-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ced30-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ced30-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ced30-132">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="ced30-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ced30-133">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ced30-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ced30-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ced30-134">AzureRM.Relay</span></span>
* <span data-ttu-id="ced30-135">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ced30-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-136">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-137">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="ced30-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ced30-138">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="ced30-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ced30-139">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="ced30-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ced30-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced30-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ced30-141">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="ced30-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ced30-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-142">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-143">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ced30-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ced30-144">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ced30-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced30-145">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ced30-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced30-146">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ced30-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced30-147">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ced30-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced30-148">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ced30-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ced30-149">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ced30-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ced30-150">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ced30-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ced30-151">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ced30-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ced30-152">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="ced30-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ced30-153">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="ced30-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ced30-154">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="ced30-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ced30-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced30-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ced30-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced30-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ced30-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced30-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ced30-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced30-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ced30-159">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="ced30-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="ced30-160">6.12.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-161">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-162">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ced30-163">В командлете Connect-AzureRmAccount параметр TenantId переименован на Tenant и добавлен псевдоним для TenantId.</span><span class="sxs-lookup"><span data-stu-id="ced30-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ced30-164">Обновлено описание TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ced30-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="ced30-165">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="ced30-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ced30-166">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ced30-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ced30-167">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="ced30-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ced30-168">Устранена проблема, при которой командлет Disconnect-AzureRmAccount вызывал сбой при отсутствии подключения.</span><span class="sxs-lookup"><span data-stu-id="ced30-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="ced30-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ced30-169">AzureRM.Automation</span></span>
* <span data-ttu-id="ced30-170">Имя файла библиотеки DLL командлетов переименовано на Microsoft.Azure.Commands.Automation.dll.</span><span class="sxs-lookup"><span data-stu-id="ced30-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ced30-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced30-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ced30-172">Добавлена операция Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ced30-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-173">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-174">Добавлены командлеты Add-AzureRmVmssVMDataDisk и Remove-AzureRmVmssVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="ced30-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ced30-175">Get-AzureRmVMImage отображает AutomaticOSUpgradeProperties.</span><span class="sxs-lookup"><span data-stu-id="ced30-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ced30-176">Устранена проблема, при которой значения параметров SetAzureRmVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="ced30-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ced30-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced30-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ced30-178">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ced30-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ced30-179">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="ced30-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ced30-180">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ced30-180">AzureRM.Insights</span></span>
* <span data-ttu-id="ced30-181">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="ced30-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ced30-182">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ced30-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ced30-183">Исправлена проблема № 7513 [Insights], ппри которой для командлета Set-AzureRMDiagnosticSetting требовалось явное указание категорий во время создания параметра.</span><span class="sxs-lookup"><span data-stu-id="ced30-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ced30-184">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="ced30-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-185">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-186">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ced30-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ced30-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced30-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ced30-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ced30-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ced30-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ced30-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ced30-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ced30-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ced30-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced30-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ced30-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ced30-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ced30-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced30-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ced30-194">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="ced30-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ced30-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ced30-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ced30-196">Добавлена поддержка общих файловых ресурсов Azure в Службах восстановления.</span><span class="sxs-lookup"><span data-stu-id="ced30-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-197">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-198">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="ced30-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ced30-199">Разрешено перечисление ресурсов с использованием параметра -ResourceId для командлета Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ced30-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-201">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="ced30-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ced30-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced30-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ced30-203">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="ced30-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ced30-204">Исправлен командлет Add-AzureRmServiceFabricClusterCertificate.</span><span class="sxs-lookup"><span data-stu-id="ced30-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ced30-205">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ced30-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ced30-206">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ced30-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ced30-207">Исправлен командлет Update-AzureRmServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ced30-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="ced30-208">6.11.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-209">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-210">Устранена проблема с Get-AzureRmSubscription в CloudShell.</span><span class="sxs-lookup"><span data-stu-id="ced30-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="ced30-211">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ced30-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ced30-212">AzureRM.Backup</span></span>
* <span data-ttu-id="ced30-213">Командлеты Azure Backup объявлены нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="ced30-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-214">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-215">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.</span><span class="sxs-lookup"><span data-stu-id="ced30-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="ced30-216">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ced30-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ced30-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced30-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ced30-218">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="ced30-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ced30-219">Get-AzureRmDataLakeStoreVirtualNetworkRule — позволяет получить или вывести правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ced30-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ced30-220">Add-AzureRmDataLakeStoreVirtualNetworkRule — позволяет добавить правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ced30-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ced30-221">Set-AzureRmDataLakeStoreVirtualNetworkRule — позволяет изменить определенное правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ced30-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ced30-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule — позволяет удалить правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ced30-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-223">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-224">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="ced30-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ced30-225">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ced30-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-226">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-227">Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение.</span><span class="sxs-lookup"><span data-stu-id="ced30-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ced30-228">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="ced30-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="ced30-229">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ced30-230">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ced30-230">Azure.Storage</span></span>
* <span data-ttu-id="ced30-231">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="ced30-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ced30-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ced30-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ced30-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ced30-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ced30-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced30-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ced30-235">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ced30-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-236">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-237">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="ced30-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ced30-238">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="ced30-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="ced30-239">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="ced30-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ced30-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ced30-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ced30-241">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ced30-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-242">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-243">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="ced30-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ced30-244">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ced30-244">new cmdlets added</span></span>
    - <span data-ttu-id="ced30-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced30-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ced30-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced30-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ced30-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced30-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ced30-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced30-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ced30-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="ced30-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ced30-251">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="ced30-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ced30-252">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="ced30-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="ced30-253">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ced30-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ced30-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ced30-255">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="ced30-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ced30-256">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="ced30-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-257">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-258">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ced30-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="ced30-259">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="ced30-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ced30-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-260">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-261">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="ced30-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ced30-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ced30-262">AzureRM.Storage</span></span>
* <span data-ttu-id="ced30-263">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="ced30-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ced30-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ced30-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ced30-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ced30-265">AzureRM.Websites</span></span>
* <span data-ttu-id="ced30-266">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="ced30-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ced30-267">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="ced30-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="ced30-268">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ced30-269">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ced30-269">General</span></span>
* <span data-ttu-id="ced30-270">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="ced30-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ced30-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-271">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-272">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="ced30-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="ced30-273">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="ced30-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="ced30-274">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="ced30-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="ced30-275">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ced30-275">Azure.Storage</span></span>
* <span data-ttu-id="ced30-276">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="ced30-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="ced30-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ced30-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ced30-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced30-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="ced30-279">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="ced30-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-280">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-281">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="ced30-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="ced30-282">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="ced30-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="ced30-283">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="ced30-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ced30-284">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="ced30-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="ced30-285">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="ced30-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ced30-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ced30-286">AzureRM.Dns</span></span>
* <span data-ttu-id="ced30-287">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ced30-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ced30-288">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ced30-288">AzureRM.Insights</span></span>
* <span data-ttu-id="ced30-289">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="ced30-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="ced30-290">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="ced30-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="ced30-291">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="ced30-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="ced30-292">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="ced30-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="ced30-293">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="ced30-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-294">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-295">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ced30-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="ced30-296">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="ced30-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="ced30-297">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="ced30-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ced30-298">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="ced30-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ced30-299">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="ced30-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="ced30-300">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ced30-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="ced30-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ced30-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ced30-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ced30-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ced30-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="ced30-306">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="ced30-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="ced30-307">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="ced30-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="ced30-308">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ced30-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="ced30-309">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ced30-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="ced30-310">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ced30-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="ced30-311">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ced30-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="ced30-312">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ced30-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="ced30-313">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="ced30-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="ced30-314">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ced30-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="ced30-315">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="ced30-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="ced30-316">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ced30-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="ced30-317">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ced30-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="ced30-318">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="ced30-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="ced30-319">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ced30-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="ced30-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ced30-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ced30-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ced30-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ced30-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ced30-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ced30-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ced30-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ced30-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ced30-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ced30-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ced30-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ced30-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ced30-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="ced30-329">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="ced30-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="ced30-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced30-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ced30-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced30-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ced30-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ced30-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="ced30-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ced30-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="ced30-334">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="ced30-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="ced30-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced30-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ced30-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced30-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="ced30-337">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ced30-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="ced30-338">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="ced30-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="ced30-339">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="ced30-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="ced30-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ced30-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ced30-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ced30-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ced30-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ced30-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="ced30-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ced30-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ced30-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ced30-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ced30-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ced30-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ced30-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ced30-352">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ced30-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ced30-354">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="ced30-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ced30-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ced30-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ced30-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced30-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ced30-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ced30-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="ced30-359">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="ced30-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="ced30-360">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="ced30-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="ced30-361">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="ced30-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="ced30-362">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="ced30-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="ced30-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ced30-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="ced30-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="ced30-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ced30-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ced30-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ced30-366">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="ced30-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ced30-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ced30-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ced30-368">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="ced30-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-369">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-370">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="ced30-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="ced30-371">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="ced30-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="ced30-372">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="ced30-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="ced30-373">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="ced30-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="ced30-374">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="ced30-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-376">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="ced30-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="ced30-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="ced30-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="ced30-378">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="ced30-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="ced30-379">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="ced30-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ced30-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ced30-380">AzureRM.Storage</span></span>
* <span data-ttu-id="ced30-381">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="ced30-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="ced30-382">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ced30-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="ced30-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced30-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ced30-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced30-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ced30-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced30-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ced30-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced30-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ced30-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ced30-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ced30-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ced30-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ced30-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ced30-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ced30-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ced30-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ced30-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ced30-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ced30-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ced30-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ced30-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ced30-393">AzureRM.Websites</span></span>
* <span data-ttu-id="ced30-394">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="ced30-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="ced30-395">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="ced30-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="ced30-396">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="ced30-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="ced30-397">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ced30-398">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ced30-398">General</span></span>
* <span data-ttu-id="ced30-399">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ced30-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ced30-400">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="ced30-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ced30-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced30-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ced30-402">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ced30-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ced30-403">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="ced30-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ced30-404">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="ced30-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ced30-405">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="ced30-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ced30-406">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ced30-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ced30-407">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="ced30-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ced30-408">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="ced30-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ced30-409">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="ced30-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ced30-410">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="ced30-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ced30-411">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="ced30-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ced30-412">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="ced30-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ced30-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-413">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-414">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ced30-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ced30-415">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="ced30-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ced30-416">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ced30-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ced30-417">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="ced30-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-418">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-419">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="ced30-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ced30-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ced30-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ced30-421">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="ced30-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ced30-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-422">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-423">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ced30-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-425">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="ced30-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ced30-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ced30-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ced30-427">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ced30-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ced30-428">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ced30-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ced30-429">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="ced30-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ced30-430">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ced30-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ced30-431">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="ced30-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ced30-432">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="ced30-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ced30-433">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ced30-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ced30-434">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ced30-435">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ced30-435">General</span></span>
* <span data-ttu-id="ced30-436">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ced30-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ced30-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-437">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-438">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ced30-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-439">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-440">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ced30-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ced30-441">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="ced30-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ced30-442">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="ced30-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ced30-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced30-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="ced30-444">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="ced30-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-445">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-446">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="ced30-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ced30-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ced30-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ced30-448">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="ced30-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-449">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-450">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="ced30-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-452">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="ced30-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ced30-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ced30-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ced30-454">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ced30-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ced30-455">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ced30-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ced30-456">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="ced30-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ced30-457">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ced30-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ced30-458">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="ced30-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ced30-459">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="ced30-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ced30-460">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ced30-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ced30-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ced30-461">AzureRM.Websites</span></span>
* <span data-ttu-id="ced30-462">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ced30-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ced30-463">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-464">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-465">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ced30-466">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="ced30-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ced30-467">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="ced30-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ced30-468">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ced30-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ced30-469">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ced30-469">Azure.Storage</span></span>
* <span data-ttu-id="ced30-470">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="ced30-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="ced30-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ced30-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ced30-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced30-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ced30-473">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ced30-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced30-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ced30-475">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ced30-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced30-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ced30-477">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ced30-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ced30-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ced30-479">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ced30-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ced30-480">AzureRM.Automation</span></span>
* <span data-ttu-id="ced30-481">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ced30-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ced30-482">AzureRM.Backup</span></span>
* <span data-ttu-id="ced30-483">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ced30-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ced30-484">AzureRM.Batch</span></span>
* <span data-ttu-id="ced30-485">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ced30-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ced30-486">AzureRM.Billing</span></span>
* <span data-ttu-id="ced30-487">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ced30-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced30-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="ced30-489">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ced30-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced30-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ced30-491">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-492">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-493">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ced30-494">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ced30-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ced30-495">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ced30-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ced30-496">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="ced30-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ced30-497">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="ced30-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ced30-498">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="ced30-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="ced30-499">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ced30-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ced30-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ced30-501">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ced30-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ced30-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ced30-503">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ced30-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ced30-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ced30-505">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ced30-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ced30-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ced30-507">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ced30-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ced30-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ced30-509">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ced30-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced30-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ced30-511">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ced30-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ced30-512">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="ced30-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ced30-513">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ced30-514">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ced30-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ced30-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ced30-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ced30-516">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ced30-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ced30-517">AzureRM.Dns</span></span>
* <span data-ttu-id="ced30-518">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ced30-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ced30-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ced30-520">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ced30-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced30-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="ced30-522">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ced30-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced30-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ced30-524">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ced30-525">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ced30-525">AzureRM.Insights</span></span>
* <span data-ttu-id="ced30-526">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ced30-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced30-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="ced30-528">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ced30-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced30-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ced30-530">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ced30-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ced30-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ced30-532">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ced30-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ced30-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ced30-534">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ced30-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ced30-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ced30-536">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ced30-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ced30-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ced30-538">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ced30-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ced30-539">AzureRM.Media</span></span>
* <span data-ttu-id="ced30-540">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-541">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-542">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ced30-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ced30-543">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ced30-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ced30-544">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ced30-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ced30-545">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ced30-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ced30-546">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ced30-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ced30-547">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ced30-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ced30-548">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="ced30-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ced30-549">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="ced30-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ced30-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ced30-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ced30-551">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ced30-552">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="ced30-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ced30-553">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ced30-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced30-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ced30-555">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ced30-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ced30-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ced30-557">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ced30-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced30-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ced30-559">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ced30-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ced30-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ced30-561">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="ced30-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ced30-562">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="ced30-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ced30-563">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="ced30-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ced30-564">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ced30-565">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ced30-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ced30-566">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="ced30-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ced30-567">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="ced30-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ced30-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ced30-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ced30-569">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ced30-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ced30-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ced30-571">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ced30-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ced30-572">AzureRM.Relay</span></span>
* <span data-ttu-id="ced30-573">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-574">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-575">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="ced30-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ced30-576">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ced30-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ced30-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ced30-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ced30-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ced30-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ced30-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ced30-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ced30-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ced30-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ced30-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ced30-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ced30-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ced30-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ced30-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ced30-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ced30-584">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ced30-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ced30-585">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ced30-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ced30-586">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ced30-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ced30-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ced30-588">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-590">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ced30-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced30-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ced30-592">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ced30-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-593">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-594">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ced30-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ced30-595">AzureRM.Storage</span></span>
* <span data-ttu-id="ced30-596">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ced30-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ced30-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ced30-598">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ced30-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ced30-599">AzureRM.Tags</span></span>
* <span data-ttu-id="ced30-600">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ced30-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ced30-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ced30-602">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ced30-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ced30-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ced30-604">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ced30-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ced30-605">AzureRM.Websites</span></span>
* <span data-ttu-id="ced30-606">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ced30-607">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ced30-608">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ced30-608">General</span></span>
* <span data-ttu-id="ced30-609">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ced30-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ced30-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-610">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-611">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="ced30-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ced30-612">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="ced30-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ced30-613">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ced30-613">Azure.Storage</span></span>
* <span data-ttu-id="ced30-614">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="ced30-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ced30-615">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="ced30-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ced30-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced30-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ced30-617">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="ced30-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ced30-618">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="ced30-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ced30-619">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="ced30-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ced30-620">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="ced30-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ced30-621">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="ced30-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ced30-622">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="ced30-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-623">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-624">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="ced30-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ced30-625">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="ced30-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ced30-626">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="ced30-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ced30-627">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="ced30-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ced30-628">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="ced30-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ced30-629">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="ced30-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ced30-630">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="ced30-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ced30-631">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="ced30-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ced30-632">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="ced30-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ced30-633">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="ced30-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ced30-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ced30-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ced30-635">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="ced30-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ced30-636">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="ced30-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ced30-637">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ced30-638">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ced30-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ced30-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced30-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ced30-640">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="ced30-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ced30-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced30-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="ced30-642">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="ced30-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ced30-643">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ced30-643">AzureRM.Insights</span></span>
* <span data-ttu-id="ced30-644">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="ced30-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ced30-645">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="ced30-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ced30-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced30-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ced30-647">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="ced30-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-648">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-649">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="ced30-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-650">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-651">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ced30-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ced30-652">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ced30-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-654">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="ced30-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ced30-655">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="ced30-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ced30-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-656">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-657">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ced30-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ced30-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ced30-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ced30-659">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ced30-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ced30-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="ced30-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ced30-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="ced30-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ced30-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="ced30-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ced30-663">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="ced30-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ced30-664">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="ced30-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ced30-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ced30-665">AzureRM.Storage</span></span>
* <span data-ttu-id="ced30-666">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="ced30-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ced30-667">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="ced30-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ced30-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced30-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ced30-669">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="ced30-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ced30-670">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="ced30-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ced30-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ced30-671">AzureRM.Tags</span></span>
* <span data-ttu-id="ced30-672">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="ced30-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ced30-673">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-674">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-675">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="ced30-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ced30-676">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ced30-676">Azure.Storage</span></span>
* <span data-ttu-id="ced30-677">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="ced30-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="ced30-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ced30-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="ced30-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ced30-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ced30-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced30-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ced30-681">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ced30-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ced30-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ced30-682">AzureRM.Automation</span></span>
* <span data-ttu-id="ced30-683">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="ced30-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-684">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-685">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ced30-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ced30-686">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="ced30-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ced30-687">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="ced30-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ced30-688">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="ced30-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ced30-689">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="ced30-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ced30-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced30-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="ced30-691">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="ced30-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ced30-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced30-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ced30-693">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="ced30-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ced30-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ced30-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ced30-695">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="ced30-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-696">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-697">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="ced30-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ced30-698">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="ced30-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ced30-699">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="ced30-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ced30-700">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="ced30-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ced30-701">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="ced30-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ced30-702">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="ced30-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ced30-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ced30-703">AzureRM.Relay</span></span>
* <span data-ttu-id="ced30-704">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="ced30-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-705">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-706">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="ced30-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ced30-707">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="ced30-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ced30-708">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="ced30-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ced30-709">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="ced30-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ced30-710">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="ced30-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-712">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="ced30-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ced30-713">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="ced30-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ced30-714">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ced30-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ced30-715">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ced30-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ced30-716">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ced30-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ced30-717">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ced30-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ced30-718">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="ced30-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ced30-719">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="ced30-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ced30-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced30-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ced30-721">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="ced30-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ced30-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-722">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-723">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="ced30-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ced30-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="ced30-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ced30-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="ced30-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ced30-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ced30-726">AzureRM.Websites</span></span>
* <span data-ttu-id="ced30-727">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="ced30-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ced30-728">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="ced30-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ced30-729">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="ced30-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ced30-730">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ced30-731">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ced30-731">General</span></span>
* <span data-ttu-id="ced30-732">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="ced30-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ced30-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-733">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-734">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="ced30-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-735">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-736">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="ced30-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ced30-737">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="ced30-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ced30-738">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="ced30-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ced30-739">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="ced30-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ced30-740">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="ced30-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ced30-741">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="ced30-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ced30-742">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="ced30-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ced30-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ced30-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ced30-744">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="ced30-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ced30-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="ced30-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ced30-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="ced30-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ced30-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ced30-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ced30-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced30-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ced30-749">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ced30-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ced30-750">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="ced30-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ced30-751">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="ced30-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ced30-752">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="ced30-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ced30-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced30-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="ced30-754">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="ced30-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ced30-755">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="ced30-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ced30-756">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ced30-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ced30-757">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ced30-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ced30-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced30-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ced30-759">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ced30-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-760">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-761">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="ced30-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ced30-762">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="ced30-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ced30-763">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="ced30-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ced30-764">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="ced30-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ced30-765">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ced30-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ced30-766">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ced30-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ced30-767">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ced30-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ced30-768">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="ced30-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ced30-769">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="ced30-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ced30-770">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="ced30-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ced30-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ced30-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ced30-772">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="ced30-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ced30-773">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="ced30-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ced30-774">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="ced30-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-775">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-776">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="ced30-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ced30-777">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="ced30-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ced30-778">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="ced30-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ced30-779">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="ced30-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ced30-780">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ced30-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ced30-781">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="ced30-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ced30-782">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="ced30-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ced30-783">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ced30-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ced30-784">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="ced30-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ced30-785">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="ced30-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ced30-786">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ced30-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ced30-787">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="ced30-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ced30-788">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="ced30-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ced30-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced30-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ced30-790">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ced30-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ced30-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-791">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-792">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ced30-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ced30-793">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="ced30-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ced30-794">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-795">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-796">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="ced30-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ced30-797">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="ced30-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ced30-798">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ced30-798">Azure.Storage</span></span>
* <span data-ttu-id="ced30-799">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="ced30-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-800">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-801">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="ced30-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ced30-802">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ced30-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ced30-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ced30-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ced30-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ced30-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ced30-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ced30-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ced30-806">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="ced30-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ced30-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ced30-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ced30-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ced30-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ced30-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ced30-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ced30-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ced30-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ced30-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ced30-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ced30-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ced30-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ced30-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ced30-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ced30-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ced30-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ced30-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ced30-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ced30-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ced30-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ced30-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ced30-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ced30-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ced30-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ced30-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ced30-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ced30-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ced30-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ced30-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ced30-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ced30-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ced30-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ced30-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ced30-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ced30-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ced30-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ced30-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ced30-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ced30-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ced30-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ced30-827">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="ced30-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ced30-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced30-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ced30-829">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="ced30-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ced30-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced30-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ced30-831">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="ced30-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ced30-832">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="ced30-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ced30-833">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="ced30-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ced30-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ced30-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ced30-835">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="ced30-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ced30-836">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="ced30-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ced30-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-837">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-838">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="ced30-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ced30-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ced30-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ced30-840">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="ced30-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ced30-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ced30-841">AzureRM.Websites</span></span>
* <span data-ttu-id="ced30-842">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="ced30-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ced30-843">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ced30-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ced30-844">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ced30-845">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="ced30-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ced30-846">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="ced30-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ced30-847">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-848">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-849">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="ced30-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ced30-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ced30-850">AzureRM.Compute</span></span>
* <span data-ttu-id="ced30-851">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="ced30-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ced30-852">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="ced30-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ced30-853">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="ced30-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ced30-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ced30-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ced30-855">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="ced30-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ced30-856">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="ced30-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ced30-857">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="ced30-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ced30-858">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="ced30-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ced30-859">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ced30-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ced30-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced30-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ced30-861">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ced30-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ced30-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-862">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-863">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="ced30-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ced30-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ced30-864">AzureRM.Resources</span></span>
* <span data-ttu-id="ced30-865">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="ced30-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ced30-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ced30-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ced30-867">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ced30-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ced30-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-868">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-869">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="ced30-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ced30-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="ced30-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ced30-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="ced30-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ced30-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ced30-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ced30-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ced30-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ced30-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ced30-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ced30-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ced30-875">AzureRM.Websites</span></span>
* <span data-ttu-id="ced30-876">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="ced30-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ced30-877">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ced30-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ced30-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ced30-878">AzureRM.Profile</span></span>
* <span data-ttu-id="ced30-879">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="ced30-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ced30-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced30-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ced30-881">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="ced30-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ced30-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced30-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ced30-883">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="ced30-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ced30-884">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="ced30-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ced30-885">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ced30-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ced30-886">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="ced30-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ced30-887">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="ced30-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ced30-888">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ced30-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ced30-889">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="ced30-889">Added support for MSI identity</span></span>
* <span data-ttu-id="ced30-890">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="ced30-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ced30-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ced30-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ced30-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced30-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ced30-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ced30-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ced30-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ced30-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ced30-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ced30-895">AzureRM.Batch</span></span>
* <span data-ttu-id="ced30-896">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="ced30-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ced30-897">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="ced30-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ced30-898">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="ced30-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="ced30-899">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="ced30-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ced30-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced30-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ced30-901">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="ced30-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ced30-902">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ced30-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ced30-903">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ced30-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ced30-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ced30-904">AzureRM.Network</span></span>
* <span data-ttu-id="ced30-905">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="ced30-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ced30-906">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="ced30-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ced30-907">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ced30-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ced30-908">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ced30-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ced30-909">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ced30-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ced30-910">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ced30-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ced30-911">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ced30-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ced30-912">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="ced30-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ced30-913">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ced30-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ced30-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced30-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ced30-915">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="ced30-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ced30-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ced30-916">AzureRM.Sql</span></span>
* <span data-ttu-id="ced30-917">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="ced30-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ced30-918">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="ced30-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ced30-919">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="ced30-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ced30-920">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="ced30-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ced30-921">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="ced30-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ced30-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="ced30-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ced30-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="ced30-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ced30-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ced30-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ced30-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ced30-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ced30-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ced30-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ced30-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ced30-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ced30-928">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ced30-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>