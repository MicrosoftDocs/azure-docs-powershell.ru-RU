---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399756"
---
# <span data-ttu-id="02a76-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="02a76-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="02a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a76-102">SYNOPSIS</span></span>
<span data-ttu-id="02a76-103">Обновление балансиров нагрузки переднего входа</span><span class="sxs-lookup"><span data-stu-id="02a76-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="02a76-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02a76-104">SYNTAX</span></span>

### <span data-ttu-id="02a76-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02a76-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a76-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a76-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a76-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a76-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02a76-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02a76-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a76-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02a76-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a76-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02a76-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a76-114">DESCRIPTION</span></span>
<span data-ttu-id="02a76-115">Для балансиента загрузки front Door обновляется **cmdlet Set-AzFrontDoor.**</span><span class="sxs-lookup"><span data-stu-id="02a76-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="02a76-116">Если входные параметры не предоставлены, будут использоваться старые параметры из существующей передней двери.</span><span class="sxs-lookup"><span data-stu-id="02a76-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="02a76-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02a76-117">EXAMPLES</span></span>

### <span data-ttu-id="02a76-118">Пример 1. Обновление существующей передней двери с помощью FrontDoorName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="02a76-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="02a76-119">обновить существующий FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="02a76-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="02a76-120">Пример 2. Обновление существующей передней двери с помощью объекта PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="02a76-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="02a76-121">обновить существующий FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="02a76-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="02a76-122">Пример 3. Обновление существующей передней двери с помощью ResourceId</span><span class="sxs-lookup"><span data-stu-id="02a76-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="02a76-123">обновить существующий FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="02a76-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="02a76-124">Пример 4. Обновление свойства BackendPoolSetting EnforceCertificateNameCheck существующей передней двери с -DisableCertificateNameCheck switch parameter</span><span class="sxs-lookup"><span data-stu-id="02a76-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="02a76-125">Перед обновлением передней двери можно определить с помощью FrontoorName и ResourceGroupName, объекта PSFrontDoor или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="02a76-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="02a76-126">(Примеры см. выше в трех примерах. В примере ниже используется объект PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="02a76-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="02a76-127">обновить существующий FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="02a76-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="02a76-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02a76-128">PARAMETERS</span></span>

### <span data-ttu-id="02a76-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="02a76-129">-BackendPool</span></span>
<span data-ttu-id="02a76-130">Backendpools available to routing rule.</span><span class="sxs-lookup"><span data-stu-id="02a76-130">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="02a76-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="02a76-132">Параметры всех backendPools.</span><span class="sxs-lookup"><span data-stu-id="02a76-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a76-133">-DefaultProfile</span></span>
<span data-ttu-id="02a76-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02a76-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a76-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="02a76-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="02a76-136">Следует ли отключить проверку имени сертификата по HTTPS-запросам во все пулы backend.</span><span class="sxs-lookup"><span data-stu-id="02a76-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="02a76-137">Никакие действия с запросами, не относясьми к HTTPS-запросам.</span><span class="sxs-lookup"><span data-stu-id="02a76-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="02a76-138">-EnabledState</span></span>
<span data-ttu-id="02a76-139">Состояние эксплуатации балансиров нагрузки переднего входа.</span><span class="sxs-lookup"><span data-stu-id="02a76-139">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="02a76-140">-FrontendEndpoint</span></span>
<span data-ttu-id="02a76-141">Конечные точки переднего входа, доступные для правила маршрутки.</span><span class="sxs-lookup"><span data-stu-id="02a76-141">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="02a76-142">-HealthProbeSetting</span></span>
<span data-ttu-id="02a76-143">Параметры безопасности, связанные с этим экземпляром передней двери.</span><span class="sxs-lookup"><span data-stu-id="02a76-143">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02a76-144">-InputObject</span></span>
<span data-ttu-id="02a76-145">Объект передней двери, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="02a76-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="02a76-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="02a76-147">Параметры балансировки нагрузки, связанные с этим экземпляром передней двери.</span><span class="sxs-lookup"><span data-stu-id="02a76-147">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-148">-Name</span><span class="sxs-lookup"><span data-stu-id="02a76-148">-Name</span></span>
<span data-ttu-id="02a76-149">Название передней двери, которое нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="02a76-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a76-150">-ResourceGroupName</span></span>
<span data-ttu-id="02a76-151">Группа ресурсов, к которой относится front Door.</span><span class="sxs-lookup"><span data-stu-id="02a76-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02a76-152">-ResourceId</span></span>
<span data-ttu-id="02a76-153">Resource Id of the Front Door to update</span><span class="sxs-lookup"><span data-stu-id="02a76-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="02a76-154">-RoutingRule</span></span>
<span data-ttu-id="02a76-155">Правила маршрутов, связанные с этим frontDoor</span><span class="sxs-lookup"><span data-stu-id="02a76-155">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a76-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="02a76-156">-Tag</span></span>
<span data-ttu-id="02a76-157">Теги, которые связываются с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="02a76-157">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="02a76-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a76-158">-Confirm</span></span>
<span data-ttu-id="02a76-159">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02a76-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a76-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a76-160">-WhatIf</span></span>
<span data-ttu-id="02a76-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02a76-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a76-162">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02a76-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a76-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a76-163">CommonParameters</span></span>
<span data-ttu-id="02a76-164">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a76-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a76-165">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02a76-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a76-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02a76-166">INPUTS</span></span>

### <span data-ttu-id="02a76-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="02a76-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="02a76-168">System.String</span><span class="sxs-lookup"><span data-stu-id="02a76-168">System.String</span></span>
## <span data-ttu-id="02a76-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02a76-169">OUTPUTS</span></span>

### <span data-ttu-id="02a76-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="02a76-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="02a76-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02a76-171">NOTES</span></span>

## <span data-ttu-id="02a76-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02a76-172">RELATED LINKS</span></span>

<span data-ttu-id="02a76-173">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="02a76-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>