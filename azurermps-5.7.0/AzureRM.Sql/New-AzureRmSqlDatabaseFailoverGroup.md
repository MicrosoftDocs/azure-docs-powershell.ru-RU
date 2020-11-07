---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557044"
---
# <span data-ttu-id="633c1-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="633c1-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="633c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="633c1-102">SYNOPSIS</span></span>
<span data-ttu-id="633c1-103">Эта команда создает новую группу отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="633c1-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="633c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="633c1-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="633c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="633c1-105">DESCRIPTION</span></span>
<span data-ttu-id="633c1-106">Создание новой группы отработки отказа базы данных Azure SQL для указанных серверов.</span><span class="sxs-lookup"><span data-stu-id="633c1-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>

<span data-ttu-id="633c1-107">Две конечные точки TDS базы данных SQL Azure создаются на FailoverGroupName. SqlDatabaseDnsSuffix (например, FailoverGroupName.database.windows.net) и FailoverGroupName. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="633c1-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="633c1-108">Эти конечные точки можно использовать для подключения к основным и дополнительным серверам в группе отработки отказа, соответственно.</span><span class="sxs-lookup"><span data-stu-id="633c1-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="633c1-109">Если проблема связана с основным сервером, автоматический переход на конечные точки и базы данных будет срабатывать в соответствии с политикой перемещения при сбое и льготным периодом для группы, на которую отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="633c1-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="633c1-110">Вновь созданные группы отработки отказа не содержат баз данных.</span><span class="sxs-lookup"><span data-stu-id="633c1-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="633c1-111">Чтобы управлять набором баз данных в группе отработки отказа, используйте командлеты Add-AzureRmSqlDatabaseToFailoverGroup и Remove-AzureRmSqlDatabaseFromFailoverGroup.</span><span class="sxs-lookup"><span data-stu-id="633c1-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>

<span data-ttu-id="633c1-112">Во время предварительного просмотра компонента "группы отработки отказа" для параметра "-GracePeriodWithDataLossHours" поддерживаются только значения, превышающие или равные 1 часу.</span><span class="sxs-lookup"><span data-stu-id="633c1-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="633c1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="633c1-113">EXAMPLES</span></span>

### <span data-ttu-id="633c1-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="633c1-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="633c1-115">Эта команда создает новую группу отработки отказа с автоматическим включением политики отработки отказов для двух серверов в одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="633c1-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="633c1-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="633c1-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="633c1-117">Эта команда создает новую группу отработки отказа с политикой перемещения при сбое "вручную" для двух серверов в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="633c1-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="633c1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="633c1-118">PARAMETERS</span></span>

### <span data-ttu-id="633c1-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="633c1-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="633c1-120">Должен ли отказ на сервере-получателе инициировать автоматический переход конечной точки, доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="633c1-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="633c1-121">Эта функция пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="633c1-121">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633c1-122">-DefaultProfile</span></span>
<span data-ttu-id="633c1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="633c1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633c1-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="633c1-124">-FailoverGroupName</span></span>
<span data-ttu-id="633c1-125">Имя создаваемой группы отработки отказа базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="633c1-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="633c1-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="633c1-126">-FailoverPolicy</span></span>
<span data-ttu-id="633c1-127">Политика перемещения при сбое для группы Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="633c1-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633c1-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="633c1-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="633c1-129">Интервал перед автоматическим переходом на другой ресурс инициируется при возникновении сбоя на сервере основного сервера, и отработка отказа не может быть завершена без потери данных.</span><span class="sxs-lookup"><span data-stu-id="633c1-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633c1-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633c1-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="633c1-131">Имя вторичной группы ресурсов для группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="633c1-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="633c1-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="633c1-132">-PartnerServerName</span></span>
<span data-ttu-id="633c1-133">Имя сервера, на который производится резервная копия базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="633c1-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="633c1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633c1-134">-ResourceGroupName</span></span>
<span data-ttu-id="633c1-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="633c1-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="633c1-136">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="633c1-136">-ServerName</span></span>
<span data-ttu-id="633c1-137">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="633c1-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="633c1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633c1-138">CommonParameters</span></span>
<span data-ttu-id="633c1-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="633c1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633c1-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="633c1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633c1-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="633c1-141">INPUTS</span></span>

### <span data-ttu-id="633c1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="633c1-142">System.String</span></span>

## <span data-ttu-id="633c1-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="633c1-143">OUTPUTS</span></span>

### <span data-ttu-id="633c1-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="633c1-144">System.Object</span></span>

## <span data-ttu-id="633c1-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="633c1-145">NOTES</span></span>

## <span data-ttu-id="633c1-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="633c1-146">RELATED LINKS</span></span>

[<span data-ttu-id="633c1-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="633c1-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="633c1-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="633c1-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="633c1-149">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="633c1-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="633c1-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="633c1-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="633c1-151">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="633c1-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="633c1-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="633c1-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="633c1-153">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="633c1-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)