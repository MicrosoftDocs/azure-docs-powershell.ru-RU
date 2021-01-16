---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413892"
---
# <span data-ttu-id="43a1f-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="43a1f-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="43a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="43a1f-103">Удаляет ресурс из коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="43a1f-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="43a1f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43a1f-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="43a1f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="43a1f-106">Удаляет ресурс из коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="43a1f-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="43a1f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43a1f-107">EXAMPLES</span></span>

### <span data-ttu-id="43a1f-108">Пример 1. Удаление ресурса из коллекции "Перемещение"</span><span class="sxs-lookup"><span data-stu-id="43a1f-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="43a1f-109">Удалите ресурс из коллекции "Перемещение" в рамках указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="43a1f-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="43a1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43a1f-110">PARAMETERS</span></span>

### <span data-ttu-id="43a1f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43a1f-111">-AsJob</span></span>
<span data-ttu-id="43a1f-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="43a1f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="43a1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a1f-113">-DefaultProfile</span></span>
<span data-ttu-id="43a1f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43a1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43a1f-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="43a1f-115">-MoveCollectionName</span></span>
<span data-ttu-id="43a1f-116">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="43a1f-116">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a1f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43a1f-117">-Name</span></span>
<span data-ttu-id="43a1f-118">Имя перемещение ресурса.</span><span class="sxs-lookup"><span data-stu-id="43a1f-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a1f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="43a1f-119">-NoWait</span></span>
<span data-ttu-id="43a1f-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="43a1f-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="43a1f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43a1f-121">-PassThru</span></span>
<span data-ttu-id="43a1f-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="43a1f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="43a1f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a1f-123">-ResourceGroupName</span></span>
<span data-ttu-id="43a1f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43a1f-124">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a1f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43a1f-125">-SubscriptionId</span></span>
<span data-ttu-id="43a1f-126">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="43a1f-126">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a1f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43a1f-127">-Confirm</span></span>
<span data-ttu-id="43a1f-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43a1f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43a1f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a1f-129">-WhatIf</span></span>
<span data-ttu-id="43a1f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43a1f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43a1f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43a1f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43a1f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a1f-132">CommonParameters</span></span>
<span data-ttu-id="43a1f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a1f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a1f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43a1f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a1f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43a1f-135">INPUTS</span></span>

## <span data-ttu-id="43a1f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43a1f-136">OUTPUTS</span></span>

### <span data-ttu-id="43a1f-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="43a1f-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="43a1f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43a1f-138">NOTES</span></span>

<span data-ttu-id="43a1f-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="43a1f-139">ALIASES</span></span>

## <span data-ttu-id="43a1f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43a1f-140">RELATED LINKS</span></span>
