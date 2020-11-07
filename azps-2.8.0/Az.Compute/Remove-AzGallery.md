---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: ac098616d2ee92b4d6910034735824289b971f5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721799"
---
# <span data-ttu-id="a4872-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="a4872-101">Remove-AzGallery</span></span>

## <span data-ttu-id="a4872-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4872-102">SYNOPSIS</span></span>
<span data-ttu-id="a4872-103">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="a4872-103">Delete a gallery.</span></span>

## <span data-ttu-id="a4872-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4872-104">SYNTAX</span></span>

### <span data-ttu-id="a4872-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4872-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4872-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a4872-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4872-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a4872-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4872-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4872-108">DESCRIPTION</span></span>
<span data-ttu-id="a4872-109">Удаление коллекции.</span><span class="sxs-lookup"><span data-stu-id="a4872-109">Delete a gallery.</span></span>

## <span data-ttu-id="a4872-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4872-110">EXAMPLES</span></span>

### <span data-ttu-id="a4872-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4872-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="a4872-112">Удаление указанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="a4872-112">Delete the given gallery.</span></span>

## <span data-ttu-id="a4872-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4872-113">PARAMETERS</span></span>

### <span data-ttu-id="a4872-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4872-114">-AsJob</span></span>
<span data-ttu-id="a4872-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a4872-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4872-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4872-116">-DefaultProfile</span></span>
<span data-ttu-id="a4872-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4872-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4872-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a4872-118">-Force</span></span>
<span data-ttu-id="a4872-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4872-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4872-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4872-120">-InputObject</span></span>
<span data-ttu-id="a4872-121">Объект коллекции PS</span><span class="sxs-lookup"><span data-stu-id="a4872-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4872-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4872-122">-Name</span></span>
<span data-ttu-id="a4872-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="a4872-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4872-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4872-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4872-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4872-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4872-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4872-126">-ResourceId</span></span>
<span data-ttu-id="a4872-127">Идентификатор ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="a4872-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="a4872-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4872-128">-Confirm</span></span>
<span data-ttu-id="a4872-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4872-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4872-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4872-130">-WhatIf</span></span>
<span data-ttu-id="a4872-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4872-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4872-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4872-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4872-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4872-133">CommonParameters</span></span>
<span data-ttu-id="a4872-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4872-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4872-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4872-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4872-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4872-136">INPUTS</span></span>

### <span data-ttu-id="a4872-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a4872-137">System.String</span></span>

### <span data-ttu-id="a4872-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="a4872-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="a4872-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4872-139">OUTPUTS</span></span>

### <span data-ttu-id="a4872-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a4872-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a4872-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4872-141">NOTES</span></span>

## <span data-ttu-id="a4872-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4872-142">RELATED LINKS</span></span>