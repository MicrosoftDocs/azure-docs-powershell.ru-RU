---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407647"
---
# <span data-ttu-id="50c40-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50c40-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="50c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c40-102">SYNOPSIS</span></span>
<span data-ttu-id="50c40-103">Изменяет конфигурацию группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="50c40-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="50c40-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50c40-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c40-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50c40-105">DESCRIPTION</span></span>
<span data-ttu-id="50c40-106">Эта команда изменяет конфигурацию группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="50c40-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="50c40-107">Для выполнения команды следует использовать основной сервер группы отбойных команд.</span><span class="sxs-lookup"><span data-stu-id="50c40-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="50c40-108">Для управления набором баз данных в группе используйте add-AzSqlDatabaseToFailoverGroup и Remove-AzSqlDatabaseFromFailoverGroup.</span><span class="sxs-lookup"><span data-stu-id="50c40-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="50c40-109">Во время предварительного просмотра функции "Группы отката" для параметра "-GracePeriodWithDataLossHours" поддерживаются только значения, которые больше или равны 1 часу.</span><span class="sxs-lookup"><span data-stu-id="50c40-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="50c40-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50c40-110">EXAMPLES</span></span>

### <span data-ttu-id="50c40-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50c40-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="50c40-112">Устанавливает для группы отключки политику отключки "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="50c40-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="50c40-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="50c40-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="50c40-114">Устанавливает для группы отбойных отбойов политику отс неудачной передачи "Вручную", перенаправив в группу отбойных передач.</span><span class="sxs-lookup"><span data-stu-id="50c40-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="50c40-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50c40-115">PARAMETERS</span></span>

### <span data-ttu-id="50c40-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="50c40-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="50c40-117">Должно ли сбой на дополнительном сервере запускать автоматическую отключку конечной точки, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="50c40-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c40-118">-DefaultProfile</span></span>
<span data-ttu-id="50c40-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="50c40-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50c40-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="50c40-120">-FailoverGroupName</span></span>
<span data-ttu-id="50c40-121">Имя группы отбойного SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="50c40-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="50c40-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="50c40-122">-FailoverPolicy</span></span>
<span data-ttu-id="50c40-123">Политика отополномо для группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="50c40-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c40-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="50c40-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="50c40-125">Интервал до начала автоматического отключания в случае сбойов на основном сервере.</span><span class="sxs-lookup"><span data-stu-id="50c40-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="50c40-126">Это означает, что база данных Azure SQL не начнет автоматически отключиться до истечения льготного периода.</span><span class="sxs-lookup"><span data-stu-id="50c40-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="50c40-127">Обратите внимание, что отбой с параметром AllowDataLoss может привести к потере данных из-за природы асинхронной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="50c40-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c40-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50c40-128">-ResourceGroupName</span></span>
<span data-ttu-id="50c40-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50c40-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c40-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50c40-130">-ServerName</span></span>
<span data-ttu-id="50c40-131">Имя основного сервера баз данных Azure SQL группы failover.</span><span class="sxs-lookup"><span data-stu-id="50c40-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c40-132">CommonParameters</span></span>
<span data-ttu-id="50c40-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c40-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50c40-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c40-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50c40-135">INPUTS</span></span>

### <span data-ttu-id="50c40-136">System.String</span><span class="sxs-lookup"><span data-stu-id="50c40-136">System.String</span></span>

## <span data-ttu-id="50c40-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50c40-137">OUTPUTS</span></span>

### <span data-ttu-id="50c40-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="50c40-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="50c40-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50c40-139">NOTES</span></span>

## <span data-ttu-id="50c40-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50c40-140">RELATED LINKS</span></span>

[<span data-ttu-id="50c40-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50c40-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50c40-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50c40-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50c40-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50c40-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="50c40-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50c40-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="50c40-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50c40-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50c40-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="50c40-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="50c40-147">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="50c40-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)