---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 744fbba1497cb3d006d177880fe5afef80c6e465
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721796"
---
# <span data-ttu-id="dcf7e-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="dcf7e-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="dcf7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcf7e-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf7e-103">Удаление определения картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="dcf7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcf7e-104">SYNTAX</span></span>

### <span data-ttu-id="dcf7e-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcf7e-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf7e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="dcf7e-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf7e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="dcf7e-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf7e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcf7e-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf7e-109">Удаление определения картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="dcf7e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcf7e-110">EXAMPLES</span></span>

### <span data-ttu-id="dcf7e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dcf7e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="dcf7e-112">Удалите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="dcf7e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcf7e-113">PARAMETERS</span></span>

### <span data-ttu-id="dcf7e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcf7e-114">-AsJob</span></span>
<span data-ttu-id="dcf7e-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dcf7e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcf7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf7e-116">-DefaultProfile</span></span>
<span data-ttu-id="dcf7e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf7e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dcf7e-118">-Force</span></span>
<span data-ttu-id="dcf7e-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcf7e-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="dcf7e-120">-GalleryName</span></span>
<span data-ttu-id="dcf7e-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcf7e-122">-InputObject</span></span>
<span data-ttu-id="dcf7e-123">Объект определения изображения в коллекции PS</span><span class="sxs-lookup"><span data-stu-id="dcf7e-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf7e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcf7e-124">-Name</span></span>
<span data-ttu-id="dcf7e-125">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf7e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf7e-126">-ResourceGroupName</span></span>
<span data-ttu-id="dcf7e-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="dcf7e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf7e-128">-ResourceId</span></span>
<span data-ttu-id="dcf7e-129">Идентификатор ресурса для определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="dcf7e-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="dcf7e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcf7e-130">-Confirm</span></span>
<span data-ttu-id="dcf7e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf7e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf7e-132">-WhatIf</span></span>
<span data-ttu-id="dcf7e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf7e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf7e-135">CommonParameters</span></span>
<span data-ttu-id="dcf7e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcf7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf7e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcf7e-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf7e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcf7e-138">INPUTS</span></span>

### <span data-ttu-id="dcf7e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf7e-139">System.String</span></span>

### <span data-ttu-id="dcf7e-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="dcf7e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="dcf7e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcf7e-141">OUTPUTS</span></span>

### <span data-ttu-id="dcf7e-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="dcf7e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dcf7e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcf7e-143">NOTES</span></span>

## <span data-ttu-id="dcf7e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcf7e-144">RELATED LINKS</span></span>