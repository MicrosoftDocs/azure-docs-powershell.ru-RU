---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402151"
---
# <span data-ttu-id="4f136-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="4f136-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="4f136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f136-102">SYNOPSIS</span></span>
<span data-ttu-id="4f136-103">Сведения об импорте или экспорте базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4f136-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="4f136-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4f136-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f136-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f136-105">DESCRIPTION</span></span>
<span data-ttu-id="4f136-106">Cmdlet **Get-AzSqlDatabaseImportExportStatus** получает сведения об импорте файла bacpac из учетной записи хранения в базу данных Azure SQL или экспорте базы данных Azure SQL в качестве файла bacpac в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="4f136-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="4f136-107">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="4f136-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4f136-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4f136-108">EXAMPLES</span></span>

### <span data-ttu-id="4f136-109">Пример 1. Просмотр состояния импорта и экспорта базы SQL</span><span class="sxs-lookup"><span data-stu-id="4f136-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="4f136-110">Эта команда получает состояние запроса на импорт или экспорт базы данных по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="4f136-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="4f136-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f136-111">PARAMETERS</span></span>

### <span data-ttu-id="4f136-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f136-112">-DefaultProfile</span></span>
<span data-ttu-id="4f136-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4f136-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f136-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="4f136-114">-OperationStatusLink</span></span>
<span data-ttu-id="4f136-115">Указывает ссылку состояния, возвращаемую из New-AzSqlDatabaseExport или New-AzSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="4f136-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="4f136-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f136-116">-Confirm</span></span>
<span data-ttu-id="4f136-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f136-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f136-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f136-118">-WhatIf</span></span>
<span data-ttu-id="4f136-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f136-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f136-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4f136-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f136-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f136-121">CommonParameters</span></span>
<span data-ttu-id="4f136-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f136-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f136-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f136-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f136-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f136-124">INPUTS</span></span>

### <span data-ttu-id="4f136-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4f136-125">System.String</span></span>

## <span data-ttu-id="4f136-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f136-126">OUTPUTS</span></span>

### <span data-ttu-id="4f136-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="4f136-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="4f136-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4f136-128">NOTES</span></span>
* <span data-ttu-id="4f136-129">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="4f136-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="4f136-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f136-130">RELATED LINKS</span></span>

[<span data-ttu-id="4f136-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="4f136-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="4f136-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="4f136-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="4f136-133">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="4f136-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)