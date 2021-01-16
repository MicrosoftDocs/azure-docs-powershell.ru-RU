---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396276"
---
# <span data-ttu-id="b3c3f-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="b3c3f-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="b3c3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c3f-103">Удаляет группу active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="b3c3f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3c3f-104">SYNTAX</span></span>

### <span data-ttu-id="b3c3f-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3c3f-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3c3f-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3c3f-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3c3f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3c3f-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3c3f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3c3f-108">DESCRIPTION</span></span>
<span data-ttu-id="b3c3f-109">Удаляет группу active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="b3c3f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3c3f-110">EXAMPLES</span></span>

### <span data-ttu-id="b3c3f-111">Пример 1. Удаление группы по ид объекта</span><span class="sxs-lookup"><span data-stu-id="b3c3f-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b3c3f-112">Удаляет группу с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE' из клиента.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="b3c3f-113">Пример 2. Удаление группы с помощью piping</span><span class="sxs-lookup"><span data-stu-id="b3c3f-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="b3c3f-114">Получает группу с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE' и каналами, которые Remove-AzADGroup, чтобы удалить группу из клиента.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="b3c3f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3c3f-115">PARAMETERS</span></span>

### <span data-ttu-id="b3c3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c3f-116">-DefaultProfile</span></span>
<span data-ttu-id="b3c3f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c3f-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b3c3f-118">-DisplayName</span></span>
<span data-ttu-id="b3c3f-119">Отображаемая группа, которая будет удалена.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c3f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b3c3f-120">-Force</span></span>
<span data-ttu-id="b3c3f-121">При этом не запросить подтверждение удаления группы.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="b3c3f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3c3f-122">-InputObject</span></span>
<span data-ttu-id="b3c3f-123">Объектное представление удаляемой группы.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c3f-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3c3f-124">-ObjectId</span></span>
<span data-ttu-id="b3c3f-125">Удаляемая группа с ид объекта.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c3f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3c3f-126">-PassThru</span></span>
<span data-ttu-id="b3c3f-127">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b3c3f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3c3f-128">-Confirm</span></span>
<span data-ttu-id="b3c3f-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3c3f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3c3f-130">-WhatIf</span></span>
<span data-ttu-id="b3c3f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3c3f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3c3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c3f-133">CommonParameters</span></span>
<span data-ttu-id="b3c3f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c3f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3c3f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c3f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3c3f-136">INPUTS</span></span>

### <span data-ttu-id="b3c3f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b3c3f-137">System.String</span></span>

### <span data-ttu-id="b3c3f-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="b3c3f-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="b3c3f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3c3f-139">OUTPUTS</span></span>

### <span data-ttu-id="b3c3f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3c3f-140">System.Boolean</span></span>

## <span data-ttu-id="b3c3f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3c3f-141">NOTES</span></span>

## <span data-ttu-id="b3c3f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3c3f-142">RELATED LINKS</span></span>