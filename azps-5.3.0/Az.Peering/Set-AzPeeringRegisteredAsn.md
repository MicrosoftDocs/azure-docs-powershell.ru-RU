---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424828"
---
# <span data-ttu-id="480f8-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="480f8-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="480f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="480f8-102">SYNOPSIS</span></span>
<span data-ttu-id="480f8-103">Задает или обновляет зарегистрированное ASN из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="480f8-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="480f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="480f8-104">SYNTAX</span></span>

### <span data-ttu-id="480f8-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="480f8-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="480f8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="480f8-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="480f8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="480f8-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="480f8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="480f8-108">DESCRIPTION</span></span>
<span data-ttu-id="480f8-109">Разрешает обновление зарегистрированного asN-ресурса из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="480f8-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="480f8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="480f8-110">EXAMPLES</span></span>

### <span data-ttu-id="480f8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="480f8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="480f8-112">Обновляет asN по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="480f8-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="480f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="480f8-113">PARAMETERS</span></span>

### <span data-ttu-id="480f8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="480f8-114">-AsJob</span></span>
<span data-ttu-id="480f8-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="480f8-115">Run in the background.</span></span>

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

### <span data-ttu-id="480f8-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="480f8-116">-Asn</span></span>
<span data-ttu-id="480f8-117">AsN, который нужно зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="480f8-117">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="480f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480f8-118">-DefaultProfile</span></span>
<span data-ttu-id="480f8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="480f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480f8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="480f8-120">-InputObject</span></span>
<span data-ttu-id="480f8-121">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="480f8-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="480f8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="480f8-122">-Name</span></span>
<span data-ttu-id="480f8-123">AsN, который нужно зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="480f8-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="480f8-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="480f8-124">-PeeringName</span></span>
<span data-ttu-id="480f8-125">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="480f8-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="480f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="480f8-127">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="480f8-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="480f8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="480f8-128">-ResourceId</span></span>
<span data-ttu-id="480f8-129">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="480f8-129">The resource id string name.</span></span>

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

### <span data-ttu-id="480f8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="480f8-130">-Confirm</span></span>
<span data-ttu-id="480f8-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="480f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="480f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="480f8-132">-WhatIf</span></span>
<span data-ttu-id="480f8-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="480f8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="480f8-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="480f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="480f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480f8-135">CommonParameters</span></span>
<span data-ttu-id="480f8-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480f8-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="480f8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480f8-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="480f8-138">INPUTS</span></span>

### <span data-ttu-id="480f8-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="480f8-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="480f8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="480f8-140">System.String</span></span>

## <span data-ttu-id="480f8-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="480f8-141">OUTPUTS</span></span>

### <span data-ttu-id="480f8-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="480f8-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="480f8-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="480f8-143">NOTES</span></span>

## <span data-ttu-id="480f8-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="480f8-144">RELATED LINKS</span></span>