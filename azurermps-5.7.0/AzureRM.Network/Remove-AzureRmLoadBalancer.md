---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 13ece8d5bb6ec42e59f6a44910d3a3d46dd9d844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560256"
---
# <span data-ttu-id="535d8-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="535d8-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="535d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="535d8-102">SYNOPSIS</span></span>
<span data-ttu-id="535d8-103">Удаляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="535d8-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="535d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="535d8-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="535d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="535d8-105">DESCRIPTION</span></span>
<span data-ttu-id="535d8-106">Командлет **Remove-AzureRmLoadBalancer** Удаляет службу балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="535d8-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="535d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="535d8-107">EXAMPLES</span></span>

### <span data-ttu-id="535d8-108">Пример 1: Удаление подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="535d8-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="535d8-109">Эта команда удаляет подсистему балансировки нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="535d8-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="535d8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="535d8-110">PARAMETERS</span></span>

### <span data-ttu-id="535d8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="535d8-111">-AsJob</span></span>
<span data-ttu-id="535d8-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="535d8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="535d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535d8-113">-DefaultProfile</span></span>
<span data-ttu-id="535d8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="535d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535d8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="535d8-115">-Force</span></span>
<span data-ttu-id="535d8-116">Указывает на то, что этот командлет удаляет подсистему балансировки нагрузки независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="535d8-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535d8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="535d8-117">-Name</span></span>
<span data-ttu-id="535d8-118">Указывает имя подсистемы балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="535d8-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="535d8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="535d8-119">-PassThru</span></span>
<span data-ttu-id="535d8-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="535d8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="535d8-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="535d8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="535d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="535d8-123">Указывает имя группы ресурсов, содержащей подсистему балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="535d8-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="535d8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="535d8-124">-Confirm</span></span>
<span data-ttu-id="535d8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="535d8-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535d8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="535d8-126">-WhatIf</span></span>
<span data-ttu-id="535d8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="535d8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="535d8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="535d8-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535d8-129">CommonParameters</span></span>
<span data-ttu-id="535d8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="535d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535d8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="535d8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535d8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="535d8-132">INPUTS</span></span>

### <span data-ttu-id="535d8-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="535d8-133">None</span></span>
<span data-ttu-id="535d8-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="535d8-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="535d8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="535d8-135">OUTPUTS</span></span>

## <span data-ttu-id="535d8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="535d8-136">NOTES</span></span>

## <span data-ttu-id="535d8-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="535d8-137">RELATED LINKS</span></span>

[<span data-ttu-id="535d8-138">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="535d8-138">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="535d8-139">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="535d8-139">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="535d8-140">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="535d8-140">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

