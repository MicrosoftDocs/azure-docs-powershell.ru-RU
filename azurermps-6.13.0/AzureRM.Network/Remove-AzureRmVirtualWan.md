---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
ms.openlocfilehash: 1ff9eb4307c4419dd303d74f7528a8ee0d50bdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562800"
---
# <span data-ttu-id="c59d8-101">Remove-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c59d8-101">Remove-AzureRmVirtualWan</span></span>

## <span data-ttu-id="c59d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c59d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c59d8-103">Удаляет виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="c59d8-103">Removes an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c59d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c59d8-104">SYNTAX</span></span>

### <span data-ttu-id="c59d8-105">ByVirtualWanName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c59d8-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59d8-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c59d8-106">ByVirtualWanObject</span></span>
```
Remove-AzureRmVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59d8-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c59d8-107">ByVirtualWanResourceId</span></span>
```
Remove-AzureRmVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c59d8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c59d8-108">DESCRIPTION</span></span>
<span data-ttu-id="c59d8-109">Удаляет виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="c59d8-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c59d8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c59d8-110">EXAMPLES</span></span>

### <span data-ttu-id="c59d8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c59d8-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="c59d8-112">Этот пример создает виртуальную глобальную сеть в группе ресурсов, а затем немедленно удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="c59d8-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c59d8-113">Чтобы отключить вывод запроса при удалении виртуальной глобальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="c59d8-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="c59d8-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c59d8-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="c59d8-115">Этот пример создает виртуальную глобальную сеть в группе ресурсов, а затем немедленно удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="c59d8-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c59d8-116">Это удаление происходит при использовании объекта виртуальной глобальной сети, возвращенного командой New-AzureRmVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c59d8-116">This deletion happens using the virtual wan object returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="c59d8-117">Чтобы отключить вывод запроса при удалении виртуальной глобальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="c59d8-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="c59d8-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c59d8-118">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="c59d8-119">Этот пример создает виртуальную глобальную сеть в группе ресурсов, а затем немедленно удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="c59d8-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c59d8-120">Это удаление происходит при использовании идентификатора виртуального глобального ресурса, возвращенного командой New-AzureRmVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c59d8-120">This deletion happens using the virtual wan resource id returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="c59d8-121">Чтобы отключить вывод запроса при удалении виртуальной глобальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="c59d8-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="c59d8-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c59d8-122">PARAMETERS</span></span>

### <span data-ttu-id="c59d8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59d8-123">-DefaultProfile</span></span>
<span data-ttu-id="c59d8-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c59d8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59d8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c59d8-125">-Force</span></span>
<span data-ttu-id="c59d8-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c59d8-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c59d8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c59d8-127">-InputObject</span></span>
<span data-ttu-id="c59d8-128">Объект виртуальной глобальной сети, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c59d8-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c59d8-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c59d8-129">-Name</span></span>
<span data-ttu-id="c59d8-130">Имя виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="c59d8-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59d8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c59d8-131">-PassThru</span></span>
<span data-ttu-id="c59d8-132">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c59d8-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c59d8-133">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c59d8-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c59d8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59d8-134">-ResourceGroupName</span></span>
<span data-ttu-id="c59d8-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c59d8-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59d8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c59d8-136">-ResourceId</span></span>
<span data-ttu-id="c59d8-137">Идентификатор ресурса Azure для виртуальной глобальной сети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c59d8-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59d8-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c59d8-138">-Confirm</span></span>
<span data-ttu-id="c59d8-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c59d8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59d8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59d8-140">-WhatIf</span></span>
<span data-ttu-id="c59d8-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c59d8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59d8-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c59d8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59d8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59d8-143">CommonParameters</span></span>
<span data-ttu-id="c59d8-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c59d8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59d8-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c59d8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59d8-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c59d8-146">INPUTS</span></span>

### <span data-ttu-id="c59d8-147">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c59d8-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="c59d8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c59d8-148">System.String</span></span>

## <span data-ttu-id="c59d8-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c59d8-149">OUTPUTS</span></span>

### <span data-ttu-id="c59d8-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c59d8-150">System.Boolean</span></span>

## <span data-ttu-id="c59d8-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="c59d8-151">NOTES</span></span>

## <span data-ttu-id="c59d8-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c59d8-152">RELATED LINKS</span></span>