---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: ab1fcfa9b050f795a464488df51768b95996eb8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329072"
---
# <span data-ttu-id="dfd90-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="dfd90-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="dfd90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfd90-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd90-103">Импорт файла BACPAC и создание базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="dfd90-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="dfd90-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dfd90-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfd90-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfd90-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd90-106">Для импорта файла bacpac из учетной записи хранилища Azure в новую базу данных Azure импортируется SQL **AzSqlDataImport.**</span><span class="sxs-lookup"><span data-stu-id="dfd90-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="dfd90-107">Запрос на состояние импорта базы данных может быть отправлен для получения сведений о состоянии для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="dfd90-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="dfd90-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dfd90-108">EXAMPLES</span></span>

### <span data-ttu-id="dfd90-109">Пример 1. Создание запроса на импорт для файла BACPAC</span><span class="sxs-lookup"><span data-stu-id="dfd90-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="dfd90-110">Эта команда создает запрос на импорт .bacpac в новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="dfd90-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="dfd90-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfd90-111">PARAMETERS</span></span>

### <span data-ttu-id="dfd90-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="dfd90-112">-AdministratorLogin</span></span>
<span data-ttu-id="dfd90-113">Указывает имя администратора SQL домена.</span><span class="sxs-lookup"><span data-stu-id="dfd90-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="dfd90-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="dfd90-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="dfd90-115">Пароль администратора SQL пользователя.</span><span class="sxs-lookup"><span data-stu-id="dfd90-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd90-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="dfd90-116">-AuthenticationType</span></span>
<span data-ttu-id="dfd90-117">Определяет тип проверки подлинности, используемой для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="dfd90-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="dfd90-118">Этот параметр по умолчанию SQL, если тип проверки подлинности не задан.</span><span class="sxs-lookup"><span data-stu-id="dfd90-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="dfd90-119">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="dfd90-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfd90-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="dfd90-120">SQL.</span></span>
<span data-ttu-id="dfd90-121">SQL проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="dfd90-121">SQL authentication.</span></span>
<span data-ttu-id="dfd90-122">Задайте для параметров *AdministratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль SQL администратора.</span><span class="sxs-lookup"><span data-stu-id="dfd90-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="dfd90-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="dfd90-123">ADPassword.</span></span>
<span data-ttu-id="dfd90-124">Проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dfd90-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="dfd90-125">*Задайте для administratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль администратора Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dfd90-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="dfd90-126">Этот параметр доступен только на серверах SQL Database V12.</span><span class="sxs-lookup"><span data-stu-id="dfd90-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd90-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="dfd90-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="dfd90-128">Максимальный размер импортируемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="dfd90-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd90-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dfd90-129">-DatabaseName</span></span>
<span data-ttu-id="dfd90-130">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="dfd90-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="dfd90-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd90-131">-DefaultProfile</span></span>
<span data-ttu-id="dfd90-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dfd90-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfd90-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="dfd90-133">-Edition</span></span>
<span data-ttu-id="dfd90-134">Выпуск новой базы данных, в который нужно импортироваться.</span><span class="sxs-lookup"><span data-stu-id="dfd90-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="dfd90-135">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="dfd90-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfd90-136">Premium</span><span class="sxs-lookup"><span data-stu-id="dfd90-136">Premium</span></span>
- <span data-ttu-id="dfd90-137">Базовая</span><span class="sxs-lookup"><span data-stu-id="dfd90-137">Basic</span></span>
- <span data-ttu-id="dfd90-138">Стандартный</span><span class="sxs-lookup"><span data-stu-id="dfd90-138">Standard</span></span>
- <span data-ttu-id="dfd90-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="dfd90-139">DataWarehouse</span></span>
- <span data-ttu-id="dfd90-140">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="dfd90-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical, Hyperscale

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd90-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd90-141">-ResourceGroupName</span></span>
<span data-ttu-id="dfd90-142">Имя группы ресурсов для сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="dfd90-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="dfd90-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dfd90-143">-ServerName</span></span>
<span data-ttu-id="dfd90-144">Указывает имя сервера базы SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="dfd90-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="dfd90-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="dfd90-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="dfd90-146">Указывает имя цели службы, которая будет назначаться базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dfd90-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="dfd90-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="dfd90-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="dfd90-148">The sql server resource id to create private link</span><span class="sxs-lookup"><span data-stu-id="dfd90-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="dfd90-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="dfd90-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="dfd90-150">ИД ресурса учетной записи хранения для создания частной ссылки</span><span class="sxs-lookup"><span data-stu-id="dfd90-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="dfd90-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="dfd90-151">-StorageKey</span></span>
<span data-ttu-id="dfd90-152">Указывает ключ доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dfd90-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="dfd90-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="dfd90-153">-StorageKeyType</span></span>
<span data-ttu-id="dfd90-154">Определяет тип ключа доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dfd90-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="dfd90-155">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="dfd90-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfd90-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="dfd90-156">StorageAccessKey.</span></span>
<span data-ttu-id="dfd90-157">Использует ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dfd90-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="dfd90-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="dfd90-158">SharedAccessKey.</span></span>
<span data-ttu-id="dfd90-159">Использует ключ подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="dfd90-159">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd90-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="dfd90-160">-StorageUri</span></span>
<span data-ttu-id="dfd90-161">URI BLOB-файла bacpac.</span><span class="sxs-lookup"><span data-stu-id="dfd90-161">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd90-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="dfd90-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="dfd90-163">Если задается этот условия, будет создана частная ссылка для учетной записи хранения и (или) SQL сервера</span><span class="sxs-lookup"><span data-stu-id="dfd90-163">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd90-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfd90-164">-Confirm</span></span>
<span data-ttu-id="dfd90-165">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dfd90-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfd90-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd90-166">-WhatIf</span></span>
<span data-ttu-id="dfd90-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd90-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd90-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dfd90-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfd90-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd90-169">CommonParameters</span></span>
<span data-ttu-id="dfd90-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd90-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd90-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfd90-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd90-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfd90-172">INPUTS</span></span>

### <span data-ttu-id="dfd90-173">System.String</span><span class="sxs-lookup"><span data-stu-id="dfd90-173">System.String</span></span>

## <span data-ttu-id="dfd90-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dfd90-174">OUTPUTS</span></span>

### <span data-ttu-id="dfd90-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="dfd90-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="dfd90-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dfd90-176">NOTES</span></span>
* <span data-ttu-id="dfd90-177">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="dfd90-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="dfd90-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfd90-178">RELATED LINKS</span></span>

[<span data-ttu-id="dfd90-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="dfd90-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="dfd90-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="dfd90-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="dfd90-181">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="dfd90-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
