---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: ac17206073ff9992c8569da884d1d53c385bccbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721482"
---
# <span data-ttu-id="34082-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="34082-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="34082-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34082-102">SYNOPSIS</span></span>
<span data-ttu-id="34082-103">Удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="34082-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="34082-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34082-104">SYNTAX</span></span>

### <span data-ttu-id="34082-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34082-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34082-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="34082-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34082-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34082-107">DESCRIPTION</span></span>
<span data-ttu-id="34082-108">Командлет **Remove-AzDataFactoryDataset** удаляет набор данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="34082-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="34082-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34082-109">EXAMPLES</span></span>

### <span data-ttu-id="34082-110">Пример 1: удаление набора данных</span><span class="sxs-lookup"><span data-stu-id="34082-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="34082-111">Эта команда удаляет набор данных с именем DAWikiAggregatedData из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="34082-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="34082-112">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="34082-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="34082-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34082-113">PARAMETERS</span></span>

### <span data-ttu-id="34082-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="34082-114">-DataFactory</span></span>
<span data-ttu-id="34082-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="34082-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="34082-116">Этот командлет удаляет набор данных из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="34082-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34082-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="34082-117">-DataFactoryName</span></span>
<span data-ttu-id="34082-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="34082-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="34082-119">Этот командлет удаляет набор данных из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="34082-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="34082-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34082-120">-DefaultProfile</span></span>
<span data-ttu-id="34082-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="34082-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34082-122">-Force</span><span class="sxs-lookup"><span data-stu-id="34082-122">-Force</span></span>
<span data-ttu-id="34082-123">Указывает на то, что этот командлет удаляет набор данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="34082-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="34082-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34082-124">-Name</span></span>
<span data-ttu-id="34082-125">Указывает имя набора данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="34082-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34082-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34082-126">-ResourceGroupName</span></span>
<span data-ttu-id="34082-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="34082-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="34082-128">Этот командлет удаляет набор данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="34082-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="34082-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34082-129">-Confirm</span></span>
<span data-ttu-id="34082-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34082-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34082-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34082-131">-WhatIf</span></span>
<span data-ttu-id="34082-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34082-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34082-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34082-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34082-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34082-134">CommonParameters</span></span>
<span data-ttu-id="34082-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34082-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34082-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34082-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34082-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34082-137">INPUTS</span></span>

### <span data-ttu-id="34082-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="34082-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="34082-139">System. String</span><span class="sxs-lookup"><span data-stu-id="34082-139">System.String</span></span>

## <span data-ttu-id="34082-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34082-140">OUTPUTS</span></span>

### <span data-ttu-id="34082-141">System. void</span><span class="sxs-lookup"><span data-stu-id="34082-141">System.Void</span></span>

## <span data-ttu-id="34082-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="34082-142">NOTES</span></span>
* <span data-ttu-id="34082-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="34082-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="34082-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34082-144">RELATED LINKS</span></span>

[<span data-ttu-id="34082-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="34082-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="34082-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="34082-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

