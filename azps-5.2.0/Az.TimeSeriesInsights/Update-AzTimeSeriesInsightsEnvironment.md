---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401591"
---
# <span data-ttu-id="37ede-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="37ede-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="37ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37ede-102">SYNOPSIS</span></span>
<span data-ttu-id="37ede-103">Обновляет среду с указанным именем в указанной группе подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37ede-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="37ede-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37ede-104">SYNTAX</span></span>

### <span data-ttu-id="37ede-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37ede-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37ede-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37ede-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37ede-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37ede-107">DESCRIPTION</span></span>
<span data-ttu-id="37ede-108">Обновляет среду с указанным именем в указанной группе подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37ede-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="37ede-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37ede-109">EXAMPLES</span></span>

### <span data-ttu-id="37ede-110">Пример 1. Обновление среды статистики по ряду времени (gen1)</span><span class="sxs-lookup"><span data-stu-id="37ede-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="37ede-111">Эта команда обновляет среду статистики по ряду времени (Gen1).</span><span class="sxs-lookup"><span data-stu-id="37ede-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="37ede-112">Пример 2. Обновление среды статистики по ряду времени «Один»"</span><span class="sxs-lookup"><span data-stu-id="37ede-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="37ede-113">Эта команда обновляет среду статистики по ряду времени (Gen1).</span><span class="sxs-lookup"><span data-stu-id="37ede-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="37ede-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37ede-114">PARAMETERS</span></span>

### <span data-ttu-id="37ede-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37ede-115">-AsJob</span></span>
<span data-ttu-id="37ede-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="37ede-116">Run the command as a job</span></span>

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

### <span data-ttu-id="37ede-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ede-117">-DefaultProfile</span></span>
<span data-ttu-id="37ede-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37ede-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37ede-119">-InputObject</span></span>
<span data-ttu-id="37ede-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="37ede-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-121">-Name</span><span class="sxs-lookup"><span data-stu-id="37ede-121">-Name</span></span>
<span data-ttu-id="37ede-122">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37ede-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="37ede-123">-NoWait</span></span>
<span data-ttu-id="37ede-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="37ede-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="37ede-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ede-125">-ResourceGroupName</span></span>
<span data-ttu-id="37ede-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="37ede-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37ede-127">-SubscriptionId</span></span>
<span data-ttu-id="37ede-128">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="37ede-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="37ede-129">-Tag</span></span>
<span data-ttu-id="37ede-130">Пары ключевых значений дополнительных свойств для среды.</span><span class="sxs-lookup"><span data-stu-id="37ede-130">Key-value pairs of additional properties for the environment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37ede-131">-Confirm</span></span>
<span data-ttu-id="37ede-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ede-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ede-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ede-133">-WhatIf</span></span>
<span data-ttu-id="37ede-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ede-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ede-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="37ede-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ede-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ede-136">CommonParameters</span></span>
<span data-ttu-id="37ede-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ede-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ede-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37ede-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ede-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37ede-139">INPUTS</span></span>

### <span data-ttu-id="37ede-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="37ede-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="37ede-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37ede-141">OUTPUTS</span></span>

### <span data-ttu-id="37ede-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="37ede-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="37ede-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37ede-143">NOTES</span></span>

<span data-ttu-id="37ede-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="37ede-144">ALIASES</span></span>

<span data-ttu-id="37ede-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="37ede-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37ede-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="37ede-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37ede-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37ede-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37ede-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="37ede-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37ede-149">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="37ede-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="37ede-150">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="37ede-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="37ede-151">`[EventSourceName <String>]`: имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="37ede-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="37ede-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="37ede-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37ede-153">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="37ede-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="37ede-154">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="37ede-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="37ede-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="37ede-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="37ede-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37ede-156">RELATED LINKS</span></span>
