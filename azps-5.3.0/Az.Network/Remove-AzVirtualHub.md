---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519951"
---
# <span data-ttu-id="7e56a-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7e56a-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="7e56a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e56a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e56a-103">Удаляет ресурс Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7e56a-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="7e56a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e56a-104">SYNTAX</span></span>

### <span data-ttu-id="7e56a-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e56a-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e56a-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7e56a-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e56a-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7e56a-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e56a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e56a-108">DESCRIPTION</span></span>
<span data-ttu-id="7e56a-109">Удаляет ресурс Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7e56a-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="7e56a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e56a-110">EXAMPLES</span></span>

### <span data-ttu-id="7e56a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e56a-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="7e56a-112">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор на западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="7e56a-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="7e56a-113">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="7e56a-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="7e56a-114">Затем он удаляет виртуальный концентратор с помощью его resourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7e56a-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="7e56a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7e56a-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="7e56a-116">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор на западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="7e56a-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="7e56a-117">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="7e56a-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="7e56a-118">Затем он удаляет виртуальный концентратор с помощью входного объекта.</span><span class="sxs-lookup"><span data-stu-id="7e56a-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="7e56a-119">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7e56a-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="7e56a-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7e56a-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="7e56a-121">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор на западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="7e56a-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="7e56a-122">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="7e56a-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="7e56a-123">Затем он удаляет виртуальный концентратор с помощью piping powershell, используя выходные данные из Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7e56a-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="7e56a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e56a-124">PARAMETERS</span></span>

### <span data-ttu-id="7e56a-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e56a-125">-AsJob</span></span>
<span data-ttu-id="7e56a-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7e56a-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e56a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e56a-127">-DefaultProfile</span></span>
<span data-ttu-id="7e56a-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e56a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e56a-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7e56a-129">-Force</span></span>
<span data-ttu-id="7e56a-130">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="7e56a-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7e56a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e56a-131">-InputObject</span></span>
<span data-ttu-id="7e56a-132">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7e56a-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e56a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="7e56a-133">-Name</span></span>
<span data-ttu-id="7e56a-134">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="7e56a-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e56a-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e56a-135">-PassThru</span></span>
<span data-ttu-id="7e56a-136">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7e56a-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e56a-137">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7e56a-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e56a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e56a-138">-ResourceGroupName</span></span>
<span data-ttu-id="7e56a-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e56a-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e56a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e56a-140">-ResourceId</span></span>
<span data-ttu-id="7e56a-141">ИД ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7e56a-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e56a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e56a-142">-Confirm</span></span>
<span data-ttu-id="7e56a-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e56a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e56a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e56a-144">-WhatIf</span></span>
<span data-ttu-id="7e56a-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e56a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e56a-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e56a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e56a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e56a-147">CommonParameters</span></span>
<span data-ttu-id="7e56a-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e56a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e56a-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e56a-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e56a-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e56a-150">INPUTS</span></span>

### <span data-ttu-id="7e56a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7e56a-151">System.String</span></span>

### <span data-ttu-id="7e56a-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7e56a-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="7e56a-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e56a-153">OUTPUTS</span></span>

### <span data-ttu-id="7e56a-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7e56a-154">System.Boolean</span></span>

## <span data-ttu-id="7e56a-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e56a-155">NOTES</span></span>

## <span data-ttu-id="7e56a-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e56a-156">RELATED LINKS</span></span>

[<span data-ttu-id="7e56a-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7e56a-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="7e56a-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7e56a-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="7e56a-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7e56a-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)