---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566124"
---
# <span data-ttu-id="b6ae3-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b6ae3-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b6ae3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ae3-103">Удаляет развертывание группы ресурсов и связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6ae3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6ae3-104">SYNTAX</span></span>

### <span data-ttu-id="b6ae3-105">RemoveByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6ae3-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6ae3-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b6ae3-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ae3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6ae3-107">DESCRIPTION</span></span>
<span data-ttu-id="b6ae3-108">Командлет **Remove-AzureRmResourceGroupDeployment** удаляет развертывание группы ресурсов Azure и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="b6ae3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6ae3-109">EXAMPLES</span></span>

## <span data-ttu-id="b6ae3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6ae3-110">PARAMETERS</span></span>

### <span data-ttu-id="b6ae3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6ae3-111">-ApiVersion</span></span>
<span data-ttu-id="b6ae3-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b6ae3-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ae3-114">-DefaultProfile</span></span>
<span data-ttu-id="b6ae3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6ae3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-116">-ID</span><span class="sxs-lookup"><span data-stu-id="b6ae3-116">-Id</span></span>
<span data-ttu-id="b6ae3-117">Указывает идентификатор развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6ae3-118">-Name</span></span>
<span data-ttu-id="b6ae3-119">Указывает имя развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="b6ae3-120">-Pre</span></span>
<span data-ttu-id="b6ae3-121">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ae3-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6ae3-123">Указывает имя удаляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6ae3-124">-Confirm</span></span>
<span data-ttu-id="b6ae3-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ae3-126">-WhatIf</span></span>
<span data-ttu-id="b6ae3-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ae3-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ae3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ae3-129">CommonParameters</span></span>
<span data-ttu-id="b6ae3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ae3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ae3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ae3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6ae3-132">INPUTS</span></span>

### <span data-ttu-id="b6ae3-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="b6ae3-133">None</span></span>
<span data-ttu-id="b6ae3-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b6ae3-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6ae3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6ae3-135">OUTPUTS</span></span>

### <span data-ttu-id="b6ae3-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6ae3-136">System.Boolean</span></span>

## <span data-ttu-id="b6ae3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6ae3-137">NOTES</span></span>

## <span data-ttu-id="b6ae3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6ae3-138">RELATED LINKS</span></span>

[<span data-ttu-id="b6ae3-139">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b6ae3-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b6ae3-140">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b6ae3-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b6ae3-141">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b6ae3-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b6ae3-142">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b6ae3-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)

