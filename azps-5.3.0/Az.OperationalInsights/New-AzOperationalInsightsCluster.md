---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506831"
---
# <span data-ttu-id="78da8-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="78da8-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="78da8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78da8-102">SYNOPSIS</span></span>
<span data-ttu-id="78da8-103">Создание кластера</span><span class="sxs-lookup"><span data-stu-id="78da8-103">Create cluster</span></span>

## <span data-ttu-id="78da8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78da8-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78da8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78da8-105">DESCRIPTION</span></span>

<span data-ttu-id="78da8-106">Создание кластера</span><span class="sxs-lookup"><span data-stu-id="78da8-106">Create cluster</span></span>

## <span data-ttu-id="78da8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78da8-107">EXAMPLES</span></span>

### <span data-ttu-id="78da8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78da8-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="78da8-109">Создание кластера</span><span class="sxs-lookup"><span data-stu-id="78da8-109">Create cluster</span></span>

## <span data-ttu-id="78da8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78da8-110">PARAMETERS</span></span>

### <span data-ttu-id="78da8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78da8-111">-AsJob</span></span>
<span data-ttu-id="78da8-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="78da8-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="78da8-113">-ClusterName</span></span>
<span data-ttu-id="78da8-114">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="78da8-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78da8-115">-DefaultProfile</span></span>
<span data-ttu-id="78da8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78da8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="78da8-117">-IdentityType</span></span>
<span data-ttu-id="78da8-118">типом удостоверения может быть значение "SystemAssigned", "None".</span><span class="sxs-lookup"><span data-stu-id="78da8-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-119">-Location</span><span class="sxs-lookup"><span data-stu-id="78da8-119">-Location</span></span>
<span data-ttu-id="78da8-120">Географический регион, в который будет развернут кластер.</span><span class="sxs-lookup"><span data-stu-id="78da8-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78da8-121">-ResourceGroupName</span></span>
<span data-ttu-id="78da8-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78da8-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="78da8-123">-SkuCapacity</span></span>
<span data-ttu-id="78da8-124">Значение SKU должно быть кратно 100 и в диапазоне от 1000 до 2000.</span><span class="sxs-lookup"><span data-stu-id="78da8-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="78da8-125">-SkuName</span></span>
<span data-ttu-id="78da8-126">Имя SKU, теперь может быть только "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="78da8-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-127">-Теги</span><span class="sxs-lookup"><span data-stu-id="78da8-127">-Tags</span></span>
<span data-ttu-id="78da8-128">Теги кластера</span><span class="sxs-lookup"><span data-stu-id="78da8-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78da8-129">-Confirm</span></span>
<span data-ttu-id="78da8-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78da8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78da8-131">-WhatIf</span></span>
<span data-ttu-id="78da8-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78da8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78da8-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78da8-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78da8-134">CommonParameters</span></span>
<span data-ttu-id="78da8-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78da8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78da8-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78da8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78da8-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78da8-137">INPUTS</span></span>

### <span data-ttu-id="78da8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="78da8-138">System.String</span></span>

## <span data-ttu-id="78da8-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78da8-139">OUTPUTS</span></span>

### <span data-ttu-id="78da8-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="78da8-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="78da8-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78da8-141">NOTES</span></span>

## <span data-ttu-id="78da8-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78da8-142">RELATED LINKS</span></span>