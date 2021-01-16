---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508885"
---
# <span data-ttu-id="707d7-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="707d7-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="707d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="707d7-102">SYNOPSIS</span></span>
<span data-ttu-id="707d7-103">Получает свойства пропускной способности "Приобр" в коллекции MongoDB.</span><span class="sxs-lookup"><span data-stu-id="707d7-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="707d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="707d7-104">SYNTAX</span></span>

### <span data-ttu-id="707d7-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="707d7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="707d7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="707d7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="707d7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="707d7-107">DESCRIPTION</span></span>
<span data-ttu-id="707d7-108">С помощью cmdlet **get-AzCosmosDBMongoDBCollectionThroughput** можно получить свойства пропускной способности коллекции MongoDB.</span><span class="sxs-lookup"><span data-stu-id="707d7-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="707d7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="707d7-109">EXAMPLES</span></span>

### <span data-ttu-id="707d7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="707d7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="707d7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="707d7-111">PARAMETERS</span></span>

### <span data-ttu-id="707d7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="707d7-112">-AccountName</span></span>
<span data-ttu-id="707d7-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="707d7-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707d7-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="707d7-114">-Confirm</span></span>
<span data-ttu-id="707d7-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="707d7-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707d7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="707d7-116">-DatabaseName</span></span>
<span data-ttu-id="707d7-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="707d7-117">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707d7-118">-DefaultProfile</span></span>
<span data-ttu-id="707d7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="707d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707d7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="707d7-120">-InputObject</span></span>
<span data-ttu-id="707d7-121">При этом он возвращает коллекцию с соответствующей пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="707d7-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="707d7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="707d7-122">-Name</span></span>
<span data-ttu-id="707d7-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="707d7-123">Collection name.</span></span>

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

### <span data-ttu-id="707d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="707d7-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="707d7-125">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707d7-126">-WhatIf</span></span>
<span data-ttu-id="707d7-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="707d7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="707d7-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="707d7-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707d7-129">CommonParameters</span></span>
<span data-ttu-id="707d7-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="707d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707d7-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="707d7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707d7-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="707d7-132">INPUTS</span></span>

### <span data-ttu-id="707d7-133">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="707d7-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="707d7-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="707d7-134">OUTPUTS</span></span>

### <span data-ttu-id="707d7-135">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="707d7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="707d7-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="707d7-136">NOTES</span></span>

## <span data-ttu-id="707d7-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="707d7-137">RELATED LINKS</span></span>