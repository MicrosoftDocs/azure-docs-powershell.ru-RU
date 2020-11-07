---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e936d237589aec46d0f677344dfcd4274e19816d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557771"
---
# <span data-ttu-id="c3f51-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c3f51-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="c3f51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3f51-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f51-103">Удаляет конвейер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c3f51-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3f51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3f51-104">SYNTAX</span></span>

### <span data-ttu-id="c3f51-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3f51-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3f51-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3f51-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3f51-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3f51-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3f51-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3f51-108">DESCRIPTION</span></span>
<span data-ttu-id="c3f51-109">Командлет Remove-AzureRmDataFactoryV2Pipeline удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f51-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="c3f51-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3f51-110">EXAMPLES</span></span>

### <span data-ttu-id="c3f51-111">Пример 1: удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="c3f51-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="c3f51-112">Этот командлет удаляет конвейер с именем DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c3f51-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="c3f51-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="c3f51-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="c3f51-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3f51-114">PARAMETERS</span></span>

### <span data-ttu-id="c3f51-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3f51-115">-Confirm</span></span>
<span data-ttu-id="c3f51-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c3f51-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f51-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c3f51-117">-DataFactoryName</span></span>
<span data-ttu-id="c3f51-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c3f51-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c3f51-119">Этот командлет удаляет конвейер из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c3f51-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f51-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c3f51-120">-Force</span></span>
<span data-ttu-id="c3f51-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c3f51-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c3f51-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3f51-122">-Name</span></span>
<span data-ttu-id="c3f51-123">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c3f51-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f51-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3f51-124">-InputObject</span></span>
<span data-ttu-id="c3f51-125">Указывает объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="c3f51-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="c3f51-126">Этот командлет удаляет конвейер, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c3f51-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3f51-127">-ResourceGroupName</span></span>
<span data-ttu-id="c3f51-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f51-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c3f51-129">Этот командлет удаляет конвейер из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c3f51-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f51-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3f51-130">-ResourceId</span></span>
<span data-ttu-id="c3f51-131">Идентификатор ресурса Azure для конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c3f51-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f51-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f51-132">-WhatIf</span></span>
<span data-ttu-id="c3f51-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="c3f51-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c3f51-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f51-134">-DefaultProfile</span></span>
<span data-ttu-id="c3f51-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f51-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3f51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f51-136">CommonParameters</span></span>
<span data-ttu-id="c3f51-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3f51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f51-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3f51-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f51-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3f51-139">INPUTS</span></span>

### <span data-ttu-id="c3f51-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c3f51-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="c3f51-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c3f51-141">System.String</span></span>

## <span data-ttu-id="c3f51-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3f51-142">OUTPUTS</span></span>

### <span data-ttu-id="c3f51-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="c3f51-143">System.Object</span></span>

## <span data-ttu-id="c3f51-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3f51-144">NOTES</span></span>
<span data-ttu-id="c3f51-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="c3f51-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c3f51-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3f51-146">RELATED LINKS</span></span>

[<span data-ttu-id="c3f51-147">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c3f51-147">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c3f51-148">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c3f51-148">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c3f51-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c3f51-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
