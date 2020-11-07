---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 65330f1024820c725cfb9a6b142000866063dc37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721254"
---
# <span data-ttu-id="73b65-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="73b65-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="73b65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73b65-102">SYNOPSIS</span></span>
<span data-ttu-id="73b65-103">Извлекает объект PSProjectTask, связанный с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="73b65-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="73b65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73b65-104">SYNTAX</span></span>

### <span data-ttu-id="73b65-105">ListByComponent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73b65-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="73b65-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="73b65-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="73b65-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="73b65-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="73b65-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="73b65-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="73b65-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b65-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="73b65-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73b65-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73b65-114">DESCRIPTION</span></span>
<span data-ttu-id="73b65-115">Командлет Get-AzDataMigrationTask извлекает свойства, связанные с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="73b65-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="73b65-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73b65-116">EXAMPLES</span></span>

### <span data-ttu-id="73b65-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73b65-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="73b65-118">В приведенном выше примере показано, как использовать командлет Get-AzDataMigrationTask для получения свойств, связанных с задачей миграции службы миграции баз данных Azure, на основе имени задачи, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="73b65-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="73b65-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="73b65-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="73b65-120">В приведенном выше примере показано, как использовать командлет Get-AzDataMigrationTask, чтобы извлечь все задачи миграции, связанные с объектом PSProject, который передается в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="73b65-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="73b65-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73b65-121">PARAMETERS</span></span>

### <span data-ttu-id="73b65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73b65-122">-DefaultProfile</span></span>
<span data-ttu-id="73b65-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73b65-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73b65-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="73b65-124">-Expand</span></span>
<span data-ttu-id="73b65-125">Развернуть вывод</span><span class="sxs-lookup"><span data-stu-id="73b65-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73b65-126">-InputObject</span></span>
<span data-ttu-id="73b65-127">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="73b65-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73b65-128">-Name</span></span>
<span data-ttu-id="73b65-129">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="73b65-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="73b65-130">-ProjectName</span></span>
<span data-ttu-id="73b65-131">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="73b65-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73b65-132">-ResourceGroupName</span></span>
<span data-ttu-id="73b65-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73b65-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73b65-134">-ResourceId</span></span>
<span data-ttu-id="73b65-135">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="73b65-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="73b65-136">-ResultType</span></span>
<span data-ttu-id="73b65-137">Развертывание результатов с данным типом результата.</span><span class="sxs-lookup"><span data-stu-id="73b65-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="73b65-138">-ServiceName</span></span>
<span data-ttu-id="73b65-139">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="73b65-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="73b65-140">-TaskType</span></span>
<span data-ttu-id="73b65-141">Фильтрация по TaskType.</span><span class="sxs-lookup"><span data-stu-id="73b65-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b65-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b65-142">CommonParameters</span></span>
<span data-ttu-id="73b65-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73b65-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b65-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73b65-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b65-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73b65-145">INPUTS</span></span>

### <span data-ttu-id="73b65-146">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="73b65-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="73b65-147">System. String</span><span class="sxs-lookup"><span data-stu-id="73b65-147">System.String</span></span>

## <span data-ttu-id="73b65-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73b65-148">OUTPUTS</span></span>

### <span data-ttu-id="73b65-149">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="73b65-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="73b65-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="73b65-150">NOTES</span></span>

## <span data-ttu-id="73b65-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73b65-151">RELATED LINKS</span></span>