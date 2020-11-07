---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: 5681b046afb6682809d9b2dc744784514c2aefa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565326"
---
# <span data-ttu-id="be45b-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="be45b-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="be45b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be45b-102">SYNOPSIS</span></span>
<span data-ttu-id="be45b-103">Возобновляет базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="be45b-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be45b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be45b-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be45b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be45b-105">DESCRIPTION</span></span>
<span data-ttu-id="be45b-106">Командлет **Resume-AzureRmSqlDatabase** возобновляет базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="be45b-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="be45b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be45b-107">EXAMPLES</span></span>

### <span data-ttu-id="be45b-108">Пример 1: возобновление базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="be45b-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="be45b-109">Эта команда Возобновляет приостановленную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="be45b-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="be45b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be45b-110">PARAMETERS</span></span>

### <span data-ttu-id="be45b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be45b-111">-AsJob</span></span>
<span data-ttu-id="be45b-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="be45b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be45b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be45b-113">-DatabaseName</span></span>
<span data-ttu-id="be45b-114">Указывает имя базы данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="be45b-114">Specifies the name of the database that this cmdlet resumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be45b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be45b-115">-DefaultProfile</span></span>
<span data-ttu-id="be45b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="be45b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be45b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be45b-117">-ResourceGroupName</span></span>
<span data-ttu-id="be45b-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="be45b-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="be45b-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="be45b-119">-ServerName</span></span>
<span data-ttu-id="be45b-120">Указывает имя сервера, на котором размещается база данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="be45b-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="be45b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be45b-121">-Confirm</span></span>
<span data-ttu-id="be45b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be45b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be45b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be45b-123">-WhatIf</span></span>
<span data-ttu-id="be45b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be45b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be45b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be45b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be45b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be45b-126">CommonParameters</span></span>
<span data-ttu-id="be45b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be45b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be45b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be45b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be45b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be45b-129">INPUTS</span></span>

### <span data-ttu-id="be45b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="be45b-130">System.String</span></span>

## <span data-ttu-id="be45b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be45b-131">OUTPUTS</span></span>

### <span data-ttu-id="be45b-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="be45b-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="be45b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="be45b-133">NOTES</span></span>
* <span data-ttu-id="be45b-134">Командлет **Resume-AzureRmSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="be45b-134">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="be45b-135">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="be45b-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="be45b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be45b-136">RELATED LINKS</span></span>

[<span data-ttu-id="be45b-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="be45b-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="be45b-138">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="be45b-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="be45b-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="be45b-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="be45b-140">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="be45b-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="be45b-141">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="be45b-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="be45b-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="be45b-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

