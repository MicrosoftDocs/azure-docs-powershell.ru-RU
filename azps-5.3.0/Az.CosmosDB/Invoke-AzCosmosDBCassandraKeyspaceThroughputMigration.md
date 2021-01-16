---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508865"
---
# <span data-ttu-id="2abb7-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="2abb7-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="2abb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2abb7-102">SYNOPSIS</span></span>
<span data-ttu-id="2abb7-103">Используйте этот метод для переноса пропускной способности для автоматической передачи с ручной пропускной способностью и наоборот.</span><span class="sxs-lookup"><span data-stu-id="2abb7-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="2abb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2abb7-104">SYNTAX</span></span>

### <span data-ttu-id="2abb7-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2abb7-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2abb7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2abb7-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2abb7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2abb7-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2abb7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2abb7-108">DESCRIPTION</span></span>
<span data-ttu-id="2abb7-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="2abb7-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="2abb7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2abb7-110">EXAMPLES</span></span>

### <span data-ttu-id="2abb7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2abb7-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="2abb7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2abb7-112">PARAMETERS</span></span>

### <span data-ttu-id="2abb7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2abb7-113">-AccountName</span></span>
<span data-ttu-id="2abb7-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="2abb7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2abb7-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2abb7-115">-Confirm</span></span>
<span data-ttu-id="2abb7-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2abb7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2abb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abb7-117">-DefaultProfile</span></span>
<span data-ttu-id="2abb7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2abb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2abb7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2abb7-119">-InputObject</span></span>
<span data-ttu-id="2abb7-120">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="2abb7-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2abb7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2abb7-121">-Name</span></span>
<span data-ttu-id="2abb7-122">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="2abb7-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="2abb7-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2abb7-123">-ParentObject</span></span>
<span data-ttu-id="2abb7-124">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="2abb7-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2abb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2abb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="2abb7-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2abb7-126">Name of resource group.</span></span>

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

### <span data-ttu-id="2abb7-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="2abb7-127">-ThroughputType</span></span>
<span data-ttu-id="2abb7-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="2abb7-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="2abb7-129">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="2abb7-129">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2abb7-130">-WhatIf</span></span>
<span data-ttu-id="2abb7-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2abb7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2abb7-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2abb7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2abb7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abb7-133">CommonParameters</span></span>
<span data-ttu-id="2abb7-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2abb7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abb7-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2abb7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abb7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2abb7-136">INPUTS</span></span>

### <span data-ttu-id="2abb7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="2abb7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="2abb7-138">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="2abb7-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="2abb7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2abb7-139">OUTPUTS</span></span>

### <span data-ttu-id="2abb7-140">Microsoft.Azure.Commands.GetsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2abb7-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2abb7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2abb7-141">NOTES</span></span>

## <span data-ttu-id="2abb7-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2abb7-142">RELATED LINKS</span></span>