---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 93895a7fffe40309b73c3929f88ffebfe203767f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567377"
---
# <span data-ttu-id="858c3-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="858c3-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="858c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="858c3-102">SYNOPSIS</span></span>
<span data-ttu-id="858c3-103">Удаление долгосрочной резервной копии хранения.</span><span class="sxs-lookup"><span data-stu-id="858c3-103">Deletes a long term retention backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="858c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="858c3-104">SYNTAX</span></span>

### <span data-ttu-id="858c3-105">RemoveBackupDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="858c3-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858c3-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="858c3-106">RemoveBackupByInputObject</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858c3-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="858c3-107">RemoveBackupByResourceId</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858c3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="858c3-108">DESCRIPTION</span></span>
<span data-ttu-id="858c3-109">Командлет **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** удаляет указанную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="858c3-109">The **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="858c3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="858c3-110">EXAMPLES</span></span>

### <span data-ttu-id="858c3-111">Пример 1: удаление одной резервной копии</span><span class="sxs-lookup"><span data-stu-id="858c3-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="858c3-112">Удаление резервной копии с именем 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="858c3-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="858c3-113">Пример 2: удаление всех резервных копий для местоположения</span><span class="sxs-lookup"><span data-stu-id="858c3-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzureRmSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="858c3-114">Эта команда удаляет все долгосрочные резервные копии хранения для местоположения northeurope.</span><span class="sxs-lookup"><span data-stu-id="858c3-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="858c3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="858c3-115">PARAMETERS</span></span>

### <span data-ttu-id="858c3-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="858c3-116">-BackupName</span></span>
<span data-ttu-id="858c3-117">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="858c3-117">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="858c3-118">-DatabaseName</span></span>
<span data-ttu-id="858c3-119">Имя базы данных SQL Azure, из которой находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="858c3-119">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858c3-120">-DefaultProfile</span></span>
<span data-ttu-id="858c3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="858c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="858c3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="858c3-122">-Force</span></span>
<span data-ttu-id="858c3-123">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="858c3-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="858c3-124">-InputObject</span></span>
<span data-ttu-id="858c3-125">Удаляемый объект резервного копирования базы данных для хранения.</span><span class="sxs-lookup"><span data-stu-id="858c3-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-126">-Location</span><span class="sxs-lookup"><span data-stu-id="858c3-126">-Location</span></span>
<span data-ttu-id="858c3-127">Расположение исходного сервера резервных копий.</span><span class="sxs-lookup"><span data-stu-id="858c3-127">The location of the backups' source server.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="858c3-128">-ResourceId</span></span>
<span data-ttu-id="858c3-129">Идентификатор ресурса резервной копии базы данных, для которого необходимо удалить архив.</span><span class="sxs-lookup"><span data-stu-id="858c3-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-130">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="858c3-130">-ServerName</span></span>
<span data-ttu-id="858c3-131">Имя сервера Azure SQL Server, в котором находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="858c3-131">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="858c3-132">-Confirm</span></span>
<span data-ttu-id="858c3-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="858c3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858c3-134">-WhatIf</span></span>
<span data-ttu-id="858c3-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="858c3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="858c3-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="858c3-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858c3-137">CommonParameters</span></span>
<span data-ttu-id="858c3-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="858c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="858c3-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858c3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858c3-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="858c3-140">INPUTS</span></span>

### <span data-ttu-id="858c3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="858c3-141">System.String</span></span>
<span data-ttu-id="858c3-142">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="858c3-142">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="858c3-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="858c3-143">OUTPUTS</span></span>

### <span data-ttu-id="858c3-144">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="858c3-144">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="858c3-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="858c3-145">NOTES</span></span>

## <span data-ttu-id="858c3-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="858c3-146">RELATED LINKS</span></span>

[<span data-ttu-id="858c3-147">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="858c3-147">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="858c3-148">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="858c3-148">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="858c3-149">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="858c3-149">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="858c3-150">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="858c3-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)