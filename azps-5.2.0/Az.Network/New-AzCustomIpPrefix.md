---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402740"
---
# <span data-ttu-id="b7f2d-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7f2d-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="b7f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f2d-103">Создание ресурса CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7f2d-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="b7f2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7f2d-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7f2d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f2d-106">Для **создания пользовательского ресурса CustomIpPrefix создается cmdlet New-AzCustomIpPrefix.**</span><span class="sxs-lookup"><span data-stu-id="b7f2d-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="b7f2d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7f2d-107">EXAMPLES</span></span>

### <span data-ttu-id="b7f2d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7f2d-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="b7f2d-109">Эта команда создает новый ресурс CustomIpPrefix с именем $prefixName в группе ресурсов $rgName со ссылкой 40.40.40.0/24 in westus</span><span class="sxs-lookup"><span data-stu-id="b7f2d-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="b7f2d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7f2d-110">PARAMETERS</span></span>

### <span data-ttu-id="b7f2d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7f2d-111">-AsJob</span></span>
<span data-ttu-id="b7f2d-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b7f2d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7f2d-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="b7f2d-113">-Cidr</span></span>
<span data-ttu-id="b7f2d-114">The CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f2d-115">-DefaultProfile</span></span>
<span data-ttu-id="b7f2d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f2d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="b7f2d-117">-Location</span></span>
<span data-ttu-id="b7f2d-118">Расположение CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f2d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7f2d-119">-Name</span></span>
<span data-ttu-id="b7f2d-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7f2d-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f2d-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7f2d-123">-Tag</span></span>
<span data-ttu-id="b7f2d-124">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f2d-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="b7f2d-125">-Zone</span></span>
<span data-ttu-id="b7f2d-126">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f2d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7f2d-127">-Confirm</span></span>
<span data-ttu-id="b7f2d-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f2d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f2d-129">-WhatIf</span></span>
<span data-ttu-id="b7f2d-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7f2d-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f2d-132">CommonParameters</span></span>
<span data-ttu-id="b7f2d-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f2d-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7f2d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f2d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7f2d-135">INPUTS</span></span>

### <span data-ttu-id="b7f2d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b7f2d-136">System.String</span></span>

### <span data-ttu-id="b7f2d-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b7f2d-137">System.String[]</span></span>

### <span data-ttu-id="b7f2d-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7f2d-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7f2d-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7f2d-139">OUTPUTS</span></span>

### <span data-ttu-id="b7f2d-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7f2d-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="b7f2d-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7f2d-141">NOTES</span></span>

## <span data-ttu-id="b7f2d-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7f2d-142">RELATED LINKS</span></span>

[<span data-ttu-id="b7f2d-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7f2d-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="b7f2d-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7f2d-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="b7f2d-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7f2d-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)