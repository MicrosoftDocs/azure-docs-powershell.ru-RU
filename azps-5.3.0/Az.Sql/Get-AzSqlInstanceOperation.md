---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506649"
---
# <span data-ttu-id="7b058-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="7b058-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="7b058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b058-102">SYNOPSIS</span></span>
<span data-ttu-id="7b058-103">Возвращает SQL операций управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7b058-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="7b058-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b058-104">SYNTAX</span></span>

### <span data-ttu-id="7b058-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b058-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b058-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b058-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b058-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b058-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b058-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b058-108">DESCRIPTION</span></span>
<span data-ttu-id="7b058-109">Этот Get-AzSqlInstanceOperation получает сведения об операциях с SQL управляемым экземпляром.</span><span class="sxs-lookup"><span data-stu-id="7b058-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="7b058-110">Вы можете просмотреть все операции с управляемым экземпляром или конкретную операцию, укав ее имя.</span><span class="sxs-lookup"><span data-stu-id="7b058-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="7b058-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b058-111">EXAMPLES</span></span>

### <span data-ttu-id="7b058-112">Пример 1. Получить все операции экземпляра</span><span class="sxs-lookup"><span data-stu-id="7b058-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="7b058-113">Эта команда возвращает все операции, которые SQL управляемым экземпляром.</span><span class="sxs-lookup"><span data-stu-id="7b058-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="7b058-114">Пример 2. Получить определенную операцию</span><span class="sxs-lookup"><span data-stu-id="7b058-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="7b058-115">Эта команда получает операцию с именем 5870c6d8-6703-4b27-8ae4-687b4ca7caea в SQL управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="7b058-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="7b058-116">Пример 3. Использование ид ресурса операции</span><span class="sxs-lookup"><span data-stu-id="7b058-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="7b058-117">Эта команда получает операцию с id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span><span class="sxs-lookup"><span data-stu-id="7b058-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="7b058-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b058-118">PARAMETERS</span></span>

### <span data-ttu-id="7b058-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b058-119">-DefaultProfile</span></span>
<span data-ttu-id="7b058-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b058-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b058-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="7b058-121">-ManagedInstanceName</span></span>
<span data-ttu-id="7b058-122">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7b058-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b058-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7b058-123">-Name</span></span>
<span data-ttu-id="7b058-124">Имя операции.</span><span class="sxs-lookup"><span data-stu-id="7b058-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b058-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b058-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b058-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b058-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b058-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b058-127">-ResourceId</span></span>
<span data-ttu-id="7b058-128">Идентификатор ресурса для операции управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7b058-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b058-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b058-129">CommonParameters</span></span>
<span data-ttu-id="7b058-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b058-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b058-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b058-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b058-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b058-132">INPUTS</span></span>

### <span data-ttu-id="7b058-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7b058-133">System.String</span></span>

## <span data-ttu-id="7b058-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b058-134">OUTPUTS</span></span>

### <span data-ttu-id="7b058-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="7b058-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="7b058-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b058-136">NOTES</span></span>

## <span data-ttu-id="7b058-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b058-137">RELATED LINKS</span></span>