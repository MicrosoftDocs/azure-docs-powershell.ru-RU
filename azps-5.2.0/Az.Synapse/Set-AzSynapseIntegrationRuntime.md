---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393388"
---
# <span data-ttu-id="7cd4e-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7cd4e-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="7cd4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd4e-103">Обновляет время интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="7cd4e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7cd4e-104">SYNTAX</span></span>

### <span data-ttu-id="7cd4e-105">SetByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7cd4e-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd4e-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="7cd4e-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd4e-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="7cd4e-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd4e-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="7cd4e-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd4e-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd4e-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd4e-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd4e-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd4e-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7cd4e-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd4e-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7cd4e-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd4e-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cd4e-113">DESCRIPTION</span></span>
<span data-ttu-id="7cd4e-114">Cmdlet **Set-AzSynapseIntegrationRuntime** обновляет время интеграции с определенными параметрами.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="7cd4e-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7cd4e-115">EXAMPLES</span></span>

### <span data-ttu-id="7cd4e-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7cd4e-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="7cd4e-117">Этот cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="7cd4e-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7cd4e-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="7cd4e-119">Он добавляет рабочее пространство для использования общего рабочего времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="7cd4e-120">При использовании `-SharedIntegrationRuntimeResourceId` параметра `-Type` также необходимо включить в него параметр.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="7cd4e-121">Обратите внимание, что рабочей области необходимо предоставить разрешение на использование времени интеграции перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="7cd4e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cd4e-122">PARAMETERS</span></span>

### <span data-ttu-id="7cd4e-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="7cd4e-123">-AuthKey</span></span>
<span data-ttu-id="7cd4e-124">Ключ проверки подлинности для самостоятельной интеграции с запуском.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="7cd4e-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="7cd4e-126">Учетные данные администратора базы данных каталога для времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="7cd4e-127">-CatalogPricingTier</span></span>
<span data-ttu-id="7cd4e-128">Уровень цены для базы данных каталога, уровень интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd4e-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="7cd4e-130">Конечная точка сервера базы данных каталога, интегрированная со временем интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="7cd4e-131">-DataFlowComputeType</span></span>
<span data-ttu-id="7cd4e-132">Вычислять тип кластера потоков данных, который будет выполнять задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="7cd4e-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="7cd4e-134">Основное количество кластеров потоков данных, которые выполняют задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="7cd4e-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="7cd4e-136">Параметр времени жизни (в минутах) кластера потоков данных, который выполняет задание потока данных.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="7cd4e-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="7cd4e-138">Имя Self-Hosted интеграции Runtime, используемой в качестве прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="7cd4e-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="7cd4e-140">Имя связанной службы хранилища BLOB-приложений Azure, которая ссылается на промежуточное хранилище данных, которое будет использоваться при переносе данных между Self-Hosted и Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="7cd4e-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="7cd4e-142">Путь к промежуточному храну данных, используемый при переносе данных между Self-Hosted и runtimes интеграции Azure и SSIS, если не заверен, будет использоваться контейнер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd4e-143">-DefaultProfile</span></span>
<span data-ttu-id="7cd4e-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-145">-Description</span><span class="sxs-lookup"><span data-stu-id="7cd4e-145">-Description</span></span>
<span data-ttu-id="7cd4e-146">Описание времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-146">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="7cd4e-147">-Edition</span></span>
<span data-ttu-id="7cd4e-148">Выпуск для интеграции служб SSIS runtime, который может быть стандартным или корпоративным, по умолчанию является стандартным, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="7cd4e-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="7cd4e-150">Express custom setup for SSIS integration runtime which could be used to setup configurations and 3-party components without custom setup script.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-151">-Force</span><span class="sxs-lookup"><span data-stu-id="7cd4e-151">-Force</span></span>
<span data-ttu-id="7cd4e-152">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-152">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd4e-153">-InputObject</span></span>
<span data-ttu-id="7cd4e-154">Объект интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7cd4e-155">-LicenseType</span></span>
<span data-ttu-id="7cd4e-156">Тип лицензии, который вы хотите выбрать для ИД SSIS.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="7cd4e-157">Существует два типа: LicenseIncluded или BasePrice.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="7cd4e-158">Если у вас есть право на использование преимущества гибридного использования Azure (AHUB), выберите BasePrice.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="7cd4e-159">Если нет, выберите LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-160">-Location</span><span class="sxs-lookup"><span data-stu-id="7cd4e-160">-Location</span></span>
<span data-ttu-id="7cd4e-161">Описание времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="7cd4e-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="7cd4e-163">Максимальное количество параллельных выполнения на каждого узла для управляемой специализированной интеграции во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-164">-Name</span><span class="sxs-lookup"><span data-stu-id="7cd4e-164">-Name</span></span>
<span data-ttu-id="7cd4e-165">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="7cd4e-166">-NodeCount</span></span>
<span data-ttu-id="7cd4e-167">Количество целевых узлов в времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="7cd4e-168">-NodeSize</span></span>
<span data-ttu-id="7cd4e-169">Размер узла время запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="7cd4e-170">-PublicIP</span></span>
<span data-ttu-id="7cd4e-171">Статические общедоступные IP-адреса, которые будут использовать время запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd4e-172">-ResourceGroupName</span></span>
<span data-ttu-id="7cd4e-173">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd4e-174">-ResourceId</span></span>
<span data-ttu-id="7cd4e-175">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="7cd4e-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="7cd4e-177">URI SAS контейнера BLOB-lob Azure, который содержит сценарий настройки.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd4e-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="7cd4e-179">ИД ресурса для общей самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7cd4e-180">-Subnet</span></span>
<span data-ttu-id="7cd4e-181">Имя подсети в VNet.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-182">-Type</span><span class="sxs-lookup"><span data-stu-id="7cd4e-182">-Type</span></span>
<span data-ttu-id="7cd4e-183">Тип времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-183">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="7cd4e-184">-VNetId</span></span>
<span data-ttu-id="7cd4e-185">ИД VNet, к которому будет приступать интеграция со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7cd4e-186">-WorkspaceName</span></span>
<span data-ttu-id="7cd4e-187">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7cd4e-188">-WorkspaceObject</span></span>
<span data-ttu-id="7cd4e-189">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cd4e-190">-Confirm</span></span>
<span data-ttu-id="7cd4e-191">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd4e-192">-WhatIf</span></span>
<span data-ttu-id="7cd4e-193">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd4e-194">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd4e-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd4e-195">CommonParameters</span></span>
<span data-ttu-id="7cd4e-196">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd4e-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd4e-197">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cd4e-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd4e-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cd4e-198">INPUTS</span></span>

### <span data-ttu-id="7cd4e-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7cd4e-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7cd4e-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7cd4e-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7cd4e-201">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7cd4e-201">OUTPUTS</span></span>

### <span data-ttu-id="7cd4e-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7cd4e-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7cd4e-203">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7cd4e-203">NOTES</span></span>

## <span data-ttu-id="7cd4e-204">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cd4e-204">RELATED LINKS</span></span>