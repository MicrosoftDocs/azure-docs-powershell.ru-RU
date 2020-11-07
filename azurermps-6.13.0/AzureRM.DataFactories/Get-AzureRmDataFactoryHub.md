---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: d1015a5f401b0cb91731bafe93ead02e2bf3068f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568927"
---
# <span data-ttu-id="c161c-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c161c-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="c161c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c161c-102">SYNOPSIS</span></span>
<span data-ttu-id="c161c-103">Получение сведений о концентраторах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c161c-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c161c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c161c-104">SYNTAX</span></span>

### <span data-ttu-id="c161c-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c161c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c161c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c161c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c161c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c161c-107">DESCRIPTION</span></span>
<span data-ttu-id="c161c-108">Командлет **Get-AzureRmDataFactoryHub** получает сведения о концентраторах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c161c-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="c161c-109">Если указать имя сервера, этот командлет получает сведения об этом центре.</span><span class="sxs-lookup"><span data-stu-id="c161c-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="c161c-110">Если имя не задано, этот командлет получает сведения обо всех концентраторах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="c161c-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="c161c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c161c-111">EXAMPLES</span></span>

### <span data-ttu-id="c161c-112">Пример 1: получение всех концентраторов данных</span><span class="sxs-lookup"><span data-stu-id="c161c-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="c161c-113">Эта команда получает все концентраторы данных в группе ресурсов Azure с именем ADFResourceGroup и фабрики данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="c161c-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="c161c-114">Пример 2: получение определенного концентратора данных</span><span class="sxs-lookup"><span data-stu-id="c161c-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="c161c-115">Эта команда получает сведения о концентраторе с именем MyDataHub в группе ресурсов Azure с именем ADFResourceGroup и фабрике данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="c161c-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="c161c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c161c-116">PARAMETERS</span></span>

### <span data-ttu-id="c161c-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="c161c-117">-DataFactory</span></span>
<span data-ttu-id="c161c-118">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="c161c-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c161c-119">Этот командлет получает сведения о концентраторах в фабрике данных, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c161c-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c161c-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c161c-120">-DataFactoryName</span></span>
<span data-ttu-id="c161c-121">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c161c-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c161c-122">Этот командлет получает сведения о концентраторах в фабрике данных, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c161c-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c161c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c161c-123">-DefaultProfile</span></span>
<span data-ttu-id="c161c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c161c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c161c-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c161c-125">-Name</span></span>
<span data-ttu-id="c161c-126">Указывает имя центра, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c161c-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c161c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c161c-127">-ResourceGroupName</span></span>
<span data-ttu-id="c161c-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c161c-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c161c-129">Этот командлет получает сведения о концентраторах, относящихся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c161c-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c161c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c161c-130">CommonParameters</span></span>
<span data-ttu-id="c161c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c161c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c161c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c161c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c161c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c161c-133">INPUTS</span></span>

### <span data-ttu-id="c161c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c161c-134">System.String</span></span>

### <span data-ttu-id="c161c-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c161c-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c161c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c161c-136">OUTPUTS</span></span>

### <span data-ttu-id="c161c-137">Microsoft. Azure. Commands. Factoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="c161c-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="c161c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c161c-138">NOTES</span></span>
* <span data-ttu-id="c161c-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="c161c-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c161c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c161c-140">RELATED LINKS</span></span>

[<span data-ttu-id="c161c-141">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c161c-141">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="c161c-142">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c161c-142">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)

