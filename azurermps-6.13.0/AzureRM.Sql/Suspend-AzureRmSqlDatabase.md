---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/suspend-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 5ceee1509ed5c47611f68645a6cf1665b9df8408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562507"
---
# <span data-ttu-id="a0180-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0180-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a0180-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0180-102">SYNOPSIS</span></span>
<span data-ttu-id="a0180-103">Приостанавливает базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="a0180-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0180-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0180-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0180-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0180-105">DESCRIPTION</span></span>
<span data-ttu-id="a0180-106">Командлет **Suspend-AzureRmSqlDatabase** приостанавливает базу данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a0180-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a0180-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0180-107">EXAMPLES</span></span>

### <span data-ttu-id="a0180-108">Пример 1: Приостановка базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a0180-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a0180-109">Эта команда приостанавливает активную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a0180-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a0180-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0180-110">PARAMETERS</span></span>

### <span data-ttu-id="a0180-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0180-111">-AsJob</span></span>
<span data-ttu-id="a0180-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a0180-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0180-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0180-113">-DatabaseName</span></span>
<span data-ttu-id="a0180-114">Указывает имя базы данных, к которой приостанавливается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a0180-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="a0180-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0180-115">-DefaultProfile</span></span>
<span data-ttu-id="a0180-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a0180-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0180-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0180-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0180-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="a0180-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a0180-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a0180-119">-ServerName</span></span>
<span data-ttu-id="a0180-120">Указывает имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="a0180-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="a0180-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0180-121">-Confirm</span></span>
<span data-ttu-id="a0180-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0180-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0180-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0180-123">-WhatIf</span></span>
<span data-ttu-id="a0180-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0180-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0180-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0180-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0180-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0180-126">CommonParameters</span></span>
<span data-ttu-id="a0180-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0180-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0180-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0180-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0180-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0180-129">INPUTS</span></span>

### <span data-ttu-id="a0180-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a0180-130">System.String</span></span>

## <span data-ttu-id="a0180-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0180-131">OUTPUTS</span></span>

### <span data-ttu-id="a0180-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a0180-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a0180-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0180-133">NOTES</span></span>
* <span data-ttu-id="a0180-134">Командлет **Suspend-AzureRmSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a0180-134">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a0180-135">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a0180-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a0180-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0180-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0180-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0180-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a0180-138">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0180-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="a0180-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0180-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a0180-140">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0180-140">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="a0180-141">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0180-141">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="a0180-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a0180-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

