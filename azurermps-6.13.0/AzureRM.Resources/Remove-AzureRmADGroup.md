---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
ms.openlocfilehash: f9aa1f3d45a50a59c118abea4278bfed1725fa9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562691"
---
# <span data-ttu-id="c2eba-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="c2eba-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="c2eba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2eba-102">SYNOPSIS</span></span>
<span data-ttu-id="c2eba-103">Удаление группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2eba-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2eba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2eba-104">SYNTAX</span></span>

### <span data-ttu-id="c2eba-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2eba-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2eba-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2eba-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2eba-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2eba-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2eba-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2eba-108">DESCRIPTION</span></span>
<span data-ttu-id="c2eba-109">Удаление группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2eba-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="c2eba-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2eba-110">EXAMPLES</span></span>

### <span data-ttu-id="c2eba-111">Пример 1: удаление группировки по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="c2eba-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c2eba-112">Удаляет из клиента группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="c2eba-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="c2eba-113">Пример 2: Удаление группы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="c2eba-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="c2eba-114">Получает группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и каналами, которые нужно Remove-AzureRmADGroup, чтобы удалить группу из клиента.</span><span class="sxs-lookup"><span data-stu-id="c2eba-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="c2eba-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2eba-115">PARAMETERS</span></span>

### <span data-ttu-id="c2eba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2eba-116">-DefaultProfile</span></span>
<span data-ttu-id="c2eba-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2eba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2eba-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2eba-118">-DisplayName</span></span>
<span data-ttu-id="c2eba-119">Отображаемое имя группы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c2eba-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="c2eba-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c2eba-120">-Force</span></span>
<span data-ttu-id="c2eba-121">Если этот элемент указан, подтверждение удаления группы не запрашивается.</span><span class="sxs-lookup"><span data-stu-id="c2eba-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2eba-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2eba-122">-InputObject</span></span>
<span data-ttu-id="c2eba-123">Объектное представление удаляемой группы.</span><span class="sxs-lookup"><span data-stu-id="c2eba-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eba-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c2eba-124">-ObjectId</span></span>
<span data-ttu-id="c2eba-125">Идентификатор объекта группы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c2eba-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eba-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2eba-126">-PassThru</span></span>
<span data-ttu-id="c2eba-127">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c2eba-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2eba-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2eba-128">-Confirm</span></span>
<span data-ttu-id="c2eba-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2eba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2eba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2eba-130">-WhatIf</span></span>
<span data-ttu-id="c2eba-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2eba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2eba-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2eba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2eba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2eba-133">CommonParameters</span></span>
<span data-ttu-id="c2eba-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2eba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2eba-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2eba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2eba-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2eba-136">INPUTS</span></span>

### <span data-ttu-id="c2eba-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c2eba-137">System.Guid</span></span>

### <span data-ttu-id="c2eba-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c2eba-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="c2eba-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2eba-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c2eba-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2eba-140">OUTPUTS</span></span>

### <span data-ttu-id="c2eba-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2eba-141">System.Boolean</span></span>

## <span data-ttu-id="c2eba-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2eba-142">NOTES</span></span>

## <span data-ttu-id="c2eba-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2eba-143">RELATED LINKS</span></span>