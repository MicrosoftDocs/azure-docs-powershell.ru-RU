---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 1cada55b8db886d85f88d34254c8814cdfc44665
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566502"
---
# <span data-ttu-id="b9d80-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b9d80-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="b9d80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9d80-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d80-103">Проверка существования элемента каталога.</span><span class="sxs-lookup"><span data-stu-id="b9d80-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9d80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9d80-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9d80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9d80-105">DESCRIPTION</span></span>
<span data-ttu-id="b9d80-106">Командлет **Test-AzureRmDataLakeAnalyticsCatalogItem** проверяет наличие элемента каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b9d80-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="b9d80-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9d80-107">EXAMPLES</span></span>

### <span data-ttu-id="b9d80-108">Пример 1: Проверка наличия элемента каталога</span><span class="sxs-lookup"><span data-stu-id="b9d80-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="b9d80-109">Эта команда проверяет, существует ли указанный элемент схемы.</span><span class="sxs-lookup"><span data-stu-id="b9d80-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="b9d80-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9d80-110">PARAMETERS</span></span>

### <span data-ttu-id="b9d80-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b9d80-111">-Account</span></span>
<span data-ttu-id="b9d80-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b9d80-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d80-113">-DefaultProfile</span></span>
<span data-ttu-id="b9d80-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b9d80-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9d80-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b9d80-115">-ItemType</span></span>
<span data-ttu-id="b9d80-116">Указывает тип элемента каталога для элемента, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="b9d80-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="b9d80-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b9d80-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b9d80-118">База</span><span class="sxs-lookup"><span data-stu-id="b9d80-118">Database</span></span>
- <span data-ttu-id="b9d80-119">Схемы</span><span class="sxs-lookup"><span data-stu-id="b9d80-119">Schema</span></span>
- <span data-ttu-id="b9d80-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="b9d80-120">Assembly</span></span>
- <span data-ttu-id="b9d80-121">Таблич</span><span class="sxs-lookup"><span data-stu-id="b9d80-121">Table</span></span>
- <span data-ttu-id="b9d80-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="b9d80-122">TablePartition</span></span>
- <span data-ttu-id="b9d80-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="b9d80-123">TableValuedFunction</span></span>
- <span data-ttu-id="b9d80-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="b9d80-124">TableStatistics</span></span>
- <span data-ttu-id="b9d80-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="b9d80-125">ExternalDataSource</span></span>
- <span data-ttu-id="b9d80-126">Технический</span><span class="sxs-lookup"><span data-stu-id="b9d80-126">View</span></span>
- <span data-ttu-id="b9d80-127">Процедур</span><span class="sxs-lookup"><span data-stu-id="b9d80-127">Procedure</span></span>
- <span data-ttu-id="b9d80-128">Скрыт</span><span class="sxs-lookup"><span data-stu-id="b9d80-128">Secret</span></span>
- <span data-ttu-id="b9d80-129">Член</span><span class="sxs-lookup"><span data-stu-id="b9d80-129">Credential</span></span>
- <span data-ttu-id="b9d80-130">Лично</span><span class="sxs-lookup"><span data-stu-id="b9d80-130">Types</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d80-131">-Path</span><span class="sxs-lookup"><span data-stu-id="b9d80-131">-Path</span></span>
<span data-ttu-id="b9d80-132">Задает путь к извлекаемому элементу или путь к родительскому элементу для списка элементов.</span><span class="sxs-lookup"><span data-stu-id="b9d80-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d80-133">CommonParameters</span></span>
<span data-ttu-id="b9d80-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9d80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d80-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9d80-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d80-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9d80-136">INPUTS</span></span>

### <span data-ttu-id="b9d80-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b9d80-137">System.String</span></span>

### <span data-ttu-id="b9d80-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="b9d80-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="b9d80-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="b9d80-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="b9d80-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9d80-140">OUTPUTS</span></span>

### <span data-ttu-id="b9d80-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9d80-141">System.Boolean</span></span>

## <span data-ttu-id="b9d80-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9d80-142">NOTES</span></span>

## <span data-ttu-id="b9d80-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9d80-143">RELATED LINKS</span></span>

[<span data-ttu-id="b9d80-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b9d80-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)

