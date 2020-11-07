---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 8fe939bfb959a1a6bc2dc043dbc3948943aa2c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721737"
---
# <span data-ttu-id="e08a6-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e08a6-101">Restart-AzVM</span></span>

## <span data-ttu-id="e08a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e08a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e08a6-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="e08a6-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e08a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e08a6-104">SYNTAX</span></span>

### <span data-ttu-id="e08a6-105">RestartResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e08a6-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08a6-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e08a6-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08a6-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e08a6-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e08a6-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e08a6-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08a6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e08a6-109">DESCRIPTION</span></span>
<span data-ttu-id="e08a6-110">Командлет **restart-AzVM** перезапустит виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="e08a6-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e08a6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e08a6-111">EXAMPLES</span></span>

### <span data-ttu-id="e08a6-112">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e08a6-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e08a6-113">Эта команда перезапускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e08a6-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e08a6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e08a6-114">PARAMETERS</span></span>

### <span data-ttu-id="e08a6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e08a6-115">-AsJob</span></span>
<span data-ttu-id="e08a6-116">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="e08a6-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e08a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08a6-117">-DefaultProfile</span></span>
<span data-ttu-id="e08a6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e08a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e08a6-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e08a6-119">-Id</span></span>
<span data-ttu-id="e08a6-120">ИДЕНТИФИКАТОР виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e08a6-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08a6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e08a6-121">-Name</span></span>
<span data-ttu-id="e08a6-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e08a6-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08a6-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="e08a6-123">-NoWait</span></span>
<span data-ttu-id="e08a6-124">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="e08a6-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e08a6-125">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="e08a6-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e08a6-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="e08a6-126">-PerformMaintenance</span></span>
<span data-ttu-id="e08a6-127">Для выполнения обслуживания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e08a6-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e08a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="e08a6-129">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e08a6-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08a6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e08a6-130">-Confirm</span></span>
<span data-ttu-id="e08a6-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e08a6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08a6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08a6-132">-WhatIf</span></span>
<span data-ttu-id="e08a6-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e08a6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e08a6-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e08a6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08a6-135">CommonParameters</span></span>
<span data-ttu-id="e08a6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e08a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08a6-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e08a6-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08a6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e08a6-138">INPUTS</span></span>

### <span data-ttu-id="e08a6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e08a6-139">System.String</span></span>

### <span data-ttu-id="e08a6-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e08a6-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e08a6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e08a6-141">OUTPUTS</span></span>

### <span data-ttu-id="e08a6-142">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e08a6-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="e08a6-143">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e08a6-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e08a6-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e08a6-144">NOTES</span></span>

## <span data-ttu-id="e08a6-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e08a6-145">RELATED LINKS</span></span>

[<span data-ttu-id="e08a6-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e08a6-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e08a6-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e08a6-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e08a6-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e08a6-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e08a6-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e08a6-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e08a6-150">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="e08a6-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e08a6-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e08a6-151">Update-AzVM</span></span>](./Update-AzVM.md)

