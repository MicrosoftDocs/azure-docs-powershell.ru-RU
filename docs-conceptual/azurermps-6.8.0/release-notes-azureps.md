---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117135"
---
# <a name="release-notes"></a><span data-ttu-id="a90c8-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="a90c8-103">Release notes</span></span>

<span data-ttu-id="a90c8-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="a90c8-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="a90c8-105">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a90c8-106">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a90c8-106">General</span></span>
* <span data-ttu-id="a90c8-107">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a90c8-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-108">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-109">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="a90c8-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a90c8-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a90c8-110">AzureRM.Compute</span></span>
* <span data-ttu-id="a90c8-111">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="a90c8-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a90c8-112">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="a90c8-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a90c8-113">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="a90c8-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a90c8-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a90c8-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="a90c8-115">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="a90c8-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a90c8-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a90c8-116">AzureRM.Network</span></span>
* <span data-ttu-id="a90c8-117">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="a90c8-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a90c8-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a90c8-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a90c8-119">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="a90c8-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a90c8-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a90c8-120">AzureRM.Resources</span></span>
* <span data-ttu-id="a90c8-121">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="a90c8-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a90c8-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90c8-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a90c8-123">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="a90c8-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a90c8-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a90c8-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a90c8-125">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="a90c8-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a90c8-126">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="a90c8-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a90c8-127">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="a90c8-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a90c8-128">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="a90c8-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a90c8-129">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="a90c8-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a90c8-130">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="a90c8-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a90c8-131">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="a90c8-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a90c8-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a90c8-132">AzureRM.Websites</span></span>
* <span data-ttu-id="a90c8-133">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a90c8-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="a90c8-134">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-135">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-136">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a90c8-137">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="a90c8-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="a90c8-138">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="a90c8-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="a90c8-139">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="a90c8-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="a90c8-140">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a90c8-140">Azure.Storage</span></span>
* <span data-ttu-id="a90c8-141">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="a90c8-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="a90c8-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a90c8-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a90c8-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90c8-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a90c8-144">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="a90c8-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90c8-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="a90c8-146">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a90c8-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90c8-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a90c8-148">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="a90c8-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a90c8-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="a90c8-150">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a90c8-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a90c8-151">AzureRM.Automation</span></span>
* <span data-ttu-id="a90c8-152">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a90c8-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a90c8-153">AzureRM.Backup</span></span>
* <span data-ttu-id="a90c8-154">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a90c8-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a90c8-155">AzureRM.Batch</span></span>
* <span data-ttu-id="a90c8-156">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="a90c8-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="a90c8-157">AzureRM.Billing</span></span>
* <span data-ttu-id="a90c8-158">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a90c8-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a90c8-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="a90c8-160">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a90c8-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a90c8-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a90c8-162">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a90c8-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a90c8-163">AzureRM.Compute</span></span>
* <span data-ttu-id="a90c8-164">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a90c8-165">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a90c8-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="a90c8-166">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a90c8-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="a90c8-167">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="a90c8-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a90c8-168">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="a90c8-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a90c8-169">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="a90c8-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="a90c8-170">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="a90c8-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a90c8-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="a90c8-172">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="a90c8-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a90c8-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="a90c8-174">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="a90c8-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="a90c8-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="a90c8-176">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a90c8-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a90c8-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a90c8-178">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a90c8-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a90c8-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a90c8-180">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a90c8-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90c8-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a90c8-182">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a90c8-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="a90c8-183">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="a90c8-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a90c8-184">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a90c8-185">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a90c8-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="a90c8-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a90c8-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="a90c8-187">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a90c8-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a90c8-188">AzureRM.Dns</span></span>
* <span data-ttu-id="a90c8-189">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a90c8-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a90c8-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a90c8-191">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a90c8-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a90c8-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="a90c8-193">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="a90c8-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a90c8-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="a90c8-195">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a90c8-196">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="a90c8-196">AzureRM.Insights</span></span>
* <span data-ttu-id="a90c8-197">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a90c8-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a90c8-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="a90c8-199">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a90c8-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90c8-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a90c8-201">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a90c8-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a90c8-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a90c8-203">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="a90c8-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a90c8-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="a90c8-205">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="a90c8-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a90c8-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="a90c8-207">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="a90c8-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a90c8-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="a90c8-209">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="a90c8-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="a90c8-210">AzureRM.Media</span></span>
* <span data-ttu-id="a90c8-211">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a90c8-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a90c8-212">AzureRM.Network</span></span>
* <span data-ttu-id="a90c8-213">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a90c8-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="a90c8-214">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="a90c8-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a90c8-215">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a90c8-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="a90c8-216">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="a90c8-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a90c8-217">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="a90c8-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a90c8-218">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="a90c8-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a90c8-219">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="a90c8-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="a90c8-220">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="a90c8-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="a90c8-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a90c8-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="a90c8-222">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="a90c8-223">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="a90c8-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a90c8-224">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a90c8-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a90c8-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a90c8-226">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a90c8-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a90c8-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a90c8-228">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="a90c8-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90c8-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="a90c8-230">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a90c8-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a90c8-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a90c8-232">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="a90c8-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="a90c8-233">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="a90c8-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="a90c8-234">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="a90c8-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="a90c8-235">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a90c8-236">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="a90c8-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="a90c8-237">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="a90c8-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a90c8-238">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="a90c8-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a90c8-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a90c8-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a90c8-240">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a90c8-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a90c8-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a90c8-242">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a90c8-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a90c8-243">AzureRM.Relay</span></span>
* <span data-ttu-id="a90c8-244">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a90c8-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a90c8-245">AzureRM.Resources</span></span>
* <span data-ttu-id="a90c8-246">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="a90c8-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="a90c8-247">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a90c8-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="a90c8-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a90c8-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="a90c8-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a90c8-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="a90c8-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a90c8-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="a90c8-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a90c8-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="a90c8-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a90c8-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="a90c8-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a90c8-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="a90c8-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a90c8-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="a90c8-255">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a90c8-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="a90c8-256">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a90c8-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="a90c8-257">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a90c8-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a90c8-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a90c8-259">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a90c8-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90c8-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a90c8-261">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a90c8-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90c8-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a90c8-263">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a90c8-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a90c8-264">AzureRM.Sql</span></span>
* <span data-ttu-id="a90c8-265">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a90c8-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a90c8-266">AzureRM.Storage</span></span>
* <span data-ttu-id="a90c8-267">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="a90c8-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="a90c8-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="a90c8-269">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a90c8-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a90c8-270">AzureRM.Tags</span></span>
* <span data-ttu-id="a90c8-271">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a90c8-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a90c8-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a90c8-273">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="a90c8-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="a90c8-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="a90c8-275">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a90c8-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a90c8-276">AzureRM.Websites</span></span>
* <span data-ttu-id="a90c8-277">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="a90c8-278">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a90c8-279">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a90c8-279">General</span></span>
* <span data-ttu-id="a90c8-280">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a90c8-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-281">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-282">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a90c8-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="a90c8-283">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="a90c8-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a90c8-284">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a90c8-284">Azure.Storage</span></span>
* <span data-ttu-id="a90c8-285">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="a90c8-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="a90c8-286">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="a90c8-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a90c8-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90c8-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a90c8-288">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="a90c8-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a90c8-289">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="a90c8-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a90c8-290">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="a90c8-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a90c8-291">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="a90c8-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a90c8-292">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="a90c8-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a90c8-293">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="a90c8-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a90c8-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a90c8-294">AzureRM.Compute</span></span>
* <span data-ttu-id="a90c8-295">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="a90c8-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a90c8-296">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="a90c8-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a90c8-297">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="a90c8-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a90c8-298">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="a90c8-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a90c8-299">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="a90c8-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a90c8-300">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="a90c8-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a90c8-301">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="a90c8-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a90c8-302">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="a90c8-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a90c8-303">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="a90c8-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a90c8-304">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="a90c8-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a90c8-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a90c8-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a90c8-306">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="a90c8-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a90c8-307">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="a90c8-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a90c8-308">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a90c8-309">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="a90c8-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a90c8-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90c8-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a90c8-311">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="a90c8-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a90c8-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a90c8-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="a90c8-313">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="a90c8-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a90c8-314">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="a90c8-314">AzureRM.Insights</span></span>
* <span data-ttu-id="a90c8-315">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="a90c8-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a90c8-316">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="a90c8-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a90c8-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90c8-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a90c8-318">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="a90c8-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a90c8-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a90c8-319">AzureRM.Network</span></span>
* <span data-ttu-id="a90c8-320">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="a90c8-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a90c8-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a90c8-321">AzureRM.Resources</span></span>
* <span data-ttu-id="a90c8-322">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="a90c8-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a90c8-323">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="a90c8-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a90c8-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90c8-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a90c8-325">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="a90c8-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a90c8-326">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="a90c8-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a90c8-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a90c8-327">AzureRM.Sql</span></span>
* <span data-ttu-id="a90c8-328">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a90c8-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a90c8-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a90c8-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a90c8-330">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a90c8-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a90c8-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="a90c8-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a90c8-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="a90c8-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a90c8-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="a90c8-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a90c8-334">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="a90c8-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a90c8-335">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="a90c8-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a90c8-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a90c8-336">AzureRM.Storage</span></span>
* <span data-ttu-id="a90c8-337">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="a90c8-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a90c8-338">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="a90c8-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a90c8-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a90c8-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a90c8-340">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="a90c8-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a90c8-341">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a90c8-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a90c8-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a90c8-342">AzureRM.Tags</span></span>
* <span data-ttu-id="a90c8-343">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="a90c8-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a90c8-344">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-345">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-346">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="a90c8-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a90c8-347">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a90c8-347">Azure.Storage</span></span>
* <span data-ttu-id="a90c8-348">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="a90c8-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="a90c8-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a90c8-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="a90c8-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a90c8-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a90c8-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90c8-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a90c8-352">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a90c8-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a90c8-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a90c8-353">AzureRM.Automation</span></span>
* <span data-ttu-id="a90c8-354">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="a90c8-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a90c8-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a90c8-355">AzureRM.Compute</span></span>
* <span data-ttu-id="a90c8-356">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a90c8-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a90c8-357">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="a90c8-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a90c8-358">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="a90c8-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a90c8-359">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="a90c8-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a90c8-360">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="a90c8-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a90c8-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a90c8-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="a90c8-362">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="a90c8-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a90c8-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90c8-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a90c8-364">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="a90c8-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a90c8-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a90c8-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a90c8-366">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="a90c8-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a90c8-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a90c8-367">AzureRM.Network</span></span>
* <span data-ttu-id="a90c8-368">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="a90c8-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a90c8-369">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a90c8-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a90c8-370">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="a90c8-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a90c8-371">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="a90c8-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a90c8-372">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="a90c8-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a90c8-373">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="a90c8-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a90c8-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a90c8-374">AzureRM.Relay</span></span>
* <span data-ttu-id="a90c8-375">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="a90c8-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a90c8-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a90c8-376">AzureRM.Resources</span></span>
* <span data-ttu-id="a90c8-377">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="a90c8-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a90c8-378">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="a90c8-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a90c8-379">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="a90c8-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a90c8-380">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="a90c8-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a90c8-381">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="a90c8-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a90c8-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90c8-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a90c8-383">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="a90c8-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a90c8-384">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="a90c8-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a90c8-385">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a90c8-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a90c8-386">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a90c8-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a90c8-387">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a90c8-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a90c8-388">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a90c8-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a90c8-389">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="a90c8-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a90c8-390">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="a90c8-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a90c8-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90c8-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a90c8-392">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="a90c8-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a90c8-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a90c8-393">AzureRM.Sql</span></span>
* <span data-ttu-id="a90c8-394">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="a90c8-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a90c8-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="a90c8-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a90c8-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="a90c8-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a90c8-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a90c8-397">AzureRM.Websites</span></span>
* <span data-ttu-id="a90c8-398">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="a90c8-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a90c8-399">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="a90c8-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a90c8-400">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="a90c8-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a90c8-401">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a90c8-402">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a90c8-402">General</span></span>
* <span data-ttu-id="a90c8-403">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="a90c8-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-404">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-405">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="a90c8-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a90c8-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a90c8-406">AzureRM.Compute</span></span>
* <span data-ttu-id="a90c8-407">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="a90c8-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a90c8-408">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="a90c8-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a90c8-409">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="a90c8-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a90c8-410">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="a90c8-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a90c8-411">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="a90c8-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a90c8-412">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="a90c8-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a90c8-413">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="a90c8-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a90c8-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a90c8-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a90c8-415">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="a90c8-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a90c8-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="a90c8-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a90c8-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="a90c8-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a90c8-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a90c8-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a90c8-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90c8-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a90c8-420">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a90c8-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a90c8-421">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="a90c8-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a90c8-422">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="a90c8-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a90c8-423">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="a90c8-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a90c8-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a90c8-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="a90c8-425">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="a90c8-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a90c8-426">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="a90c8-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a90c8-427">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a90c8-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a90c8-428">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="a90c8-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a90c8-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90c8-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a90c8-430">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a90c8-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a90c8-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a90c8-431">AzureRM.Network</span></span>
* <span data-ttu-id="a90c8-432">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="a90c8-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a90c8-433">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="a90c8-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a90c8-434">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="a90c8-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a90c8-435">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="a90c8-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a90c8-436">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="a90c8-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a90c8-437">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="a90c8-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a90c8-438">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="a90c8-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a90c8-439">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="a90c8-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a90c8-440">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="a90c8-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a90c8-441">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="a90c8-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a90c8-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a90c8-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a90c8-443">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="a90c8-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a90c8-444">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="a90c8-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a90c8-445">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="a90c8-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a90c8-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a90c8-446">AzureRM.Resources</span></span>
* <span data-ttu-id="a90c8-447">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="a90c8-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a90c8-448">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="a90c8-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a90c8-449">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="a90c8-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a90c8-450">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="a90c8-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a90c8-451">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a90c8-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a90c8-452">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a90c8-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a90c8-453">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="a90c8-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a90c8-454">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a90c8-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a90c8-455">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a90c8-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a90c8-456">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="a90c8-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a90c8-457">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a90c8-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a90c8-458">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="a90c8-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a90c8-459">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="a90c8-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a90c8-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90c8-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a90c8-461">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="a90c8-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a90c8-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a90c8-462">AzureRM.Sql</span></span>
* <span data-ttu-id="a90c8-463">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="a90c8-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a90c8-464">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="a90c8-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a90c8-465">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-466">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-467">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="a90c8-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a90c8-468">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="a90c8-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a90c8-469">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a90c8-469">Azure.Storage</span></span>
* <span data-ttu-id="a90c8-470">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="a90c8-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a90c8-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a90c8-471">AzureRM.Compute</span></span>
* <span data-ttu-id="a90c8-472">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="a90c8-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a90c8-473">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a90c8-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a90c8-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a90c8-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a90c8-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a90c8-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a90c8-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a90c8-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a90c8-477">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="a90c8-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a90c8-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90c8-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a90c8-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90c8-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a90c8-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90c8-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a90c8-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a90c8-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a90c8-482">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="a90c8-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a90c8-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a90c8-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a90c8-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a90c8-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a90c8-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a90c8-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a90c8-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a90c8-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a90c8-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a90c8-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a90c8-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a90c8-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a90c8-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a90c8-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a90c8-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a90c8-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a90c8-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a90c8-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a90c8-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a90c8-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a90c8-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a90c8-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a90c8-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a90c8-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a90c8-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a90c8-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a90c8-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a90c8-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a90c8-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a90c8-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a90c8-498">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="a90c8-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a90c8-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90c8-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a90c8-500">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="a90c8-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a90c8-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a90c8-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a90c8-502">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="a90c8-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a90c8-503">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="a90c8-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a90c8-504">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="a90c8-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a90c8-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a90c8-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a90c8-506">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="a90c8-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a90c8-507">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="a90c8-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a90c8-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a90c8-508">AzureRM.Sql</span></span>
* <span data-ttu-id="a90c8-509">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="a90c8-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a90c8-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a90c8-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a90c8-511">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="a90c8-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a90c8-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a90c8-512">AzureRM.Websites</span></span>
* <span data-ttu-id="a90c8-513">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="a90c8-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a90c8-514">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a90c8-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a90c8-515">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a90c8-516">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="a90c8-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a90c8-517">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a90c8-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a90c8-518">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-519">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-520">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="a90c8-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a90c8-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a90c8-521">AzureRM.Compute</span></span>
* <span data-ttu-id="a90c8-522">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="a90c8-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a90c8-523">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="a90c8-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a90c8-524">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="a90c8-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a90c8-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a90c8-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a90c8-526">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="a90c8-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a90c8-527">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="a90c8-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a90c8-528">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="a90c8-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a90c8-529">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="a90c8-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a90c8-530">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="a90c8-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a90c8-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90c8-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a90c8-532">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a90c8-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a90c8-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a90c8-533">AzureRM.Network</span></span>
* <span data-ttu-id="a90c8-534">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="a90c8-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a90c8-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a90c8-535">AzureRM.Resources</span></span>
* <span data-ttu-id="a90c8-536">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="a90c8-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a90c8-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a90c8-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a90c8-538">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a90c8-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a90c8-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a90c8-539">AzureRM.Sql</span></span>
* <span data-ttu-id="a90c8-540">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="a90c8-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a90c8-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="a90c8-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a90c8-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="a90c8-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a90c8-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a90c8-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a90c8-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a90c8-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a90c8-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a90c8-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a90c8-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a90c8-546">AzureRM.Websites</span></span>
* <span data-ttu-id="a90c8-547">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="a90c8-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a90c8-548">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a90c8-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a90c8-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a90c8-549">AzureRM.Profile</span></span>
* <span data-ttu-id="a90c8-550">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="a90c8-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a90c8-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90c8-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a90c8-552">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="a90c8-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a90c8-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90c8-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a90c8-554">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="a90c8-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a90c8-555">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="a90c8-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a90c8-556">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a90c8-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a90c8-557">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="a90c8-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a90c8-558">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="a90c8-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a90c8-559">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="a90c8-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a90c8-560">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="a90c8-560">Added support for MSI identity</span></span>
* <span data-ttu-id="a90c8-561">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="a90c8-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a90c8-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a90c8-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a90c8-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90c8-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a90c8-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a90c8-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a90c8-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a90c8-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a90c8-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a90c8-566">AzureRM.Batch</span></span>
* <span data-ttu-id="a90c8-567">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="a90c8-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a90c8-568">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="a90c8-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a90c8-569">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="a90c8-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="a90c8-570">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="a90c8-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a90c8-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90c8-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a90c8-572">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="a90c8-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a90c8-573">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a90c8-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a90c8-574">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a90c8-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a90c8-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a90c8-575">AzureRM.Network</span></span>
* <span data-ttu-id="a90c8-576">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="a90c8-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a90c8-577">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="a90c8-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a90c8-578">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a90c8-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a90c8-579">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a90c8-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a90c8-580">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a90c8-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a90c8-581">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a90c8-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a90c8-582">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a90c8-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a90c8-583">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="a90c8-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a90c8-584">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a90c8-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a90c8-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90c8-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a90c8-586">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="a90c8-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a90c8-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a90c8-587">AzureRM.Sql</span></span>
* <span data-ttu-id="a90c8-588">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="a90c8-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a90c8-589">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="a90c8-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a90c8-590">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="a90c8-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a90c8-591">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="a90c8-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a90c8-592">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="a90c8-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a90c8-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="a90c8-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a90c8-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="a90c8-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a90c8-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a90c8-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a90c8-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a90c8-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a90c8-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a90c8-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a90c8-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a90c8-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a90c8-599">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a90c8-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>