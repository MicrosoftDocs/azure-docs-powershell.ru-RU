---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: c121834f618dacdb1c2116852b7537f88d323bd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721494"
---
# <span data-ttu-id="85264-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="85264-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="85264-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85264-102">SYNOPSIS</span></span>
<span data-ttu-id="85264-103">Создает центр для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="85264-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="85264-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85264-104">SYNTAX</span></span>

### <span data-ttu-id="85264-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85264-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85264-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="85264-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85264-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85264-107">DESCRIPTION</span></span>
<span data-ttu-id="85264-108">Командлет **New-AzDataFactoryHub** создает Hub для фабрики данных Azure в указанной группе ресурсов Azure и в указанной фабрике данных с указанным определением файла.</span><span class="sxs-lookup"><span data-stu-id="85264-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="85264-109">После того как вы создадите центр, вы можете использовать его для хранения и управления связанными службами в группе, а также добавлять конвейеры в этот центр.</span><span class="sxs-lookup"><span data-stu-id="85264-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="85264-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85264-110">EXAMPLES</span></span>

### <span data-ttu-id="85264-111">Пример 1: создание концентратора</span><span class="sxs-lookup"><span data-stu-id="85264-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="85264-112">Эта команда создает концентратор с именем ContosoDataHub в группе ресурсов ADFResourceGroup и фабрика данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="85264-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="85264-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85264-113">PARAMETERS</span></span>

### <span data-ttu-id="85264-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="85264-114">-DataFactory</span></span>
<span data-ttu-id="85264-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="85264-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="85264-116">Этот командлет создает концентратор для фабрики данных, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="85264-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="85264-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="85264-117">-DataFactoryName</span></span>
<span data-ttu-id="85264-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="85264-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="85264-119">Этот командлет создает концентратор для фабрики данных, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="85264-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="85264-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85264-120">-DefaultProfile</span></span>
<span data-ttu-id="85264-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="85264-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85264-122">-Файл</span><span class="sxs-lookup"><span data-stu-id="85264-122">-File</span></span>
<span data-ttu-id="85264-123">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание концентратора.</span><span class="sxs-lookup"><span data-stu-id="85264-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85264-124">-Force</span><span class="sxs-lookup"><span data-stu-id="85264-124">-Force</span></span>
<span data-ttu-id="85264-125">Указывает, что этот командлет заменяет существующий концентратор без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="85264-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="85264-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85264-126">-Name</span></span>
<span data-ttu-id="85264-127">Указывает имя создаваемого концентратора.</span><span class="sxs-lookup"><span data-stu-id="85264-127">Specifies the name of the hub to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85264-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85264-128">-ResourceGroupName</span></span>
<span data-ttu-id="85264-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="85264-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="85264-130">Этот командлет создает концентратор, принадлежащий группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="85264-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="85264-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85264-131">-Confirm</span></span>
<span data-ttu-id="85264-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85264-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85264-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85264-133">-WhatIf</span></span>
<span data-ttu-id="85264-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85264-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85264-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85264-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85264-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85264-136">CommonParameters</span></span>
<span data-ttu-id="85264-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85264-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85264-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85264-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85264-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85264-139">INPUTS</span></span>

### <span data-ttu-id="85264-140">System. String</span><span class="sxs-lookup"><span data-stu-id="85264-140">System.String</span></span>

### <span data-ttu-id="85264-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="85264-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="85264-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85264-142">OUTPUTS</span></span>

### <span data-ttu-id="85264-143">Microsoft. Azure. Commands. Factoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="85264-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="85264-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="85264-144">NOTES</span></span>
* <span data-ttu-id="85264-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="85264-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="85264-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85264-146">RELATED LINKS</span></span>

[<span data-ttu-id="85264-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="85264-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="85264-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="85264-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)

