---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 107881e8d9ac1f631b9a90dbf68ba096a59cefb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721790"
---
# <span data-ttu-id="3deb9-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="3deb9-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="3deb9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3deb9-102">SYNOPSIS</span></span>
<span data-ttu-id="3deb9-103">Удаляет группу узлов.</span><span class="sxs-lookup"><span data-stu-id="3deb9-103">Removes a host group.</span></span>

## <span data-ttu-id="3deb9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3deb9-104">SYNTAX</span></span>

### <span data-ttu-id="3deb9-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3deb9-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3deb9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3deb9-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3deb9-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3deb9-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3deb9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3deb9-108">DESCRIPTION</span></span>
<span data-ttu-id="3deb9-109">Этот командлет удалит группу узлов</span><span class="sxs-lookup"><span data-stu-id="3deb9-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="3deb9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3deb9-110">EXAMPLES</span></span>

### <span data-ttu-id="3deb9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3deb9-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="3deb9-112">Эта команда возвращает или удаляет указанную группу узлов.</span><span class="sxs-lookup"><span data-stu-id="3deb9-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="3deb9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3deb9-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="3deb9-114">Эта команда удаляет указанную группу узлов.</span><span class="sxs-lookup"><span data-stu-id="3deb9-114">This command removes the given host group.</span></span>

## <span data-ttu-id="3deb9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3deb9-115">PARAMETERS</span></span>

### <span data-ttu-id="3deb9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3deb9-116">-AsJob</span></span>
<span data-ttu-id="3deb9-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3deb9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3deb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3deb9-118">-DefaultProfile</span></span>
<span data-ttu-id="3deb9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3deb9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3deb9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3deb9-120">-InputObject</span></span>
<span data-ttu-id="3deb9-121">Локальный объект группы узла.</span><span class="sxs-lookup"><span data-stu-id="3deb9-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3deb9-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3deb9-122">-Name</span></span>
<span data-ttu-id="3deb9-123">Имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="3deb9-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3deb9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3deb9-124">-ResourceGroupName</span></span>
<span data-ttu-id="3deb9-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3deb9-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3deb9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3deb9-126">-ResourceId</span></span>
<span data-ttu-id="3deb9-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3deb9-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3deb9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3deb9-128">-Confirm</span></span>
<span data-ttu-id="3deb9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3deb9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3deb9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3deb9-130">-WhatIf</span></span>
<span data-ttu-id="3deb9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3deb9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3deb9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3deb9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3deb9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3deb9-133">CommonParameters</span></span>
<span data-ttu-id="3deb9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3deb9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3deb9-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3deb9-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3deb9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3deb9-136">INPUTS</span></span>

### <span data-ttu-id="3deb9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3deb9-137">System.String</span></span>

### <span data-ttu-id="3deb9-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="3deb9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="3deb9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3deb9-139">OUTPUTS</span></span>

### <span data-ttu-id="3deb9-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3deb9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3deb9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3deb9-141">NOTES</span></span>

## <span data-ttu-id="3deb9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3deb9-142">RELATED LINKS</span></span>