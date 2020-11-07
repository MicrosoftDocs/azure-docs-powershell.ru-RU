---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 5a14bce37e9cad196bd9fa6ebfe115b998a2769b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721091"
---
# <span data-ttu-id="61e1d-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="61e1d-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="61e1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="61e1d-103">Обновите контроллер DevSpaces, чтобы добавить теги.</span><span class="sxs-lookup"><span data-stu-id="61e1d-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="61e1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61e1d-104">SYNTAX</span></span>

### <span data-ttu-id="61e1d-105">DevSpacesControllerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61e1d-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e1d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e1d-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e1d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e1d-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e1d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61e1d-108">DESCRIPTION</span></span>
<span data-ttu-id="61e1d-109">Обновите контроллер DevSpaces, чтобы добавить теги.</span><span class="sxs-lookup"><span data-stu-id="61e1d-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="61e1d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61e1d-110">EXAMPLES</span></span>

### <span data-ttu-id="61e1d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61e1d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="61e1d-112">Пометьте контроллер DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="61e1d-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="61e1d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61e1d-113">PARAMETERS</span></span>

### <span data-ttu-id="61e1d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e1d-114">-DefaultProfile</span></span>
<span data-ttu-id="61e1d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61e1d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e1d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e1d-116">-InputObject</span></span>
<span data-ttu-id="61e1d-117">Объект PSController, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="61e1d-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e1d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61e1d-118">-Name</span></span>
<span data-ttu-id="61e1d-119">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="61e1d-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e1d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e1d-120">-ResourceGroupName</span></span>
<span data-ttu-id="61e1d-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="61e1d-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e1d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61e1d-122">-ResourceId</span></span>
<span data-ttu-id="61e1d-123">Идентификатор ресурса DevSpaces</span><span class="sxs-lookup"><span data-stu-id="61e1d-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e1d-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="61e1d-124">-Tag</span></span>
<span data-ttu-id="61e1d-125">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61e1d-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e1d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61e1d-126">-Confirm</span></span>
<span data-ttu-id="61e1d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61e1d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e1d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e1d-128">-WhatIf</span></span>
<span data-ttu-id="61e1d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61e1d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e1d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61e1d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e1d-131">CommonParameters</span></span>
<span data-ttu-id="61e1d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61e1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e1d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e1d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e1d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61e1d-134">INPUTS</span></span>

### <span data-ttu-id="61e1d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="61e1d-135">System.String</span></span>

### <span data-ttu-id="61e1d-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="61e1d-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="61e1d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61e1d-137">OUTPUTS</span></span>

### <span data-ttu-id="61e1d-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="61e1d-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="61e1d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="61e1d-139">NOTES</span></span>

## <span data-ttu-id="61e1d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61e1d-140">RELATED LINKS</span></span>