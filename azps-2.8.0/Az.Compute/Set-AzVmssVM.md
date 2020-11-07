---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721650"
---
# <span data-ttu-id="5948a-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="5948a-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="5948a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5948a-102">SYNOPSIS</span></span>
<span data-ttu-id="5948a-103">Изменяет состояние экземпляра VMSS.</span><span class="sxs-lookup"><span data-stu-id="5948a-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="5948a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5948a-104">SYNTAX</span></span>

### <span data-ttu-id="5948a-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5948a-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5948a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="5948a-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5948a-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="5948a-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5948a-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="5948a-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5948a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5948a-109">DESCRIPTION</span></span>
<span data-ttu-id="5948a-110">Командлет **Set-AzVmssVM** изменяет состояние экземпляра набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5948a-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="5948a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5948a-111">EXAMPLES</span></span>

## <span data-ttu-id="5948a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5948a-112">PARAMETERS</span></span>

### <span data-ttu-id="5948a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5948a-113">-AsJob</span></span>
<span data-ttu-id="5948a-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5948a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5948a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5948a-115">-DefaultProfile</span></span>
<span data-ttu-id="5948a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5948a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5948a-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5948a-117">-InstanceId</span></span>
<span data-ttu-id="5948a-118">Указывает идентификатор экземпляра VMSS, для которого этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="5948a-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5948a-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="5948a-119">-PerformMaintenance</span></span>
<span data-ttu-id="5948a-120">Указывает на то, что этот командлет выполняет обслуживание виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="5948a-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5948a-121">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="5948a-121">-Redeploy</span></span>
<span data-ttu-id="5948a-122">Указывает на то, что этот командлет повторно развертывает виртуальную машину в VMSS.</span><span class="sxs-lookup"><span data-stu-id="5948a-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5948a-123">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="5948a-123">-Reimage</span></span>
<span data-ttu-id="5948a-124">Указывает на то, что этот командлет переобразировать экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="5948a-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5948a-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="5948a-125">-ReimageAll</span></span>
<span data-ttu-id="5948a-126">Указывает, что командлет переобразует все диски в экземпляре VMSS.</span><span class="sxs-lookup"><span data-stu-id="5948a-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5948a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5948a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5948a-128">Указывает имя группы ресурсов, которая содержит экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="5948a-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5948a-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5948a-129">-VMScaleSetName</span></span>
<span data-ttu-id="5948a-130">Указывает имя экземпляра VMSS, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5948a-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5948a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5948a-131">-Confirm</span></span>
<span data-ttu-id="5948a-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5948a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5948a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5948a-133">-WhatIf</span></span>
<span data-ttu-id="5948a-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5948a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5948a-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5948a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5948a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5948a-136">CommonParameters</span></span>
<span data-ttu-id="5948a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5948a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5948a-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5948a-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5948a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5948a-139">INPUTS</span></span>

### <span data-ttu-id="5948a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5948a-140">System.String</span></span>

## <span data-ttu-id="5948a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5948a-141">OUTPUTS</span></span>

### <span data-ttu-id="5948a-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5948a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5948a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="5948a-143">NOTES</span></span>

## <span data-ttu-id="5948a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5948a-144">RELATED LINKS</span></span>

[<span data-ttu-id="5948a-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="5948a-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)