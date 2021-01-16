---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424815"
---
# <span data-ttu-id="cdf2f-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="cdf2f-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="cdf2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf2f-103">Задает или обновляет зарегистрированный префикс от родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="cdf2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cdf2f-104">SYNTAX</span></span>

### <span data-ttu-id="cdf2f-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cdf2f-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdf2f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cdf2f-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdf2f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdf2f-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdf2f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdf2f-108">DESCRIPTION</span></span>
<span data-ttu-id="cdf2f-109">Разрешает обновление зарегистрированного префикса от родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="cdf2f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cdf2f-110">EXAMPLES</span></span>

### <span data-ttu-id="cdf2f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cdf2f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="cdf2f-112">Обновляет префикс по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="cdf2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdf2f-113">PARAMETERS</span></span>

### <span data-ttu-id="cdf2f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdf2f-114">-AsJob</span></span>
<span data-ttu-id="cdf2f-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-115">Run in the background.</span></span>

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

### <span data-ttu-id="cdf2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf2f-116">-DefaultProfile</span></span>
<span data-ttu-id="cdf2f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdf2f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdf2f-118">-InputObject</span></span>
<span data-ttu-id="cdf2f-119">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="cdf2f-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf2f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cdf2f-120">-Name</span></span>
<span data-ttu-id="cdf2f-121">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf2f-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="cdf2f-122">-PeeringName</span></span>
<span data-ttu-id="cdf2f-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf2f-124">-Префикс</span><span class="sxs-lookup"><span data-stu-id="cdf2f-124">-Prefix</span></span>
<span data-ttu-id="cdf2f-125">Префикс IPv4 сеанса</span><span class="sxs-lookup"><span data-stu-id="cdf2f-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="cdf2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdf2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="cdf2f-127">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf2f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdf2f-128">-ResourceId</span></span>
<span data-ttu-id="cdf2f-129">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="cdf2f-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf2f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdf2f-130">-Confirm</span></span>
<span data-ttu-id="cdf2f-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdf2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdf2f-132">-WhatIf</span></span>
<span data-ttu-id="cdf2f-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdf2f-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdf2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf2f-135">CommonParameters</span></span>
<span data-ttu-id="cdf2f-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf2f-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdf2f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf2f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdf2f-138">INPUTS</span></span>

### <span data-ttu-id="cdf2f-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="cdf2f-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="cdf2f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cdf2f-140">System.String</span></span>

## <span data-ttu-id="cdf2f-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdf2f-141">OUTPUTS</span></span>

### <span data-ttu-id="cdf2f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="cdf2f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="cdf2f-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cdf2f-143">NOTES</span></span>

## <span data-ttu-id="cdf2f-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdf2f-144">RELATED LINKS</span></span>