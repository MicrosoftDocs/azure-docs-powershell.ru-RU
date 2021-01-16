---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328891"
---
# <span data-ttu-id="a7db3-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="a7db3-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="a7db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7db3-102">SYNOPSIS</span></span>
<span data-ttu-id="a7db3-103">Удалите контроллер DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a7db3-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="a7db3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7db3-104">SYNTAX</span></span>

### <span data-ttu-id="a7db3-105">DevSpacesControllerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7db3-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7db3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7db3-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7db3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7db3-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7db3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7db3-108">DESCRIPTION</span></span>
<span data-ttu-id="a7db3-109">Удалите контроллер DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a7db3-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="a7db3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7db3-110">EXAMPLES</span></span>

### <span data-ttu-id="a7db3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7db3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="a7db3-112">Удалите контроллер DevSpaces с именем devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="a7db3-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="a7db3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7db3-113">PARAMETERS</span></span>

### <span data-ttu-id="a7db3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7db3-114">-AsJob</span></span>
<span data-ttu-id="a7db3-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a7db3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7db3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7db3-116">-DefaultProfile</span></span>
<span data-ttu-id="a7db3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7db3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7db3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7db3-118">-InputObject</span></span>
<span data-ttu-id="a7db3-119">Объект PSController, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="a7db3-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a7db3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a7db3-120">-Name</span></span>
<span data-ttu-id="a7db3-121">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a7db3-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="a7db3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7db3-122">-PassThru</span></span>
<span data-ttu-id="a7db3-123">Возвращает "Истина", если удаление успешно.</span><span class="sxs-lookup"><span data-stu-id="a7db3-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="a7db3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7db3-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7db3-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a7db3-125">Resource group name</span></span>

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

### <span data-ttu-id="a7db3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7db3-126">-ResourceId</span></span>
<span data-ttu-id="a7db3-127">ИД ресурса DevSpaces</span><span class="sxs-lookup"><span data-stu-id="a7db3-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="a7db3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7db3-128">-Confirm</span></span>
<span data-ttu-id="a7db3-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7db3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7db3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7db3-130">-WhatIf</span></span>
<span data-ttu-id="a7db3-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7db3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7db3-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7db3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7db3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7db3-133">CommonParameters</span></span>
<span data-ttu-id="a7db3-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7db3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7db3-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7db3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7db3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7db3-136">INPUTS</span></span>

### <span data-ttu-id="a7db3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a7db3-137">System.String</span></span>

### <span data-ttu-id="a7db3-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="a7db3-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="a7db3-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7db3-139">OUTPUTS</span></span>

### <span data-ttu-id="a7db3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7db3-140">System.Boolean</span></span>

## <span data-ttu-id="a7db3-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7db3-141">NOTES</span></span>

## <span data-ttu-id="a7db3-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7db3-142">RELATED LINKS</span></span>