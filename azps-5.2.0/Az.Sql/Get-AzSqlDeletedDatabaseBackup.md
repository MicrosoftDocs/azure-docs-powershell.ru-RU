---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401607"
---
# <span data-ttu-id="b57d0-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b57d0-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="b57d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b57d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b57d0-103">Удаляет базу данных, которую можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="b57d0-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="b57d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b57d0-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b57d0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b57d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b57d0-106">Чтобы восстановить удаленную резервную копию SQL базы данных **Get-AzSqlDeletedDatabaseBackup,** можно восстановить указанный SQL или все удаленные резервные копии, которые можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="b57d0-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="b57d0-107">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="b57d0-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b57d0-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b57d0-108">EXAMPLES</span></span>

### <span data-ttu-id="b57d0-109">Пример 1. Все удаленные резервные копии базы данных на сервере</span><span class="sxs-lookup"><span data-stu-id="b57d0-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="b57d0-110">Эта команда получает все удаленные резервные копии баз данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="b57d0-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="b57d0-111">Пример 2. Получить указанную удаленную резервную копию базы данных</span><span class="sxs-lookup"><span data-stu-id="b57d0-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="b57d0-112">Эта команда получает удаленную резервную копию базы данных contosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="b57d0-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="b57d0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b57d0-113">PARAMETERS</span></span>

### <span data-ttu-id="b57d0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b57d0-114">-DatabaseName</span></span>
<span data-ttu-id="b57d0-115">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b57d0-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57d0-116">-DefaultProfile</span></span>
<span data-ttu-id="b57d0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b57d0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b57d0-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="b57d0-118">-DeletionDate</span></span>
<span data-ttu-id="b57d0-119">Указывает дату удаления базы данных в качестве объекта **даты** и времени.</span><span class="sxs-lookup"><span data-stu-id="b57d0-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="b57d0-120">Чтобы получить объект **даты и времени,** воспользуйтесь Get-Date.</span><span class="sxs-lookup"><span data-stu-id="b57d0-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b57d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="b57d0-122">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="b57d0-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b57d0-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b57d0-123">-ServerName</span></span>
<span data-ttu-id="b57d0-124">Имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="b57d0-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="b57d0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b57d0-125">-Confirm</span></span>
<span data-ttu-id="b57d0-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b57d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b57d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b57d0-127">-WhatIf</span></span>
<span data-ttu-id="b57d0-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b57d0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b57d0-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b57d0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b57d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57d0-130">CommonParameters</span></span>
<span data-ttu-id="b57d0-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b57d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57d0-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b57d0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57d0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b57d0-133">INPUTS</span></span>

### <span data-ttu-id="b57d0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b57d0-134">System.String</span></span>

### <span data-ttu-id="b57d0-135">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b57d0-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b57d0-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b57d0-136">OUTPUTS</span></span>

### <span data-ttu-id="b57d0-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="b57d0-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="b57d0-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b57d0-138">NOTES</span></span>

## <span data-ttu-id="b57d0-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b57d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="b57d0-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b57d0-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b57d0-141">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="b57d0-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)