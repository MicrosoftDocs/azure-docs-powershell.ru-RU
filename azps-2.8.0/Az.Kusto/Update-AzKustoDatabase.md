---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 05d01d776f03ec3bbfe4e9bf6bd438ba8f002afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720562"
---
# <span data-ttu-id="2e414-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="2e414-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="2e414-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e414-102">SYNOPSIS</span></span>
<span data-ttu-id="2e414-103">Обновление существующей базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="2e414-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="2e414-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e414-104">SYNTAX</span></span>

### <span data-ttu-id="2e414-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e414-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e414-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e414-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e414-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e414-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e414-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e414-108">DESCRIPTION</span></span>
<span data-ttu-id="2e414-109">Обновление существующей базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="2e414-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="2e414-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e414-110">EXAMPLES</span></span>

### <span data-ttu-id="2e414-111">Пример 1: обновление существующей базы данных по имени</span><span class="sxs-lookup"><span data-stu-id="2e414-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="2e414-112">Приведенная выше команда обновляет период бездействия при удалении базы данных Kusto "mykustodatabase" в кластере "mykustocluster", обнаруженном в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="2e414-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="2e414-113">Пример 2. Обновление существующей базы данных с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="2e414-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="2e414-114">Вышеприведенная команда получает базу данных Kusto "mykustodatabase" в кластере "mykustocluster", обнаруженную в группе ресурсов "testrg" с помощью `Get-AzKustoDatabase` командлета, а затем передается результат, чтобы `Update-AzKustoDatabase` Обновить период с мягким удалением базы данных до пяти дней.</span><span class="sxs-lookup"><span data-stu-id="2e414-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="2e414-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e414-115">PARAMETERS</span></span>

### <span data-ttu-id="2e414-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="2e414-116">-ClusterName</span></span>
<span data-ttu-id="2e414-117">Имя кластера, в котором находится база данных</span><span class="sxs-lookup"><span data-stu-id="2e414-117">Name of cluster under which the database exists</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e414-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e414-118">-DefaultProfile</span></span>
<span data-ttu-id="2e414-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e414-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e414-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="2e414-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="2e414-121">Количество дней, в течение которых данные будут храниться в кэше для ускорения запросов</span><span class="sxs-lookup"><span data-stu-id="2e414-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e414-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e414-122">-InputObject</span></span>
<span data-ttu-id="2e414-123">Объект базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="2e414-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e414-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e414-124">-Name</span></span>
<span data-ttu-id="2e414-125">Имя обновляемой базы данных</span><span class="sxs-lookup"><span data-stu-id="2e414-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e414-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e414-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e414-127">Имя группы ресурсов, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="2e414-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e414-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e414-128">-ResourceId</span></span>
<span data-ttu-id="2e414-129">ИД ресурса Kusto базы данных.</span><span class="sxs-lookup"><span data-stu-id="2e414-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="2e414-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="2e414-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="2e414-131">Количество дней, в течение которых данные будут храниться, прежде чем она станет доступна для запросов</span><span class="sxs-lookup"><span data-stu-id="2e414-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e414-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e414-132">-Confirm</span></span>
<span data-ttu-id="2e414-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e414-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e414-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e414-134">-WhatIf</span></span>
<span data-ttu-id="2e414-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e414-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e414-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e414-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e414-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e414-137">CommonParameters</span></span>
<span data-ttu-id="2e414-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e414-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e414-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e414-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e414-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e414-140">INPUTS</span></span>

### <span data-ttu-id="2e414-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2e414-141">System.String</span></span>

### <span data-ttu-id="2e414-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="2e414-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="2e414-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e414-143">OUTPUTS</span></span>

### <span data-ttu-id="2e414-144">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="2e414-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="2e414-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e414-145">NOTES</span></span>

## <span data-ttu-id="2e414-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e414-146">RELATED LINKS</span></span>