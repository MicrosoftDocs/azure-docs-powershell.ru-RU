---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 7019fc7345b4296d9c35f11c6acec5bf5a42d966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568138"
---
# <span data-ttu-id="d2546-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d2546-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="d2546-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2546-102">SYNOPSIS</span></span>
<span data-ttu-id="d2546-103">Создает копию базы данных SQL, в которой используется моментальный снимок в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d2546-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2546-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2546-104">SYNTAX</span></span>

### <span data-ttu-id="d2546-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2546-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2546-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="d2546-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2546-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2546-107">DESCRIPTION</span></span>
<span data-ttu-id="d2546-108">Командлет **New-AzureRmSqlDatabaseCopy** создает копию базы данных Azure SQL, в которой используется моментальный снимок данных в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d2546-108">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="d2546-109">Используйте этот командлет вместо командлета Start-AzureSqlDatabaseCopy, чтобы создать единовременно разовую копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2546-109">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="d2546-110">Этот командлет возвращает объект **базы данных** копии.</span><span class="sxs-lookup"><span data-stu-id="d2546-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="d2546-111">Примечание. Используйте командлет New-AzureRmSqlDatabaseSecondary, чтобы настроить георепликацию для базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2546-111">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="d2546-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="d2546-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d2546-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2546-113">EXAMPLES</span></span>

## <span data-ttu-id="d2546-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2546-114">PARAMETERS</span></span>

### <span data-ttu-id="d2546-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2546-115">-AsJob</span></span>
<span data-ttu-id="d2546-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d2546-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2546-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d2546-117">-ComputeGeneration</span></span>
<span data-ttu-id="d2546-118">Вычислено поколение, назначаемое новой копии.</span><span class="sxs-lookup"><span data-stu-id="d2546-118">The compute generation to assign to the new copy.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2546-119">-CopyDatabaseName</span></span>
<span data-ttu-id="d2546-120">Указывает имя копии базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d2546-120">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2546-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="d2546-122">Указывает имя группы ресурсов Azure, в которую нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="d2546-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="d2546-123">-CopyServerName</span></span>
<span data-ttu-id="d2546-124">Указывает имя сервера SQL Server, на котором размещается копия.</span><span class="sxs-lookup"><span data-stu-id="d2546-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2546-125">-DatabaseName</span></span>
<span data-ttu-id="d2546-126">Указывает имя базы данных SQL для копирования.</span><span class="sxs-lookup"><span data-stu-id="d2546-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="d2546-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2546-127">-DefaultProfile</span></span>
<span data-ttu-id="d2546-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2546-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2546-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d2546-129">-ElasticPoolName</span></span>
<span data-ttu-id="d2546-130">Указывает имя эластичного пула, в который нужно назначить копию.</span><span class="sxs-lookup"><span data-stu-id="d2546-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d2546-131">-LicenseType</span></span>
<span data-ttu-id="d2546-132">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d2546-132">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2546-133">-ResourceGroupName</span></span>
<span data-ttu-id="d2546-134">Указывает имя группы ресурсов, содержащей базу данных, которую необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="d2546-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="d2546-135">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d2546-135">-ServerName</span></span>
<span data-ttu-id="d2546-136">Указывает имя сервера SQL Server, содержащего базу данных, которую необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="d2546-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="d2546-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d2546-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="d2546-138">Указывает имя цели обслуживания, которую нужно назначить копии.</span><span class="sxs-lookup"><span data-stu-id="d2546-138">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-139">-Теги</span><span class="sxs-lookup"><span data-stu-id="d2546-139">-Tags</span></span>
<span data-ttu-id="d2546-140">Задает пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с копией базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d2546-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="d2546-141">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="d2546-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="d2546-142">-VCore</span></span>
<span data-ttu-id="d2546-143">Vcore номера копий базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d2546-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2546-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2546-144">-Confirm</span></span>
<span data-ttu-id="d2546-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2546-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2546-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2546-146">-WhatIf</span></span>
<span data-ttu-id="d2546-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2546-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2546-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2546-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2546-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2546-149">CommonParameters</span></span>
<span data-ttu-id="d2546-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2546-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2546-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2546-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2546-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2546-152">INPUTS</span></span>

### <span data-ttu-id="d2546-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d2546-153">System.String</span></span>

## <span data-ttu-id="d2546-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2546-154">OUTPUTS</span></span>

### <span data-ttu-id="d2546-155">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="d2546-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="d2546-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2546-156">NOTES</span></span>

## <span data-ttu-id="d2546-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2546-157">RELATED LINKS</span></span>

[<span data-ttu-id="d2546-158">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d2546-158">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="d2546-159">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="d2546-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)