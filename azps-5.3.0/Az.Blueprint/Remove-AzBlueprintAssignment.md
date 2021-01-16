---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509442"
---
# <span data-ttu-id="bd02d-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="bd02d-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="bd02d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd02d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd02d-103">Удалите руководство из подписки или группы управления.</span><span class="sxs-lookup"><span data-stu-id="bd02d-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="bd02d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd02d-104">SYNTAX</span></span>

### <span data-ttu-id="bd02d-105">BySubscriptionAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd02d-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd02d-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="bd02d-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd02d-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="bd02d-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd02d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd02d-108">DESCRIPTION</span></span>
<span data-ttu-id="bd02d-109">Удалите чертеж, который назначен подписке.</span><span class="sxs-lookup"><span data-stu-id="bd02d-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="bd02d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd02d-110">EXAMPLES</span></span>

### <span data-ttu-id="bd02d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd02d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="bd02d-112">Удалите из указанной подписки название, указанное по имени.</span><span class="sxs-lookup"><span data-stu-id="bd02d-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="bd02d-113">Командлет запросит подтверждение перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="bd02d-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="bd02d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd02d-114">PARAMETERS</span></span>

### <span data-ttu-id="bd02d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd02d-115">-DefaultProfile</span></span>
<span data-ttu-id="bd02d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd02d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd02d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd02d-117">-InputObject</span></span>
<span data-ttu-id="bd02d-118">Объект назначения «Чертеж».</span><span class="sxs-lookup"><span data-stu-id="bd02d-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd02d-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="bd02d-119">-ManagementGroupId</span></span>
<span data-ttu-id="bd02d-120">ИД группы управления, в которой сохранено назначение "Чертеж".</span><span class="sxs-lookup"><span data-stu-id="bd02d-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd02d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bd02d-121">-Name</span></span>
<span data-ttu-id="bd02d-122">Название задания «Чертеж».</span><span class="sxs-lookup"><span data-stu-id="bd02d-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd02d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd02d-123">-PassThru</span></span>
<span data-ttu-id="bd02d-124">При этом будет возвращен объект, представляющий удаленную задачу Blueprint.</span><span class="sxs-lookup"><span data-stu-id="bd02d-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="bd02d-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bd02d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bd02d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd02d-126">-SubscriptionId</span></span>
<span data-ttu-id="bd02d-127">По подписке будет развернут чертеж, на который будет развернуто задание.</span><span class="sxs-lookup"><span data-stu-id="bd02d-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd02d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd02d-128">-Confirm</span></span>
<span data-ttu-id="bd02d-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd02d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd02d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd02d-130">-WhatIf</span></span>
<span data-ttu-id="bd02d-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd02d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd02d-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd02d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd02d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd02d-133">CommonParameters</span></span>
<span data-ttu-id="bd02d-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd02d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd02d-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd02d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd02d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd02d-136">INPUTS</span></span>

### <span data-ttu-id="bd02d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bd02d-137">System.String</span></span>

### <span data-ttu-id="bd02d-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="bd02d-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="bd02d-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd02d-139">OUTPUTS</span></span>

### <span data-ttu-id="bd02d-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="bd02d-140">System.Object</span></span>
## <span data-ttu-id="bd02d-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd02d-141">NOTES</span></span>

## <span data-ttu-id="bd02d-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd02d-142">RELATED LINKS</span></span>