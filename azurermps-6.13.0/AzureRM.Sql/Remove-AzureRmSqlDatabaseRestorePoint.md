---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: be4a4f418268d1e2523e13d5a779f911381c7309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566369"
---
# <span data-ttu-id="1f498-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="1f498-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="1f498-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f498-102">SYNOPSIS</span></span>
<span data-ttu-id="1f498-103">Удаляет указанную точку восстановления из базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="1f498-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f498-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f498-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f498-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f498-105">DESCRIPTION</span></span>
<span data-ttu-id="1f498-106">Командлет **Remove-AzureRmSqlDatabaseRestorePoint** удаляет указанную точку восстановления из базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1f498-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="1f498-107">Этот командлет в настоящее время поддерживается службой хранилища данных SQL Server в Azure.</span><span class="sxs-lookup"><span data-stu-id="1f498-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="1f498-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f498-108">EXAMPLES</span></span>

### <span data-ttu-id="1f498-109">Пример 1: Удаление точки восстановления</span><span class="sxs-lookup"><span data-stu-id="1f498-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="1f498-110">Эта команда удаляет точку восстановления для базы данных SQL Azure, заданной датой создания.</span><span class="sxs-lookup"><span data-stu-id="1f498-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="1f498-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f498-111">PARAMETERS</span></span>

### <span data-ttu-id="1f498-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f498-112">-DatabaseName</span></span>
<span data-ttu-id="1f498-113">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="1f498-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="1f498-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f498-114">-DefaultProfile</span></span>
<span data-ttu-id="1f498-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f498-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f498-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f498-116">-PassThru</span></span>
<span data-ttu-id="1f498-117">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="1f498-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1f498-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f498-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f498-119">Указывает имя группы ресурсов, которой назначена база данных SQL.</span><span class="sxs-lookup"><span data-stu-id="1f498-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="1f498-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="1f498-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="1f498-121">Указывает дату создания точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="1f498-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f498-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1f498-122">-ServerName</span></span>
<span data-ttu-id="1f498-123">Указывает имя сервера AzureSQL, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="1f498-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="1f498-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f498-124">-Confirm</span></span>
<span data-ttu-id="1f498-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f498-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f498-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f498-126">-WhatIf</span></span>
<span data-ttu-id="1f498-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f498-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f498-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f498-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f498-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f498-129">CommonParameters</span></span>
<span data-ttu-id="1f498-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f498-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f498-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f498-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f498-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f498-132">INPUTS</span></span>

### <span data-ttu-id="1f498-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="1f498-133">System.DateTime</span></span>

### <span data-ttu-id="1f498-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f498-134">System.String</span></span>

## <span data-ttu-id="1f498-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f498-135">OUTPUTS</span></span>

### <span data-ttu-id="1f498-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="1f498-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="1f498-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f498-137">NOTES</span></span>

## <span data-ttu-id="1f498-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f498-138">RELATED LINKS</span></span>