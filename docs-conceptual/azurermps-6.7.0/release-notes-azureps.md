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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018705"
---
# <a name="release-notes"></a><span data-ttu-id="a38c1-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="a38c1-103">Release notes</span></span>

<span data-ttu-id="a38c1-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="a38c1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="a38c1-105">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a38c1-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a38c1-106">AzureRM.Profile</span></span>
* <span data-ttu-id="a38c1-107">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a38c1-108">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="a38c1-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="a38c1-109">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="a38c1-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="a38c1-110">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="a38c1-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="a38c1-111">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a38c1-111">Azure.Storage</span></span>
* <span data-ttu-id="a38c1-112">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="a38c1-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="a38c1-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a38c1-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a38c1-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a38c1-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a38c1-115">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="a38c1-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a38c1-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="a38c1-117">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a38c1-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a38c1-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a38c1-119">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="a38c1-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a38c1-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="a38c1-121">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a38c1-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a38c1-122">AzureRM.Automation</span></span>
* <span data-ttu-id="a38c1-123">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a38c1-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a38c1-124">AzureRM.Backup</span></span>
* <span data-ttu-id="a38c1-125">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a38c1-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a38c1-126">AzureRM.Batch</span></span>
* <span data-ttu-id="a38c1-127">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="a38c1-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="a38c1-128">AzureRM.Billing</span></span>
* <span data-ttu-id="a38c1-129">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a38c1-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a38c1-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="a38c1-131">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a38c1-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a38c1-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a38c1-133">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a38c1-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a38c1-134">AzureRM.Compute</span></span>
* <span data-ttu-id="a38c1-135">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a38c1-136">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a38c1-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="a38c1-137">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a38c1-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="a38c1-138">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="a38c1-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a38c1-139">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="a38c1-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a38c1-140">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="a38c1-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="a38c1-141">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="a38c1-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a38c1-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="a38c1-143">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="a38c1-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a38c1-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="a38c1-145">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="a38c1-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="a38c1-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="a38c1-147">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a38c1-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a38c1-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a38c1-149">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a38c1-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a38c1-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a38c1-151">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a38c1-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a38c1-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a38c1-153">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a38c1-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="a38c1-154">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="a38c1-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a38c1-155">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a38c1-156">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a38c1-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="a38c1-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a38c1-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="a38c1-158">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a38c1-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a38c1-159">AzureRM.Dns</span></span>
* <span data-ttu-id="a38c1-160">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a38c1-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a38c1-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a38c1-162">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a38c1-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a38c1-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="a38c1-164">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="a38c1-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a38c1-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="a38c1-166">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a38c1-167">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="a38c1-167">AzureRM.Insights</span></span>
* <span data-ttu-id="a38c1-168">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a38c1-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a38c1-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="a38c1-170">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a38c1-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a38c1-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a38c1-172">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a38c1-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a38c1-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a38c1-174">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="a38c1-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a38c1-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="a38c1-176">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="a38c1-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a38c1-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="a38c1-178">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="a38c1-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a38c1-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="a38c1-180">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="a38c1-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="a38c1-181">AzureRM.Media</span></span>
* <span data-ttu-id="a38c1-182">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a38c1-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a38c1-183">AzureRM.Network</span></span>
* <span data-ttu-id="a38c1-184">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a38c1-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="a38c1-185">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="a38c1-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a38c1-186">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a38c1-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="a38c1-187">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="a38c1-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a38c1-188">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="a38c1-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a38c1-189">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="a38c1-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a38c1-190">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="a38c1-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="a38c1-191">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="a38c1-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="a38c1-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a38c1-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="a38c1-193">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="a38c1-194">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="a38c1-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a38c1-195">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a38c1-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a38c1-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a38c1-197">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a38c1-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a38c1-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a38c1-199">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="a38c1-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a38c1-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="a38c1-201">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a38c1-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a38c1-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a38c1-203">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="a38c1-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="a38c1-204">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="a38c1-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="a38c1-205">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="a38c1-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="a38c1-206">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a38c1-207">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="a38c1-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="a38c1-208">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="a38c1-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a38c1-209">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="a38c1-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a38c1-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a38c1-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a38c1-211">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a38c1-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a38c1-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a38c1-213">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a38c1-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a38c1-214">AzureRM.Relay</span></span>
* <span data-ttu-id="a38c1-215">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a38c1-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a38c1-216">AzureRM.Resources</span></span>
* <span data-ttu-id="a38c1-217">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="a38c1-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="a38c1-218">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="a38c1-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="a38c1-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a38c1-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="a38c1-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a38c1-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="a38c1-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a38c1-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="a38c1-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a38c1-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="a38c1-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a38c1-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="a38c1-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a38c1-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="a38c1-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a38c1-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="a38c1-226">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a38c1-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="a38c1-227">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a38c1-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="a38c1-228">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a38c1-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a38c1-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a38c1-230">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a38c1-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a38c1-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a38c1-232">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a38c1-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a38c1-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a38c1-234">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a38c1-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a38c1-235">AzureRM.Sql</span></span>
* <span data-ttu-id="a38c1-236">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a38c1-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a38c1-237">AzureRM.Storage</span></span>
* <span data-ttu-id="a38c1-238">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="a38c1-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="a38c1-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="a38c1-240">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a38c1-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a38c1-241">AzureRM.Tags</span></span>
* <span data-ttu-id="a38c1-242">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a38c1-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a38c1-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a38c1-244">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="a38c1-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="a38c1-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="a38c1-246">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a38c1-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a38c1-247">AzureRM.Websites</span></span>
* <span data-ttu-id="a38c1-248">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="a38c1-249">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a38c1-250">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a38c1-250">General</span></span>
* <span data-ttu-id="a38c1-251">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a38c1-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a38c1-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a38c1-252">AzureRM.Profile</span></span>
* <span data-ttu-id="a38c1-253">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a38c1-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="a38c1-254">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="a38c1-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a38c1-255">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a38c1-255">Azure.Storage</span></span>
* <span data-ttu-id="a38c1-256">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="a38c1-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="a38c1-257">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="a38c1-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a38c1-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a38c1-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a38c1-259">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="a38c1-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a38c1-260">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="a38c1-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a38c1-261">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="a38c1-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a38c1-262">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="a38c1-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a38c1-263">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="a38c1-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a38c1-264">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="a38c1-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a38c1-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a38c1-265">AzureRM.Compute</span></span>
* <span data-ttu-id="a38c1-266">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="a38c1-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a38c1-267">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="a38c1-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a38c1-268">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="a38c1-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a38c1-269">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="a38c1-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a38c1-270">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="a38c1-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a38c1-271">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="a38c1-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a38c1-272">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="a38c1-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a38c1-273">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="a38c1-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a38c1-274">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="a38c1-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a38c1-275">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="a38c1-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a38c1-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a38c1-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a38c1-277">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="a38c1-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a38c1-278">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="a38c1-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a38c1-279">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a38c1-280">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="a38c1-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a38c1-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a38c1-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a38c1-282">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="a38c1-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a38c1-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a38c1-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="a38c1-284">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="a38c1-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a38c1-285">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="a38c1-285">AzureRM.Insights</span></span>
* <span data-ttu-id="a38c1-286">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="a38c1-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a38c1-287">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="a38c1-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a38c1-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a38c1-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a38c1-289">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="a38c1-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a38c1-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a38c1-290">AzureRM.Network</span></span>
* <span data-ttu-id="a38c1-291">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="a38c1-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a38c1-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a38c1-292">AzureRM.Resources</span></span>
* <span data-ttu-id="a38c1-293">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="a38c1-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a38c1-294">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="a38c1-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a38c1-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a38c1-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a38c1-296">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="a38c1-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a38c1-297">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="a38c1-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a38c1-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a38c1-298">AzureRM.Sql</span></span>
* <span data-ttu-id="a38c1-299">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a38c1-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a38c1-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a38c1-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a38c1-301">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a38c1-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a38c1-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="a38c1-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a38c1-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="a38c1-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a38c1-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="a38c1-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a38c1-305">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="a38c1-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a38c1-306">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="a38c1-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a38c1-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a38c1-307">AzureRM.Storage</span></span>
* <span data-ttu-id="a38c1-308">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="a38c1-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a38c1-309">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="a38c1-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a38c1-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a38c1-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a38c1-311">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="a38c1-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a38c1-312">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a38c1-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a38c1-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a38c1-313">AzureRM.Tags</span></span>
* <span data-ttu-id="a38c1-314">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="a38c1-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a38c1-315">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a38c1-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a38c1-316">AzureRM.Profile</span></span>
* <span data-ttu-id="a38c1-317">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="a38c1-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a38c1-318">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a38c1-318">Azure.Storage</span></span>
* <span data-ttu-id="a38c1-319">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="a38c1-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="a38c1-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a38c1-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="a38c1-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a38c1-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a38c1-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a38c1-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a38c1-323">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a38c1-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a38c1-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a38c1-324">AzureRM.Automation</span></span>
* <span data-ttu-id="a38c1-325">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="a38c1-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a38c1-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a38c1-326">AzureRM.Compute</span></span>
* <span data-ttu-id="a38c1-327">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a38c1-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a38c1-328">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="a38c1-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a38c1-329">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="a38c1-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a38c1-330">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="a38c1-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a38c1-331">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="a38c1-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a38c1-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a38c1-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="a38c1-333">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="a38c1-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a38c1-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a38c1-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a38c1-335">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="a38c1-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a38c1-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a38c1-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a38c1-337">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="a38c1-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a38c1-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a38c1-338">AzureRM.Network</span></span>
* <span data-ttu-id="a38c1-339">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="a38c1-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a38c1-340">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="a38c1-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a38c1-341">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="a38c1-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a38c1-342">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="a38c1-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a38c1-343">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="a38c1-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a38c1-344">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="a38c1-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a38c1-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a38c1-345">AzureRM.Relay</span></span>
* <span data-ttu-id="a38c1-346">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="a38c1-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a38c1-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a38c1-347">AzureRM.Resources</span></span>
* <span data-ttu-id="a38c1-348">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="a38c1-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a38c1-349">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="a38c1-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a38c1-350">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="a38c1-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a38c1-351">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="a38c1-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a38c1-352">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="a38c1-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a38c1-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a38c1-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a38c1-354">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="a38c1-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a38c1-355">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="a38c1-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a38c1-356">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a38c1-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a38c1-357">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a38c1-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a38c1-358">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a38c1-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a38c1-359">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="a38c1-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a38c1-360">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="a38c1-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a38c1-361">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="a38c1-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a38c1-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a38c1-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a38c1-363">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="a38c1-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a38c1-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a38c1-364">AzureRM.Sql</span></span>
* <span data-ttu-id="a38c1-365">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="a38c1-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a38c1-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="a38c1-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a38c1-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="a38c1-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a38c1-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a38c1-368">AzureRM.Websites</span></span>
* <span data-ttu-id="a38c1-369">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="a38c1-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a38c1-370">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="a38c1-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a38c1-371">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="a38c1-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a38c1-372">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a38c1-373">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="a38c1-373">General</span></span>
* <span data-ttu-id="a38c1-374">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="a38c1-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a38c1-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a38c1-375">AzureRM.Profile</span></span>
* <span data-ttu-id="a38c1-376">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="a38c1-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a38c1-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a38c1-377">AzureRM.Compute</span></span>
* <span data-ttu-id="a38c1-378">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="a38c1-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a38c1-379">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="a38c1-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a38c1-380">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="a38c1-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a38c1-381">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="a38c1-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a38c1-382">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="a38c1-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a38c1-383">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="a38c1-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a38c1-384">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="a38c1-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a38c1-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a38c1-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a38c1-386">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="a38c1-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a38c1-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="a38c1-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a38c1-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="a38c1-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a38c1-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a38c1-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a38c1-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a38c1-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a38c1-391">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a38c1-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a38c1-392">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="a38c1-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a38c1-393">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="a38c1-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a38c1-394">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="a38c1-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a38c1-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a38c1-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="a38c1-396">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="a38c1-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a38c1-397">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="a38c1-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a38c1-398">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a38c1-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a38c1-399">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="a38c1-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a38c1-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a38c1-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a38c1-401">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a38c1-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a38c1-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a38c1-402">AzureRM.Network</span></span>
* <span data-ttu-id="a38c1-403">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="a38c1-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a38c1-404">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="a38c1-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a38c1-405">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="a38c1-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a38c1-406">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="a38c1-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a38c1-407">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="a38c1-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a38c1-408">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="a38c1-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a38c1-409">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="a38c1-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a38c1-410">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="a38c1-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a38c1-411">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="a38c1-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a38c1-412">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="a38c1-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a38c1-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a38c1-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a38c1-414">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="a38c1-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a38c1-415">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="a38c1-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a38c1-416">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="a38c1-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a38c1-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a38c1-417">AzureRM.Resources</span></span>
* <span data-ttu-id="a38c1-418">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="a38c1-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a38c1-419">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="a38c1-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a38c1-420">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="a38c1-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a38c1-421">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="a38c1-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a38c1-422">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a38c1-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a38c1-423">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a38c1-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a38c1-424">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="a38c1-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a38c1-425">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a38c1-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a38c1-426">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a38c1-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a38c1-427">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="a38c1-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a38c1-428">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="a38c1-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a38c1-429">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="a38c1-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a38c1-430">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="a38c1-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a38c1-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a38c1-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a38c1-432">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="a38c1-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a38c1-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a38c1-433">AzureRM.Sql</span></span>
* <span data-ttu-id="a38c1-434">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="a38c1-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a38c1-435">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="a38c1-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a38c1-436">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a38c1-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a38c1-437">AzureRM.Profile</span></span>
* <span data-ttu-id="a38c1-438">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="a38c1-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a38c1-439">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="a38c1-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a38c1-440">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="a38c1-440">Azure.Storage</span></span>
* <span data-ttu-id="a38c1-441">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="a38c1-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a38c1-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a38c1-442">AzureRM.Compute</span></span>
* <span data-ttu-id="a38c1-443">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="a38c1-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a38c1-444">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="a38c1-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a38c1-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a38c1-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a38c1-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a38c1-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a38c1-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a38c1-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a38c1-448">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="a38c1-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a38c1-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a38c1-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a38c1-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a38c1-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a38c1-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a38c1-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a38c1-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a38c1-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a38c1-453">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="a38c1-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a38c1-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a38c1-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a38c1-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a38c1-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a38c1-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a38c1-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a38c1-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a38c1-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a38c1-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a38c1-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a38c1-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a38c1-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a38c1-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a38c1-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a38c1-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a38c1-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a38c1-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a38c1-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a38c1-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a38c1-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a38c1-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a38c1-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a38c1-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a38c1-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a38c1-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a38c1-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a38c1-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a38c1-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a38c1-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a38c1-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a38c1-469">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="a38c1-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a38c1-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a38c1-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a38c1-471">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="a38c1-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a38c1-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a38c1-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a38c1-473">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="a38c1-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a38c1-474">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="a38c1-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a38c1-475">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="a38c1-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a38c1-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a38c1-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a38c1-477">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="a38c1-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a38c1-478">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="a38c1-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a38c1-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a38c1-479">AzureRM.Sql</span></span>
* <span data-ttu-id="a38c1-480">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="a38c1-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a38c1-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a38c1-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a38c1-482">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="a38c1-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a38c1-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a38c1-483">AzureRM.Websites</span></span>
* <span data-ttu-id="a38c1-484">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="a38c1-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a38c1-485">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a38c1-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a38c1-486">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a38c1-487">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="a38c1-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a38c1-488">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a38c1-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a38c1-489">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a38c1-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a38c1-490">AzureRM.Profile</span></span>
* <span data-ttu-id="a38c1-491">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="a38c1-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a38c1-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a38c1-492">AzureRM.Compute</span></span>
* <span data-ttu-id="a38c1-493">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="a38c1-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a38c1-494">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="a38c1-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a38c1-495">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="a38c1-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a38c1-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a38c1-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a38c1-497">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="a38c1-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a38c1-498">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="a38c1-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a38c1-499">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="a38c1-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a38c1-500">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="a38c1-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a38c1-501">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="a38c1-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a38c1-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a38c1-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a38c1-503">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a38c1-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a38c1-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a38c1-504">AzureRM.Network</span></span>
* <span data-ttu-id="a38c1-505">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="a38c1-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a38c1-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a38c1-506">AzureRM.Resources</span></span>
* <span data-ttu-id="a38c1-507">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="a38c1-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a38c1-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a38c1-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a38c1-509">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a38c1-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a38c1-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a38c1-510">AzureRM.Sql</span></span>
* <span data-ttu-id="a38c1-511">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="a38c1-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a38c1-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="a38c1-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a38c1-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="a38c1-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a38c1-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a38c1-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a38c1-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a38c1-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a38c1-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a38c1-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a38c1-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a38c1-517">AzureRM.Websites</span></span>
* <span data-ttu-id="a38c1-518">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="a38c1-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a38c1-519">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="a38c1-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a38c1-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a38c1-520">AzureRM.Profile</span></span>
* <span data-ttu-id="a38c1-521">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="a38c1-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a38c1-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a38c1-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a38c1-523">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="a38c1-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a38c1-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a38c1-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a38c1-525">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="a38c1-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a38c1-526">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="a38c1-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a38c1-527">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a38c1-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a38c1-528">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="a38c1-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a38c1-529">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="a38c1-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a38c1-530">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="a38c1-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a38c1-531">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="a38c1-531">Added support for MSI identity</span></span>
* <span data-ttu-id="a38c1-532">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="a38c1-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a38c1-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a38c1-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a38c1-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a38c1-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a38c1-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a38c1-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a38c1-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a38c1-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a38c1-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a38c1-537">AzureRM.Batch</span></span>
* <span data-ttu-id="a38c1-538">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="a38c1-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a38c1-539">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="a38c1-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a38c1-540">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="a38c1-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="a38c1-541">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="a38c1-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a38c1-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a38c1-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a38c1-543">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="a38c1-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a38c1-544">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a38c1-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a38c1-545">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="a38c1-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a38c1-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a38c1-546">AzureRM.Network</span></span>
* <span data-ttu-id="a38c1-547">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="a38c1-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a38c1-548">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="a38c1-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a38c1-549">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a38c1-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a38c1-550">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a38c1-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a38c1-551">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a38c1-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a38c1-552">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a38c1-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a38c1-553">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a38c1-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a38c1-554">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="a38c1-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a38c1-555">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="a38c1-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a38c1-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a38c1-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a38c1-557">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="a38c1-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a38c1-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a38c1-558">AzureRM.Sql</span></span>
* <span data-ttu-id="a38c1-559">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="a38c1-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a38c1-560">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="a38c1-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a38c1-561">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="a38c1-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a38c1-562">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="a38c1-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a38c1-563">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="a38c1-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a38c1-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="a38c1-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a38c1-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="a38c1-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a38c1-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a38c1-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a38c1-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a38c1-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a38c1-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a38c1-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a38c1-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a38c1-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a38c1-570">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a38c1-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>