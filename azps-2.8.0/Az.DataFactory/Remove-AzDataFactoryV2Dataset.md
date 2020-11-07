---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 8d1a4dfcaaa101a87fc687e78b8086823be7caab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721469"
---
# <span data-ttu-id="92313-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="92313-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="92313-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92313-102">SYNOPSIS</span></span>
<span data-ttu-id="92313-103">Удаляет набор данных из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="92313-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="92313-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92313-104">SYNTAX</span></span>

### <span data-ttu-id="92313-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92313-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92313-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92313-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92313-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92313-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92313-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92313-108">DESCRIPTION</span></span>
<span data-ttu-id="92313-109">Командлет Remove-AzDataFactoryV2Dataset удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="92313-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="92313-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92313-110">EXAMPLES</span></span>

### <span data-ttu-id="92313-111">Пример 1: удаление набора данных</span><span class="sxs-lookup"><span data-stu-id="92313-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="92313-112">Эта команда удаляет набор данных с именем DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="92313-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="92313-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="92313-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="92313-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92313-114">PARAMETERS</span></span>

### <span data-ttu-id="92313-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="92313-115">-DataFactoryName</span></span>
<span data-ttu-id="92313-116">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="92313-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="92313-117">Этот командлет удаляет набор данных из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="92313-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="92313-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92313-118">-DefaultProfile</span></span>
<span data-ttu-id="92313-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92313-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92313-120">-Force</span><span class="sxs-lookup"><span data-stu-id="92313-120">-Force</span></span>
<span data-ttu-id="92313-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="92313-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="92313-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92313-122">-InputObject</span></span>
<span data-ttu-id="92313-123">Указывает объект набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="92313-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92313-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92313-124">-Name</span></span>
<span data-ttu-id="92313-125">Указывает имя набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="92313-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92313-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92313-126">-ResourceGroupName</span></span>
<span data-ttu-id="92313-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="92313-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="92313-128">Этот командлет удаляет набор данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="92313-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="92313-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92313-129">-ResourceId</span></span>
<span data-ttu-id="92313-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="92313-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="92313-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92313-131">-Confirm</span></span>
<span data-ttu-id="92313-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92313-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92313-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92313-133">-WhatIf</span></span>
<span data-ttu-id="92313-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="92313-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="92313-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92313-135">CommonParameters</span></span>
<span data-ttu-id="92313-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92313-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92313-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92313-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92313-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92313-138">INPUTS</span></span>

### <span data-ttu-id="92313-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="92313-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="92313-140">System. String</span><span class="sxs-lookup"><span data-stu-id="92313-140">System.String</span></span>

## <span data-ttu-id="92313-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92313-141">OUTPUTS</span></span>

### <span data-ttu-id="92313-142">System. void</span><span class="sxs-lookup"><span data-stu-id="92313-142">System.Void</span></span>

## <span data-ttu-id="92313-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="92313-143">NOTES</span></span>
<span data-ttu-id="92313-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="92313-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="92313-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92313-145">RELATED LINKS</span></span>

[<span data-ttu-id="92313-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="92313-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="92313-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="92313-147">Set-AzDataFactoryV2Dataset</span></span>]()